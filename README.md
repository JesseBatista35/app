asso 1 — copiar na 955 (intranet) e testar agora. Como root na 955:

bash
mkdir -p /apl/sigsj/properties
cd /apl/sigsj/properties
scp p585600@10.116.88.96:/apl/sigsj/properties/\*.properties .
chown -R jboss:jboss /apl/sigsj
chmod 644 /apl/sigsj/properties/*.properties
ls -la /apl/sigsj/properties/

Depois testa (não precisa reiniciar, mas se o bundle for lido no boot pode precisar — testa primeiro sem):

bash
curl -s -o /dev/null -w "intranet default.jsp: %{http_code}\n" http://10.116.194.179/sigsj_intranet/default.jsp

E o teste real: login pelo navegador e ver se o bemVindo.xhtml renderiza. Se ainda der 500, aí reinicia o JBoss (systemctl restart jboss-eap-standalone) e testa de novo — alguns bundles só recarregam no start.

Se renderizar → confirmado, os properties eram a causa. Replicamos nas outras duas VMs e eu monto o custom.sh definitivo.
Se ainda der NPE na GJ02 → aí é código mesmo (devs), e passamos.

Passo 2 — depois de confirmar, eu te entrego o custom.sh (log4j + properties) pra commitar em configuration/ dos 3 repos, e a esteira passa a entregar sozinha. O conteúdo dos properties já tenho; só falta os devs confirmarem que concordam com esses valores pra DES (mas estão com cara de DES corretos).

Roda o passo 1 e me diz se o intranet subiu a tela pós-login. Se subir, já comemora — o intranet fica completo (auth + avisos), e sobra só o internet (banco SGSJSD01) e o custom.sh definitivo.
