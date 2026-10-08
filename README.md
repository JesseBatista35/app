oc project sihdg-tqs
oc rsh sihdg-jboss8-tqs-33-xb8lm
timeout 5 bash -c '</dev/tcp/10.116.29.201/31153' && echo "porta ok" || echo "porta falhou"

oc get netnamespace sihdg-tqs -o yaml
oc get egressip
