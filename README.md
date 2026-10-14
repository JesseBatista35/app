
[p585600@caddeapllx2193 ~]$
[p585600@caddeapllx2193 ~]$
[p585600@caddeapllx2193 ~]$ findmnt -t nfs4 -o TARGET,SOURCE | sort
/eFinanceira_ctc/siexc     nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
/eFinanceira/siexc/entrada nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
/integracoes/SIISF         nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF
/legado                    nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
/opt/sigdb                 192.168.227.59:/export/sicql_bovespa
/producao                  192.168.227.59:/export/sicql_bovespa
└─/producao/SWIFT          192.168.227.59:/export/sicql_bovespa
/SIAPC                     nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC
/SIEXC                     192.168.227.59:/export/sicql_bovespa
/siexc_incoming            nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
/siexc                     nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
/SIEXC_SWIFT               192.168.227.59:/export/sicql_bovespa
/SIGPL                     nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
/suporte                   nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
TARGET                     SOURCE
[p585600@caddeapllx2193 ~]$
[p585600@caddeapllx2193 ~]$
[p585600@caddeapllx2193 ~]$
[p585600@caddeapllx2193 ~]$ findmnt -t nfs4 -o TARGET | sort -u | wc -l
15
[p585600@caddeapllx2193 ~]$

