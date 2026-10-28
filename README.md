oc get pv,pvc -n sisib-des | grep -i sisib
oc rsh -n sisib-des <pod-sisib-arquivos-de-quebra>
df -h /sisib
touch /sisib/teste_mount && ls -l /sisib && rm /sisib/teste_mount
