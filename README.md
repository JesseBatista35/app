# 1) No navegador (F12 > Network, "Preserve log"), abra a URL TQS e veja:
#    - a requisição para login.des.caixa/.../auth?client_id=...&redirect_uri=...  (anote realm e client_id)
#    - qual requisição ANTES dela trouxe a URL do SSO: /api/<algo de config>, assets/*.json ou só main.*.js

# 2) Frontend TQS: a URL está fixa no bundle?
oc project sihdg-tqs
oc get pods
oc rsh <pod-frontend>
grep -rl "login.des" /opt/app-root/src /usr/share/nginx/html 2>/dev/null
grep -rl "login.tqs" /opt/app-root/src /usr/share/nginx/html 2>/dev/null
cat /etc/nginx/conf.d/*.conf | grep proxy_pass      # valor real do __HTTP_SERVICE_API__

# 3) Backend TQS: standalone com DES?
oc rsh <pod-sihdg-jboss8-tqs>
grep -n -iE "login\.(des|tqs)|auth-server-url|provider-url|realm" $JBOSS_HOME/standalone/configuration/standalone*.xml
env | grep -iE "sso|keycloak|oidc|login"
