Bom dia, Vinicius! Tudo bem, e com você?

Pelo que levantamos, o agente no caddeapllx2501 está configurado e comunicando com o servidor. Os pontos pendentes são:

Regra de firewall cxextrlx038 (10.192.224.54) → caddeapllx2501 (10.116.200.250), TCP 7016, que vocês ficaram de solicitar. Sem ela, o Control-M não consegue entregar o job para a máquina. Podem me passar o número da REQ para eu acompanhar?
Job em "Wait Condition" com o "Run Now" rejeitado (CTM5366 Bypass command is rejected). Isso é configuração e permissão do job no servidor Control-M. Vale verificar em "Waiting Info" quais condições estão pendentes, ou pedir ao administrador do Control-M para liberar o bypass.
Script: o job segue chamando simil-precificacao-rotinas-batch.sh. Se o script foi renomeado no repositório, é preciso rodar a release de novo para publicá-lo em /producao.

Assim que a regra for aplicada, faço o monitoramento no servidor durante o teste. Se ainda assim quiserem uma agenda, podem falar com o meu gestor, Flávio Gagliardi.
