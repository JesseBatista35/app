
-sh-4.2$
-sh-4.2$ oc exec sicow-penhor-okd-des-68-qnfbk -n sicow-des -- ls -la /opt/jboss/standalone/configuration/ | grep -iE "vault|keystore|\.dat|jks"
-rw-r--r--. 1 root root  1199 Oct 23 16:35 VAULT.dat
-rw-------. 1  185 root  2038 Oct 23 16:38 application.keystore
-rw-r--r--. 1 root root 76063 Oct 23 16:35 caixa-truststore-acteste-nprd-sicow.jks
-rw-r--r--. 1 root root 39055 Oct 23 16:35 caixa-truststore-acteste-nprd.jks
-rw-r--r--. 1 root root   506 Oct 23 16:35 vault-sicow-des.keystore
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get dc sicow-penhor-okd-des -n sicow-des -o yaml | grep -iE -B2 -A6 "vault|keystore"
                    f:name: {}
                    f:subPath: {}
                  k:{"mountPath":"/opt/jboss/standalone/configuration/VAULT.dat"}:
                    .: {}
                    f:mountPath: {}
                    f:name: {}
                    f:subPath: {}
                  k:{"mountPath":"/opt/jboss/standalone/configuration/caixa-truststore-acteste-nprd-sicow.jks"}:
                    .: {}
--
                    f:name: {}
                    f:subPath: {}
                  k:{"mountPath":"/opt/jboss/standalone/configuration/vault-sicow-des.keystore"}:
                    .: {}
                    f:mountPath: {}
                    f:name: {}
                    f:subPath: {}
                  k:{"mountPath":"/tmp/standalone-okd.xml"}:
                    .: {}
--
                  f:name: {}
                f:name: {}
              k:{"name":"vault-sicow-des-keystore"}:
                .: {}
                f:name: {}
                f:secret:
                  .: {}
                  f:defaultMode: {}
                  f:secretName: {}
              k:{"name":"vault-sicow-penhor-okd"}:
                .: {}
                f:configMap:
                  .: {}
                  f:defaultMode: {}
                  f:name: {}
                f:name: {}
--
          name: caixa-truststore-acteste-nprd-sicow-jks
          subPath: caixa-truststore-acteste-nprd-sicow.jks
        - mountPath: /opt/jboss/standalone/configuration/vault-sicow-des.keystore
          name: vault-sicow-des-keystore
          subPath: vault-sicow-des.keystore
        - mountPath: /opt/jboss/standalone/configuration/VAULT.dat
          name: vault-sicow-penhor-okd
          subPath: VAULT.dat
        - mountPath: /tmp/standalone-okd.xml
          name: jboss-config-sicow-penhor-okd
          subPath: standalone-okd.xml
        - mountPath: /opt/jboss/bin/standalone.conf
          name: java-config-sicow-penhor-okd
          subPath: standalone.conf
--
          defaultMode: 420
          secretName: caixa-truststore-acteste-nprd-sicow-jks
      - name: vault-sicow-des-keystore
        secret:
          defaultMode: 420
          secretName: vault-sicow-des-keystore
      - configMap:
          defaultMode: 420
          name: vault-sicow-penhor-okd
        name: vault-sicow-penhor-okd
      - configMap:
          defaultMode: 420
          name: jboss-config-sicow-penhor-okd
        name: jboss-config-sicow-penhor-okd
      - configMap:
          defaultMode: 420
-sh-4.2$





ta mais voce tem certeza que o conres precisa disso.. se bem que na w.o ele diz correçoes iguasl do peho masi minha duvia é se relamente a aplicacao precisa disso
