
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
5
OutOfSync
1
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

 OutOfSync
from HEAD (e73c3e5)
Auto sync is enabled.
Author:
ansible-connect-emu[bot] <230244411+ansible-connect-emu[bot]@users.noreply.github.com> -
Comment:
Merge pull request #7 from caixagithub/update-image-sipgs-backen
LAST SYNC 

 Sync OK
to e73c3e5
Succeeded 4 minutes ago (Wed Oct 14 2026 09:26:06 GMT-0300)
Author:
ansible-connect-emu[bot] <230244411+ansible-connect-emu[bot]@users.noreply.github.com> -
Comment:
Merge pull request #7 from caixagithub/update-image-sipgs-backen
APP CONDITIONS
 2 Warnings
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
 OutOfSync
Previous12Next
Items per page: 10 

Podpod
sipgs-backend-bff-simulacao-des-745dbb95bb-n794n
 SUMMARY EVENTS LOGS
containing
INFO exec -a "java" java -XX:MaxRAMPercentage=80.0 -XX:+UseParallelGC -XX:MinHeapFreeRatio=10 -XX:MaxHeapFreeRatio=20 -XX:GCTimeRatio=4 -XX:AdaptiveSizePolicyWeight=90 -XX:+ExitOnOutOfMemoryError -Dquarkus.http.host=0.0.0.0 -Djava.util.logging.manager=org.jboss.logmanager.LogManager -cp "." -jar /deployments/quarkus-run.jar
INFO running in /deployments
__  ____  __  _____   ___  __ ____  ______
 --/ __ \/ / / / _ | / _ \/ //_/ / / / __/
 -/ /_/ / /_/ / __ |/ , _/ ,< / /_/ /\ \
--\___\_\____/_/ |_/_/|_/_/|_|\____/___/
2026-10-13 18:50:34,046 INFO  [io.quarkus] (main) backend-bff-simulacao 1.0.0 on JVM (powered by Quarkus 3.36.1) started in 9.097s. Listening on: http://0.0.0.0:8080
2026-10-13 18:50:34,047 INFO  [io.quarkus] (main) Profile prod activated.
2026-10-13 18:50:34,048 INFO  [io.quarkus] (main) Installed features: [agroal, cdi, hibernate-orm, hibernate-orm-panache, jdbc-h2, narayana-jta, rest, rest-jackson, smallrye-context-propagation, smallrye-health, smallrye-openapi, vertx]




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
5
OutOfSync
1
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

 OutOfSync
from HEAD (e73c3e5)
Auto sync is enabled.
Author:
ansible-connect-emu[bot] <230244411+ansible-connect-emu[bot]@users.noreply.github.com> -
Comment:
Merge pull request #7 from caixagithub/update-image-sipgs-backen
LAST SYNC 

 Sync OK
to e73c3e5
Succeeded 4 minutes ago (Wed Oct 14 2026 09:26:06 GMT-0300)
Author:
ansible-connect-emu[bot] <230244411+ansible-connect-emu[bot]@users.noreply.github.com> -
Comment:
Merge pull request #7 from caixagithub/update-image-sipgs-backen
APP CONDITIONS
 2 Warnings
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
 OutOfSync
Previous12Next
Items per page: 10 

Podpod
sipgs-backend-bff-simulacao-des-745dbb95bb-n794n
 SUMMARY EVENTS LOGS
KIND
Pod
NAME
sipgs-backend-bff-simulacao-des-745dbb95bb-n794n   
NAMESPACE
sipgs-backend-bff-simulacao   
CREATED AT
10/13/2026 15:50:16 (18 hours ago)
IMAGES
027574771582.dkr.ecr.sa-east-1.amazonaws.com/sipgs/backend-bff-simulacao/sipgs-backend-bff-simulacao:38449076556
STATE
Running
CONTAINER STATE
sipgs-backend-bff-simulacao-des
Container is running. It is started and ready.
HEALTH
 Healthy
LINKS
Live Manifest

Hide Managed FieldsEnable Word Wrap
123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100101102103104105106107108109110111112113114115116117118119120121122123124125126127128129130131132133134135136137138139140141142143144145146147148149150151152153154155156157158159160161162163164165166167168169170171172173174175176177178179180181182183184
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

