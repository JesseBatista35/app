
[p585600@caddeapllx2651 ~]$ ps -ef --forest | grep -E "Agent\.(Listener|Worker)|ansible-playbook|ssh .*caddeapllx2651" | grep -v grep
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ df -h /opt/ads-agent
df: /opt/ads-agent: Arquivo ou diretório inexistente
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ ls -la ~/.ansible/cp/ 2>/dev/null
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ getent passwd 20003846
sansbp01:*:20003846:20001077:Usuario do Ansible - WO0000049756814:/home/sansbp01:/bin/bash
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo grep "Accepted" /var/log/secure | grep "Oct 28" | grep -v p585600 | tail -5
Oct 28 11:08:12 caddeapllx2651 sshd[126599]: Accepted password for sansbp01 from 10.122.155.64 port 54210 ssh2
Oct 28 11:31:04 caddeapllx2651 sshd[138146]: Accepted password for p981778 from 10.122.150.31 port 42420 ssh2
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
