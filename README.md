# esperar o server voltar a "running" e o deploy subir
until /opt/server/bin/jboss-cli.sh -c --command=':read-attribute(name=server-state)' 2>/dev/null | grep -q running; do sleep 3; done
/opt/server/bin/jboss-cli.sh -c --command='/deployment=sihdg-3.22.0.1.ear:read-attribute(name=status)'
/opt/server/bin/jboss-cli.sh -c --command='/system-property=SIHDG-SEC_URL_SERV_AUTH:read-resource'
curl -sk https://sihdg-jboss8-tqs.apps.nprd.caixa/sihdg-api/api/seguranca/configuracao-seguranca; echo


cd /tmp && python3 - <<'EOF'
import zipfile, io, re
ear = zipfile.ZipFile('/opt/server/standalone/deployments/sihdg-3.22.0.1.ear')
war = zipfile.ZipFile(io.BytesIO(ear.read('sihdg-api.war')))
core = zipfile.ZipFile(io.BytesIO(war.read('WEB-INF/lib/sihdg-core-3.22.0.1.jar')))
alvos = [(war, 'WEB-INF/classes/br/gov/caixa/arquitetura/javaee/api/comum/seguranca/keycloak/OidcConfigurationProvider.class'),
         (core, 'br/gov/caixa/arquitetura/javaee/core/comum/config/seguranca/SecuritySettings.class')]
for z, n in alvos:
    print('==', n.split('/')[-1])
    for s in re.findall(rb'[\x20-\x7e]{4,}', z.read(n)):
        s = s.decode()
        if not s.startswith(('(', 'L', 'java/', 'Ljava')) or 'SEC' in s or 'http' in s:
            print('  ', s)
EOF
















