Também vale mandar ao Paulo os números REQ000146953662 / REQ000146953837 como modelo atualizado do VIP.
 
Descrição da solicitação: Criação de VIP para a URL sigsj-intranet.des.caixa

Apontamento/Balanceamento para o servidor:
IP: 10.116.194.179
HOST: caddeapllx955.agil.nprd.caixa.gov.br

http://sigsj-intranet.des.caixa
Porta 80

Favor instalar o certificado da requisição abaixo:
WO0000082153634 REQ000146906949 - sigsj-intranet.des.caixa

https://sigsj-intranet.des.caixa
Qual o tipo de serviço?: Alterar configurações em balanceador
Detalhe do serviço: VIP
Atividade a ser executada: Solicitar inclusão de VIP
Qual é o nome do sistema/serviço?: 
Qual é o VIP de acesso ao sistema/serviço?: 
Qual é o FQDN de acesso ao sistema/serviço?: 


1. Segue script para criação do VIP solicitado:

=> IP do VIP alocado: 10.116.180.8.

OBS.: Lembrando que o certificado será instalado somente no VIP, entregando ao servidor na porta 80.


((( PLANO DE EXECUÇÃO )))

CADDEAPRLB003-1 (10.122.82.100)
add ns ip 10.116.180.8 255.255.255.255 -type VIP -snmp DISABLED -hostRoute ENABLED
add server LB_SR_CADDEAPLLX955 10.116.194.179
add serviceGroup LB_SG_10.116.180.8_HTTP_80 HTTP -maxClient 0 -maxReq 0 -cip DISABLED -usip NO -useproxyport YES -cltTimeout 180 -svrTimeout 360 -CKA NO -TCPB NO -CMP NO -netProfile NETPROF_SNAT
add lb vserver LB_VS_10.116.180.8_HTTP_80 HTTP 10.116.180.8 80 -persistenceType NONE -timeout 15 -cltTimeout 180 -comment siccp-intra.esteiras.hmp.caixa -RHIstate ACTIVE
add lb vserver LB_VS_10.116.180.8_SSL_443 SSL 10.116.180.8 443 -persistenceType SOURCEIP -timeout 15 -cltTimeout 180 -comment siccp-intra.esteiras.hmp.caixa -RHIstate ACTIVE
bind lb vserver LB_VS_10.116.180.8_HTTP_80 LB_SG_ALWAYS_UP_HTTP_80
bind lb vserver LB_VS_10.116.180.8_SSL_443 LB_SG_10.116.180.8_HTTP_80
bind lb vserver LB_VS_10.116.180.8_HTTP_80 -policyName http_to_https_pol -priority 1 -gotoPriorityExpression END -type REQUEST
bind serviceGroup LB_SG_10.116.180.8_HTTP_80 LB_SR_CADDEAPLLX955 80
bind serviceGroup LB_SG_10.116.180.8_HTTP_80 -monitorName CEF_TCP_DEFAULT_MON
set ssl vserver LB_VS_10.116.180.8_SSL_443 -sslProfile CEF_SSL_PROFILE_FRONTEND_SECURITY
save ns config


((( PLANO DE VALIDAÇÃO )))

CADDEAPRLB003-1 (10.122.82.100)

sh lb vserver LB_VS_10.116.180.8_SSL_443


((( PLANO DE ROLLBACK )))

rm lb vserver LB_VS_10.116.180.8_HTTP_80 HTTP
rm lb vserver LB_VS_10.116.180.8_SSL_443 SSL
rm serviceGroup LB_SG_10.116.180.8_HTTP_80 HTTP
rm server LB_SR_CADDEAPLLX955 10.116.194.179
rm ns ip 10.116.180.8
save ns config


2. A equipe de segurança precisa gerar e disponibilizar o certificado no balanceado para que possamos aplicar ao novo VIP criado.


Atenciosamente,
Valdir Soares
TELEDATA\CETEL\REDE

é essa mesmo da pra pedir aqui

