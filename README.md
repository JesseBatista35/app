caixa-base-chart:

#-------#
# IMAGE #
#-------#

  image:
    # variavel de imagem do tipo de aplicação
    repository: acrcentralcaixanprd.azurecr.io/sidvi/backend-spring-desenvolve-ai/sidvi-backend-spring-desenvolve-ai
    tag: "38610478820"
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

#-----------------#
# ROLLING UPDATE STRATEGY #
#-----------------#

  strategy:
    maxSurge: 25%
    maxUnavailable: 50%


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
        - "sidvi-backend-spring-desenvolve-ai.apl.tqs.private.azure"
      - port:
         number: 443
         name: https-custom
         protocol: HTTPS
       tls:
         mode: SIMPLE
         credentialName: akvs-sidvi-backend-spring-desenvolve-ai # Nome do secret do certificado
       hosts:
         - sidvi-backend-spring-desenvolve-ai.tqs.caixa
      prefix:
        - /
      targetPort: 80 
  
#-------------#
#  RESOURCES  #
#-------------#

  resources:
    requests:
      cpu: 500m
      memory: 1024Mi
    limits:
      cpu: 1500m
      memory: 2048Mi


#----------#
#  PROBES  #
#----------#

  probes:  
    enabled: true
    useDefaults: false  
    livenessProbe: 
      initialDelaySeconds: 30
      periodSeconds: 15
      failureThreshold: 10
      successThreshold: 1
      httpGet:
        path: /api/v1/health/liveness     
        port: 8080
    readinessProbe: 
      initialDelaySeconds: 15
      periodSeconds: 15
      failureThreshold: 3
      successThreshold: 1
      httpGet:
        path: /api/v1/health/readiness     
        port: 8080


#-------------#
#  CONFIGMAP  #
#-------------#

  configMapRefs:
    - name: cm-sidvi-backend-spring-desenvolve-ai
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
      value: "appssiiga"

#-------------# 
#   SECRETS   # 
#-------------# 


  secretRefs:
  env:
    - name: AZURE_OPENAI_API_KEY
      value: akvs-azure-openai-api-key@azurekeyvault
    - name: PAT_ENCRYPTION_SECRET
      value: akvs-pat-encryption-secret@azurekeyvault
    - name: PAT_ENCRYPTION_SALT
      value: akvs-pat-encryption-salt@azurekeyvault
    - name: AZURE_BLOB_CONNECTION_STRING
      value: akvs-azure-blob-connection-string@azurekeyvault
    - name: KEYCLOAK_CLIENT_SECRET
      value: akvs-keycloak-client-secret@azurekeyvault
    - name: SPRING_DATASOURCE_USERNAME
      value: akvs-spring-datasource-username@azurekeyvault
    - name: SPRING_DATASOURCE_PASSWORD
      value: akvs-spring-datasource-password@azurekeyvault
    - name: MCP_GITHUB_PAT
      value: akvs-mcp-github-pat@azurekeyvault






corrige ai o que tem que corrigri
