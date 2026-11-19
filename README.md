<img width="1877" height="995" alt="image" src="https://github.com/user-attachments/assets/d81390cb-81c0-456e-a8b4-e4b58d89b2af" />



ot@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]# mkdir -p /apl/sigsj/properties
cd /apl/sigsj/properties
scp p585600@10.116.88.96:/apl/sigsj/properties/\*.properties .
chown -R jboss:jboss /apl/sigsj
chmod 644 /apl/sigsj/properties/*.properties
ls -la /apl/sigsj/properties/
The authenticity of host '10.116.88.96 (10.116.88.96)' can't be established.
RSA key fingerprint is SHA256:4syI7cyn+8y4NieUzq5i1LX5sM/BfCSfRTH5Yn7TfcU.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '10.116.88.96' (RSA) to the list of known hosts.
***********************************************************************
(1) - Este e um computador privado de propriedade da Caixa Economica
Federal. Usuarios autorizados e nao autorizados nao possuem direitos de
divulgar as informacoes contidas aqui.
(2) - Ao fazer uso do sistema, o usuario esta ciente que pode estar
sendo monitorado, interceptado e auditado pelo departamento competente
da Caixa Economica Federal.
(3) - O uso nao autorizado ou improprio deste sistema pode resultar em
um processo disciplinar administrativo e/ou punicao atraves de acoes
civis ou criminais. Ao continuar o uso deste sistema, indica que voce
esta ciente e concordando com os termos e condicoes acima descritos.

Pressione <Control+D> IMEDIATAMENTE se voce nao concorda com as
condicoes deste aviso
***********************************************************************
p585600@10.116.88.96's password:
b2b.properties                                                                                                                                                       100% 1357     1.7MB/s   00:00
config.properties                                                                                                                                                    100%  279   474.1KB/s   00:00
release.properties                                                                                                                                                   100%   24    43.1KB/s   00:00
total 12
drwxr-xr-x 2 jboss jboss   79 nov 19 15:17 .
drwxr-xr-x 3 jboss jboss   24 nov 19 15:17 ..
-rw-r--r-- 1 jboss jboss 1357 nov 19 15:17 b2b.properties
-rw-r--r-- 1 jboss jboss  279 nov 19 15:17 config.properties
-rw-r--r-- 1 jboss jboss   24 nov 19 15:17 release.properties
[root@caddeapllx955 properties]#
[root@caddeapllx955 properties]#
[root@caddeapllx955 properties]#
[root@caddeapllx955 properties]# curl -s -o /dev/null -w "intranet default.jsp: %{http_code}\n" http://10.116.194.179/sigsj_intranet/default.jsp
intranet default.jsp: 200
[root@caddeapllx955 properties]#
[root@caddeapllx955 properties]#
[root@caddeapllx955 properties]#
