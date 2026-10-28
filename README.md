P=$(sudo readlink /proc/162569/fd/0 | tr -dc 0-9); echo "pipe=$P"
sudo find /proc/[0-9]*/fd -lname "pipe:\[$P\]" 2>/dev/null
ps -o pid,ppid,user,lstart,cmd -p <PIDs que aparecerem, exceto 162569>
ls -l /etc/init.d/
