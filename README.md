O Marcio trouxe quatro pontos. Dois deles mudam o plano.

1. Senha do SIGSJ04 (internet TQS): o security-domain não vai no campo de senha.
No JBoss 5 do legado, o datasource não guarda a senha nele mesmo. Ele aponta para um <security-domain>, e a senha fica dentro desse domínio (no login-config.xml), normalmente codificada. Com o nome do security-domain no SIGSJ04_PASSWORD, o JBoss vai mandar esse nome como senha para o Oracle, e a conexão falha com ORA-01017.

O caminho certo é o SIGSJ04_PASSWORD receber a senha real do usuário de TQS, como secreta. Quem tem essa senha é a Gisele ou o DBA. Não precisa criar variável de security-domain: o standalone novo já usa usuário e senha direto, e é assim que o internet DES funciona.

2. JVM_PROXY_HOST com proxydes.caixa no TQS. A dúvida faz sentido, mas eu não confirmaria sem testar. Na VM do internet TQS (2865):

bash
nslookup proxytqs.caixa
nslookup proxydes.caixa

Compare também com o valor dessa variável no grupo TQS de outro sistema que já roda em TQS na esteira. Se proxytqs.caixa existir e for o padrão nos outros TQS, troque. Se não resolver, mantém proxydes.

3. Intranet não usa Oracle: isso simplifica tudo. Se o intranet não acessa banco, o datasource SIGSJ04 não deveria estar no standalone dele. Hoje ele atrapalha: com os tokens na master, a release do TQS vai falhar no Replace Tokens por falta das variáveis. Antes de remover, confirme que nada no pacote referencia o datasource (no 2863):

bash
cd /tmp && mkdir -p intra && cd intra
unzip -o -q /opt/jboss-eap/standalone/deployments/sigsj_intranet-ear.ear
grep -rl 'SIGSJ04\|datasources/' . 2>/dev/null | head
Se não voltar nada: removam do SIGSJ-intranet-config o bloco <datasource ... SIGSJ04 ...> e a linha do ojdbc8 no jboss-deployments. Aí o intranet TQS sobe sem precisar de variável de banco.
Se voltar algum arquivo: me manda que a gente vê antes de mexer.

4. Boleto precisa de URL: fica registrado. Entra no pedido das URLs junto com intranet e internet.

Internet reimplantado pelo Marcio: depois da nova release, valide no 2865:

bash
grep -iE 'SIGSJ04|ORA-[0-9]|faltam' /logs/jboss/jboss-eap/standalone/sigsj-internet/server.log | tail -10

Se aparecer ORA-01017, é o item 1: o nome do security-domain foi usado como senha.

Sugestão de resposta para o Marcio:

Obrigado, Marcio!

Senha: no JBoss 5 o datasource referencia um security-domain onde a senha fica guardada; no JBoss 7.4 da esteira usamos usuário e senha direto no datasource. Então o SIGSJ04_PASSWORD precisa ter a senha real do usuário de TQS (como secreta), não o nome do security-domain. Não precisa criar variável de security domain. Conseguem passar a senha do usuário de TQS (ou confirmar com o DBA)?
Proxy: vou validar se o proxytqs.caixa resolve nas VMs de TQS e te retorno.
Intranet sem Oracle: ótimo. Nesse caso sugiro remover o datasource SIGSJ04 do SIGSJ-intranet-config (e o ojdbc8 do jboss-deployments), senão a release vai cobrar as variáveis de banco sem necessidade. Vou só confirmar no pacote que nada referencia o datasource.
Boleto: anotado, vamos incluir no pedido das URLs.





Microsoft Windows [versão 10.0.26200.9711]
(c) Microsoft Corporation. Todos os direitos reservados.

C:\Users\p585600>nslookup proxytqs.caixa
Servidor:  dfaddssd001.corp.caixa.gov.br
Address:  10.222.149.10

*** dfaddssd001.corp.caixa.gov.br não encontrou proxytqs.caixa: Non-existent domain

C:\Users\p585600>nslookup proxydes.caixa
Servidor:  dfaddssd001.corp.caixa.gov.br
Address:  10.222.149.10

Nome:    proxydes.caixa
Addresses:  10.252.32.65
          10.252.32.63


C:\Users\p585600

nao existe proxytqs aqui



p585600@10.116.202.53's password:
Last login: Fri Nov  6 16:31:37 2026 from 10.122.150.31
[p585600@caddeapllx2863 ~]$
[p585600@caddeapllx2863 ~]$
[p585600@caddeapllx2863 ~]$ cd /tmp && mkdir -p intra && cd intra
[p585600@caddeapllx2863 intra]$
[p585600@caddeapllx2863 intra]$
[p585600@caddeapllx2863 intra]$ unzip -o -q /opt/jboss-eap/standalone/deployments/sigsj_intranet-ear.ear
[p585600@caddeapllx2863 intra]$
[p585600@caddeapllx2863 intra]$
[p585600@caddeapllx2863 intra]$ grep -rl 'SIGSJ04\|datasources/' . 2>/dev/null | head
[p585600@caddeapllx2863 intra]$
