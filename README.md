
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo grep -E "Accepted|session opened|Disconnected|Connection closed" /var/log/secure | grep "Oct 28" | tail -30
Oct 28 11:39:36 caddeapllx2651 sudo[149012]: pam_unix(sudo-i:session): session opened for user root(uid=0) by (uid=20003846)
Oct 28 11:39:37 caddeapllx2651 sudo[149057]: pam_unix(sudo-i:session): session opened for user root(uid=0) by (uid=20003846)
Oct 28 11:39:37 caddeapllx2651 sudo[149167]: pam_unix(sudo-i:session): session opened for user root(uid=0) by (uid=20003846)
Oct 28 11:39:37 caddeapllx2651 sudo[149212]: pam_unix(sudo-i:session): session opened for user root(uid=0) by (uid=20003846)
Oct 28 11:39:37 caddeapllx2651 sudo[149257]: pam_unix(sudo-i:session): session opened for user root(uid=0) by (uid=20003846)
Oct 28 11:39:40 caddeapllx2651 sudo[149364]: pam_unix(sudo-i:session): session opened for user root(uid=0) by (uid=20003846)
Oct 28 11:39:43 caddeapllx2651 sudo[149409]: pam_unix(sudo-i:session): session opened for user root(uid=0) by (uid=20003846)
Oct 28 11:39:44 caddeapllx2651 sudo[149455]: pam_unix(sudo-i:session): session opened for user root(uid=0) by (uid=20003846)
Oct 28 11:39:44 caddeapllx2651 sudo[149502]: pam_unix(sudo-i:session): session opened for user root(uid=0) by (uid=20003846)
Oct 28 11:39:47 caddeapllx2651 sudo[149558]: pam_unix(sudo-i:session): session opened for user root(uid=0) by (uid=20003846)
Oct 28 11:39:48 caddeapllx2651 sudo[149603]: pam_unix(sudo-i:session): session opened for user root(uid=0) by (uid=20003846)
Oct 28 11:39:49 caddeapllx2651 sudo[149648]: pam_unix(sudo-i:session): session opened for user root(uid=0) by (uid=20003846)
Oct 28 11:39:49 caddeapllx2651 sudo[149691]: pam_unix(sudo-i:session): session opened for user root(uid=0) by (uid=20003846)
Oct 28 11:39:49 caddeapllx2651 sudo[149734]: pam_unix(sudo-i:session): session opened for user root(uid=0) by (uid=20003846)
Oct 28 11:39:50 caddeapllx2651 sudo[149781]: pam_unix(sudo-i:session): session opened for user root(uid=0) by (uid=20003846)
Oct 28 11:39:50 caddeapllx2651 sudo[149826]: pam_unix(sudo-i:session): session opened for user root(uid=0) by (uid=20003846)
Oct 28 11:39:50 caddeapllx2651 sudo[149875]: pam_unix(sudo-i:session): session opened for user root(uid=0) by (uid=20003846)
Oct 28 11:40:01 caddeapllx2651 sudo[150072]: pam_unix(sudo-i:session): session opened for user root(uid=0) by (uid=20003846)
Oct 28 11:40:01 caddeapllx2651 sudo[150115]: pam_unix(sudo-i:session): session opened for user root(uid=0) by (uid=20003846)
Oct 28 11:40:02 caddeapllx2651 sudo[150207]: pam_unix(sudo-i:session): session opened for user root(uid=0) by (uid=20003846)
Oct 28 12:04:10 caddeapllx2651 runuser[150430]: pam_unix(runuser:session): session opened for user jboss(uid=30000115) by (uid=0)
Oct 28 12:04:10 caddeapllx2651 runuser[150434]: pam_unix(runuser:session): session opened for user jboss(uid=30000115) by (uid=0)
Oct 28 12:04:10 caddeapllx2651 runuser[150438]: pam_unix(runuser:session): session opened for user jboss(uid=30000115) by (uid=0)
Oct 28 12:06:35 caddeapllx2651 sshd[150907]: Accepted password for p585600 from 10.122.150.31 port 47362 ssh2
Oct 28 12:06:35 caddeapllx2651 systemd[150910]: pam_unix(systemd-user:session): session opened for user p585600(uid=10585600) by (uid=0)
Oct 28 12:06:36 caddeapllx2651 sshd[150907]: pam_unix(sshd:session): session opened for user p585600(uid=10585600) by (uid=0)
Oct 28 12:10:03 caddeapllx2651 sudo[150979]: pam_unix(sudo:session): session opened for user root(uid=0) by p585600(uid=10585600)
Oct 28 12:10:20 caddeapllx2651 sudo[150984]: pam_unix(sudo:session): session opened for user root(uid=0) by p585600(uid=10585600)
Oct 28 12:10:34 caddeapllx2651 sudo[150996]: pam_unix(sudo:session): session opened for user root(uid=0) by p585600(uid=10585600)
Oct 28 12:13:22 caddeapllx2651 sudo[151028]: pam_unix(sudo:session): session opened for user root(uid=0) by p585600(uid=10585600)
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
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
