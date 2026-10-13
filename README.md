up
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$ ip -s link show ens224; sleep 30; ip -s link show ens224
3: ens224: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state UP mode DEFAULT group default qlen 1000
    link/ether 00:50:56:82:a5:1d brd ff:ff:ff:ff:ff:ff
    RX:  bytes  packets errors dropped  missed   mcast
    1770595403 24354178      0   23822       0       8
    TX:  bytes  packets errors dropped carrier collsns
         25732      492      0       0       0       0
    altname enp19s0
3: ens224: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state UP mode DEFAULT group default qlen 1000
    link/ether 00:50:56:82:a5:1d brd ff:ff:ff:ff:ff:ff
    RX:  bytes  packets errors dropped  missed   mcast
    1770654619 24354970      0   23822       0       8
    TX:  bytes  packets errors dropped carrier collsns
         25732      492      0       0       0       0
    altname enp19s0
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
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
[p585600@caddeapllx2821 ~]$
