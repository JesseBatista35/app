# 1) Para qual banco o datasource aponta?
grep -n -iE "connection-url|jndi-name" /opt/server/standalone/configuration/standalone.xml

# 2) System properties (ps não existe na imagem, então vai pelo /proc)
tr '\0' '\n' < /proc/1/cmdline | grep -iE "^-D|login|sso"
grep -n "<property name" /opt/server/standalone/configuration/standalone.xml

# 3) A URL está empacotada no deployment?
ls -la /opt/server/standalone/deployments/
cd /tmp && python3 - <<'EOF'
import zipfile, glob, re
for f in glob.glob('/opt/server/standalone/deployments/*.[wej]ar'):
    z = zipfile.ZipFile(f)
    for n in z.namelist():
        if n.endswith(('.properties','.yml','.yaml','.json','.xml','.class')):
            d = z.read(n)
            if b'login.des' in d or b'login.tqs' in d or b'urlServidorAutorizacao' in d:
                print(f, n)
EOF
