Using project "sinfs-tqs".
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc set volume dc/sinfs-tqs -n sinfs-tqs
deploymentconfigs/sinfs-tqs
  secret/accaixa-v4 as accaixa-v4
    mounted at /opt/jboss/standalone/configuration/cacerts_sinfs_intra_tqs2
  empty directory as secrets
    mounted at /usr/src/app/secrets_files
  configMap/sinfs-tqs-script-bt-check as script-bt-volume
  configMap/jboss-config-sinfs as jboss-config-sinfs
    mounted at /tmp/standalone-okd.xml
  configMap/java-config-sinfs as java-config-sinfs
    mounted at /opt/jboss/bin/standalone.conf
  configMap/jconnector-config-sinfs as jconnector-config-sinfs
    mounted at /tmp/sinfs_jconnector.properties
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
