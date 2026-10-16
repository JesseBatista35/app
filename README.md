
-sh-4.2$ ^C
-sh-4.2$ oc get netnamespace simpf-des
NAME        NETID      EGRESS IPS
simpf-des   12461632   ["10.116.220.37"]
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ nslookup ceadecldlx071.nprd.caixa
Server:         10.122.150.12
Address:        10.122.150.12#53

Non-authoritative answer:
Name:   ceadecldlx071.nprd.caixa
Address: 10.116.208.91

-sh-4.2$ c exec -n simpf-des simpf-backend-des-447-gzfdw -- getent hosts sctdeapllx0018.df.caixa
-sh: c: comando não encontrado
-sh-4.2$ oc exec -n simpf-des simpf-backend-des-447-gzfdw -- getent hosts sctdeapllx0018.df.caixa
10.116.83.19    sctdeapllx0018.df.caixa
-sh-4.2$
