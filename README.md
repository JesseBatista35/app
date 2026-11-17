
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$ ls -l /opt/jboss/jboss-eap/dc/configuration/domain*.xml
cp -p /opt/jboss/jboss-eap/dc/configuration/domain.xml /tmp/domain.xml.bkp_ccr_dc_$(date +%Y%m%d_%H%M)
ls -l /tmp/domain.xml.bkp_ccr_dc_*
grep -c "ccr-api.war" /opt/jboss/jboss-eap/dc/configuration/domain.xml
-rw-r--r-- 1 jboss jboss 332581 Nov 16 14:47 /opt/jboss/jboss-eap/dc/configuration/domain.xml
-rw-r--r-- 1 p585600 usucef 332581 Nov 16 14:47 /tmp/domain.xml.bkp_ccr_dc_20261117_1517
1
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$
