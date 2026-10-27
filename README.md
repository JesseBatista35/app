cd /opt/SUNWas8/domains/das01/config
export LD_LIBRARY_PATH=/opt/SUNWas8/lib
cp -p ~/bkp_nss_20261027/cert8.db ~/bkp_nss_20261027/key3.db ~/bkp_nss_20261027/secmod.db .
ls -l cert8.db key3.db secmod.db
/opt/SUNWas8/lib/certutil -L -d . | grep s1as
