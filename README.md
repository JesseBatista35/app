cd /tmp && python3 - <<'EOF'
import zipfile, io, re
def scan(z, path):
    for n in z.namelist():
        d = z.read(n)
        if n.endswith(('.war','.jar')):
            try: scan(zipfile.ZipFile(io.BytesIO(d)), path+'!/'+n)
            except Exception: pass
            continue
        if n.endswith(('.properties','.yml','.yaml','.json','.xml','.class')):
            hits = set(re.findall(rb'login\.(?:des|tqs)\.caixa[^\x00"\s]*|SIHDG-SEC_\w+|SEC_\w*(?:URL|SERVIDOR|AUTORIZ|REALM|CLIENT)\w*|urlServidorAutorizacao', d))
            if hits: print(path+'!/'+n, sorted(h.decode(errors="ignore") for h in hits))
scan(zipfile.ZipFile('/opt/server/standalone/deployments/sihdg-3.22.0.1.ear'), 'ear')
EOF
