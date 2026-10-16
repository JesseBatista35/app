
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec -n simpf-des simpf-backend-des-447-gzfdw -- timeout 5 bash -c 'cat < /dev/null > /dev/tcp/10.116.83.19/22' && echo OK22
OK22
-sh-4.2$ oc exec -n simpf-des simpf-backend-des-447-gzfdw -- timeout 10 bash -c 'cat < /dev/null > /dev/tcp/10.116.83.19/8443' && echo OK8443 || echo FALHA8443
command terminated with exit code 124
FALHA8443
-sh-4.2$




-sh-4.1$ sudo tcpdump -ni any host 10.116.220.37
tcpdump: verbose output suppressed, use -v or -vv for full protocol decode
listening on any, link-type LINUX_SLL (Linux cooked), capture size 65535 bytes
13:13:13.315863 IP 10.116.220.37.42722 > 10.116.83.19.ssh: Flags [S], seq 2582279065, win 64860, options [mss 1380,sackOK,TS val 268895636 ecr 0,nop,wscale 7], length 0
13:13:13.315908 IP 10.116.83.19.ssh > 10.116.220.37.42722: Flags [S.], seq 2052772758, ack 2582279066, win 14480, options [mss 1460,sackOK,TS val 176533861 ecr 268895636,nop,wscale 7], length 0
13:13:13.316490 IP 10.116.220.37.42722 > 10.116.83.19.ssh: Flags [.], ack 1, win 507, options [nop,nop,TS val 268895637 ecr 176533861], length 0
13:13:13.317583 IP 10.116.220.37.42722 > 10.116.83.19.ssh: Flags [F.], seq 1, ack 1, win 507, options [nop,nop,TS val 268895639 ecr 176533861], length 0
13:13:13.318069 IP 10.116.83.19.ssh > 10.116.220.37.42722: Flags [.], ack 2, win 114, options [nop,nop,TS val 176533863 ecr 268895639], length 0
13:13:13.320637 IP 10.116.83.19.ssh > 10.116.220.37.42722: Flags [P.], seq 1:22, ack 2, win 114, options [nop,nop,TS val 176533866 ecr 268895639], length 21
13:13:13.321005 IP 10.116.83.19.ssh > 10.116.220.37.42722: Flags [F.], seq 22, ack 2, win 114, options [nop,nop,TS val 176533866 ecr 268895639], length 0
13:13:13.321278 IP 10.116.220.37.42722 > 10.116.83.19.ssh: Flags [R], seq 2582279067, win 0, length 0

