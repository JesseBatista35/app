ls -la /apl/sigsj/properties/
echo "--- conteudo (sem senha) ---"
grep -riE "gj02|aviso|sirot|host|url" /apl/sigsj/properties/ 2>/dev/null | grep -viE "senha|password" | head
