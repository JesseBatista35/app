
[p585600@caddeapllx2864 ~]$ df -h
Sist. Arq.                         Tam. Usado Disp. Uso% Montado em
devtmpfs                           4,0M     0  4,0M   0% /dev
tmpfs                              1,8G     0  1,8G   0% /dev/shm
tmpfs                              730M   69M  662M  10% /run
/dev/mapper/VG_PRINCIPAL-LV_BARRA  9,0G  2,8G  6,2G  32% /
/dev/mapper/VG_PRINCIPAL-LV_VAR    5,0G 1006M  4,0G  20% /var
/dev/mapper/VG_PRINCIPAL-LV_OPT     10G  1,3G  8,7G  14% /opt
/dev/mapper/VG_PRINCIPAL-LV_LOGS   2,0G   64M  1,9G   4% /logs
/dev/mapper/VG_PRINCIPAL-LV_TMP    960M  960M  248K 100% /tmp
/dev/sda1                          960M  224M  737M  24% /boot
tmpfs                              365M  4,0K  365M   1% /run/user/10585600
[p585600@caddeapllx2864 ~]$ df -i
Sist. Arq.                           Inós IUsado  ILivre IUso% Montado em
devtmpfs                           461674    387  461287    1% /dev
tmpfs                              466932      1  466931    1% /dev/shm
tmpfs                              819200    721  818479    1% /run
/dev/mapper/VG_PRINCIPAL-LV_BARRA 4716544  67475 4649069    2% /
/dev/mapper/VG_PRINCIPAL-LV_VAR   2621440   2814 2618626    1% /var
/dev/mapper/VG_PRINCIPAL-LV_OPT   5242880  21859 5221021    1% /opt
/dev/mapper/VG_PRINCIPAL-LV_LOGS  1048576     74 1048502    1% /logs
/dev/mapper/VG_PRINCIPAL-LV_TMP       752     53     699    8% /tmp
/dev/sda1                          524288    358  523930    1% /boot
tmpfs                               93386     22   93364    1% /run/user/10585600
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$ sudo du -xh / --max-depth=2 2>/dev/null | sort -rh | head -20
[sudo] senha para p585600:
2,7G    /usr
2,7G    /
972M    /usr/share
739M    /usr/lib
509M    /usr/lib64
144M    /usr/local
115M    /usr/libexec
111M    /usr/bin
69M     /usr/sbin
38M     /etc
26M     /usr/include
12M     /etc/udev
8,3M    /etc/qualys
4,9M    /etc/selinux
4,1M    /etc/filebeat
1,9M    /etc/pki
1,6M    /etc/metricbeat
1,2M    /etc/pcp
844K    /usr/src
616K    /etc/ssh
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$ sudo du -sh /opt/*/jboss*/standalone/log /opt/*/jboss*/standalone/tmp /opt/*/jboss*/standalone/data 2>/dev/null
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$ sudo du -sh /tmp /var/tmp /var/cache/dnf /var/log
921M    /tmp
9,3M    /var/tmp
545M    /var/cache/dnf
128M    /var/log
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$ sudo find / -xdev \( -name "*.hprof" -o -name "core.*" \) -size +100M -exec ls -lh {} \; 2>/dev/null
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$ sudo dnf clean all
sudo find /tmp /var/tmp -type f -mtime +1 -delete
sudo journalctl --vacuum-size=200M
Atualizando repositórios do Subscription Management.
109 arquivos removidos
Vacuuming done, freed 0B of archived journals from /run/log/journal/175ac1f969f3427fab134cbfff65eae3.
Vacuuming done, freed 0B of archived journals from /run/log/journal.
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$ sudo find <JBOSS_HOME>/standalone/log -name "*.log.*" -mtime +7 -delete
-sh: JBOSS_HOME: Arquivo ou diretório inexistente
[p585600@caddeapllx2864 ~]$
