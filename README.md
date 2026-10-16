cd /tmp && python3 - <<'EOF'
import zipfile, io, re
cnt = {'arq':0, 'cls':0}
def scan(z, path):
    for n in z.namelist():
        d = z.read(n)
        if n.endswith(('.war','.jar')):
            print('abrindo', path+'!/'+n)
            try: scan(zipfile.ZipFile(io.BytesIO(d)), path+'!/'+n)
            except Exception as e: print('  falhou:', e)
            continue
        cnt['arq'] += 1
        if n.endswith('.class'): cnt['cls'] += 1
        hits = set(re.findall(rb'login\.(?:des|tqs)\.caixa[^\x00"\s]*|SIHDG-SEC_\w+|SEC_\w+|urlServidorAutorizacao|configuracao-seguranca', d))
        if hits: print('>>', path+'!/'+n, sorted(h.decode(errors="ignore") for h in hits))
scan(zipfile.ZipFile('/opt/server/standalone/deployments/sihdg-3.22.0.1.ear'), 'ear')
print(cnt)
EOF
