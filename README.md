
-sh-4.2$ POD=simcn-backend-des-277-fh2hg
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get dc simcn-backend-des -n simcn-des -o jsonpath='{range .spec.template.spec.containers[*].volumeMounts[*]}{.name}{" -> "}{.mountPath}{"\n"}{end}'
simcn-backend-data-des -> /simcn
caixa-truststore-acteste-nprd-jks -> /opt/jboss/standalone/configuration/caixa-truststore-acteste-nprd.jks
jboss-config-simcn-backend -> /tmp/standalone-okd.xml
java-config-simcn-backend -> /opt/jboss/bin/standalone.conf
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec -n simcn-des $POD -- df -h | grep -i ifs
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/UP_SIMCN   20G  3.0M   20G   1% /simcn
-sh-4.2$ oc exec -n simcn-des $POD -- ls -la /simcn
total 76
drwxrwxrwx. 6 30000030 20000957  135 Aug 27 12:20 .
dr-xr-xr-x. 1 root     root       41 Oct 13 16:36 ..
-rw-r--r--. 1 nobody   20000957    0 Aug 27 12:20 TESTE
drwxrwxr-x. 2 30000115 20000957   59 Mar 19  2026 cacheJson
drwxrwxr-x. 3 30000115 20000957 1616 Sep 18 14:32 conciliacao
drwxrwxr-x. 3 30000115 20000957   21 Mar 18  2026 relatoriosLegados
drwxr-xr-x. 2 30000030 20000957  138 Apr 21 02:20 tmp
-sh-4.2$ oc exec -n simcn-des $POD -- ls -la /simcn/upload/des/simcn
ls: cannot access /simcn/upload/des/simcn: No such file or directory
command terminated with exit code 2
-sh-4.2$ oc exec -n simcn-des $POD -- sh -c 'touch /simcn/upload/des/simcn/.teste_cesti && rm /simcn/upload/des/simcn/.teste_cesti && echo ESCRITA_OK'
touch: cannot touch '/simcn/upload/des/simcn/.teste_cesti': No such file or directory
command terminated with exit code 1
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get node ceadecldlx071.nprd.caixa -o wide
NAME                       STATUS    ROLES     AGE       VERSION           INTERNAL-IP     EXTERNAL-IP   OS-IMAGE                        KERNEL-VERSION           CONTAINER-RUNTIME
ceadecldlx071.nprd.caixa   Ready     worker    2y93d     v1.25.8+27e744f   10.116.208.91   <none>        Fedora CoreOS 37.20230322.3.0   6.1.18-200.fc37.x86_64   cri-o://1.25.1
-sh-4.2$
