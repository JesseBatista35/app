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
