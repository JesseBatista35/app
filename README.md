hostname -f

# o mount está ativo aqui? se estiver, já funcionou em algum momento
mount | grep -i arquivos; df -h /arquivos-recebidos 2>/dev/null

# a rota até o endpoint existe? testa a 443 (HTTPS do blob) no mesmo IP
timeout 5 bash -c '</dev/tcp/10.244.61.74/443' && echo "443 OK" || echo "443 FALHOU"
