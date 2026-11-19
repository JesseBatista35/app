que o log registrou nesse clique. Na 2854:

bash
grep -n "Autenticacao\|SenhasSIIBC\|SIROT\|SIPER\|ERROR" /opt/jboss-eap/standalone/log/server.log | tail -40

E, pra pegar só o erro do horário do teste (agora, 11:3x):

bash
sed -n '/2026-11-19 11:3/,$p' /opt/jboss-eap/standalone/log/server.log | grep -A30 "Autenticacao" | head -60

Me manda a saída. O que interessa é qual exceção aparece agora:

Se ainda for UnsatisfiedLinkError/SenhasSIIBC → a lib não carregou pra esse contexto (vemos o porquê).
Se for o ORA-01017/SIGSJ04 → é o banco, que já mapeamos (usuário SGSJSD01 + senha), e aí o login só vai funcionar depois de corrigir o datasource.
Se for erro de SIROT/SIPER/CONNECTOR-FARM → é a comunicação com o SIROT (host/porta CONNECTOR-FARM-HOST), outro ponto.

Minha aposta é no banco: o fluxo de login consulta o usuário, e isso bate no SIGSJ04, que está com ORA-01017. Se for isso, confirma que a prioridade agora é a senha do SGSJSD01 pra destravar o login. Mas só o log confirma — manda que eu te digo qual é.
