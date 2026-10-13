oc get dc/sinfs-tqs -n sinfs-tqs -o yaml > dc-sinfs-tqs-backup.yaml
oc set volume dc/sinfs-tqs -n sinfs-tqs --remove --name=accaixa-v4
