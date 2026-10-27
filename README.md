DOM=/opt/SUNWas8/domains/das01
cd $DOM/config
export LD_LIBRARY_PATH=/opt/SUNWas8/lib
CU=$(ls /opt/SUNWas8/bin/certutil /opt/SUNWas8/lib/certutil 2>/dev/null | head -1); echo $CU

# 1. backup
mkdir -p ~/bkp_nss_20261027 && cp -p cert8.db key3.db secmod.db ~/bkp_nss_20261027/

# 2. ver o cert atual (nome, trust flags e subject)
$CU -L -d .
$CU -L -d . -n s1as

# 3. remover o vencido e criar um novo autoassinado (pede a master password)
$CU -D -d . -n s1as
$CU -S -d . -n s1as -x -t "CTu,u,u" -v 120 -k rsa -g 2048 \
    -s "CN=sspdeaplux0100.caixa,OU=Sun Java System Application Server,O=Caixa,C=BR"
$CU -L -d . -n s1as | egrep -i 'Not After|Subject'


mv ~/.asadmintruststore ~/.asadmintruststore.old 2>/dev/null
/opt/SUNWas8/bin/asadmin stop-domain das01
/opt/SUNWas8/bin/asadmin start-domain --user ASadmin das01


/opt/SUNWas8/bin/asadmin list-instances --host localhost --port 14848 --user ASadmin --passwordfile /opt/SUNWas8/config/passwordfile.conf
/opt/SUNWas8/bin/asadmin list-application-refs --host localhost --port 14848 --user ASadmin --passwordfile /opt/SUNWas8/config/passwordfile.conf dsv01
/opt/SUNWas8/bin/asadmin undeploy --host localhost --port 14848 --user ASadmin --passwordfile /opt/SUNWas8/config/passwordfile.conf --target dsv01 sidmf
