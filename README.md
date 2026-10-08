
sihdg-jboss8-tqs-33-deploy      0/1       Error       0          11m
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc rsh sihdg-jboss8-tqs-34-87l6z
sh-5.1$ timeout 5 bash -c '</dev/tcp/10.116.29.201/31153' && echo "porta ok" || echo "porta falhou"
porta falhou
sh-5.1$ oc get netnamespace sihdg-tqs -o yaml
sh: oc: command not found
sh-5.1$ oc get egressip
sh: oc: command not found
sh-5.1$
