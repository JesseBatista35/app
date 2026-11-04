deployment-info --name=SIEMP

ssh p585600@10.116.97.52
sudo sh -c 'tail -f /opt/jboss/jboss-eap/hc/servers/*/log/server.log' | grep -iE --line-buffered "empresas|WFLYSRV0010|WFLYSRV0021|faltam|WELD-001408|Registered web context"




[domain@localhost:9443 /] deployment-info --name=SIEMP
NAME  RUNTIME-NAME
SIEMP siemp-ear-14.37.0.6.ear

SERVER-GROUP    STATE
siemp           enabled
sifec-intranet  not added
sifec-intranet2 not added
sipen           not added

[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]



p585600@10.116.97.52's password:
[p585600@cbrdeapllx465 ~]$
[p585600@cbrdeapllx465 ~]$
[p585600@cbrdeapllx465 ~]$
[p585600@cbrdeapllx465 ~]$ sudo sh -c 'tail -f /opt/jboss/jboss-eap/hc/servers/*/log/server.log' | grep -iE --line-buffered "empresas|WFLYSRV0010|WFLYSRV0021|faltam|WELD-001408|Registered web context"

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for p585600:
Sorry, user p585600 is not allowed to execute '/usr/bin/sh -c tail -f /opt/jboss/jboss-eap/hc/servers/*/log/server.log' as root on cbrdeapllx465.
[p585600@cbrdeapllx465 ~]$
[p585600@cbrdeapllx465 ~]$
[p585600@cbrdeapllx465 ~]$
[p585600@cbrdeapllx465 ~]$
