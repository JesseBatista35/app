app:
  name: siarx-backend-autoridade-registro-des
project:
  name: des
labels:
  appName: siarx-backend-autoridade-registro
  environment: des
source:
  repo: "https://github.com/caixagithub/siarx-backend-autoridade-registro-infranprd"
  path: des
sourcevar:
  repo: "https://github.com/caixagithub/siarx-globalnprd"
  path: des
  values: global.yaml  
cluster:
  destination:  
    name: aks-siarx-nprd
    namespace: siarx-backend-autoridade-registro


    esse  acima foi o que eu ajusteri


gitops/apps/siarx-backend-certificados/des
/config.yaml


    app:
  name: siarx-backend-certificados-hmp
project:
  name: hmp
labels:
  appName: siarx-backend-certificados
  environment: hmp
source:
  repo: "https://github.com/caixagithub/siarx-backend-certificados-infranprd"
  path: hmp
sourcevar:
  repo: "https://github.com/caixagithub/siarx-globalnprd"
  path: hmp
  values: global.yaml  
cluster:
  destination:  
    name: aks-siarx-nprd
    namespace: siarx-backend-certificados
