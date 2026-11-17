ls -l /opt/jboss/jboss-eap/dc/configuration/domain*.xml
cp -p /opt/jboss/jboss-eap/dc/configuration/domain.xml /tmp/domain.xml.bkp_ccr_dc_$(date +%Y%m%d_%H%M)
ls -l /tmp/domain.xml.bkp_ccr_dc_*
grep -c "ccr-api.war" /opt/jboss/jboss-eap/dc/configuration/domain.xml
