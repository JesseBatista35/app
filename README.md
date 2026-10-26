keytool -list -keystore /opt/ctmage/ctm/cm/AI/data/security/apcerts -storepass changeit | grep -c trustedCertEntry
keytool -list -keystore /opt/ctmage/ctm/cm/AI/data/security/apcerts.bkp.202610061641 -storepass changeit | grep -c trustedCertEntry
