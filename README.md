No legado, o datasource usava um security-domain, e é lá que está o usuário de aplicação correto. Como o SIGSJ rodava no 0039 (era o java.library.path dele), dá para ver o usuário certo lá, sem precisar mexer na senha:

bash
# no sspdeapllx0039, como root
grep -rl "SIGSJ04" / --include=*-ds.xml --include=login-config.xml --include=*.xml 2>/dev/null | grep -v "/proc/" | head

Achando o arquivo, olha só o user-name / username (não cola senha aqui):

bash
grep -n -i -B2 -A8 "SIGSJ04" <arquivo> | grep -iE "user|security-domain|application-policy|jndi|connection-url"

Com isso, a correção é: usuário de aplicação + senha correta no standalone-full-ha.xml do SIGSJ-internet-config (user-name) e na variável SIGSJ04_PASSWORD do EC DES. Depois roda a release de DES. A senha correta vem dos devs/DBA ou da Segurança, como em TQS, e vai no privado. Vale conferir também o user-name do TQS, que pode ter o mesmo problema.

Bônus, sobre a acentuação (“Usuï¿½rio nï¿½o”): o JBoss 4 legado rodava com -Dfile.encoding=ISO8859_1 (vimos isso no ps do 0045), e a aplicação é toda ISO-8859-1. Dá para testar adicionando no standalone.conf da 2854:

JAVA_OPTS="$JAVA_OPTS -Dfile.encoding=ISO-8859-1"

É só um teste, e só vale depois de resolver o banco. Combina com os devs antes, porque muda o encoding default da JVM inteira. As imagens e o CSS quebrados continuam sendo o ponto dos estáticos (URL_STATICS) com os devs.

Para a sala, dá para resumir assim:
