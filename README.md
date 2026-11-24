.2$ oc rsh sicow-seg-okd-des-72-xk8dv
sh-4.2$
sh-4.2$
sh-4.2$
sh-4.2$ echo "JBOSS_HOME=$JBOSS_HOME  JBOSS_MODULEPATH=$JBOSS_MODULEPATH"
JBOSS_HOME=/opt/jboss  JBOSS_MODULEPATH=
sh-4.2$
sh-4.2$
sh-4.2$ ps -ef | grep -o '\-mp [^ ]*'
-mp /opt/jboss/modules
-mp [^
sh-4.2$
sh-4.2$
sh-4.2$ ls -l /opt/jboss/modules/br/gov/caixa/siusr/main/ 2>&1
ls: cannot access /opt/jboss/modules/br/gov/caixa/siusr/main/: No such file or directory
sh-4.2$
sh-4.2$
sh-4.2$ ls -l $JBOSS_HOME/modules/br/gov/caixa/siusr/main/ 2>&1
ls: cannot access /opt/jboss/modules/br/gov/caixa/siusr/main/: No such file or directory
sh-4.2$
sh-4.2$
sh-4.2$ cat $JBOSS_HOME/modules/br/gov/caixa/siusr/main/module.xml
cat: /opt/jboss/modules/br/gov/caixa/siusr/main/module.xml: No such file or directory
sh-4.2$
sh-4.2$
sh-4.2$
sh-4.2$
sh-4.2$
sh-4.2$
sh-4.2$ ls -R /opt/jboss/modules/br/gov/caixa/ 2>&1 | head -50
ls: cannot access /opt/jboss/modules/br/gov/caixa/: No such file or directory
sh-4.2$
sh-4.2$
sh-4.2$ ls -l /opt/jboss/modules/br/gov/caixa/siusr/main/
ls: cannot access /opt/jboss/modules/br/gov/caixa/siusr/main/: No such file or directory
sh-4.2$
sh-4.2$
sh-4.2$ cat /opt/jboss/modules/br/gov/caixa/siusr/main/module.xml
cat: /opt/jboss/modules/br/gov/caixa/siusr/main/module.xml: No such file or directory
sh-4.2$
sh-4.2$
sh-4.2$ mount | grep -i modules
sh-4.2$
sh-4.2$ mount | grep -i modules
sh-4.2$
sh-4.2$
sh-4.2$ df -h /opt/jboss/modules/br/gov/caixa/siusr/main/ 2>&1
df: '/opt/jboss/modules/br/gov/caixa/siusr/main/': No such file or directory
sh-4.2$
sh-4.2$
sh-4.2$
sh-4.2$
sh-4.2$ exit
exit
command terminated with exit code 1
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get dc sicow-portal-okd-des -o yaml | grep -iA5 -E 'volumeMounts|volumes|image:'
                f:volumeMounts:
                  k:{"mountPath":"/usr/src/app/secrets_files"}:
                    .: {}
                    f:mountPath: {}
                    f:name: {}
            f:imagePullSecrets:
--
                f:image: {}
                f:imagePullPolicy: {}
                f:name: {}
                f:resources:
                  .: {}
                  f:limits:
--
                f:volumeMounts:
                  .: {}
                  k:{"mountPath":"/usr/src/app/secrets_files"}:
                    .: {}
                    f:mountPath: {}
                    f:name: {}
--
                f:image: {}
                f:imagePullPolicy: {}
                f:name: {}
                f:resources: {}
                f:terminationMessagePath: {}
                f:terminationMessagePolicy: {}
                f:volumeMounts:
                  .: {}
                  k:{"mountPath":"/script"}:
                    .: {}
                    f:mountPath: {}
                    f:name: {}
--
            f:volumes:
              k:{"name":"script-bt-volume"}:
                .: {}
                f:configMap:
                  .: {}
                  f:defaultMode: {}
--
                f:image: {}
                f:volumeMounts:
                  .: {}
                  k:{"mountPath":"/opt/jboss/bin/standalone.conf"}:
                    .: {}
                    f:mountPath: {}
                    f:name: {}
--
            f:volumes:
              .: {}
              k:{"name":"caixa-truststore-acteste-nprd-sicow-jks"}:
                .: {}
                f:name: {}
                f:secret:
--
        image: default-route-openshift-image-registry.apps.produtos4.caixa/build-images-ads/sicow-portal-okd:1.0.36.1
        imagePullPolicy: Always
        livenessProbe:
          failureThreshold: 3
          initialDelaySeconds: 120
          periodSeconds: 10
--
        volumeMounts:
        - mountPath: /usr/src/app/secrets_files
          name: secrets
        - mountPath: /sicow
          name: sicow-portal-okd-data-des
        - mountPath: /opt/jboss/standalone/configuration/caixa-truststore-acteste-nprd-sicow.jks
--
        image: default-route-openshift-image-registry.apps.produtos4.caixa/openshift/secrets-agent:v23.3.2
        imagePullPolicy: IfNotPresent
        name: secrets-agent-sidecar
        resources:
          limits:
            memory: 400Mi
--
        volumeMounts:
        - mountPath: /usr/src/app/secrets_files
          name: secrets
      - command:
        - /bin/bash
        - /script/bt-check.sh
--
        image: default-route-openshift-image-registry.apps.produtos4.caixa/openshift/ubi:9.3-1552
        imagePullPolicy: IfNotPresent
        name: secrets-check
        resources: {}
        terminationMessagePath: /dev/termination-log
        terminationMessagePolicy: File
        volumeMounts:
        - mountPath: /usr/src/app/secrets_files
          name: secrets
        - mountPath: /script
          name: script-bt-volume
      restartPolicy: Always
--
      volumes:
      - emptyDir:
          medium: Memory
        name: secrets
      - configMap:
          defaultMode: 420
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get dc sicow-seg-okd-des    -o yaml | grep -iA5 -E 'volumeMounts|volumes|image:'
                f:volumeMounts:
                  k:{"mountPath":"/opt/jboss/standalone/configuration/caixa-truststore-acteste-nprd.jks"}:
                    .: {}
                    f:mountPath: {}
                    f:name: {}
                    f:subPath: {}
            f:volumes:
              k:{"name":"caixa-truststore-acteste-nprd-jks"}:
                .: {}
                f:name: {}
                f:secret:
                  .: {}
--
                f:image: {}
                f:volumeMounts:
                  .: {}
                  k:{"mountPath":"/opt/jboss/bin/standalone.conf"}:
                    .: {}
                    f:mountPath: {}
                    f:name: {}
--
            f:volumes:
              .: {}
              k:{"name":"java-config-sicow-seg-okd"}:
                .: {}
                f:configMap:
                  .: {}
--
        image: default-route-openshift-image-registry.apps.produtos4.caixa/build-images-ads/sicow-seg-okd:1.0.38.7
        imagePullPolicy: Always
        livenessProbe:
          failureThreshold: 3
          initialDelaySeconds: 120
          periodSeconds: 10
--
        volumeMounts:
        - mountPath: /opt/jboss/standalone/configuration/caixa-truststore-acteste-nprd.jks
          name: caixa-truststore-acteste-nprd-jks
          subPath: caixa-truststore-acteste-nprd.jks
        - mountPath: /sicow
          name: sicow-seg-okd-data-des
--
      volumes:
      - name: caixa-truststore-acteste-nprd-jks
        secret:
          defaultMode: 420
          secretName: caixa-truststore-acteste-nprd-jks
      - name: sicow-seg-okd-data-des
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get bc -o yaml | grep -iE 'from|name:|uri|ref'
-sh-4.2$




jboss-modules
group_id:artifact_id:version:extension
br.gov.caixa.siusr:siusr-loginModule:1.11.0:jar



Skip to main content
Azure DevOps
projetos
/
Caixa
/
Repos
/
Files
/

SICOW-seg-okd
Search


Caixa

Overview

Boards

Repos
Files
Commits
Pushes
Branches
Tags
Pull requests

Pipelines

Test Plans

Artifacts
Project settings
SICOW-seg-okd

src
main
java
resources
webapp
test
java
resources
.gitignore
cli-offline.sh
jboss-deployments
jboss-modules
pom.xml
README.md

1.0.38.7

/
.gitignore
.gitignore

Edit

Contents
History
Compare
Blame

123456
/target/
/.settings
/.project
/.classpath
/bin/

Showing 25 filtered items.

Get started and run this pipeline for the first time!

Showing 29 filtered items.

Showing 25 filtered items.

Row 2. Clickable

Expanded

Collapsed

Expanded

Collapsed







