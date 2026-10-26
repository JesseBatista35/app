/opt/ctmage/JRE/bin/java -version

ls -la /opt/ctmage/JRE/bin/java
ls -la /opt/ctmage/ctm/cm/AI/data/security/

# data de modificação do trustStore/keyStore — se foi mexido recentemente, bate com o início do 401
stat /opt/ctmage/ctm/cm/AI/data/security/apcerts
stat /opt/ctmage/ctm/cm/AI/data/security/apks
