[p585600@caddeapllx2193 ~]$ grep -E 'sigdb|SWIFT|SIEXC_SWIFT|eFinanceira' /etc/fstab
192.168.227.59:/export/sicql_bovespa /SIEXC_SWIFT nfs rw,sync,hard 0 0
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /eFinanceira/siexc/entrada nfs rw,sync,hard 0 0
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /eFinanceira_ctc/siexc nfs rw,sync,hard 0 0
192.168.227.59:/export/sicql_bovespa /opt/sigdb nfs rw,sync,hard 0 0
192.168.227.59:/export/sicql_bovespa /producao/SWIFT nfs rw,sync,hard 0 0
[p585600@caddeapllx2193 ~]$
[p585600@caddeapllx2193 ~]$
[p585600@caddeapllx2193 ~]$ sudo mkdir -p /opt/sigdb /producao/SWIFT /SIEXC_SWIFT /eFinanceira/siexc/entrada

Presumimos que você recebeu as instruções de sempre do administrador
de sistema local. Basicamente, resume-se a estas três coisas:

    #1) Respeite a privacidade dos outros.
    #2) Pense antes de digitar.
    #3) Com grandes poderes vêm grandes responsabilidades.

[sudo] senha para p585600:
Sinto muito, tente novamente.
[sudo] senha para p585600:
[p585600@caddeapllx2193 ~]$
[p585600@caddeapllx2193 ~]$
[p585600@caddeapllx2193 ~]$
[p585600@caddeapllx2193 ~]$ ^C
[p585600@caddeapllx2193 ~]$ sudo mkdir -p /opt/sigdb /producao/SWIFT /SIEXC_SWIFT /eFinanceira/siexc/entrada
[p585600@caddeapllx2193 ~]$ sudo mount -t nfs 192.168.227.59:/export/sicql_bovespa /SIEXC_SWIFT
[p585600@caddeapllx2193 ~]$ sudo mount -t nfs nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /eFinanceira/siexc/entrada
[p585600@caddeapllx2193 ~]$
[p585600@caddeapllx2193 ~]$
[p585600@caddeapllx2193 ~]$ sudo su
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]# mkdir -p /opt/sigdb /producao/SWIFT /SIEXC_SWIFT /eFinanceira/siexc/entrada
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]# mount -t nfs 192.168.227.59:/export/sicql_bovespa /SIEXC_SWIFT
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]# mount -t nfs nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /eFinanceira/siexc/entrada
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
