Isso! Roda a release de DES do intranet agora. Quando terminar, valida na 955 que veio tudo pela esteira:

bash
echo "== custom.sh chegou? =="
head -3 /opt/jboss-eap/standalone/configuration/custom.sh

echo "== arquivos nos destinos =="
ls -la /log_jboss/config-log4j/
ls -la /apl/sigsj/properties/

echo "== a pasta de origem foi esvaziada pelo mv? =="
ls -la /opt/jboss-eap/standalone/configuration/properties/ 2>/dev/null

echo "== app respondendo =="
curl -s -o /dev/null -w "intranet default.jsp: %{http_code}\n" http://10.116.194.179/sigsj_intranet/default.jsp

O que tem que vir:

custom.sh presente;
/log_jboss/config-log4j/sigsj_intranet.xml lá;
/apl/sigsj/properties/ com os 3 properties;
a pasta de origem (configuration/properties/) vazia (o mv levou os arquivos) — isso confirma que o custom.sh rodou;
default.jsp 200.

Se vier tudo certo, faz o login no navegador (https://sigsj-intranet.des.caixa/sigsj_intranet/) pra confirmar que o pós-login abre. Aí o intranet está 100% pela esteira e seguimos pro internet e boleto.
