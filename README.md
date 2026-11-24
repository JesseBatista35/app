# o que existe de módulo Caixa em cada pod
ls -R /opt/jboss/modules/br/gov/caixa/ 2>&1 | head -50

# o siusr existe no PORTAL? (rodar no pod do portal)
ls -l /opt/jboss/modules/br/gov/caixa/siusr/main/
cat /opt/jboss/modules/br/gov/caixa/siusr/main/module.xml

# ele vem de um mount (ConfigMap/PV) ou está gravado na imagem?
mount | grep -i modules
df -h /opt/jboss/modules/br/gov/caixa/siusr/main/ 2>&1



FORA DO POD
oc get dc sicow-portal-okd-des -o yaml | grep -iA5 -E 'volumeMounts|volumes|image:'
oc get dc sicow-seg-okd-des    -o yaml | grep -iA5 -E 'volumeMounts|volumes|image:'
oc get bc -o yaml | grep -iE 'from|name:|uri|ref'
