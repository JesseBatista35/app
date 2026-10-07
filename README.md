-sh-4.2$ hostname -f
caddeapllx1537.agil.nprd.caixa.gov.br
-sh-4.2$
-sh-4.2$
-sh-4.2$ cat /opt/jboss-eap/standalone/configuration/custom.sh
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

-sh-4.2$
-sh-4.2$
-sh-4.2$ sudo mkdir -p /arquivos-recebidos

Presumimos que você recebeu as instruções de sempre do administrador
de sistema local. Basicamente, resume-se a estas três coisas:

    #1) Respeite a privacidade dos outros.
    #2) Pense antes de digitar.
    #3) Com grandes poderes vêm grandes responsabilidades.

[sudo] senha para p585600:
-sh-4.2$
-sh-4.2$
-sh-4.2$ sudo chown jboss:jboss /arquivos-recebidos
-sh-4.2$
-sh-4.2$
-sh-4.2$ sudo chmod 770 /arquivos-recebidos
-sh-4.2$
-sh-4.2$
-sh-4.2$ sudo bash /opt/jboss-eap/standalone/configuration/custom.sh; echo "rc=$?"
umount: /arquivos-recebidos: not mounted
mv: impossível obter estado de “/opt/jboss-eap/standalone/configuration/sybase-module.xml”: Arquivo ou diretório não encontrado
mv: impossível obter estado de “/opt/jboss-eap/standalone/configuration/sql-module.xml”: Arquivo ou diretório não encontrado
mv: impossível obter estado de “/opt/jboss-eap/standalone/configuration/db2-module.xml”: Arquivo ou diretório não encontrado


