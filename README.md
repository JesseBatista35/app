4.2$
-sh-4.2$
-sh-4.2$ oc rsh sicow-seg-okd-des-72-xk8dv
sh-4.2$
sh-4.2$
sh-4.2$
sh-4.2$ echo "JBOSS_HOME=$JBOSS_HOME  JBOSS_MODULEPATH=$JBOSS_MODULEPATH"
JBOSS_HOME=/opt/jboss  JBOSS_MODULEPATH=
sh-4.2$
sh-4.2$
sh-4.2$ ps -ef | grep -o '\-mp [^ ]*'
-mp /opt/jboss/modules
-mp [^
sh-4.2$
sh-4.2$
sh-4.2$ ls -l /opt/jboss/modules/br/gov/caixa/siusr/main/ 2>&1
ls: cannot access /opt/jboss/modules/br/gov/caixa/siusr/main/: No such file or directory
sh-4.2$
sh-4.2$
sh-4.2$ ls -l $JBOSS_HOME/modules/br/gov/caixa/siusr/main/ 2>&1
ls: cannot access /opt/jboss/modules/br/gov/caixa/siusr/main/: No such file or directory
sh-4.2$
sh-4.2$
sh-4.2$ cat $JBOSS_HOME/modules/br/gov/caixa/siusr/main/module.xml
cat: /opt/jboss/modules/br/gov/caixa/siusr/main/module.xml: No such file or directory
sh-4.2$
sh-4.2$
sh-4.2$
sh-4.2$
