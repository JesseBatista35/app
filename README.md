oc get dc sihdg-jboss8-des -o jsonpath='{range .spec.template.spec.containers[0].volumeMounts[*]}{.name}{"\t"}{.mountPath}{"\n"}{end}'
oc get dc sihdg-jboss8-des -o jsonpath='{range .spec.template.spec.volumes[*]}{.name}{"\t"}{.persistentVolumeClaim.claimName}{"\n"}{end}'


oc set volume dc/sihdg-jboss8-des --add --overwrite \
  --name=sihdg-sinaf-data-des \
  --type=persistentVolumeClaim --claim-name=sihdg-sinaf-data-des \
  --mount-path=/sihdg_des --containers=sihdg-jboss8-des

  oc rsh <pod-novo>
df -h | grep sihdg
mkdir /sihdg_des/Arquivos_SINAF
ls -la /sihdg_des
