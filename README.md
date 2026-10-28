for p in 3516221 3516222; do sudo find /proc/[0-9]*/fd -lname "pipe:\[$p\]" 2>/dev/null; done

ps -o pid,ppid,user,lstart,cmd -p <PID>

ps -eo pid,ppid,user,lstart,cmd --sort=start_time | grep -E "12:2[4-5]:"
