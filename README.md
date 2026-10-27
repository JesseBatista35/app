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





-bash-5.1$
-bash-5.1$ DOM=/opt/SUNWas8/domains/das01
-bash-5.1$
-bash-5.1$
-bash-5.1$
-bash-5.1$ cd $DOM/config
-bash-5.1$
-bash-5.1$
-bash-5.1$ export LD_LIBRARY_PATH=/opt/SUNWas8/lib
-bash-5.1$
-bash-5.1$
-bash-5.1$
-bash-5.1$ CU=$(ls /opt/SUNWas8/bin/certutil /opt/SUNWas8/lib/certutil 2>/dev/null | head -1); echo $CU
/opt/SUNWas8/lib/certutil
-bash-5.1$
-bash-5.1$
-bash-5.1$
-bash-5.1$ mkdir -p ~/bkp_nss_20261027 && cp -p cert8.db key3.db secmod.db ~/bkp_nss_20261027/
-bash-5.1$
-bash-5.1$
-bash-5.1$ $CU -L -d .

Certificate Nickname                                         Trust Attributes
                                                             SSL,S/MIME,JAR/XPI

verisignclass1ca                                             T,c,c
thawtepersonalpremiumca                                      T,c,c
baltimorecodesigningca                                       T,c,c
s1as                                                         u,u,u
ac_mult_v4                                                   C,C,C
verisignclass2g2ca                                           T,c,c
verisignclass3g3ca                                           T,c,c
entrustglobalclientca                                        T,c,c
entrustsslca                                                 T,c,c
verisignclass3g2ca                                           T,c,c
thawtepremiumserverca                                        T,c,c
entrust2048ca                                                T,c,c
valicertclass2ca                                             T,c,c
sso_des_intra                                                C,C,C
equifaxsecureebusinessca1                                    T,c,c
verisignclass1g3ca                                           T,c,c
godaddyclass2ca                                              T,c,c
thawtepersonalbasicca                                        T,c,c
verisignclass1g2ca                                           T,c,c
verisignclass2g3ca                                           T,c,c
equifaxsecureca                                              T,c,c
entrustclientca                                              T,c,c
verisignserverca                                             T,c,c
geotrustglobalca                                             T,c,c
equifaxsecureebusinessca2                                    T,c,c
ac_apl_v4                                                    C,C,C
verisignclass3ca                                             T,c,c
verisignclass2ca                                             T,c,c
ac_corp_v4                                                   C,C,C
gtecybertrustglobalca                                        T,c,c
entrustgsslca                                                T,c,c
thawtepersonalfreemailca                                     T,c,c
thawteserverca                                               T,c,c
baltimorecybertrustca                                        T,c,c
starfieldclass2ca                                            T,c,c
equifaxsecureglobalebusinessca1                              T,c,c
-bash-5.1$
-bash-5.1$
-bash-5.1$ $CU -L -d . -n s1as
Certificate:
    Data:
        Version: 3 (0x2)
        Serial Number:
            00:a4:ca:9e:67
        Signature Algorithm: PKCS #1 SHA-1 With RSA Encryption
        Issuer: "CN=sspdeaplux0100,OU=Sun Java System Application Server,O=Su
            n Microsystems,L=Santa Clara,ST=California,C=US"
        Validity:
            Not Before: Mon Dec 07 20:46:23 2015
            Not After : Sun Dec 07 20:46:23 2025
        Subject: "CN=sspdeaplux0100,OU=Sun Java System Application Server,O=S
            un Microsystems,L=Santa Clara,ST=California,C=US"
        Subject Public Key Info:
            Public Key Algorithm: PKCS #1 RSA Encryption
            RSA Public Key:
                Modulus:
                    cb:f7:02:77:72:15:cc:43:66:f2:97:28:8d:38:82:21:
                    4a:6f:a2:89:8d:e9:4c:51:e4:29:fb:45:a6:19:65:a0:
                    de:6a:51:c6:ed:af:59:98:ec:26:45:de:e7:de:78:ad:
                    b4:e3:b2:ba:f8:66:50:37:59:4f:a3:71:f9:59:2b:96:
                    4a:e3:0c:e3:e9:42:60:21:df:44:c1:c1:f8:79:22:ba:
                    5a:4f:6b:f9:75:5d:c9:b4:21:b2:84:04:a1:a6:da:52:
                    d3:1f:95:11:53:01:b7:7c:52:14:f1:e1:af:9d:e6:23:
                    42:3f:58:c6:ce:bb:a2:77:2e:b4:79:66:53:46:29:0d
                Exponent: 65537 (0x10001)
    Signature Algorithm: PKCS #1 SHA-1 With RSA Encryption
    Signature:
        a0:fa:5a:3e:5f:49:81:50:53:ad:7a:0e:aa:bb:8c:03:
        26:bc:af:86:f9:2c:66:97:3f:a7:21:c0:f4:d8:0e:25:
        08:63:8f:75:89:8e:33:f3:d6:e3:11:76:4a:54:00:1d:
        de:74:94:21:9d:e5:2b:20:47:e1:63:83:79:72:c8:05:
        f4:28:0a:2c:15:f7:83:26:8c:fc:28:50:6e:91:ec:1b:
        76:e4:6c:1e:cd:3a:f9:30:29:ba:b3:72:18:96:76:93:
        53:db:a0:06:a3:ad:08:0a:d2:8f:17:b0:08:18:c5:b0:
        17:ee:08:97:14:3a:96:32:ae:6e:1f:78:25:e9:3d:26
    Fingerprint (MD5):
        06:98:7B:A0:EA:6C:0A:E6:66:3D:FE:82:D8:BA:4F:1D
    Fingerprint (SHA1):
        3C:C3:6F:42:45:99:52:13:3A:17:C3:CC:11:20:5C:65:C8:ED:C2:8F

    Certificate Trust Flags:
        SSL Flags:
            User
        Email Flags:
            User
        Object Signing Flags:
            User

-bash-5.1$
-bash-5.1$
-bash-5.1$
-bash-5.1$ $CU -D -d . -n s1as
-bash-5.1$
-bash-5.1$
-bash-5.1$ $CU -S -d . -n s1as -x -t "CTu,u,u" -v 120 -k rsa -g 2048 \
    -s "CN=sspdeaplux0100.caixa,OU=Sun Java System Application Server,O=Caixa,C=BR"
Enter Password or Pin for "NSS Certificate DB":
Enter Password or Pin for "NSS Certificate DB":
Enter Password or Pin for "NSS Certificate DB":
Enter Password or Pin for "NSS Certificate DB":
