Antes de corrigir

Não mexa no Timeout 120 global. Esse Apache é compartilhado por vários sistemas. A correção certa é um ProxyTimeout só no vhost do sigec-csc. O vhost não está em conf/ nem em conf.d/, então vamos achá-lo:

bash
grep -niE '^\s*Include' $H/conf/httpd.conf $H/conf/httpd_eap_71_esteiraagil.conf
grep -Rln --exclude-dir=logs 'sigec-csc' $H 2>/dev/null

Depois, com o arquivo encontrado:

bash
VH=caminho-que-apareceu
grep -niE 'VirtualHost|ServerName|ProxyPass|BalancerMember|timeout|ErrorLog' $VH
Correção (depois de achar o vhost)

Dentro do <VirtualHost> do sigec-csc TQS, acrescente:

apache
ProxyTimeout 600

Faça isso nos dois servidores (137 e 138) e valide antes de recarregar:

bash
sudo $H/sbin/httpd -f $H/conf/httpd.conf -d $H -f $H/conf/httpd_eap_71_esteiraagil.conf -t
sudo $H/sbin/httpd -f $H/conf/httpd.conf -d $H -f $H/conf/httpd_eap_71_esteiraagil.conf -k graceful

O graceful não derruba as conexões dos outros sistemas.

Um ponto de atenção

O vhost é gerado pela esteira (role vhost, task "Deploy Virtual Host"). A próxima release do SIGEC-CSC vai sobrescrever o ajuste manual. Para resolver de vez, veja se o template do vhost no esteira-jboss-vm aceita alguma variável de timeout. Se não aceitar, vale incluir. Isso é com quem mantém a esteira.

Me manda o vhost que eu confiro onde encaixar a linha.

Como o Claude está se saindo ne
