Então a recomendação é seguir com o VIP, usando como modelo a REQ000146953662 e o passo a passo

O fluxo fica assim:

1. Certificado TE079 para a URL (abrir primeiro, porque o número dessa REQ é citado no pedido do VIP).

2. REQ de VIP, com estes campos:
• Qual o tipo de serviço?: Alterar configurações em balanceador
• Detalhe do serviço: VIP
• Atividade a ser executada: Solicitar inclusão de VIP

Descrição:
Criação de VIP para a URL <sua-url>

Apontamento/Balanceamento para o servidor:
IP: <IP da VM do SIEMP>
HOST: <hostname da VM do SIEMP>

http://<sua-url>
Porta 80

Favor instalar o certificado da requisição abaixo:
<REQ do certificado TE079> - <sua-url>

https://<sua-url>

3. A Rede cria o VIP e informa o IP alocado. Depois a Segurança disponibiliza o certificado no balanceador para ser instalado no VIP.

4. REQ de DNS para a URL apontar para o IP do VIP.

5. Com tudo pronto, a gente ajusta as variáveis de URL na release e roda o deploy.

Qualquer dúvida é só chamar!
