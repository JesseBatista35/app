
[p585600@caddeapllx2864 ~]$ sudo ls -lahS /tmp | head -20
total 4,0K
drwxrwxrwt. 11 root  root  4,0K nov 17 17:01 .
dr-xr-xr-x. 19 root  root   267 jan 28  2025 ..
drwxr-xr-x   4 root  root    38 nov 17 17:01 siemp
drwxr-xr-x   2 jboss jboss   20 nov 12 12:08 hsperfdata_jboss
drwx------   3 root  root    17 nov  6 15:13 systemd-private-3757e1b180f44d5fb122c794685e2500-dbus-broker.service-C0iUTO
drwx------   3 root  root    17 nov 12 10:59 systemd-private-3757e1b180f44d5fb122c794685e2500-httpd-eap.service-4y79vi
drwx------   3 root  root    17 nov  6 15:13 systemd-private-3757e1b180f44d5fb122c794685e2500-kdump.service-lTdHWg
drwx------   3 root  root    17 nov  6 15:13 systemd-private-3757e1b180f44d5fb122c794685e2500-systemd-logind.service-7mKbwV
drw-------   2 root  root     6 nov 17 13:03 hsperfdata_root
drwxr-xr-x   2 jboss jboss    6 nov 17 17:01 src
drwx------   2 root  root     6 nov  6 15:13 vmware-root_814-2966103502
-rw-------   1 root  root     0 nov 17 13:02 opera_headless_check
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$ sudo du -ah /tmp 2>/dev/null | sort -rh | head -20
36K     /tmp
32K     /tmp/hsperfdata_jboss/677441
32K     /tmp/hsperfdata_jboss
0       /tmp/vmware-root_814-2966103502
0       /tmp/systemd-private-3757e1b180f44d5fb122c794685e2500-systemd-logind.service-7mKbwV/tmp
0       /tmp/systemd-private-3757e1b180f44d5fb122c794685e2500-systemd-logind.service-7mKbwV
0       /tmp/systemd-private-3757e1b180f44d5fb122c794685e2500-kdump.service-lTdHWg/tmp
0       /tmp/systemd-private-3757e1b180f44d5fb122c794685e2500-kdump.service-lTdHWg
0       /tmp/systemd-private-3757e1b180f44d5fb122c794685e2500-httpd-eap.service-4y79vi/tmp
0       /tmp/systemd-private-3757e1b180f44d5fb122c794685e2500-httpd-eap.service-4y79vi
0       /tmp/systemd-private-3757e1b180f44d5fb122c794685e2500-dbus-broker.service-C0iUTO/tmp
0       /tmp/systemd-private-3757e1b180f44d5fb122c794685e2500-dbus-broker.service-C0iUTO
0       /tmp/src
0       /tmp/siemp/META-INF/maven/br.gov.caixa.siemp/siemp-ear
0       /tmp/siemp/META-INF/maven/br.gov.caixa.siemp
0       /tmp/siemp/META-INF/maven
0       /tmp/siemp/META-INF
0       /tmp/siemp/conteudo/META-INF/maven/br.gov.caixa.siemp/siemp-ear
0       /tmp/siemp/conteudo/META-INF/maven/br.gov.caixa.siemp
0       /tmp/siemp/conteudo/META-INF/maven
[p585600@caddeapllx2864 ~]$
