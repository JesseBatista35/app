cd /tmp && python3 - <<'EOF'
import zipfile, io
ear = zipfile.ZipFile('/opt/server/standalone/deployments/sihdg-3.22.0.1.ear')
war = zipfile.ZipFile(io.BytesIO(ear.read('sihdg-api.war')))
for z in (ear, war):
    for n in z.namelist():
        if n.endswith(('pom.properties','MANIFEST.MF')): print('==',n); print(z.read(n).decode(errors='ignore'))
EOF
