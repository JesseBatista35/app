oc rsh <pod>
echo "JBOSS_HOME=$JBOSS_HOME  JBOSS_MODULEPATH=$JBOSS_MODULEPATH"
ps -ef | grep -o '\-mp [^ ]*'
ls -l /opt/jboss/modules/br/gov/caixa/siusr/main/ 2>&1
ls -l $JBOSS_HOME/modules/br/gov/caixa/siusr/main/ 2>&1
cat $JBOSS_HOME/modules/br/gov/caixa/siusr/main/module.xml
