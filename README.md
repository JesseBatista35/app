
-sh-4.2$ ssh 10.116.201.25
The authenticity of host '10.116.201.25 (10.116.201.25)' can't be established.
ECDSA key fingerprint is SHA256:c9B/MMR4TI4/AMHwh+qeJB5ls+8UelMuD9ts69F7jc0.
ECDSA key fingerprint is MD5:5c:25:ab:a6:6c:a2:9f:85:35:27:2d:33:1b:27:e7:c5.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added '10.116.201.25' (ECDSA) to the list of known hosts.
p585600@10.116.201.25's password:
Last login: Tue Oct 20 13:56:05 2026 from 10.122.150.31
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$ ls -la /opt/jboss/jboss-eap/standalone/deployments/ | grep -i sirot
ls: não foi possível acessar '/opt/jboss/jboss-eap/standalone/deployments/': Arquivo ou diretório inexistente
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$ grep -n -i -B2 -A3 "sirot" /opt/jboss/jboss-eap/standalone/configuration/standalone-full-ha.xml
grep: /opt/jboss/jboss-eap/standalone/configuration/standalone-full-ha.xml: Arquivo ou diretório inexistente
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$ grep -i "sirot" /logs/jboss/jboss-eap/standalone/sigsj-internet/server.log | grep -iE "deploy|WFLYSRV0010|jndi" | head -10
grep: /logs/jboss/jboss-eap/standalone/sigsj-internet/server.log: Arquivo ou diretório inexistente
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$ grep -nE "WFLYCTL0412|WFLYCTL0180" /logs/jboss/jboss-eap/standalone/sigsj-boleto/server.log | tail -10
47:    "WFLYCTL0412: Serviços necessários que não estão instalados:" => [
52:    "WFLYCTL0180: Os serviços com falta/indisponibilidade de dependências " => [
301:    "WFLYCTL0412: Serviços necessários que não estão instalados:" => [
306:    "WFLYCTL0180: Os serviços com falta/indisponibilidade de dependências " => [
517:    "WFLYCTL0412: Serviços necessários que não estão instalados:" => [
522:    "WFLYCTL0180: Os serviços com falta/indisponibilidade de dependências " => [
734:    "WFLYCTL0412: Serviços necessários que não estão instalados:" => [
739:    "WFLYCTL0180: Os serviços com falta/indisponibilidade de dependências " => [
950:    "WFLYCTL0412: Serviços necessários que não estão instalados:" => [
955:    "WFLYCTL0180: Os serviços com falta/indisponibilidade de dependências " => [
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
