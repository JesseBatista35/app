# internet (2854)
head -3 /opt/jboss-eap/standalone/configuration/custom.sh
ls -la /log_jboss/config-log4j/ /apl/sigsj/properties/
ls -la /opt/jboss-eap/standalone/configuration/properties/   # tem que estar vazia
curl -s -o /dev/null -w "internet: %{http_code}\n" http://10.116.202.45/sigsj_internet/

# boleto (2557)
head -3 /opt/jboss-eap/standalone/configuration/custom.sh
ls -la /log_jboss/config-log4j/ /apl/sigsj/properties/
curl -s -o /dev/null -w "boleto: %{http_code}\n" http://10.116.201.25/boletoService/contaJudicial
