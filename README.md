Prezados, 

Devido a um erro de "permission denied" no workflow de CI/CD para a aplicação sidpn-api-intra-credito-emprestimos, na task de "SYNC FORCE ARGOCD PRD" no job "ArgoCD_Deploy (DES)" (https://github.com/caixagithub/sidpn-api-intra-credito-emprestimos/actions/runs/38933075198/job/117083720461) solicitamos que seja feita a vinculação no GITOPS do repositório "sidpn-api-intra-credito-emprestimos", 

no ambiente de desenvolvimento, ao "aks-opf-des" (https://portal.azure.com/#@caixa.onmicrosoft.com/resource/subscriptions/7e75b440-44bf-4181-b28d-1d480aa181a5/resourceGroups/rg-opf-des/providers/Microsoft.ContainerService/managedClusters/aks-opf-des/overview). Acreditamos que o problema no workflow se resolverá após isso.

Atenciosamente,

Gabriel Maurício Chagas Silva
Assistente Jr.
Box Open Finance




ATUA,MENE TA ASSIM


gitops/apps/sidpn-api-intra-credito-emprestimos/des
/config.yaml


app:
  name: sidpn-api-intra-credito-emprestimos-des
project:
  name: des
labels:
  appName: sidpn-api-intra-credito-emprestimos
  environment: des
source:
  repo: "https://github.com/caixagithub/sidpn-api-intra-credito-emprestimos-infranprd"
  path: des
sourcevar:
  repo: "https://github.com/caixagithub/"
  path: des
  values: global.yaml  
cluster:
  destination:  
    name: aks-sidpn-des
    namespace: sidpn-api-intra-credito-emprestimos



    caixa-base-chart:

#-------#
# IMAGE #
#-------#

  image:
    # variavel de imagem do tipo de aplicação 
    repository: acrcentralcaixanprd.azurecr.io/sidpn/api-intra-credito-emprestimos/sidpn-api-intra-credito-emprestimos
    tag: "38933075198"
    pullPolicy: Always 


#-----#
# HPA #
#-----#

  replicaCount: 1

  autoscaling:
    enabled: false
    minReplicas: 1
    maxReplicas: 3
    targetCPUUtilizationPercentage: 85
    targetMemoryUtilizationPercentage: 85
    behavior:
      scaleDown:
        stabilizationWindowSeconds: 120 # 2 minutos para estabilizar antes de reduzir
        policies:
        - type: Percent
          value: 100  # Reduz até 100% dos pods por período
          periodSeconds: 15
      scaleUp:
        stabilizationWindowSeconds: 0  # Sem tempo de estabilização antes de aumentar
        policies:
        - type: Percent
          value: 100  # Aumenta até 100% dos pods por período
          periodSeconds: 30
        - type: Pods
          value: 4  # Aumenta no máximo 4 pods por período
          periodSeconds: 30
        selectPolicy: "Max"  # Opções: Min, Max, Disabled




sidpn-api-intra-credito-emprestimos-infranprd/des
/values.yaml


#-------------------------#
# ROLLING UPDATE STRATEGY #
#-------------------------#

  strategy:
    maxSurge: 25%
    maxUnavailable: 25%


#-----------#
#  SERVICE  #
#-----------#

  service:
    type: "ClusterIP"
    ports:
      - name: "port"
        protocol: TCP
        port: 80
        targetPort: 8080


#---------#
# INGRESS #
#---------#

  istio:  
  - name: internal
    enabled: true
    servers:
      - port:
          number: 80
          name: http-default
          protocol: HTTP
        hosts:
          - sidpn-api-intra-credito-emprestimos.apl.des.private.azure
    # prefix:
    #   - /
    # rewrite:
    #   uri: /
    targetPort: 80


#-------------#
#  RESOURCES  #
#-------------#

  resources:
    requests:
      cpu: 50m
      memory: 256Mi
    limits:
      cpu: 150m
      memory: 512Mi


#----------#
#  PROBES  #
#----------#
  
  probes:
    enabled: false  
    useDefaults: false
    startupProbe:
      initialDelaySeconds: 10
      periodSeconds: 10
      failureThreshold: 12
      httpGet:
        path: /open-banking/intranet/loans/health/live
        port: 8080
    livenessProbe: 
      initialDelaySeconds: 30
      periodSeconds: 15
      failureThreshold: 10
      successThreshold: 1
      httpGet:
        path: /open-banking/intranet/loans/health/live    
        port: 8080
#    readinessProbe: 
#      initialDelaySeconds: 15
#      periodSeconds: 15
#      failureThreshold: 3
#      successThreshold: 1
#      httpGet:
#        path: /health/ready    
#        port: 8080


#-------------#
#  CONFIGMAP  #
#-------------#

  configMapRefs:
    - name: cm-sidpn-api-intra-credito-emprestimos-des

    
#---------------#
#  TOLERATIONS  #
#---------------#

  tolerations:
    - key: "kubernetes.azure.com/scalesetpriority"
      effect: "NoSchedule"
      operator: "Equal"
      value: "spot"

    - key: "nuvem.caixa/nodepoolname"
      effect: "NoSchedule"
      operator: "Equal"
      value: "appsidpnintr"


#----------#
#   ENVS   #
#----------#

  env:

    #-------------# 
    #   SECRETS   # 
    #-------------# 

    - name: API_KEY
      value: akvs-api-des-caixa-sidpn-apikey@azurekeyvault
      
    - name: CONTAINER_LOGS_KEY
      value: akvs-ehauditoriaobdes-containers-logs-sender-key@azurekeyvault
      
    - name: AUDIT_TRAIL_KEY
      value: akvs-ehmirrormaker-ehtrilhadeauditoriaobagregadordes-sender-key@azurekeyvault
      
    - name: REDIS_KEY
      value: akvs-cachecemprestimodes-key@azurekeyvault
      
    - name: SSO_CLIENT_SECRET
      value: akvs-cli-ser-dpn-login-des-secret@azurekeyvault

    - name: SSO_CLIENT_SECRET_SINCR
      value: akvs-cli-ser-cgr-login-des-secret@azurekeyvault
    
    - name: COSMOSDB_KEY
      value: akvs-cdb-dpn-credito-des-key@azurekeyvault


    #---------#
    #   JVM   #
    #---------#

    - name: JAVA_TOOL_OPTIONS
      value: >-
        -XX:InitialRAMPercentage=40
        -XX:MaxRAMPercentage=60
        -XX:MaxDirectMemorySize=128m
        -Xss256k
        -XX:+ExitOnOutOfMemoryError

sidpn-api-intra-credito-emprestimos-infranprd/des
/ci_cd_variables.yaml


local-variables:
  ci-cd-workflow:
   - name: APIM_DISPLAYNAMEAPI
     value: API Loans - Open Finance Brasil - Intranet [sidpn-api-intra-credito-emprestimos]"
   - name: APIM_PATH
     value: "open-banking/intranet/loans"
   - name: AKS_URL
     value: "sidpn-api-intra-credito-emprestimos.apl.des.private.azure/open-banking/intranet/loans"
   - name: APIM_TAGSAPI
     value: "tagidsidpn=SIDPN,tagidintra=INTRA"
   - name: PROTOCOLO
     value: "http"
   - name: SUBSCRIPTION_ID
     value: "7e75b440-44bf-4181-b28d-1d480aa181a5"
   - name: APIM_NAME 
     value: "apimv2-internal-opf-des"
   - name: RESOURCE_GROUP
     value: "rg-opf-resources-des"
   - name: REPOSITORY_ARTIFACTS_APP
     value: "NEXUS"
   - name: JAVA_VERSION
     value: "11"

des/templates/akvs-api-des-caixa-sidpn-apikey.yaml


     apiVersion: spv.no/v2beta1
kind: AzureKeyVaultSecret
metadata:
  name: akvs-api-des-caixa-sidpn-apikey
  labels:
    {{- include "caixa-base-chart.labels" . | nindent 4 }}
spec:
  vault:
    name: kv-opf-des
    object:
      name: api-des-caixa-sidpn-apikey
      type: secret


        ub Enterprise
Users managed by Caixa Economica Federal
caixagithub
sidpn-api-intra-credito-emprestimos-infranprd
Repository navigation
Code
Issues
Pull requests
Actions
Projects
Wiki
Security and quality
5
 (5)
Insights
Settings
Files
Go to file
t
T
des
templates
akvs-api-des-caixa-sidpn-apikey.yaml
akvs-cachecemprestimodes-key.yaml
akvs-cdb-dpn-credito-des-key.yaml
akvs-cli-ser-cgr-login-des-secret.yaml
akvs-cli-ser-dpn-login-des-secret.yaml
akvs-ehauditoriaobdes-containers-logs-sender-key.yaml
akvs-ehmirrormaker-ehtrilhadeauditoriaobagregadordes-sender-key.yaml
cm-sidpn-api-intra-credito-emprestimos-des.yaml
.helmignore
Chart.yaml
ci_cd_variables.yaml
values.yaml
sidpn-api-intra-credito-emprestimos-infranprd/des/templates
/akvs-api-des-caixa-sidpn-apikey.yaml


