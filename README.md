ps -ef --forest | grep -E "sshd: sansbp01" | grep -v grep

Cancele a release 66.
sudo kill <PID do sshd: sansbp01 [priv]>
Faça o redeploy do EC DES. O agente vai precisar abrir uma conexão nova, e um “Accepted ... sansbp01” deve aparecer no secure




sudo grep p981778 /var/log/secure | grep "Oct 28"




[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ ps -ef --forest | grep -E "sshd: sansbp01" | grep -v grep
root       54198    5297  0 out23 ?        00:00:00  \_ sshd: sansbp01 [priv]
sansbp01   54200   54198  0 out23 ?        00:00:02  |   \_ sshd: sansbp01@notty
root       65770    5297  0 out23 ?        00:00:00  \_ sshd: sansbp01 [priv]
sansbp01   65772   65770  0 out23 ?        00:00:01  |   \_ sshd: sansbp01@notty
root      126599    5297  0 11:08 ?        00:00:00  \_ sshd: sansbp01 [priv]
sansbp01  126601  126599  0 11:08 ?        00:00:00  |   \_ sshd: sansbp01@notty
[p585600@caddeapllx2651 ~]$
