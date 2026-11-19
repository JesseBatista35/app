Solicitação de Liberação de Regra de Firewall – Comunicação JBoss x SIROT Connector
 
Sistema / Aplicação: SIGSJ Intranet (sigsj-intranet)
Servidor Origem: caddeapllx955 (IP: 10.116.194.179)
Servidor Destino: sspdeaplux0100 (IP: 10.116.89.101)
Porta / Protocolo: 8111 / TCP (Bidirecional / Retorno estabelecido)
Justificativa Técnica: A aplicação sigsj-intranet hospedada no caddeapllx955 necessita comunicar com o gateway SIROT Connector no sspdeaplux0100 na porta 8111/TCP. Atualmente, o servidor origem alcança o destino via ICMP (ping) e nas portas TCP 22 e 8080, mas as requisições na porta 8111/TCP sofrem timeout (CEFException: [ID=1795098566118 08111] Connection timed out). Já foi validado que o serviço Connector está ativo e escutando em *.8111 no destino (sspdeaplux0100) e que não há bloqueio nos firewalls locais de ambos os servidores.


Dados inseridos com sucesso! ID:99052 - SIGSJ Intranet


<img width="1582" height="414" alt="image" src="https://github.com/user-attachments/assets/ce1ef4a2-6982-4e10-b940-ee6331213eb3" />

Dados inseridos com sucesso! ID:99053

o jeferson ja pediu repgra para o internet e o intranet

ta certo?
