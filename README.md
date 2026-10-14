Prezados,

Analisamos o ambiente do SIMCN em DES (JBoss EAP em modo domain, server-group simcn).

Diagnóstico: o pacote é gerado corretamente pelo Jenkins, mas a etapa de deploy falhava. O undeploy da versão anterior era recusado pelo domain (WFLYCTL0063, rollback originado no host sbrdeapllx112) e, por isso, o deploy da nova versão era rejeitado (“SIMCN already exists in the deployment repository”). Com isso, a versão antiga (simcn-2.26.3.4.0-b2260.ear) permanecia ativa e as alterações não eram refletidas.

Ação realizada: removemos manualmente o deployment SIMCN do server-group simcn e do repositório de conteúdo do domain, liberando o ambiente para um novo deploy. A aplicação está fora do ar em DES até a nova execução do job.

Solicitação: por gentileza, executem novamente o job SIMCN no Jenkins, na branch desejada (último build em sprint/parcial110), e validem:

se o build termina com SUCCESS;
se as alterações esperadas estão refletidas na aplicação.
