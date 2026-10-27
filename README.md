
-bash-5.1$
-bash-5.1$
-bash-5.1$ ps -ef | grep -i das01 | grep -v grep
  sjsas8  7248     1   0 16:18:01 pts/5       0:07 /opt/SUNWas8/jdk/bin/java -server -XX:NewRatio=2 -Xms512m -Xmx3g -XX:MaxPermSize=512m -Dcom.sun.aas.defaultLogFile=/opt/SUNWas8/domains/das01/logs/server.log -Djava.endorsed.dirs=/opt/SUNWas8/lib/endorsed -Djava.security.policy=/opt/SUNWas8/domains/das01/config/server.policy -Djava.security.auth.login.config=/opt/SUNWas8/domains/das01/config/login.conf -Dsun.rmi.dgc.server.gcInterval=3600000 -Dsun.rmi.dgc.client.gcInterval=3600000 -Djava.ext.dirs=/opt/SUNWas8/jdk/jre/lib/ext:/opt/SUNWas8/domains/das01/lib/ext:/opt/SUNWas8/derby/lib:/opt/SUNWas8/lib/jdbcdrivers -Dcom.sun.enterprise.config.config_environment_factory_class=com.sun.enterprise.config.serverbeans.AppserverConfigEnvironmentFactory -Dcom.sun.enterprise.taglibs=appserv-jstl.jar,jsf-impl.jar -Dcom.sun.enterprise.taglisteners=jsf-impl.jar -Djavax.management.builder.initial=com.sun.enterprise.ee.admin.AppServerMBeanServerBuilder -Dcom.sun.appserv.pluggable.features=com.sun.enterprise.ee.server.pluggable.EEPluggableFeatureImpl -Dcom.sun.appserv.nss.db=/opt/SUNWas8/domains/das01/config -Dfile.encoding=ISO-8859-1 -Djdbc.drivers=com.pointbase.jdbc.jdbcUniversalDriver -Djavax.xml.parsers.SAXParserFactory=com.sun.org.apache.xerces.internal.jaxp.SAXParserFactoryImpl -Dcom.sun.aas.configName=server-config -Dorg.xml.sax.parser=org.xml.sax.helpers.XMLReaderAdapter -Ddomain.name=das01 -Djmx.invoke.getters=true -Djavax.xml.parsers.DocumentBuilderFactory=com.sun.org.apache.xerces.internal.jaxp.DocumentBuilderFactoryImpl -Dcom.sun.aas.promptForIdentity=true -Dorg.xml.sax.driver=com.sun.org.apache.xerces.internal.parsers.SAXParser -Dcom.sun.aas.instanceRoot=/opt/SUNWas8/domains/das01 -Djavax.xml.transform.TransformerFactory=com.sun.org.apache.xalan.internal.xsltc.trax.TransformerFactoryImpl -Dcom.sun.aas.domainName=das01 -Djava.util.logging.manager=com.sun.enterprise.server.logging.ServerLogManager -Dproduct.name=Sun-Java-System/Application-Server -Dcom.sun.enterprise.overrideablejavaxpackages=javax.faces,javax.servlet.jsp.jstl,javax.xml.bind,javax.help -Dcom.sun.aas.configRoot=/opt/SUNWas8/config -Djava.library.path=/opt/SUNWas8/jdk1.5.0_36/jre/lib/sparc/server:/opt/SUNWas8/jdk1.5.0_36/jre/lib/sparc:/opt/SUNWas8/jdk1.5.0_36/jre/../lib/sparc:/opt/SUNWas8/lib:/opt/SUNWas8/lib:/usr/lib/lwp::/oracle/app/oracle/product/10.2.0/lib32:/opt/mqm/java/lib:/usr/lib -Dcom.sun.aas.instanceName=server -Dcom.sun.aas.processLauncher=SE -cp /opt/SUNWas8/jdk/lib/tools.jar:/opt/SUNWas8/lib/appserv-rt.jar:/opt/SUNWas8/lib/rmissl.jar:/opt/SUNWas8/lib/xsdlib.jar:/opt/SUNWas8/lib/appserv-admin.jar:/opt/SUNWas8/lib/jmxremote.jar:/opt/SUNWas8/lib/saaj-impl.jar:/opt/SUNWas8/lib/jss4.jar:/opt/SUNWas8/lib/jaxr-impl.jar:/opt/SUNWas8/lib/jaxrpc-impl.jar:/opt/SUNWas8/lib/jmxremote_optional.jar:/opt/SUNWas8/lib/myfaces-api-1.1.5.jar:/opt/SUNWas8/lib/commons-logging.jar:/opt/SUNWas8/lib/log4j-1.2.8.jar:/opt/SUNWas8/lib/saaj-api.jar:/opt/SUNWas8/lib/admin-cli-ee.jar:/opt/SUNWas8/lib/appserv-ee.jar:/opt/SUNWas8/lib/jesmf-plugin.jar:/opt/SUNWas8/lib/j2ee-svc.jar:/opt/SUNWas8/lib/activation.jar:/opt/SUNWas8/lib/appserv-jstl.jar:/opt/SUNWas8/lib/appserv-cmp.jar:/opt/SUNWas8/lib/commons-launcher.jar:/opt/SUNWas8/lib/appserv-ext.jar:/opt/SUNWas8/lib/appserv-upgrade.jar:/opt/SUNWas8/lib/admin-cli.jar:/opt/SUNWas8/lib/jax-qname.jar:/opt/SUNWas8/lib/xalan.jar:/opt/SUNWas8/lib/myfaces-impl-1.1.5.jar:/opt/SUNWas8/lib/jaxr-api.jar:/opt/SUNWas8/lib/dom.jar:/opt/SUNWas8/lib/jsf-api.jar:/opt/SUNWas8/lib/jaxrpc-api.jar:/opt/SUNWas8/lib/jsf-impl.jar:/opt/SUNWas8/lib/j2ee.jar:/opt/SUNWas8/lib/relaxngDatatype.jar:/opt/SUNWas8/lib/appserv-se.jar:/opt/SUNWas8/lib/mail.jar:/opt/SUNWas8/lib/xercesImpl.jar:/opt/SUNWas8/lib/install/applications/jmsra/imqjmsra.jar:/opt/SUNWas8/imq/lib/jaxm-api.jar:/opt/SUNWas8/imq/lib/fscontext.jar:/opt/SUNWas8/lib/ant/lib/ant.jar:/opt/SUNWas8/hadb/4.4.3-21/lib/hadbjdbc4.jar:/opt/SUNWas8/lib/SUNWjdmk/5.1/lib/jdmkrt.jar:/opt/SUNWmfwk/lib/mfwk_instrum_tk.jar com.sun.enterprise.server.PEMain start
  sjsas8 22941     1   0   Oct 19 ?           0:00 /bin/sh /opt/SUNWas8/imq/bin/imqbrokerd -javahome /opt/SUNWas8/jdk -varhome /opt/SUNWas8/domains/das01/imq -name imqbroker -port 7676 -bgnd -silent
  sjsas8 22951 22941   0   Oct 19 ?           3:10 /opt/SUNWas8/jdk/bin/java -server -cp /opt/SUNWas8/imq/bin/../lib/imqbroker.jar:/opt/SUNWas8/imq/bin/../lib/imqutil.jar:/opt/SUNWas8/imq/bin/../lib/jsse.jar:/opt/SUNWas8/imq/bin/../lib/jnet.jar:/opt/SUNWas8/imq/bin/../lib/jcert.jar:/usr/lib/audit/Audit.jar:/opt/SUNWas8/imq/bin/../lib/ext:/opt/SUNWas8/imq/bin/../lib/ext -Xms32m -Xmx192m -Xss128k -Dimq.home=/opt/SUNWas8/imq/bin/.. -Dimq.varhome=/opt/SUNWas8/domains/das01/imq -Dimq.etchome=/opt/SUNWas8/imq/bin/../etc -Dimq.libhome=/opt/SUNWas8/imq/bin/../lib com.sun.messaging.jmq.jmsserver.Broker -javahome /opt/SUNWas8/jdk -varhome /opt/SUNWas8/domains/das01/imq -name imqbroker -port 7676 -bgnd -silent
-bash-5.1$
-bash-5.1$
-bash-5.1$
-bash-5.1$
-bash-5.1$ ps -ef | grep -i appservDAS | grep -v grep
-bash-5.1$
-bash-5.1$
-bash-5.1$ ps -ef | grep -i appservDAS | grep -v grep
-bash-5.1$
-bash-5.1$
-bash-5.1$
-bash-5.1$ tail -200 $DOM/logs/server.log
tail: cannot open input
-bash-5.1$
-bash-5.1$
-bash-5.1$ ls -l $DOM/config/ | grep -i -E 'lock|pid'
/config/: No such file or directory
grep: illegal option -- E
Usage: grep [-c|-l|-q] -bhinsvw pattern file . . .
-bash-5.1$
-bash-5.1$
-bash-5.1$ grep -n 'admin-listener' $DOM/config/domain.xml
grep: can't open /config/domain.xml
-bash-5.1$
-bash-5.1$
-bash-5.1$ df -h $DOM /tmp /var
Filesystem             Size   Used  Available Capacity  Mounted on
swap                  3.09G   975M      2.13G    31%    /tmp
rpool/ROOT/solaris/var
                       117G  2.64G      28.2G     9%    /var
-bash-5.1$
