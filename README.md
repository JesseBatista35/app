# SIGSJ-boleto - entrega a config externa que nao vem no EAR
# Os arquivos chegam via esteira em /opt/jboss-eap/standalone/configuration/properties/
# e sao movidos para o destino final na VM.
# O log4j do boleto grava em /log_jboss/sigsj_internet/<nome-do-servidor>.log (igual ao legado)
SRC=/opt/jboss-eap/standalone/configuration/properties

echo "Criando log4j externo do SIGSJ-boleto"
mkdir -p /log_jboss/config-log4j /log_jboss/sigsj_internet
mv $SRC/sigsj_ws_boleto.xml /log_jboss/config-log4j/.

echo "Criando properties da aplicacao (/apl/sigsj/properties)"
mkdir -p /apl/sigsj/properties
mv $SRC/config.properties  /apl/sigsj/properties/.
mv $SRC/b2b.properties     /apl/sigsj/properties/.
mv $SRC/release.properties /apl/sigsj/properties/.

chown -R jboss:jboss /log_jboss /apl/sigsj
chmod 755 /log_jboss /log_jboss/config-log4j /log_jboss/sigsj_internet /apl/sigsj /apl/sigsj/properties
chmod 644 /log_jboss/config-log4j/sigsj_ws_boleto.xml /apl/sigsj/properties/*.properties

echo "Processo concluido."



=======================


<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE log4j:configuration SYSTEM "log4j.dtd">
<log4j:configuration xmlns:log4j='http://jakarta.apache.org/log4j/'>
   <appender name="SIGSJ" class="org.apache.log4j.DailyRollingFileAppender">
       <param name="Append" value="true" />
       <param name="Encoding" value="ISO-8859-1" />
       <param name="File" value="/log_jboss/sigsj_internet/${jboss.server.name}.log" />
       <param name="DatePattern" value="'.'yyyy-MM-dd-a"></param>
       <layout class="org.apache.log4j.PatternLayout">
           <param name="ConversionPattern" value="[%5p] %d{yyyy/MM/dd HH:mm:ss} %c{2}[%t] - %m%n" />
       </layout>
   </appender>
   <logger name="br.gov.caixa.sigsj">
       <level value="DEBUG" />
   </logger>
   <root>
       <priority value="INFO" />
       <appender-ref ref="SIGSJ" />
   </root>
</log4j:configuration>
