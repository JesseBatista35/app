
-sh-4.2$
-sh-4.2$ nslookup stgsiopivendasonline.blob.core.windows.net
Server:         10.116.193.77
Address:        10.116.193.77#53

Non-authoritative answer:
stgsiopivendasonline.blob.core.windows.net      canonical name = stgsiopivendasonline.privatelink.blob.core.windows.net.
Name:   stgsiopivendasonline.privatelink.blob.core.windows.net
Address: 10.244.61.74

-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ timeout 5 bash -c '</dev/tcp/stgsiopivendasonline.blob.core.windows.net/2049' && echo "2049 OK" || echo "2049 FALHOU"
2049 FALHOU
-sh-4.2$
-sh-4.2$
-sh-4.2$ sudo timeout 30 mount -t nfs -o vers=3,nolock,proto=tcp,sec=sys \
>   stgsiopivendasonline.blob.core.windows.net:/stgsiopivendasonline/arquivosrecebidos /arquivos-recebidos; echo "rc=$?"

rc=124
-sh-4.2$
-sh-4.2$ mkdir -p /arquivos-recebidos && chown jboss:jboss /arquivos-recebidos
chown: alterando o dono de “/arquivos-recebidos”: Operação não permitida
-sh-4.2$ mountpoint -q /arquivos-recebidos && umount -f /arquivos-recebidos
-sh-4.2$ timeout 60 mount -t nfs -o vers=3,nolock,proto=tcp,sec=sys \
>   stgsiopivendasonline.blob.core.windows.net:/stgsiopivendasonline/arquivosrecebidos /arquivos-recebidos
mount: only root can use "--options" option
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
