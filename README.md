O teste não rodou de verdade — as variáveis HOST/PORT estavam vazias nessa sessão (por isso o “SEM CONEXAO :” sem IP). Vamos testar com os valores na mão. Na 2854:

bash
timeout 5 bash -c "cat < /dev/null > /dev/tcp/10.116.89.101/8111" && echo "ABRIU 10.116.89.101:8111" || echo "SEM CONEXAO 10.116.89.101:8111"

Esse é o teste que importa. Se der SEM CONEXAO, a VM não alcança o SIPER (firewall ou host/porta errado para DES), e é a causa do login falhar.

Agora, pra confirmar se 10.116.89.101:8111 é mesmo o endereço de DES (e não TQS ou outro): no legado o SIROT era externo (sirotconEjb_v2.2.7.jar), então o host/porta está dentro de um properties da aplicação, não no system-properties. Vamos procurar no EAR/WAR do legado. No 0039:

bash
B=/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet
# procura o host/porta do farm nos arquivos de config da app (inclui dentro de jars/wars explodidos)
grep -rniE "8111|farm|connector.*host|siper.*host|10\.116\.89\." $B/deploy $B/deployapp $B/tmp /apl/sigsj 2>/dev/null | grep -viE "password|senha|\.so" | head -20

# e no conteúdo do jar do sirot
cd /tmp && unzip -o $B/deployapp/sirotconEjb_v2.2.7.jar -d /tmp/sirotjar >/dev/null 2>&1
grep -rniE "8111|farm|host|10\.116\.89\.|properties" /tmp/sirotjar 2>/dev/null | head -20
find /tmp/sirotjar -name "*.properties" -exec echo "== {} ==" \; -exec cat {} \;

Manda as duas saídas. Com isso eu confirmo:

teste TCP → se é firewall/rota (abre REQ de rede) ou se a porta responde;
host do legado → se 10.116.89.101:8111 é o valor certo de DES ou se pegamos o de outro ambiente por engano.

Pela cara (getResponse nulo + provável sem conexão), minha aposta é rede/firewall entre a VM nova e o SIPER. Mas o teste confirma antes de abrirmos qualquer coisa.
