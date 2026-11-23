Atendimento: falha na release do SIMPI-batch-log-auditoria (EC DES), no passo "Cadastrar Servidor no Satellite" (release 559336, STRY00174869).

Diagnóstico: o servidor caddeapllx1668 estava registrado no Satellite com o ambiente de produção (PRD/CV-RHEL-7). Por isso o playbook não refez o registro e tentou habilitar o repositório CEF_Zabbix_Zabbix_6_REDHAT_7, que não existe nesse ambiente, e falhou com "não corresponde a um ID de repositório válido" (rc 1).

Ação realizada: executado subscription-manager clean no servidor para remover o registro local. No novo deploy, o playbook registrou o servidor de novo, já no ambiente correto.

Resultado: release 12 executada em 23/11/2026 às 10:09, concluída com sucesso, e o passo do Satellite passou. Confirmado no servidor: ambiente DEV/CV-RHEL-7.

Observação: o cadastro antigo do servidor (ambiente PRD) pode ter permanecido no Satellite como duplicado. Solicitada ao time do Satellite a remoção, sem impacto no deploy.

Atendimento encerrado com sucesso.
