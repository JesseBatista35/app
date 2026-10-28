ps -ef --forest | grep -E "sshd: sansbp01" | grep -v grep

Cancele a release 66.
sudo kill <PID do sshd: sansbp01 [priv]>
Faça o redeploy do EC DES. O agente vai precisar abrir uma conexão nova, e um “Accepted ... sansbp01” deve aparecer no secure




sudo grep p981778 /var/log/secure | grep "Oct 28"
