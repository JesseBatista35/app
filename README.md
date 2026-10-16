
-sh-4.1$
-sh-4.1$ netstat -ltn | grep 8443
tcp        0      0 :::8443                     :::*                        OUÇA
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$ sudo iptables -L INPUT -n -v --line-numbers
[sudo] password for p585600:
Chain INPUT (policy ACCEPT 0 packets, 0 bytes)
num   pkts bytes target     prot opt in     out     source               destination
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$ sudo tcpdump -ni any host 10.116.220.37 and port 8443
tcpdump: verbose output suppressed, use -v or -vv for full protocol decode
listening on any, link-type LINUX_SLL (Linux cooked), capture size 65535 bytes
^C
0 packets captured
0 packets received by filter
0 packets dropped by kernel
-sh-4.1$ oc exec -n simpf-des simpf-backend-des-447-gzfdw -- \
>   timeout 10 bash -c 'cat < /dev/null > /dev/tcp/10.116.83.19/8443' && echo OK || echo FALHA
-sh: oc: comando não encontrado
FALHA
-sh-4.1$
