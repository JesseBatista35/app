A aplicação respondendo. Lembra que antes o /siemp_java dava 404 no JBoss:
bash
curl -vk --resolve siemp.des.caixa:443:10.116.180.9 https://siemp.des.caixa/siemp_java/

Deve vir 200 ou a tela de login, e não o 404 do Undertow.

O /tmp depois do deploy:
bash
df -h /tmp

Se passou de ~80%, vale fazer o lvextend agora, antes do próximo deploy.

O DNS: se a REQ de siemp.des.caixa → 10.116.180.9 ainda não foi aberta, é o próximo passo da URL.

Me avisa se o curl voltar com algo diferente de 200 ou login.
