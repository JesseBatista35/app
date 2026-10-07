
-sh-4.2$
-sh-4.2$ timeout 5 bash -c '</dev/tcp/10.244.61.74/2049' && echo OK || echo FALHOU
FALHOU
-sh-4.2$ ^C
-sh-4.2$ hostname -f
caddeapllx1524.agil.nprd.caixa.gov.br
-sh-4.2$
-sh-4.2$
-sh-4.2$ mount | grep -i arquivos; df -h /arquivos-recebidos 2>/dev/null
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ timeout 5 bash -c '</dev/tcp/10.244.61.74/443' && echo "443 OK" || echo "443 FALHOU"
443 FALHOU
-sh-4.2$
