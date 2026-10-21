Ao executar o pipeline de APIM do repositório caixagithub/sidpn-api-intra-credito-emprestimos, a 
execução falhou na task de instalar o AZ CLI, conforme o  link detalhado na REQ.


Prezados, 

Esclarecemos que erro similar aconteceu na execução abaixo de CI/CD:

https://github.com/caixagithub/sidpn-api-intra-credito-emprestimos/actions/runs/39474461093/job/118809554569

Ambos os erros sao decorrentes da pendencia de instalação do pacote ca-certificates-java (“1 not fully installed or removed”), pois não é possível salvar o repositório de certificados Java em /etc/ssl/certs/java/cacerts, pq ele não encontra esse diretório no runner.

Solicitamos priorização da demanda, uma vez que não estamos conseguindo realizar os deploys.

Atenciosamente,

Laís Brum Romera Caraciki
Coordenadora de Projetos Matriz
Box Open Finance


Skip to content
GitHub Enterprise
Users managed by Caixa Economica Federal
caixagithub
sidpn-api-intra-credito-emprestimos
Repository navigation
Code
Issues
1
 (1)
Pull requests
Actions
Projects
Wiki
Security and quality
15
 (15)
Insights
Settings
CI/CD Workflow
CI/CD_caixagithub/sidpn-api-intra-credito-emprestimos_develop_39493089284.9 #9
All jobs
Run details
Annotations
1 error and 1 warning
CI_DES / ArgoCD_Deploy / ArgoCD_Deploy (DES)
failed 16 hours ago in 2m 12s
Search logs
12s
1s
0s
0s
0s
0s
0s
0s
0s
0s
0s
0s
0s
1m 40s
0s
6s
0s
0s
0s
5s
Run caixagithub/DevSecOps-Actions/.github/util/install_jq_curl@main
  env:
    APIM_VERSIONAPI: 
    APIM_displaynameAPI: 
    APIM_PATH: 
    APIM_SWAGGERPATH: 
    APIM_TAGSAPI: 
    APIM_POLICIESALLOPERATIONSPATH: 
    AZ_INSTALL_STATUS: none
    AZ_VERSION: latest
    INSTALL_PREREQUISITES: true
    AZ_LATEST_VERSION: 2.91.0
    environment: des
    repository_suffix: infranprd
Install JQ CURL
5s
Run sudo apt-get update && sudo apt-get install -y curl jq
    sudo apt-get update && sudo apt-get install -y curl jq
    shell: /usr/bin/bash --noprofile --norc -e -o pipefail {0}
    env:
      APIM_VERSIONAPI: 
      APIM_displaynameAPI: 
      APIM_PATH: 
      APIM_SWAGGERPATH: 
      APIM_TAGSAPI: 
      APIM_POLICIESALLOPERATIONSPATH: 
      AZ_INSTALL_STATUS: none
      AZ_VERSION: latest
      INSTALL_PREREQUISITES: true
      AZ_LATEST_VERSION: 2.91.0
      environment: des
      repository_suffix: infranprd
  Hit:1 https://cli.github.com/packages stable InRelease
  Hit:2 https://deb.nodesource.com/node_24.x nodistro InRelease
  Hit:3 https://packages.microsoft.com/repos/azure-cli noble InRelease
  Hit:4 https://packages.microsoft.com/ubuntu/24.04/prod noble InRelease
  Hit:6 https://dl.google.com/linux/chrome-stable/deb stable InRelease
  Hit:5 https://prod-cdn.packages.k8s.io/repositories/isv:/kubernetes:/core:/stable:/v1.34/deb  InRelease
  Hit:7 http://security.ubuntu.com/ubuntu noble-security InRelease
  Hit:8 http://archive.ubuntu.com/ubuntu noble InRelease
  Hit:10 http://archive.ubuntu.com/ubuntu noble-updates InRelease
  Hit:11 http://archive.ubuntu.com/ubuntu noble-backports InRelease
  Hit:12 https://ppa.launchpadcontent.net/git-core/ppa/ubuntu noble InRelease
  Hit:13 https://ppa.launchpadcontent.net/mozillateam/ppa/ubuntu noble InRelease
  Hit:9 https://packages.buildkite.com/helm-linux/helm-debian/any any InRelease
  Reading package lists...
  Reading package lists...
  Building dependency tree...
  Reading state information...
  curl is already the newest version (8.5.0-2ubuntu10.16).
  jq is already the newest version (1.7.1-3ubuntu0.24.04.2).
  0 upgraded, 0 newly installed, 0 to remove and 92 not upgraded.
  1 not fully installed or removed.
  After this operation, 0 B of additional disk space will be used.
  Setting up ca-certificates-java (20240118) ...
  Adding debian:ACCVRAIZ1.pem
  Adding debian:AC_RAIZ_FNMT-RCM.pem
  Adding debian:AC_RAIZ_FNMT-RCM_SERVIDORES_SEGUROS.pem
  Adding debian:ANF_Secure_Server_Root_CA.pem
  Adding debian:Actalis_Authentication_Root_CA.pem
  Adding debian:Amazon_Root_CA_1.pem
  Adding debian:Amazon_Root_CA_2.pem
  Adding debian:Amazon_Root_CA_3.pem
  Adding debian:Amazon_Root_CA_4.pem
  Adding debian:Atos_TrustedRoot_Root_CA_ECC_TLS_2021.pem
  Adding debian:Atos_TrustedRoot_Root_CA_RSA_TLS_2021.pem
  Adding debian:Autoridad_de_Certificacion_Firmaprofesional_CIF_A62634068.pem
  Adding debian:BJCA_Global_Root_CA1.pem
  Adding debian:BJCA_Global_Root_CA2.pem
  Adding debian:Buypass_Class_2_Root_CA.pem
  Adding debian:Buypass_Class_3_Root_CA.pem
  Adding debian:CA_Disig_Root_R2.pem
  Adding debian:CFCA_EV_ROOT.pem
  Adding debian:COMODO_ECC_Certification_Authority.pem
  Adding debian:COMODO_RSA_Certification_Authority.pem
  Adding debian:Certainly_Root_E1.pem
  Adding debian:Certainly_Root_R1.pem
  Adding debian:Certigna_Root_CA.pem
  Adding debian:Certum_EC-384_CA.pem
  Adding debian:Certum_Trusted_Network_CA.pem
  Adding debian:Certum_Trusted_Network_CA_2.pem
  Adding debian:Certum_Trusted_Root_CA.pem
  Adding debian:D-TRUST_BR_Root_CA_1_2020.pem
  Adding debian:D-TRUST_BR_Root_CA_2_2023.pem
  Adding debian:D-TRUST_EV_Root_CA_1_2020.pem
  Adding debian:D-TRUST_EV_Root_CA_2_2023.pem
  Adding debian:D-TRUST_Root_Class_3_CA_2_2009.pem
  Adding debian:D-TRUST_Root_Class_3_CA_2_EV_2009.pem
  Adding debian:DigiCert_Assured_ID_Root_G2.pem
  Adding debian:DigiCert_Assured_ID_Root_G3.pem
  Adding debian:DigiCert_Global_Root_G2.pem
  Adding debian:DigiCert_Global_Root_G3.pem
  Adding debian:DigiCert_TLS_ECC_P384_Root_G5.pem
  Adding debian:DigiCert_TLS_RSA4096_Root_G5.pem
  Adding debian:DigiCert_Trusted_Root_G4.pem
  Adding debian:GDCA_TrustAUTH_R5_ROOT.pem
  Adding debian:GTS_Root_R1.pem
  Adding debian:GTS_Root_R3.pem
  Adding debian:GTS_Root_R4.pem
  Adding debian:GlobalSign_ECC_Root_CA_-_R4.pem
  Adding debian:GlobalSign_ECC_Root_CA_-_R5.pem
  Adding debian:GlobalSign_Root_CA_-_R3.pem
  Adding debian:GlobalSign_Root_CA_-_R6.pem
  Adding debian:GlobalSign_Root_E46.pem
  Adding debian:GlobalSign_Root_R46.pem
  Adding debian:Go_Daddy_Root_Certificate_Authority_-_G2.pem
  Adding debian:HARICA_TLS_ECC_Root_CA_2021.pem
  Adding debian:HARICA_TLS_RSA_Root_CA_2021.pem
  Adding debian:Hellenic_Academic_and_Research_Institutions_ECC_RootCA_2015.pem
  Adding debian:Hellenic_Academic_and_Research_Institutions_RootCA_2015.pem
  Adding debian:HiPKI_Root_CA_-_G1.pem
  Adding debian:Hongkong_Post_Root_CA_3.pem
  Adding debian:ISRG_Root_X1.pem
  Adding debian:ISRG_Root_X2.pem
  Adding debian:IdenTrust_Commercial_Root_CA_1.pem
  Adding debian:IdenTrust_Public_Sector_Root_CA_1.pem
  Adding debian:Izenpe.com.pem
  Adding debian:Microsec_e-Szigno_Root_CA_2009.pem
  Adding debian:Microsoft_ECC_Root_Certificate_Authority_2017.pem
  Adding debian:Microsoft_RSA_Root_Certificate_Authority_2017.pem
  Adding debian:NAVER_Global_Root_Certification_Authority.pem
  Adding debian:NetLock_Arany_=Class_Gold=_Főtanúsítvány.pem
  Adding debian:OISTE_Server_Root_ECC_G1.pem
  Adding debian:OISTE_Server_Root_RSA_G1.pem
  Adding debian:OISTE_WISeKey_Global_Root_GB_CA.pem
  Adding debian:OISTE_WISeKey_Global_Root_GC_CA.pem
  Adding debian:QuoVadis_Root_CA_1_G3.pem
  Adding debian:QuoVadis_Root_CA_2_G3.pem
  Adding debian:QuoVadis_Root_CA_3_G3.pem
  Adding debian:SECOM_TLS_ECC_Root_CA_2024.pem
  Adding debian:SECOM_TLS_RSA_Root_CA_2024.pem
  Adding debian:SSL.com_EV_Root_Certification_Authority_ECC.pem
  Adding debian:SSL.com_EV_Root_Certification_Authority_RSA_R2.pem
  Adding debian:SSL.com_Root_Certification_Authority_ECC.pem
  Adding debian:SSL.com_Root_Certification_Authority_RSA.pem
  Adding debian:SSL.com_TLS_ECC_Root_CA_2022.pem
  Adding debian:SSL.com_TLS_RSA_Root_CA_2022.pem
  Adding debian:SZAFIR_ROOT_CA2.pem
  Adding debian:Sectigo_Public_Server_Authentication_Root_E46.pem
  Adding debian:Sectigo_Public_Server_Authentication_Root_R46.pem
  Adding debian:SecureSign_Root_CA14.pem
  Adding debian:SecureSign_Root_CA15.pem
  Adding debian:Security_Communication_ECC_RootCA1.pem
  Adding debian:Security_Communication_RootCA2.pem
  Adding debian:Starfield_Root_Certificate_Authority_-_G2.pem
  Adding debian:Starfield_Services_Root_Certificate_Authority_-_G2.pem
  Adding debian:SwissSign_RSA_TLS_Root_CA_2022_-_1.pem
  Adding debian:T-TeleSec_GlobalRoot_Class_2.pem
  Adding debian:T-TeleSec_GlobalRoot_Class_3.pem
  Adding debian:TUBITAK_Kamu_SM_SSL_Kok_Sertifikasi_-_Surum_1.pem
  Adding debian:TWCA_CYBER_Root_CA.pem
  Adding debian:TWCA_Global_Root_CA.pem
  Adding debian:TWCA_Root_Certification_Authority.pem
  Adding debian:Telekom_Security_TLS_ECC_Root_2020.pem
  Adding debian:Telekom_Security_TLS_RSA_Root_2023.pem
  Adding debian:Telia_EC_TLS_Root_CA_v3.pem
  Adding debian:Telia_RSA_TLS_Root_CA_v3.pem
  Adding debian:Telia_Root_CA_v2.pem
  Adding debian:TrustAsia_Global_Root_CA_G3.pem
  Adding debian:TrustAsia_Global_Root_CA_G4.pem
  Adding debian:TrustAsia_TLS_ECC_Root_CA.pem
  Adding debian:TrustAsia_TLS_RSA_Root_CA.pem
  Adding debian:TunTrust_Root_CA.pem
  Adding debian:UCA_Extended_Validation_Root.pem
  Adding debian:UCA_Global_G2_Root.pem
  Adding debian:USERTrust_ECC_Certification_Authority.pem
  Adding debian:USERTrust_RSA_Certification_Authority.pem
  Adding debian:certSIGN_Root_CA_G2.pem
  Adding debian:e-Szigno_Root_CA_2017.pem
  Adding debian:e-Szigno_TLS_Root_CA_2023.pem
  Adding debian:emSign_ECC_Root_CA_-_C3.pem
  Adding debian:emSign_Root_CA_-_C1.pem
  Adding debian:emSign_Root_CA_-_G1.pem
  Adding debian:vTrus_ECC_Root_CA.pem
  Adding debian:vTrus_Root_CA.pem
  org.debian.security.UnableToSaveKeystoreException: There was a problem saving the new Java keystore.
  	at org.debian.security.KeyStoreHandler.save(KeyStoreHandler.java:86)
  	at org.debian.security.UpdateCertificates.finish(UpdateCertificates.java:108)
  	at org.debian.security.UpdateCertificates.main(UpdateCertificates.java:54)
  Caused by: java.io.FileNotFoundException: /etc/ssl/certs/java/cacerts (No such file or directory)
  	at java.base/java.io.FileOutputStream.open0(Native Method)
  	at java.base/java.io.FileOutputStream.open(FileOutputStream.java:289)
  	at java.base/java.io.FileOutputStream.<init>(FileOutputStream.java:230)
  	at java.base/java.io.FileOutputStream.<init>(FileOutputStream.java:118)
  	at org.debian.security.KeyStoreHandler.save(KeyStoreHandler.java:82)
  	... 2 more
  dpkg: error processing package ca-certificates-java (--configure):
   installed ca-certificates-java package post-installation script subprocess returned error exit status 1
  Errors were encountered while processing:
   ca-certificates-java
  E: Sub-process /usr/bin/dpkg returned an error code (1)
  Error: Process completed with exit code 100.
0s
1s
0s
0s
0s
0s
0s
0s
0s
0s
0s
0s
0s
0s
0s
0s
0s
0s
0s
0s
1s
0s
0s







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
12
OutOfSync
0
HEALTH STATUS
Progressing
0
Suspended
0
Healthy
6
Degraded
0
Missing
0
Unknown
0
Show Orphaned
Applications
 sidpn-api-intra-credito-emprestimos-des
Application Details List
Log out
APP HEALTH 
 Healthy
SYNC STATUS 

 Synced
to HEAD (e4dcba0)
Auto sync is enabled.
Author:
ansible-connect-emu[bot] <230244411+ansible-connect-emu[bot]@users.noreply.github.com> -
Comment:
Merge pull request #7 from caixagithub/update-image-sidpn-api-in
LAST SYNC 

 Sync OK
to e4dcba0
Succeeded 21 hours ago (Tue Oct 20 2026 12:55:20 GMT-0300)
Author:
ansible-connect-emu[bot] <230244411+ansible-connect-emu[bot]@users.noreply.github.com> -
Comment:
Merge pull request #7 from caixagithub/update-image-sidpn-api-in
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
sidpn-api-intra-credito-emprestimos-des-7df9d69f5d-wv79l
Pod
-
sidpn-api-intra-credito-emprestimos
21 hours ago   10/20/26
 Healthy  
ReplicaSet
rs
sidpn-api-intra-credito-emprestimos-des-7df9d69f5d
apps/ReplicaSet
-
sidpn-api-intra-credito-emprestimos
21 hours ago   10/20/26
 Healthy  
ReplicaSet
rs
sidpn-api-intra-credito-emprestimos-des-8d948cd49
apps/ReplicaSet
-
sidpn-api-intra-credito-emprestimos
5 days ago   10/16/26
 Healthy  
ConfigMap
cm
cm-sidpn-api-intra-credito-emprestimos-des
ConfigMap
-
sidpn-api-intra-credito-emprestimos
5 days ago   10/16/26
 Synced
Endpoints
ep
sidpn-api-intra-credito-emprestimos-des
Endpoints
-
sidpn-api-intra-credito-emprestimos
5 days ago   10/16/26
Secret
secret
akv2k8s-sidpn-api-intra-credito-emprestimos-des
Secret
-
sidpn-api-intra-credito-emprestimos
5 days ago   10/16/26
Service
svc
sidpn-api-intra-credito-emprestimos-des
Service
-
sidpn-api-intra-credito-emprestimos
5 days ago   10/16/26
 Healthy   Synced
Deployment
deploy
sidpn-api-intra-credito-emprestimos-des
apps/Deployment
-
sidpn-api-intra-credito-emprestimos
5 days ago   10/16/26
 Healthy   Synced
ReplicaSet
rs
sidpn-api-intra-credito-emprestimos-des-79b47dcbcd
apps/ReplicaSet
-
sidpn-api-intra-credito-emprestimos
5 days ago   10/16/26
 Healthy  
EndpointSlice
endpointslice
sidpn-api-intra-credito-emprestimos-des-wnljv
discovery.k8s.io/EndpointSlice
-
sidpn-api-intra-credito-emprestimos
5 days ago   10/16/26
Previous12Next
Items per page: 10 

Podpod
sidpn-api-intra-credito-emprestimos-des-7df9d69f5d-wv79l
 SUMMARY EVENTS LOGS
REASON
MESSAGE
COUNT
FIRST OCCURRED
LAST OCCURRED
Pulling
Pulling image "acrcentralcaixanprd.azurecr.io/sidpn/api-intra-credito-emprestimos/sidpn-api-intra-credito-emprestimos:39451810492"
205
21h ago
Yesterday at 12:55 PM
14s ago
Today at 10:00 AM
BackOff
Back-off restarting failed container sidpn-api-intra-credito-emprestimos-des in pod sidpn-api-intra-credito-emprestimos-des-7df9d69f5d-wv79l_sidpn-api-intra-credito-emprestimos(4ff042ec-d718-49a2-a3d2-59ba97cc9ccf)
891
21h ago
Yesterday at 12:57 PM
1m ago
Today at 9:58 AM
Pulled
(combined from similar events): Successfully pulled image "acrcentralcaixanprd.azurecr.io/sidpn/api-intra-credito-emprestimos/sidpn-api-intra-credito-emprestimos:39451810492" in 101ms (101ms including waiting). Image size: 288053416 bytes.
163
20h ago
Yesterday at 1:33 PM
19m ago
Today at 9:41 AM



sidpn-api-intra-credito-emprestimos-des-7df9d69f5d-wv79l




I1021 13:00:15.725518       1 version.go:31] "version info" version="" commit="0eef8df" buildDate="2025-05-19T06:17:15Z" component="vaultenv"
I1021 13:00:15.725649       1 main.go:184] "azure key vault env injector initializing"
I1021 13:00:15.725864       1 main.go:253] "found original container command" cmd="/usr/bin/sh" args=["sh","-c","java $JAVA_OPTIONS -jar $JAVA_APP_JAR"]
I1021 13:00:15.725950       1 authentication.go:110] "checking if current auth service credentials are stale" url="http://akv2k8s-envinjector.akv2k8s.svc:80/auth/sidpn-api-intra-credito-emprestimos/sidpn-api-intra-credito-emprestimos-des-7df9d69f5d-wv79l?secret=akv2k8s-sidpn-api-intra-credito-emprestimos-des"
I1021 13:00:15.827275       1 authentication.go:123] "auth service credentials ok" url="http://akv2k8s-envinjector.akv2k8s.svc:80/auth/sidpn-api-intra-credito-emprestimos/sidpn-api-intra-credito-emprestimos-des-7df9d69f5d-wv79l?secret=akv2k8s-sidpn-api-intra-credito-emprestimos-des"
I1021 13:00:15.827595       1 authentication.go:159] "requesting azure key vault oauth token" url="https://akv2k8s-envinjector.akv2k8s.svc:9443/auth/sidpn-api-intra-credito-emprestimos/sidpn-api-intra-credito-emprestimos-des-7df9d69f5d-wv79l"
I1021 13:00:15.860537       1 authentication.go:179] "successfully received oauth token"
I1021 13:00:16.310079       1 main.go:338] "secret injected into env var" azurekeyvaultsecret="sidpn-api-intra-credito-emprestimos/akvs-cachecemprestimodes-key" env="REDIS_KEY"
I1021 13:00:16.383001       1 main.go:338] "secret injected into env var" azurekeyvaultsecret="sidpn-api-intra-credito-emprestimos/akvs-api-des-caixa-sidpn-apikey" env="API_KEY"
I1021 13:00:16.471998       1 main.go:338] "secret injected into env var" azurekeyvaultsecret="sidpn-api-intra-credito-emprestimos/akvs-cli-ser-cgr-login-des-secret" env="SSO_CLIENT_SECRET_SINCR"
I1021 13:00:16.637116       1 main.go:338] "secret injected into env var" azurekeyvaultsecret="sidpn-api-intra-credito-emprestimos/akvs-ehauditoriaobdes-containers-logs-sender-key" env="CONTAINER_LOGS_KEY"
I1021 13:00:16.724382       1 main.go:338] "secret injected into env var" azurekeyvaultsecret="sidpn-api-intra-credito-emprestimos/akvs-ehmirrormaker-ehtrilhadeauditoriaobagregadordes-sender-key" env="AUDIT_TRAIL_KEY"
I1021 13:00:16.796754       1 main.go:338] "secret injected into env var" azurekeyvaultsecret="sidpn-api-intra-credito-emprestimos/akvs-cli-ser-dpn-login-des-secret" env="SSO_CLIENT_SECRET"
I1021 13:00:16.863738       1 main.go:338] "secret injected into env var" azurekeyvaultsecret="sidpn-api-intra-credito-emprestimos/akvs-cdb-dpn-credito-des-key" env="COSMOSDB_KEY"
I1021 13:00:16.863792       1 main.go:343] "starting process with secrets in env vars" cmd="/usr/bin/sh" args=["sh","-c","java $JAVA_OPTIONS -jar $JAVA_APP_JAR"]
Picked up JAVA_TOOL_OPTIONS: -XX:InitialRAMPercentage=40 -XX:MaxRAMPercentage=60 -XX:MaxDirectMemorySize=128m -Xss256k -XX:+ExitOnOutOfMemoryError
OpenJDK 64-Bit Server VM warning: Sharing is only supported for boot loader classes because bootstrap classpath has been appended
