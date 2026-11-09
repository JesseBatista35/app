caddeapllx2863 ~]$
[p585600@caddeapllx2863 ~]$ cd /tmp && mkdir -p intra && cd intra
[p585600@caddeapllx2863 intra]$
[p585600@caddeapllx2863 intra]$
[p585600@caddeapllx2863 intra]$ unzip -o -q /opt/jboss-eap/standalone/deployments/sigsj_intranet-ear.ear
[p585600@caddeapllx2863 intra]$
[p585600@caddeapllx2863 intra]$
[p585600@caddeapllx2863 intra]$ grep -rl 'SIGSJ04\|datasources/' . 2>/dev/null | head
[p585600@caddeapllx2863 intra]$ ls
lib  META-INF  sigsj_intranet.war  sigsjintrastatic.war  sirotcon-ejb-2.3.0.1-farm.jar
[p585600@caddeapllx2863 intra]$
[p585600@caddeapllx2863 intra]$
[p585600@caddeapllx2863 intra]$
[p585600@caddeapllx2863 intra]$ for f in *.war *.jar lib/*.jar; do [ -f "$f" ] && mkdir -p "x_$(basename $f)" && unzip -o -q "$f" -d "x_$(basename $f)"; done
[p585600@caddeapllx2863 intra]$
[p585600@caddeapllx2863 intra]$
[p585600@caddeapllx2863 intra]$
[p585600@caddeapllx2863 intra]$ grep -rlE 'SIGSJ04|datasources/|persistence-unit|jdbc:oracle' . 2>/dev/null | head
[p585600@caddeapllx2863 intra]$
