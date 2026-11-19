IPs:

Servidor	IP	Função
cbrdeapllx471	10.116.97.59	Domain Controller (CLI e deploy)
cbrdeapllx473	10.116.97.79	Onde as aplicações rodam (log)
1. Baixar o SIPEN no 471 (bash)
bash
ssh p585600@10.116.97.59
sudo su
cd /tmp
curl --noproxy '*' -f -o pen-ear-2.32.0.2.ear http://binario.caixa:8081/repository/releases/br/gov/caixa/sipen/pen-ear/2.32.0.2/pen-ear-2.32.0.2.ear
ls -l pen-ear-2.32.0.2.ear
unzip -t pen-ear-2.32.0.2.ear | tail -1
2. Ver em qual server-group o SIPEN roda (CLI do 471)
bash
/opt/jboss/jboss-eap/bin/jboss-cli.sh --connect --controller=localhost:9999

Dentro do CLI:

deployment-info --name=SIPEN
:read-children-names(child-type=server-group)

Me mande as saídas. Ainda não faça o deploy. Primeiro confirmamos o server-group certo e depois te passo o comando final.
