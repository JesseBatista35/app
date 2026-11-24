2. Confirmar a route que atende o FQDN usado no teste:

bash
oc get route -A -o custom-columns=NS:.metadata.namespace,NAME:.metadata.name,HOST:.spec.host,TIMEOUT:'.metadata.annotations.haproxy\.router\.openshift\.io/timeout' | grep -i sigec-csc

3. Ver se o pod do frontend faz proxy para o backend:

bash
oc rsh deploy/<frontend> sh -c 'grep -Rni "proxy_pass\|proxy_.*timeout\|keepalive_timeout" /etc/nginx 2>/dev/null; env | grep -iE "url|api|backend"'

Se houver proxy_read_timeout 120s (ou um servidor Node antigo, cujo timeout padrão também é 120 s), achamos o problema.

4. Chamar o backend sem passar pelo frontend nem pelo proxy, com o mesmo endpoint de exportação:

bash
# de dentro do pod do frontend (mesmo caminho de rede real)
oc rsh deploy/<frontend> curl -sk -o /dev/null --max-time 600 \
  -w 'HTTP %{http_code} em %{time_total}s\n' https://10.116.193.253/<contexto>/<endpoint-export>
# depois, pela rota, com bypass de proxy (de um jumper)
curl -sk --noproxy '*' -o /dev/null --max-time 600 -w 'HTTP %{http_code} em %{time_total}s\n' \
  https://sigec-csc-frontn-des.apps.nprd.caixa/<endpoint>
Se os dois passarem de 120 s com 200, o problema está do lado do cliente: proxy corporativo ou PAC.
Se o primeiro falhar em 120 s, o problema está entre o OKD e o backend: VIP ou JBoss.

5. Na VM CADDEAPLLX765:

bash
ip -4 a | grep 10.116.193.253        # o IP é da VM ou é VIP?
ss -ltnp | grep -E ':443|:8443'      # quem escuta na 443
grep -nE 'no-request-timeout|read-timeout|write-timeout|request-parse-timeout' standalone-full-ha.xml

Ligue também o access-log do Undertow, se ainda não estiver ativo. Se o JBoss registrar 200 depois de 150 s, por exemplo, ele terminou o trabalho e alguém no meio cortou a conexão. Se o IP for VIP, aí sim cabe perguntar à Redes, de forma específica, quais são os timeouts de idle e de servidor do VIP 10.116.193.253:443.

Correção definitiva

Mesmo achando a camada, uma exportação síncrona de mais de 2 minutos fica frágil: o próximo equipamento com timeout curto quebra de novo. O ideal é o dev tornar a exportação assíncrona: dispara a geração, consulta o status e depois baixa o arquivo pronto. Vale sugerir isso na reunião.

Quando você tiver o resultado do passo 1 (cabeçalhos e corpo do 504), me mande que eu fecho o diagnóstico com você.
