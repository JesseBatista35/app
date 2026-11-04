Antes de trocar, confira os certificados da Caixa na cacerts do Linux. A cacerts padrão do Java pode não ter as ACs internas da Caixa (AC Icptestes, AC Caixa), e essas ACs são usadas no login.des.caixa, no api.des.caixa e em outros serviços internos. A do Windows provavelmente tinha. No 473:

bash
keytool -list -keystore /usr/java/openjdk-1.8.0.482/jre/lib/security/cacerts -storepass changeit | grep -iE "caixa|icp"
Se aparecerem entradas da Caixa ou da ICP: pode seguir com a troca.
Se não aparecer nada: me avise antes de trocar. Pode existir uma truststore corporativa já pronta no servidor, ou será preciso importar a cadeia. Para procurar:
bash
  sudo find /opt/jboss /etc/pki -iname "*.jks" -o -iname "*truststore*" 2>/dev/null | head

Troca (no jboss-cli do 471), depois da conferência:
