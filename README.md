
-bash-5.1$
-bash-5.1$ cd /opt/SUNWas8/domains/das01/config
-bash-5.1$
-bash-5.1$
-bash-5.1$
-bash-5.1$ export LD_LIBRARY_PATH=/opt/SUNWas8/lib
-bash-5.1$
-bash-5.1$
-bash-5.1$ cp -p ~/bkp_nss_20261027/cert8.db ~/bkp_nss_20261027/key3.db ~/bkp_nss_20261027/secmod.db .
-bash-5.1$
-bash-5.1$
-bash-5.1$ ls -l cert8.db key3.db secmod.db
-rw-------   1 sjsas8   sunjava   131072 set  5  2024 cert8.db
-rw-------   1 sjsas8   sunjava   131072 set  5  2024 key3.db
-rw-------   1 sjsas8   sunjava   131072 fev  8  2021 secmod.db
-bash-5.1$
-bash-5.1$
-bash-5.1$ /opt/SUNWas8/lib/certutil -L -d . | grep s1as
s1as                                                         u,u,u
-bash-5.1$



vamos fechar a demanda
