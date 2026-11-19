Intranet (955):

bash
ls /log_jboss/config-log4j/; echo "===="; cat /log_jboss/config-log4j/sigsj_intranet.xml

Internet (2854):

bash
ls /log_jboss/config-log4j/; echo "===="; cat /log_jboss/config-log4j/sigsj_internet.xml

Boleto (2557):

bash
ls /log_jboss/config-log4j/; echo "===="; cat /log_jboss/config-log4j/sigsj_ws_boleto.xm




[root@caddeapllx955 properties]# ls /log_jboss/config-log4j/; echo "===="; cat /log_jboss/config-log4j/sigsj_intranet.xml
sigsj_intranet.xml
====
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE log4j:configuration SYSTEM "log4j.dtd">
<log4j:configuration xmlns:log4j='http://jakarta.apache.org/log4j/'>
    <appender name="SIGSJ" class="org.apache.log4j.DailyRollingFileAppender">
        <param name="Append" value="true" />
        <param name="Encoding" value="ISO-8859-1" />
        <param name="File" value="/log_jboss/sigsj_intranet/sigsj_intranet.log" />
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
[root@caddeapllx955 properties]#




[root@caddeapllx2854 properties]#
[root@caddeapllx2854 properties]# ls /log_jboss/config-log4j/; echo "===="; cat /log_jboss/config-log4j/sigsj_internet.xml
sigsj_internet.xml
====
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE log4j:configuration SYSTEM "log4j.dtd">
<log4j:configuration xmlns:log4j='http://jakarta.apache.org/log4j/'>
    <appender name="SIGSJ" class="org.apache.log4j.DailyRollingFileAppender">
        <param name="Append" value="true" />
        <param name="Encoding" value="ISO-8859-1" />
        <param name="File" value="/log_jboss/sigsj_internet/sigsj_internet.log" />
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
[root@caddeapllx2854 properties]#




drwxr-xr-x 3 jboss jboss   24 nov 19 15:22 ..
-rw-r--r-- 1 jboss jboss 1357 nov 19 15:22 b2b.properties
-rw-r--r-- 1 jboss jboss  279 nov 19 15:22 config.properties
-rw-r--r-- 1 jboss jboss   24 nov 19 15:22 release.properties
[root@caddeapllx2557 properties]#
[root@caddeapllx2557 properties]#
[root@caddeapllx2557 properties]#
[root@caddeapllx2557 properties]#
[root@caddeapllx2557 properties]# ls /log_jboss/config-log4j/; echo "===="; cat /log_jboss/config-log4j/sigsj_ws_boleto.xm
sigsj_ws_boleto.xml
====
cat: /log_jboss/config-log4j/sigsj_ws_boleto.xm: Arquivo ou diretório inexistente
[root@caddeapllx2557 properties]#
[root@caddeapllx2557 properties]#
[root@caddeapllx2557 properties]#


no repo ja tinahsmo fgeito esse
jboss/custom.sh




#!/bin/bash
# Configuração externa do log4j do SIGSJ-internet
# A aplicação lê o XML em /log_jboss/config-log4j/XXX_INTERNET_XML_XXX (web.xml / CaixaConfigServlet)
# e grava o log em /log_jboss/sigsj_internet/
set -e

mkdir -p /log_jboss/config-log4j /log_jboss/sigsj_internet

cat > /log_jboss/config-log4j/XXX_INTERNET_XML_XXX <<'EOF'
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE log4j:configuration SYSTEM "log4j.dtd">
<log4j:configuration xmlns:log4j='http://jakarta.apache.org/log4j/'>
    <appender name="SIGSJ" class="org.apache.log4j.DailyRollingFileAppender">
        <param name="Append" value="true" />
        <param name="Encoding" value="ISO-8859-1" />
        <param name="File" value="/log_jboss/sigsj_internet/sigsj_internet.log" />
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
EOF

chown -R jboss:jboss /log_jboss
chmod 755 /log_jboss /log_jboss/config-log4j /log_jboss/sigsj_internet
chmod 644 /log_jboss/config-log4j/sigsj_internet.xml




#!/bin/bash
# Configuração externa do log4j do SIGSJ-intranet
# A aplicação lê o XML em /log_jboss/config-log4j/sigsj_intranet.xml (web.xml / CaixaConfigServlet)
# e grava o log em /log_jboss/sigsj_intranet/
set -e

mkdir -p /log_jboss/config-log4j /log_jboss/sigsj_intranet

cat > /log_jboss/config-log4j/sigsj_intranet.xml <<'EOF'
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE log4j:configuration SYSTEM "log4j.dtd">
<log4j:configuration xmlns:log4j='http://jakarta.apache.org/log4j/'>
    <appender name="SIGSJ" class="org.apache.log4j.DailyRollingFileAppender">
        <param name="Append" value="true" />
        <param name="Encoding" value="ISO-8859-1" />
        <param name="File" value="/log_jboss/sigsj_intranet/sigsj_intranet.log" />
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
EOF

chown -R jboss:jboss /log_jboss
chmod 755 /log_jboss /log_jboss/config-log4j /log_jboss/sigsj_intranet
chmod 644 /log_jboss/config-log4j/sigsj_intranet.xml



#!/bin/bash
# Configuração externa do log4j do SIGSJ-boleto
# A aplicação lê o XML em /log_jboss/config-log4j/sigsj_ws_boleto.xml
# e grava o log em /log_jboss/sigsj_internet/<nome-do-servidor>.log (igual ao legado)
set -e

mkdir -p /log_jboss/config-log4j /log_jboss/sigsj_internet

cat > /log_jboss/config-log4j/sigsj_ws_boleto.xml <<'EOF'
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
EOF

chown -R jboss:jboss /log_jboss
chmod 755 /log_jboss /log_jboss/config-log4j /log_jboss/sigsj_internet
chmod 644 /log_jboss/config-log4j/sigsj_ws_boleto.xml


agente ja tinha feito se tiver certo e sso tirar e colcoar na ppasta configuration
