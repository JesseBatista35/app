apiVersion: v1
kind: Pod
metadata:
  creationTimestamp: '2026-10-13T18:50:16Z'
  generateName: sipgs-backend-bff-simulacao-des-745dbb95bb-
  generation: 1
  labels:
    app.kubernetes.io/app: sipgs-backend-bff-simulacao-des
    app.kubernetes.io/instance: sipgs-backend-bff-simulacao-des
    app.kubernetes.io/managed-by: Helm
    app.kubernetes.io/name: sipgs-backend-bff-simulacao-des
    app.kubernetes.io/version: 1.16.0
    appName: sipgs-backend-bff-simulacao
    backstage.io/kubernetes-id: sipgs-backend-bff-simulacao
    helm.sh/chart: caixa-base-chart-1.2.2-beta11
    pod-template-hash: 745dbb95bb
    topology.kubernetes.io/region: sa-east-1
    topology.kubernetes.io/zone: sa-east-1b
  name: sipgs-backend-bff-simulacao-des-745dbb95bb-n794n
  namespace: sipgs-backend-bff-simulacao
  ownerReferences:
    - apiVersion: apps/v1
      blockOwnerDeletion: true
      controller: true
      kind: ReplicaSet
      name: sipgs-backend-bff-simulacao-des-745dbb95bb
      uid: a2898807-c8c7-4035-bafc-0cfea7ebf584
  resourceVersion: '60627955'
  uid: 00516ff1-7abf-41b3-927d-ddb394a54a16
spec:
  containers:
    - envFrom:
        - configMapRef:
            name: cm-sipgs-backend-bff-simulacao
      image: >-
        027574771582.dkr.ecr.sa-east-1.amazonaws.com/sipgs/backend-bff-simulacao/sipgs-backend-bff-simulacao:38449076556
      imagePullPolicy: Always
      livenessProbe:
        failureThreshold: 10
        httpGet:
          path: /q/health/live
          port: 8080
          scheme: HTTP
        initialDelaySeconds: 30
        periodSeconds: 15
        successThreshold: 1
        timeoutSeconds: 1
      name: sipgs-backend-bff-simulacao-des
      ports:
        - containerPort: 8080
          name: port
          protocol: TCP
      readinessProbe:
        failureThreshold: 3
        httpGet:
          path: /q/health/ready
          port: 8080
          scheme: HTTP
        initialDelaySeconds: 15
        periodSeconds: 15
        successThreshold: 1
        timeoutSeconds: 1
      resources:
        limits:
          cpu: 500m
          memory: 512Mi
        requests:
          cpu: 250m
          memory: 256Mi
      terminationMessagePath: /dev/termination-log
      terminationMessagePolicy: File
      volumeMounts:
        - mountPath: /var/run/secrets/kubernetes.io/serviceaccount
          name: kube-api-access-9flg5
          readOnly: true
  dnsPolicy: ClusterFirst
  enableServiceLinks: true
  nodeName: ip-10-249-74-214.sa-east-1.compute.internal
  preemptionPolicy: PreemptLowerPriority
  priority: 0
  restartPolicy: Always
  schedulerName: default-scheduler
  securityContext: {}
  serviceAccount: default
  serviceAccountName: default
  terminationGracePeriodSeconds: 30
  tolerations:
    - effect: NoExecute
      key: node.kubernetes.io/not-ready
      operator: Exists
      tolerationSeconds: 300
    - effect: NoExecute
      key: node.kubernetes.io/unreachable
      operator: Exists
      tolerationSeconds: 300
  volumes:
    - name: kube-api-access-9flg5
      projected:
        defaultMode: 420
        sources:
          - serviceAccountToken:
              expirationSeconds: 3607
              path: token
          - configMap:
              items:
                - key: ca.crt
                  path: ca.crt
              name: kube-root-ca.crt
          - downwardAPI:
              items:
                - fieldRef:
                    apiVersion: v1
                    fieldPath: metadata.namespace
                  path: namespace
status:
  conditions:
    - lastProbeTime: null
      lastTransitionTime: '2026-10-13T18:50:17Z'
      observedGeneration: 1
      status: 'True'
      type: PodReadyToStartContainers
    - lastProbeTime: null
      lastTransitionTime: '2026-10-13T18:50:16Z'
      observedGeneration: 1
      status: 'True'
      type: Initialized
    - lastProbeTime: null
      lastTransitionTime: '2026-10-13T18:50:41Z'
      observedGeneration: 1
      status: 'True'
      type: Ready
    - lastProbeTime: null
      lastTransitionTime: '2026-10-13T18:50:41Z'
      observedGeneration: 1
      status: 'True'
      type: ContainersReady
    - lastProbeTime: null
      lastTransitionTime: '2026-10-13T18:50:16Z'
      observedGeneration: 1
      status: 'True'
      type: PodScheduled
  containerStatuses:
    - allocatedResources:
        cpu: 250m
        memory: 256Mi
      containerID: >-
        containerd://726d373b1d4259be17c1b76cc04fdb0e5c508360d94b236ae63f6a7efd368f19
      image: >-
        027574771582.dkr.ecr.sa-east-1.amazonaws.com/sipgs/backend-bff-simulacao/sipgs-backend-bff-simulacao:38449076556
      imageID: >-
        027574771582.dkr.ecr.sa-east-1.amazonaws.com/sipgs/backend-bff-simulacao/sipgs-backend-bff-simulacao@sha256:9f8b135b540ccc5d66b86ca6ecf5cc98e5640cba8d2b2cf335fc2790952ee423
      lastState: {}
      name: sipgs-backend-bff-simulacao-des
      ready: true
      resources:
        limits:
          cpu: 500m
          memory: 512Mi
        requests:
          cpu: 250m
          memory: 256Mi
      restartCount: 0
      started: true
      state:
        running:
          startedAt: '2026-10-13T18:50:24Z'
      user:
        linux:
          gid: 0
          supplementalGroups:
            - 0
          uid: 185
      volumeMounts:
        - mountPath: /var/run/secrets/kubernetes.io/serviceaccount
          name: kube-api-access-9flg5
          readOnly: true
          recursiveReadOnly: Disabled
  hostIP: 10.249.74.214
  hostIPs:
    - ip: 10.249.74.214
  observedGeneration: 1
  phase: Running
  podIP: 100.64.119.92
  podIPs:
    - ip: 100.64.119.92
  qosClass: Burstable
  startTime: '2026-10-13T18:50:16Z'



Argo
v2.14.21+206a6ee
Argo
Applications
Settings
User Info
Documentation
Resource filters
NAME
NAME
KINDS
KINDS
SYNC STATUS
Synced
6
OutOfSync
0
HEALTH STATUS
Progressing
0
Suspended
0
Healthy
7
Degraded
1
Missing
0
Unknown
0
NAMESPACES
NAMESPACES
Show Orphaned
Applications
 sipgs-backend-bff-simulacao-des
Application Details List
Log out
APP HEALTH 
 Degraded
SYNC STATUS 

 Synced
to HEAD (e73c3e5)
Auto sync is enabled.
Author:
ansible-connect-emu[bot] <230244411+ansible-connect-emu[bot]@users.noreply.github.com> -
Comment:
Merge pull request #7 from caixagithub/update-image-sipgs-backen
LAST SYNC 

 Sync OK
to e73c3e5
Succeeded a minute ago (Wed Oct 14 2026 09:31:09 GMT-0300)
Author:
ansible-connect-emu[bot] <230244411+ansible-connect-emu[bot]@users.noreply.github.com> -
Comment:
Merge pull request #7 from caixagithub/update-image-sipgs-backen
APP CONDITIONS
 1 Warning
Previous12Next
Items per page: 10 
NAME
GROUP/KIND
SYNC ORDER
NAMESPACE
CREATED AT
STATUS
Pod
pod
sipgs-backend-bff-simulacao-des-745dbb95bb-n794n
Pod
-
sipgs-backend-bff-simulacao
18 hours ago   10/13/26
 Healthy  
ReplicaSet
rs
sipgs-backend-bff-simulacao-des-745dbb95bb
apps/ReplicaSet
-
sipgs-backend-bff-simulacao
18 hours ago   10/13/26
 Healthy  
C
certificate
sipgs-backend-bff-simulacao-des-internal-srv0-cert
cert-manager.io/Certificate
-
istio-ingress
20 hours ago   10/13/26
 Degraded   Synced
ReplicaSet
rs
sipgs-backend-bff-simulacao-des-8f4768f5
apps/ReplicaSet
-
sipgs-backend-bff-simulacao
20 hours ago   10/13/26
 Healthy  
ReplicaSet
rs
sipgs-backend-bff-simulacao-des-844cbb5c66
apps/ReplicaSet
-
sipgs-backend-bff-simulacao
21 hours ago   10/13/26
 Healthy  
Endpoints
ep
sipgs-backend-bff-simulacao-des
Endpoints
-
sipgs-backend-bff-simulacao
a day ago   10/13/26
Service
svc
sipgs-backend-bff-simulacao-des
Service
-
sipgs-backend-bff-simulacao
a day ago   10/13/26
 Healthy   Synced
Deployment
deploy
sipgs-backend-bff-simulacao-des
apps/Deployment
-
sipgs-backend-bff-simulacao
a day ago   10/13/26
 Healthy   Synced
ReplicaSet
rs
sipgs-backend-bff-simulacao-des-849f94df8
apps/ReplicaSet
-
sipgs-backend-bff-simulacao
a day ago   10/13/26
 Healthy  
ConfigMap
cm
cm-sipgs-backend-bff-simulacao
ConfigMap
-
sipgs-backend-bff-simulacao
a day ago   10/13/26
 Synced
Previous12Next
Items per page: 10 

Podpod
sipgs-backend-bff-simulacao-des-745dbb95bb-n794n
 SUMMARY EVENTS LOGS
No events available



Argo
v2.14.21+206a6ee
Argo
Applications
Settings
User Info
Documentation
Resource filters
NAME
NAME
KINDS
KINDS
SYNC STATUS
Synced
6
OutOfSync
0
HEALTH STATUS
Progressing
0
Suspended
0
Healthy
7
Degraded
1
Missing
0
Unknown
0
NAMESPACES
NAMESPACES
Show Orphaned
Applications
 sipgs-backend-bff-simulacao-des
Application Details List
Log out
APP HEALTH 
 Degraded
SYNC STATUS 

 Synced
to HEAD (e73c3e5)
Auto sync is enabled.
Author:
ansible-connect-emu[bot] <230244411+ansible-connect-emu[bot]@users.noreply.github.com> -
Comment:
Merge pull request #7 from caixagithub/update-image-sipgs-backen
LAST SYNC 

 Sync OK
to e73c3e5
Succeeded a few seconds ago (Wed Oct 14 2026 09:32:50 GMT-0300)
Author:
ansible-connect-emu[bot] <230244411+ansible-connect-emu[bot]@users.noreply.github.com> -
Comment:
Merge pull request #7 from caixagithub/update-image-sipgs-backen
APP CONDITIONS
 1 Warning
Previous12Next
Items per page: 10 
NAME
GROUP/KIND
SYNC ORDER
NAMESPACE
CREATED AT
STATUS
Pod
pod
sipgs-backend-bff-simulacao-des-745dbb95bb-n794n
Pod
-
sipgs-backend-bff-simulacao
18 hours ago   10/13/26
 Healthy  
ReplicaSet
rs
sipgs-backend-bff-simulacao-des-745dbb95bb
apps/ReplicaSet
-
sipgs-backend-bff-simulacao
18 hours ago   10/13/26
 Healthy  
C
certificate
sipgs-backend-bff-simulacao-des-internal-srv0-cert
cert-manager.io/Certificate
-
istio-ingress
20 hours ago   10/13/26
 Degraded   Synced
ReplicaSet
rs
sipgs-backend-bff-simulacao-des-8f4768f5
apps/ReplicaSet
-
sipgs-backend-bff-simulacao
20 hours ago   10/13/26
 Healthy  
ReplicaSet
rs
sipgs-backend-bff-simulacao-des-844cbb5c66
apps/ReplicaSet
-
sipgs-backend-bff-simulacao
21 hours ago   10/13/26
 Healthy  
Endpoints
ep
sipgs-backend-bff-simulacao-des
Endpoints
-
sipgs-backend-bff-simulacao
a day ago   10/13/26
Service
svc
sipgs-backend-bff-simulacao-des
Service
-
sipgs-backend-bff-simulacao
a day ago   10/13/26
 Healthy   Synced
Deployment
deploy
sipgs-backend-bff-simulacao-des
apps/Deployment
-
sipgs-backend-bff-simulacao
a day ago   10/13/26
 Healthy   Synced
ReplicaSet
rs
sipgs-backend-bff-simulacao-des-849f94df8
apps/ReplicaSet
-
sipgs-backend-bff-simulacao
a day ago   10/13/26
 Healthy  
ConfigMap
cm
cm-sipgs-backend-bff-simulacao
ConfigMap
-
sipgs-backend-bff-simulacao
a day ago   10/13/26
 Synced
Previous12Next
Items per page: 10 

C
certificate
sipgs-backend-bff-simulacao-des-internal-srv0-cert
 SUMMARY EVENTS
KIND
Certificate
NAME
sipgs-backend-bff-simulacao-des-internal-srv0-cert   
NAMESPACE
istio-ingress   
CREATED AT
10/13/2026 13:50:25 (20 hours ago)
STATUS
 Synced
HEALTH
 Degraded
HEALTH DETAILS
Issuing certificate as Secret does not exist
LINKS
Live Manifest DiffDesired Manifest

Hide Managed FieldsEnable Word Wrap
123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657
apiVersion: cert-manager.io/v1
kind: Certificate
metadata:
  annotations:
    kubectl.kubernetes.io/last-applied-configuration: >
      {"apiVersion":"cert-manager.io/v1","kind":"Certificate","metadata":{"annotations":{},"labels":{"app.kubernetes.io/instance":"sipgs-backend-bff-simulacao-des"},"name":"sipgs-backend-bff-simulacao-des-internal-srv0-cert","namespace":"istio-ingress"},"spec":{"dnsNames":["sipgs-backend-bff-simulacao.apl.des.private.aws"],"duration":"4320h","issuerRef":{"group":"awsp





