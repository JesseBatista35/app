
condicoes deste aviso
***********************************************************************
p585600@10.116.97.59's password:
Last login: Tue Nov 17 10:02:59 2026 from 10.122.150.31
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$ JH=$(ps -ef | grep -o 'jboss.home.dir=[^ ]*' | head -1 | cut -d= -f2); echo $JH
/opt/jboss/jboss-eap
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$ cp -p $JH/domain/configuration/domain.xml /tmp/domain.xml.bkp_ccr_$(date +%Y%m%d_%H%M)
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$ ls -l /tmp/domain.xml.bkp_ccr_*
-rwxr-xr-x 1 p585600 usucef 128249 Jun 12  2023 /tmp/domain.xml.bkp_ccr_20261117_1516
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$



vamos com calma
