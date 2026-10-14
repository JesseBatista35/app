grep -E 'sigdb|SWIFT|SIEXC_SWIFT|eFinanceira' /etc/fstab
sudo mkdir -p /opt/sigdb /producao/SWIFT /SIEXC_SWIFT /eFinanceira/siexc/entrada
sudo mount -t nfs 192.168.227.59:/export/sicql_bovespa /SIEXC_SWIFT
sudo mount -t nfs nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /eFinanceira/siexc/entrada
