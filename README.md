
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]# ls -la /apl/sigsj/properties/
ls: não foi possível acessar '/apl/sigsj/properties/': Arquivo ou diretório inexistente
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]# echo "--- conteudo (sem senha) ---"
grep -riE "gj02|aviso|sirot|host|url" /apl/sigsj/properties/ 2>/dev/null | grep -viE "senha|password" | head
--- conteudo (sem senha) ---
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#
