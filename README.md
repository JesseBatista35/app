ps -o pid,ppid,user,lstart,cmd -p 162567,162569
ps -ef --forest | grep -B3 -A3 -E "16256[79]" | grep -v grep
