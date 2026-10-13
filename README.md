[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$ sudo -l
[sudo] senha para p585600:
Sinto muito, tente novamente.
[sudo] senha para p585600:
Entradas de Defaults correspondentes a p585600 em caddeapllx2821:
    !visiblepw, always_set_home, match_group_by_gid, always_query_group_plugin, env_reset, env_keep="COLORS DISPLAY HOSTNAME HISTSIZE KDEDIR LS_COLORS", env_keep+="MAIL PS1 PS2 QTDIR USERNAME LANG
    LC_ADDRESS LC_CTYPE", env_keep+="LC_COLLATE LC_IDENTIFICATION LC_MEASUREMENT LC_MESSAGES", env_keep+="LC_MONETARY LC_NAME LC_NUMERIC LC_PAPER LC_TELEPHONE", env_keep+="LC_TIME LC_ALL LANGUAGE
    LINGUAS _XKB_CHARSET XAUTHORITY", secure_path=/sbin\:/bin\:/usr/sbin\:/usr/bin

Usuário p585600 pode executar os seguintes comandos em caddeapllx2821:
    (root) !/usr/bin/ksh, !/usr/local/bin/tsch, !/usr/bin/rsh, !/usr/local/bin/zsh
    (root) ALL, /etc/init.d/slapd, /usr/bin/sudo -i, !/bin/su, !/bin/sh, !/usr/bin/csh, !/usr/bin/ksh, !/usr/local/bin/tsch, !/usr/bin/rsh, !/usr/local/bin/zsh
    (root) ALL, /etc/init.d/slapd, /usr/bin/sudo -i, /bin/su, /opt/jboss/jboss-eap/bin/init.d/jboss-eap-standalone.sh stop, /opt/jboss/jboss-eap/bin/init.d/jboss-eap-standalone.sh start,
        /opt/jboss/jboss-eap/bin/init.d/jboss-eap-standalone.sh status, /usr/bin/mkdir, !/bin/sh, !/usr/bin/csh, !/usr/bin/ksh, !/usr/local/bin/tsch, !/usr/bin/rsh, !/usr/local/bin/zsh,
        !/usr/bin/script
    (root) ALL, /bin/su, /etc/init.d/slapd, /usr/bin/sudo -i, /opt/jboss/jboss-eap/bin/init.d/jboss-eap-standalone.sh stop, /opt/jboss/jboss-eap/bin/init.d/jboss-eap-standalone.sh start,
        /opt/jboss/jboss-eap/bin/init.d/jboss-eap-standalone.sh status, !/bin/sh, !/usr/bin/csh, !/usr/bin/ksh, !/usr/local/bin/tsch, !/usr/bin/rsh, !/usr/local/bin/zsh
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$ ip -4 addr show ens224
3: ens224: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state UP group default qlen 1000
    altname enp19s0
    inet 10.188.6.225/19 brd 10.188.31.255 scope global noprefixroute ens224
       valid_lft forever preferred_lft forever
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$ ssh 10.116.192.x   # caddeapllx2781
ssh: Could not resolve hostname 10.116.192.x: Name or service not known
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$ ip -4 addr show ens224
3: ens224: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state UP group default qlen 1000
    altname enp19s0
    inet 10.188.6.225/19 brd 10.188.31.255 scope global noprefixroute ens224
       valid_lft forever preferred_lft forever
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$ sudo dnf install -y tcpdump
[sudo] senha para p585600:
Atualizando repositórios do Subscription Management.
Red Hat Enterprise Linux 9 for x86_64 - Extensions (RPMs)                                                                                                             137 kB/s | 3.8 kB     00:00
Red Hat Satellite Client 6 for RHEL 9 x86_64 (RPMs)                                                                                                                   136 kB/s | 3.8 kB     00:00
Zabbix 6 REDHAT 9                                                                                                                                                      90 kB/s | 1.5 kB     00:00
Red Hat Enterprise Linux 9 for x86_64 - Supplementary (RPMs)                                                                                                          139 kB/s | 3.8 kB     00:00
Red Hat Enterprise Linux 9 for x86_64 - BaseOS (RPMs)                                                                                                                 150 kB/s | 4.1 kB     00:00
Zabbix 6.4 REDHAT 9                                                                                                                                                    89 kB/s | 1.5 kB     00:00
Red Hat Satellite Utils 6.18 for RHEL 9 x86_64 (RPMs)                                                                                                                 142 kB/s | 3.8 kB     00:00
Puppet REDHAT 9                                                                                                                                                        96 kB/s | 1.5 kB     00:00
EPEL REDHAT 9 - Everything                                                                                                                                             48 kB/s | 2.3 kB     00:00
OCS - Instaladores Redhat 9                                                                                                                                            87 kB/s | 1.5 kB     00:00
Red Hat Enterprise Linux 9 for x86_64 - AppStream (RPMs)                                                                                                              159 kB/s | 4.5 kB     00:00
Dependências resolvidas.
======================================================================================================================================================================================================
 Pacote                                    Arquitetura                              Versão                                             Repositório                                               Tam.
======================================================================================================================================================================================================
Instalando:
 tcpdump                                   x86_64                                   14:4.99.0-9.el9                                    InstallMedia-AppStream                                   547 k

Resumo da transação
======================================================================================================================================================================================================
Instalar  1 pacote

Tamanho total do download: 547 k
Tamanho depois de instalado: 1.4 M
Baixando pacotes:
tcpdump-4.99.0-9.el9.x86_64.rpm                                                                                                                                        18 MB/s | 547 kB     00:00
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Total                                                                                                                                                                  17 MB/s | 547 kB     00:00
Executando verificação da transação
Verificação de transação concluída.
Executando teste de transação
Teste de transação concluído.
Executando a transação
  Preparando          :                                                                                                                                                                           1/1
  Executando scriptlet: tcpdump-14:4.99.0-9.el9.x86_64                                                                                                                                            1/1
  Instalando          : tcpdump-14:4.99.0-9.el9.x86_64                                                                                                                                            1/1
  Executando scriptlet: tcpdump-14:4.99.0-9.el9.x86_64                                                                                                                                            1/1
  Verificando         : tcpdump-14:4.99.0-9.el9.x86_64                                                                                                                                            1/1
Produtos instalados atualizados.

Instalados:
  tcpdump-14:4.99.0-9.el9.x86_64

Concluído!
[p585600@caddeapllx2821 ~]$ sudo tcpdump -i ens224 -n -c 30 arp
dropped privs to tcpdump
tcpdump: verbose output suppressed, use -v[v]... for full protocol decode
listening on ens224, link-type EN10MB (Ethernet), snapshot length 262144 bytes
14:23:36.971789 ARP, Request who-has 1.1.1.8 tell 1.1.1.7, length 46
14:23:36.975985 ARP, Request who-has 181.0.0.8 tell 181.0.0.1, length 46
14:23:36.976029 ARP, Request who-has 192.168.234.0 tell 192.168.233.255, length 46
14:23:37.016307 ARP, Request who-has 192.168.242.20 tell 192.168.235.52, length 46
14:23:37.082084 ARP, Request who-has 192.168.234.57 tell 192.168.234.56, length 46
14:23:37.108022 ARP, Request who-has 10.188.8.107 tell 192.168.233.255, length 46
14:23:37.140824 ARP, Request who-has 10.188.8.111 tell 192.168.234.0, length 46
14:23:37.159137 ARP, Request who-has 192.168.227.27 tell 192.168.226.168, length 46
14:23:37.191886 ARP, Request who-has 192.168.230.111 tell 192.168.230.112, length 46
14:23:37.260271 ARP, Request who-has 181.0.0.3 tell 181.0.0.7, length 46
14:23:37.275423 ARP, Request who-has 192.168.122.223 tell 192.168.235.178, length 46
14:23:37.281565 ARP, Request who-has 192.168.230.112 tell 192.168.230.111, length 46
14:23:37.409310 ARP, Request who-has 192.168.229.198 tell 192.168.227.27, length 46
14:23:37.474296 ARP, Request who-has 181.0.0.3 tell 181.0.0.1, length 46
14:23:37.498250 ARP, Request who-has 192.168.234.56 tell 192.168.234.57, length 46
14:23:37.533415 ARP, Request who-has 192.168.224.132 tell 192.168.232.29, length 46
14:23:37.558686 ARP, Request who-has 192.168.226.150 tell 192.168.230.4, length 46
14:23:37.610303 ARP, Request who-has 181.0.0.8 tell 181.0.0.7, length 46
14:23:37.610443 ARP, Request who-has 181.0.0.22 tell 181.0.0.27, length 46
14:23:37.626143 ARP, Request who-has 181.0.0.22 tell 181.0.0.21, length 46
14:23:37.649046 ARP, Reply 192.168.227.9 is-at 00:14:4f:f8:ab:5a, length 46
14:23:37.649050 ARP, Reply 192.168.236.69 is-at 00:14:4f:fb:70:b5, length 46
14:23:37.683907 ARP, Request who-has 192.168.233.255 tell 192.168.234.0, length 46
14:23:37.871400 ARP, Request who-has 192.168.250.106 tell 192.168.241.246, length 46
14:23:37.887322 ARP, Request who-has 181.0.0.22 tell 181.0.0.23, length 46
14:23:37.976116 ARP, Request who-has 192.168.234.0 tell 192.168.233.255, length 46
14:23:37.978142 ARP, Request who-has 181.0.0.8 tell 181.0.0.1, length 46
14:23:37.988154 ARP, Request who-has 192.168.234.57 tell 192.168.234.56, length 46
14:23:38.002949 ARP, Request who-has 192.168.227.27 tell 192.168.229.198, length 46
14:23:38.018223 ARP, Request who-has 192.168.242.20 tell 192.168.235.52, length 46
30 packets captured
30 packets received by filter
0 packets dropped by kernel
[p585600@caddeapllx2821 ~]$
