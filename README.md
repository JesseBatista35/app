Vamos confirmar. Na 2854:

bash
# o que está configurado
grep -n "CONNECTOR-FARM" /opt/jboss-eap/standalone/configuration/standalone-full-ha.xml

# testa a conexão TCP pro host:porta do farm (troca pelos valores que o grep mostrar)
HOST=10.116.89.101; PORT=8111
timeout 5 bash -c "cat < /dev/null > /dev/tcp/$HOST/$PORT" && echo "ABRIU $HOST:$PORT" || echo "SEM CONEXAO $HOST:$PORT"

E no legado (0039), vê pra onde o SIGSJ-internet apontava o SIROT/SIPER em DES — é a referência do host/porta certos:

bash
B=/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet
grep -rniE "siper|sirot|farm|connector|host|porta|8111|conexao" $B/deployapp $B/conf 2>/dev/null | grep -viE "password|senha" | head -30
# e nas properties da aplicação
find /apl/sigsj $B -name "*.properties" 2>/dev/null | xargs grep -liE "siper|sirot|farm|host" 2>/dev/null

Me manda as saídas. O que interessa:

SEM CONEXAO → é rede/firewall ou host-porta errado. Aí comparamos com o legado e, se for firewall, abrimos regra; se for valor errado, corrigimos no config.
ABRIU → a porta responde, e o problema é mais no protocolo/SIPER (nesse caso, alinhar com os devs do SIROT).

A prioridade do login virou o SIPER/CONNECTOR-FARM. O banco segue como pendência separada (usuário SGSJSD01 + senha).
