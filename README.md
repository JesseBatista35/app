
-sh-4.2$ oc rsh sihdg-jboss8-des-113-6hhvc
sh-5.1$ df -h | grep sihdg
nprdnfs01.ad.caixa:/ifs/cpwsprd01/nprd/fs_sihdg_sinaf   50G     0   50G   0% /sihdg_sinaf
hypernprd56.ad.caixa:/fs_sihdg                          50G     0   50G   0% /sihdg_des_pwc
sh-5.1$
sh-5.1$
sh-5.1$ oc get dc sihdg-jboss8-des -o jsonpath='{range .spec.template.spec.containers[0].volumeMounts[*]}{.name}{"\t"}{.mountPath}{"\n"}{end}'
oc get dc sihdg-jboss8-des -o jsonpath='{range .spec.template.spec.volumes[*]}{.name}{"\t"}{.persistentVolumeClaim.claimName}{"\n"}{end}'
sh: oc: command not found
sh: oc: command not found
sh-5.1$
sh-5.1$
sh-5.1$ oc set volume dc/sihdg-jboss8-des --add --overwrite \
  --name=sihdg-sinaf-data-des \
  --type=persistentVolumeClaim --claim-name=sihdg-sinaf-data-des \
  --mount-path=/sihdg_des --containers=sihdg-jboss8-des
sh: oc: command not found
sh-5.1$
sh-5.1$
sh-5.1$ oc get dc sihdg-jboss8-des -o jsonpath='{range .spec.template.spec.volumes[*]}{.name}{"\t"}{.persistentVolumeClaim.claimName}{"\n"}{end}'
sh: oc: command not found
sh-5.1$
sh-5.1$
sh-5.1$ oc get dc sihdg-jboss8-des -o jsonpath='{range .spec.template.spec.containers[0].volumeMounts[*]}{.name}{"\t"}{.mountPath}{"\n"}{end}'
sh: oc: command not found
sh-5.1$
