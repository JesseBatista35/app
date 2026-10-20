<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE log4j:configuration SYSTEM "log4j.dtd">
<log4j:configuration xmlns:log4j='http://jakarta.apache.org/log4j/'>

    <appender name="SIROT2_AUDIT_LOG" class="org.apache.log4j.DailyRollingFileAppender">
        <param name="File" value="/log_jboss/sirot2/sirot2-${jboss.server.name}.log" />
        <param name="Append" value="true" />
        <param name="DatePattern" value="'.'dd" />
        <layout class="org.apache.log4j.PatternLayout">
                <param name="ConversionPattern" value="%d{HH:mm:ss} %5p [%t] (%F:%L) - %m%n"/>
        </layout>
    </appender>

    <category name="org.apache.log4j.xml">
        <priority value="debug" />
    </category>

    <category name="br.gov.caixa.sirot">
        <priority value="debug" />
        <appender-ref ref="SIROT2_AUDIT_LOG"/>
    </category>

</log4j:configuration>
