
[p585600@caddeapllx955 deployments]$
[p585600@caddeapllx955 deployments]$ sudo -u jboss rm -f sirotcon-ejb.jar.*
sudo -u jboss touch sigsj_intranet-ear.ear.dodeploy
sleep 40; ls -l | grep -E "deployed|failed"
[sudo] senha para p585600:
Sinto muito, usuário p585600 não tem permissão para executar "/bin/rm -f sirotcon-ejb.jar.deployed" como jboss em caddeapllx955.agil.nprd.caixa.gov.br.
[sudo] senha para p585600:
Sinto muito, usuário p585600 não tem permissão para executar "/bin/touch sigsj_intranet-ear.ear.dodeploy" como jboss em caddeapllx955.agil.nprd.caixa.gov.br.
-rw-r--r-- 1 jboss jboss      535 out 20 16:47 sigsj_intranet-ear.ear.failed
-rw-r--r-- 1 jboss jboss       16 out 20 16:30 sirotcon-ejb.jar.deployed
[p585600@caddeapllx955 deployments]$
