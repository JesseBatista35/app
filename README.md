sudo journalctl -k --since "2026-10-28 11:05" --until "2026-10-28 11:40" | grep -iE "nfs|not responding|hung|blocked"
sudo grep -iE "not responding|hung_task|blocked for more" /var/log/messages | grep "Oct 28"

grep -E "nfs|cifs|fuse" /proc/mounts                       # outros mounts de rede
timeout 15 df -hT >/dev/null; echo "df rc=$?"
timeout 15 findmnt >/dev/null; echo "findmnt rc=$?"
timeout 15 lsblk >/dev/null; echo "lsblk rc=$?"
timeout 15 sudo dmidecode -t system >/dev/null; echo "dmidecode rc=$?"

ps -ef --forest | grep -A5 -i ansible
