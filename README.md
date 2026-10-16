Encaminhamento à CETEL – Liberação de regra de firewall (SIMPF DES → SIGCT)

Solicitação: criar regra de firewall de rede permitindo:

Origem	Destino	Porta
10.116.220.37 (egress IP do namespace simpf-des, cluster OKD NPRD)	10.116.83.19 (sctdeapllx0018.df.caixa)	8443/TCP

Sugere-se espelhar a regra já existente para a origem 10.116.220.90 (egress IP do namespace simpf-tqs), que acessa o mesmo destino normalmente.

Contexto: o backend do SIMPF em DES não consegue se comunicar com o SIGCT. A conexão termina em HttpHostConnectException: Connection timed out, falha registrada desde 23/09/2026 e ainda ativa em 16/10/2026. O mesmo recurso funciona no ambiente TQS.

Evidências coletadas em 16/10/2026:

Origem efetiva confirmada: o namespace simpf-des possui egress IP fixo 10.116.220.37 (oc get netnamespace), e o simpf-tqs usa 10.116.220.90.
Testes de conectividade TCP:
Origem	Destino	Resultado
Pod simpf-backend-des (10.116.220.37)	10.116.83.19:8443	Timeout (sem resposta)
Pod simpf-backend-des (10.116.220.37)	10.116.83.19:22	OK
Pod simpf-backend-tqs (10.116.220.90)	10.116.83.19:8443	OK
Estação do analista	10.116.83.19:8443	OK
DNS: de dentro do pod DES, sctdeapllx0018.df.caixa resolve corretamente para 10.116.83.19.
Servidor de destino (sctdeapllx0018):
Porta 8443 em escuta em todas as interfaces (netstat: :::8443 LISTEN), atendida pelo JBoss EAP 6.4.
Sem firewall local: iptables com chain INPUT vazia e policy ACCEPT.
Captura de pacotes no destino (tcpdump -ni any host 10.116.220.37), feita durante os testes:
Porta 22: o handshake completo chega ao servidor.
     10.116.220.37.42722 > 10.116.83.19.ssh: Flags [S]
     10.116.83.19.ssh > 10.116.220.37.42722: Flags [S.]
     10.116.220.37.42722 > 10.116.83.19.ssh: Flags [.]
Porta 8443: nenhum pacote da origem 10.116.220.37 chegou ao servidor.

Conclusão: a origem 10.116.220.37 alcança o servidor (porta 22 OK), o serviço na 8443 está ativo e sem filtro local, e a mesma porta é acessível pela origem do TQS. O descarte dos pacotes 10.116.220.37 → 10.116.83.19:8443 ocorre no firewall de rede, por ausência de regra para essa origem.
