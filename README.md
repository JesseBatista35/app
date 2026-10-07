# 1. resolve para IP privado (privatelink) ou público?
nslookup stgsiopivendasonline.blob.core.windows.net

# 2. porta NFS alcançável?
timeout 5 bash -c '</dev/tcp/stgsiopivendasonline.blob.core.windows.net/2049' && echo "2049 OK" || echo "2049 FALHOU"

# 3. teste do mount com limite de tempo
sudo timeout 30 mount -t nfs -o vers=3,nolock,proto=tcp,sec=sys \
  stgsiopivendasonline.blob.core.windows.net:/stgsiopivendasonline/arquivosrecebidos /arquivos-recebidos; echo "rc=$?"
