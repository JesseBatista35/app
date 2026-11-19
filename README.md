# SIGSJ-intranet - entrega a config externa que nao vem no EAR
# Os arquivos chegam via esteira em /opt/jboss-eap/standalone/configuration/properties/
# e sao movidos para o destino final na VM.
SRC=/opt/jboss-eap/standalone/configuration/properties

echo "Criando log4j externo do SIGSJ-intranet"
mkdir -p /log_jboss/config-log4j /log_jboss/sigsj_intranet
mv $SRC/sigsj_intranet.xml /log_jboss/config-log4j/.

echo "Criando properties da aplicacao (/apl/sigsj/properties)"
mkdir -p /apl/sigsj/properties
mv $SRC/config.properties  /apl/sigsj/properties/.
mv $SRC/b2b.properties     /apl/sigsj/properties/.
mv $SRC/release.properties /apl/sigsj/properties/.

chown -R jboss:jboss /log_jboss /apl/sigsj
chmod 755 /log_jboss /log_jboss/config-log4j /log_jboss/sigsj_intranet /apl/sigsj /apl/sigsj/properties
chmod 644 /log_jboss/config-log4j/sigsj_intranet.xml /apl/sigsj/properties/*.properties

echo "Processo concluido."
