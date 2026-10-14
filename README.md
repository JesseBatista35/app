mount -t nfs 192.168.227.59:/export/sicql_bovespa /opt/sigdb
echo $?
ls -ld /producao/SWIFT
mount -t nfs 192.168.227.59:/export/sicql_bovespa /producao/SWIFT
echo $?

mkdir /producao/SWIFT
mount -t nfs 192.168.227.59:/export/sicql_bovespa /producao/SWIFT
