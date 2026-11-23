
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]# ls -la /apl/sigsj/lib/
total 20
drwxr-xr-x 2 jboss jboss    31 nov 19 11:09 .
drwxr-xr-x 4 jboss jboss    35 nov 19 15:21 ..
-rwxr-xr-x 1 jboss jboss 19315 nov 19 11:07 libSenhasSIIBC.so
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]# grep -n "library.path" /opt/jboss-eap/bin/standalone.conf
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]# ps -ef | grep -v grep | grep -o "java.library.path=[^ ]*"
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#


