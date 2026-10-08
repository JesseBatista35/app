<img width="1664" height="914" alt="image" src="https://github.com/user-attachments/assets/b1837d40-865b-47c6-9cb8-869e57d1c8bb" />


#### Permissionando pasta /opt/httpd/conf.d/ ####
chown -R apache:apache /opt/httpd/conf.d/*
chmod -R 777 /opt/httpd/conf.d/*
#Desmontando nfs
umount -f /arquivos-recebidos
# Instalando Drivers dos Bancos de Dados #

# Criando pastas dos Drivers #
cd /opt/jboss-eap/modules/system/layers/base/com
mkdir -p sybase/ase/main/
mkdir -p microsoft/sqlserver/main/


# Copiando os drivers para as pastas #
cp -rf /tmp/src/jconn4-4.jar /opt/jboss-eap/modules/system/layers/base/com/sybase/ase/main/jconn4.jar
mv -f /opt/jboss-eap/standalone/configuration/sybase-module.xml /opt/jboss-eap/modules/system/layers/base/com/sybase/ase/main/module.xml
#cd /opt/jboss-eap/modules/system/layers/base/
chown -R jboss:jboss /opt/jboss-eap/modules/system/layers/base/com/sybase/ase/main/*

cp -rf /tmp/src/sqljdbc4-4.0.jar /opt/jboss-eap/modules/system/layers/base/com/microsoft/sqlserver/main/SQLSERVER-sqljdbc4.jar
mv -f /opt/jboss-eap/standalone/configuration/sql-module.xml /opt/jboss-eap/modules/system/layers/base/com/microsoft/sqlserver/main/module.xml
#cd /opt/jboss-eap/modules/system/layers/base/
chown -R jboss:jboss /opt/jboss-eap/modules/system/layers/base/com/microsoft/sqlserver/main/*

rm -rf /opt/jboss-eap/modules/system/layers/base/com/ibm/db2/main/db2jcc4.jar
cp -rf /tmp/src/jcc-11.5.8.0.jar /opt/jboss-eap/modules/system/layers/base/com/ibm/db2/main/db2jcc4.jar
mv -f /opt/jboss-eap/standalone/configuration/db2-module.xml /opt/jboss-eap/modules/system/layers/base/com/ibm/db2/main/module.xml
chown -R jboss:jboss /opt/jboss-eap/modules/system/layers/base/com/ibm/db2/main/*

chmod -R 775 /opt/jboss-eap/standalone/deployments/*


#Montagem Blob Storage
mount -t nfs -o vers=3,nolock,proto=tcp stgsiopivendasonline.blob.core.windows.net:/stgsiopivendasonline/arquivosrecebidos /arquivos-recebidos


<img width="1712" height="909" alt="image" src="https://github.com/user-attachments/assets/ce6c8348-38d5-4400-bd63-cb25c49f4a20" />

