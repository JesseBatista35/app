
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get hostsubnet ceadecldlx084.nprd.caixa -o jsonpath='{.egressIPs}{"\n"}'
[10.116.209.59 10.116.222.206 10.116.222.190 10.116.222.6 10.116.222.5 10.116.222.164 10.116.220.210 10.116.221.46 10.116.220.180 10.116.221.183]
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ ^C
-sh-4.2$ oc get hostsubnet ceadecldlx081.nprd.caixa -o jsonpath='{.hostIP}{"\n"}'
10.116.208.101
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get hostsubnet ceadecldlx084.nprd.caixa -o jsonpath='{.hostIP}{"\n"}'

10.116.208.104
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get hostsubnet ceadecldlx081.nprd.caixa
NAME                       HOST                       HOST IP          SUBNET         EGRESS CIDRS          EGRESS IPS
ceadecldlx081.nprd.caixa   ceadecldlx081.nprd.caixa   10.116.208.101   25.1.38.0/23   ["10.116.192.0/19"]   ["10.116.220.121","10.116.221.178","10.116.221.86","10.116.220.92","10.116.220.221","10.116.220.138","10.116.209.36","10.116.221.39","10.116.222.123","10.116.220.175","10.116.221.179"]
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get hostsubnet ceadecldlx084.nprd.caixa

NAME                       HOST                       HOST IP          SUBNET         EGRESS CIDRS          EGRESS IPS
ceadecldlx084.nprd.caixa   ceadecldlx084.nprd.caixa   10.116.208.104   25.3.40.0/23   ["10.116.192.0/19"]   ["10.116.209.59","10.116.222.206","10.116.222.190","10.116.222.6","10.116.222.5","10.116.222.164","10.116.220.210","10.116.221.46","10.116.220.180","10.116.221.183"]
-sh-4.2$
