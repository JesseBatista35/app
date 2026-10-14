
[root@caddeapllx2193 p585600]# df -h -T | grep nfs
192.168.227.59:/export/sicql_bovespa                           nfs4       97M  5,3M   92M   6% /opt/sigdb
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC nfs4      5,0G 1022M  4,1G  20% /siexc_incoming
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC   nfs4       16G   41M   16G   1% /SIAPC
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF nfs4      7,0G  5,1G  1,9G  73% /integracoes/SIISF
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC nfs4      5,0G 1022M  4,1G  20% /legado
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC nfs4      5,0G 1022M  4,1G  20% /SIGPL
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC nfs4      5,0G 1022M  4,1G  20% /eFinanceira/siexc/entrada
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC nfs4      5,0G 1022M  4,1G  20% /eFinanceira_ctc/siexc
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC nfs4      5,0G 1022M  4,1G  20% /siexc
192.168.227.59:/export/sicql_bovespa                           nfs4       97M  5,3M   92M   6% /producao
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC nfs4      5,0G 1022M  4,1G  20% /suporte
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]# mount | grep -c ' /producao/SWIFT '
2
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]# umont /producao*SWIFT
bash: umont: comando não encontrado
[root@caddeapllx2193 p585600]# umont /producao/SWIFT
bash: umont: comando não encontrado
[root@caddeapllx2193 p585600]# umount /producao/SWIFT
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]# mount | grep ' /producao/SWIFT '
192.168.227.59:/export/sicql_bovespa on /producao/SWIFT type nfs4 (rw,relatime,sync,vers=4.2,rsize=262144,wsize=262144,namlen=255,hard,proto=tcp,timeo=600,retrans=2,sec=sys,clientaddr=192.168.233.69,local_lock=none,addr=192.168.227.59)
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
