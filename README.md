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
