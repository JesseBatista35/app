# o legado alcança esse host:porta?
timeout 5 bash -c "cat < /dev/null > /dev/tcp/10.116.89.101/8111" && echo "0039 ABRIU 101:8111" || echo "0039 SEM CONEXAO 101:8111"

# qual host/porta de SIPER o legado realmente usa (dentro do jar do sirot e configs globais)
cd /tmp && rm -rf sirotjar && unzip -o $B/deployapp/sirotconEjb_v2.2.7.jar -d /tmp/sirotjar >/dev/null 2>&1
find /tmp/sirotjar -name "*.properties" -exec echo "== {} ==" \; -exec cat {} \;
grep -rniE "8111|8[0-9]{3}|10\.116\.|host|ip|farm|siper|conector" /tmp/sirotjar 2>/dev/null | grep -viE "class|META-INF|password" | head -20

# config global do sirot na máquina (fora da app)
find / -iname "*sirot*" 2>/dev/null | grep -viE "/proc/|\.class" | head
cat /apl/sigsj/properties/*.properties 2>/dev/null | grep -iE "siper|sirot|farm|conector|8111|10\.116\.89\.101"
