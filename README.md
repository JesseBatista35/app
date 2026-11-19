
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$ sudo su

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for p585600:
[root@cbrdeapllx471 p585600]#
[root@cbrdeapllx471 p585600]#
[root@cbrdeapllx471 p585600]# cd /tmp/
[root@cbrdeapllx471 tmp]#
[root@cbrdeapllx471 tmp]#
[root@cbrdeapllx471 tmp]# curl --noproxy '*' -f -o pen-ear-2.32.0.2.ear http://binario.caixa:8081/repository/releases/br/gov/caixa/sipen/pen-ear/2.32.0.2/pen-ear-2.32.0.2.ear
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 27.2M  100 27.2M    0     0   115M      0 --:--:-- --:--:-- --:--:--  115M
[root@cbrdeapllx471 tmp]#
[root@cbrdeapllx471 tmp]#
[root@cbrdeapllx471 tmp]# ls -l pen-ear-2.32.0.2.ear
-rw-r--r-- 1 root root 28553606 Nov 19 14:20 pen-ear-2.32.0.2.ear
[root@cbrdeapllx471 tmp]#
[root@cbrdeapllx471 tmp]#
[root@cbrdeapllx471 tmp]# unzip -t pen-ear-2.32.0.2.ear | tail -1
No errors detected in compressed data of pen-ear-2.32.0.2.ear.
[root@cbrdeapllx471 tmp]#
[root@cbrdeapllx471 tmp]#
[root@cbrdeapllx471 tmp]# /opt/jboss/jboss-eap/bin/jboss-cli.sh --connect --controller=localhost:9999
[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /] deployment-info --name=SIPEN
NAME  RUNTIME-NAME
SIPEN sipen-2.29.0.1-2.29.0.1-b1893.ear

SERVER-GROUP    STATE
siemp           not added
sifec-intranet  not added
sifec-intranet2 not added
sipen           enabled

[domain@localhost:9999 /] :read-children-names(child-type=server-group)
{
    "outcome" => "success",
    "result" => [
        "siemp",
        "sifec-intranet",
        "sifec-intranet2",
        "sipen"
    ]
}

[domain@localhost:9999 /]
[domain@localhost:9999 /]


