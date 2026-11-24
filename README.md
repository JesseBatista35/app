bash
NS=sigec-tqs
oc get route sigec-csc-frontend-tqs -n $NS -o yaml | grep -iE 'timeout|host:'
oc get pods -n $NS -o wide | grep -i csc

Depois, com o nome do pod do frontend:

bash
POD=cole-aqui-o-nome-do-pod
oc rsh -n $NS $POD sh -c 'ps -ef | head -20; echo ---; grep -Rni "proxy_pass\|proxy_.*timeout\|server_tokens" /etc/nginx /opt/app-root/etc 2>/dev/null; echo ---; env | grep -iE "url|api|backend|proxy"'

Com isso dá para saber se o frontend repassa as chamadas para o backend (e por qual URL/IP) e se existe algum timeout de 120 s dentro do pod.

Atenção: o backend informado na WO (CADDEAPLLX765 / 10.116.193.253) foi levantado junto com o FQDN de DES. Vale conferir qual é o backend de TQS. O env do pod deve mostrar isso.

Em paralelo, se puder, peça ao dev para reproduzir em TQS com o DevTools aberto e te mandar o print da requisição do 504: Remote Address, headers e corpo da resposta. Esse print sozinho já pode apontar o proxy corporativo.
