. Adicionar o volume do secret
 
 
 
oc patch dc sihdg-angular18-tqs --type=json -p='[
  {
    "op":"add",
    "path":"/spec/template/spec/volumes/-",
    "value":{
      "name":"truststore-caixa",
      "secret":{
        "secretName":"caixa-truststore-acteste-nprd"
      }
    }
  }
]'
2. Adicionar o mount no container principal
 
 
 
oc patch dc sihdg-angular18-tqs --type=json -p='[
  {
    "op":"add",
    "path":"/spec/template/spec/containers/0/volumeMounts/-",
    "value":{
      "name":"truststore-caixa",
      "mountPath":"/deployments/ac_caixav4.jks",
      "subPath":"caixa-truststore-acteste-nprd.jks"
    }
  }
]'
