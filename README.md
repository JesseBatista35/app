cd /tmp && rm -rf earx && mkdir earx && cd earx
unzip -o /opt/jboss-eap/standalone/deployments/sigsj_intranet-ear.ear >/dev/null 2>&1
# explode os wars/jars internos também
for f in $(find . -name "*.war" -o -name "*.jar"); do d="${f}.d"; mkdir -p "$d"; unzip -o "$f" -d "$d" >/dev/null 2>&1; done

# agora procura de verdade
grep -rl "SenhasSIIBC" . 2>/dev/null
echo "--- SIROT/SIPER? ---"
grep -rliE "sirot|siper|CONNECTOR-FARM|sendRajada" . 2>/dev/null | head
echo "--- classe da lib? ---"
find . -iname "*SenhasSIIBC*" 2>/dev/null
