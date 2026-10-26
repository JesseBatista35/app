
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$ keytool -list -keystore /opt/ctmage/ctm/cm/AI/data/security/apcerts -storepass changeit | grep -c trustedCertEntry
0
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$ keytool -list -keystore /opt/ctmage/ctm/cm/AI/data/security/apcerts.bkp.202610061641 -storepass changeit | grep -c trustedCertEntry
0
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$ keytool -list -keystore /opt/ctmage/ctm/cm/AI/data/security/apcerts -storepass changeit
erro de keytool: java.io.IOException: Keystore was tampered with, or password was incorrect
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
