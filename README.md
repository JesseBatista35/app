
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]# umount /SIEXC_SWIFT
[root@caddeapllx2193 p585600]# umount /opt/sigdb
[root@caddeapllx2193 p585600]# mount | grep -E ' /SIEXC_SWIFT | /opt/sigdb | /producao/SWIFT ' | awk '{print $3}'
/SIEXC_SWIFT
/opt/sigdb
/producao/SWIFT
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]# df -h -T | grep -c nfs
10
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]# findmnt -t nfs4 -o TARGET,SOURCE | sort
/eFinanceira_ctc/siexc         nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
  └─/eFinanceira/siexc/entrada nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
/eFinanceira/siexc/entrada     nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
└─/eFinanceira/siexc/entrada   nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
/integracoes/SIISF             nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF
/legado                        nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
/opt/sigdb                     192.168.227.59:/export/sicql_bovespa
/producao                      192.168.227.59:/export/sicql_bovespa
└─/producao/SWIFT              192.168.227.59:/export/sicql_bovespa
/SIAPC                         nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC
/siexc_incoming                nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
/siexc                         nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
/SIEXC_SWIFT                   192.168.227.59:/export/sicql_bovespa
/SIGPL                         nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
/suporte                       nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
TARGET                         SOURCE
[root@caddeapllx2193 p585600]# findmnt -t nfs4 | grep -c nfs4
15
[root@caddeapllx2193 p585600]#
