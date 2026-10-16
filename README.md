2.0.3
SIHDG-jboss8
Maven

View raw log

Starting: Maven
==============================================================================
Task         : Maven
Description  : Build, test, and deploy with Apache Maven
Version      : 4.225.0
Author       : Microsoft Corporation
Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/build/maven
==============================================================================
/opt/apache-maven/apache-maven-3.9.9/bin/mvn -version
Apache Maven 3.9.9 (8e8579a9e76f7d015ee5ec7bfcdc97d260186937)
Maven home: /opt/apache-maven/apache-maven-3.9.9
Java version: 21.0.5, vendor: Red Hat, Inc., runtime: /usr/java/open-jdk-21.0.5
Default locale: pt_BR, platform encoding: UTF-8
OS name: "linux", version: "5.18.5-100.fc35.x86_64", arch: "amd64", family: "unix"
/opt/apache-maven/apache-maven-3.9.9/bin/mvn -f /opt/ads-agent/_work/5/s/pom.xml clean compile install -Dversion.app=1.0.0-SNAPSHOT
[INFO] Scanning for projects...
[ERROR] [ERROR] Some problems were encountered while processing the POMs:
[FATAL] Non-parseable POM /opt/ads-agent/_work/5/s/ear/pom.xml: end tag name </parent> must match start tag name <version> from line 25 (position: TEXT seen ...<version>3.22.0.3/version>\n    </parent>... @26:14)  @ line 26, column 14
 @ 
[ERROR] The build could not read 1 project -> [Help 1]
[ERROR]   
[ERROR]   The project  (/opt/ads-agent/_work/5/s/ear/pom.xml) has 1 error
[ERROR]     Non-parseable POM /opt/ads-agent/_work/5/s/ear/pom.xml: end tag name </parent> must match start tag name <version> from line 25 (position: TEXT seen ...<version>3.22.0.3/version>\n    </parent>... @26:14)  @ line 26, column 14 -> [Help 2]
[ERROR] 
[ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
[ERROR] Re-run Maven using the -X switch to enable full debug logging.
[ERROR] 
[ERROR] For more information about the errors and possible solutions, please read the following articles:
[ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/ProjectBuildingException
[ERROR] [Help 2] http://cwiki.apache.org/confluence/display/MAVEN/ModelParseException
The process '/opt/apache-maven/apache-maven-3.9.9/bin/mvn' failed with exit code 1
Could not retrieve code analysis results - Maven run failed.
##[error]Build failed.
Finishing: Maven
