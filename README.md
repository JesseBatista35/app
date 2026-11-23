Agora testa o login de novo (navegador) e, logo depois, olha só o que veio após 10:35:

bash
tail -40 /log_jboss/sigsj_internet/sigsj_internet.log

E roda os dois testes pra já saber qual é o próximo bloqueio (firewall ou banco):

bash
timeout 5 bash -c "cat < /dev/null > /dev/tcp/10.116.89.101/8111" && echo "SIROT OK" || echo "SIROT BLOQUEADO"
/opt/jboss-eap/bin/jboss-cli.sh -c --command="/subsystem=datasources/data-source=SIGSJ04:test-connection-in-pool"

Como interpretar o login agora:

Se o erro não for mais SenhasSIIBC → a lib carregou, ótimo.
Se vier getResponse nulo / connection timed out → SIROT (firewall 99053 ainda não aplicado). Confirma com o SIROT BLOQUEADO.
Se vier ORA-01017 → banco (senha SGSJSD01 ainda não inserida pela Segurança). Confirma com o test-connection.

Manda o tail + as duas saídas que eu te digo o que travou e o que cobrar.

E não esquece da correção no repo (senão regride de novo na próxima release): adicionar no jboss/standalone.conf do SIGSJ-internet-config, no final:

# SIGSJ - lib nativa SenhasSIIBC (criptografia SIPER/SIROT)
JAVA_OPTS="$JAVA_OPTS -Djava.library.path=/apl/sigsj/lib"
