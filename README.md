Comandos prontos para colar (SIGEC CSC)

1. Achar o namespace e a route:

bash
oc get route --all-namespaces 2>/dev/null | grep -i sigec-csc
# se der erro de permissão:
oc projects | grep -i sigec

2. Com o namespace em mãos (troque só o valor de NS):

bash
NS=sigec-des   # ajuste conforme o resultado acima
oc get route -n $NS -o yaml | grep -iE ' name:| host:|timeout'
oc get pods -n $NS | grep -i csc

Com isso confirmamos se a route sigec-csc-frontn-des (do FQDN da WO) também tem o timeout: 10m, ou se só a de TQS foi ajustada.

3. Ver se o pod do frontend faz proxy (troque POD pelo nome que saiu no passo 2):

bash
POD=nome-do-pod-frontend
oc rsh -n $NS $POD sh -c 'grep -Rni "proxy_pass\|proxy_.*timeout" /etc/nginx /opt/app-root/etc 2>/dev/null; env | grep -iE "url|api|backend"'

4. Teste de tempo direto no backend. Para este passo você precisa do caminho real da exportação, que o dev pega no DevTools (aba Network, requisição que deu 504, campo "Request URL"). Sem esse caminho não dá para rodar. Quando tiver, troque CAMINHO:

bash
CAMINHO=/contexto/api/exportacao   # pegar com o dev
oc rsh -n $NS $POD curl -sk -o /dev/null --max-time 600 \
  -w 'HTTP %{http_code} em %{time_total}s\n' "https://10.116.193.253$CAMINHO"

O teste mais rápido e mais decisivo continua sendo o do DevTools: Remote Address, cabeçalhos e corpo do 504 na máquina do dev. Se der para pedir isso a ele agora pelo Teams, já sabemos se é o proxy corporativo antes mesmo dos passos 3 e 4. Me manda as saídas dos passos 1 e 2 que eu sigo com você.
