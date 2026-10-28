#!/bin/bash
### BEGIN INIT INFO
# Provides: sigdb
# Required-Start: $local_fs $network $syslog
# Required-Stop: $local_fs $syslog
# Default-Start: 2 3 4 5
# Default-Stop: 0 1 6
# Short-Description: Sigdb Agent
# Description: Sigdb Agent
### END INIT INFO

case "$1" in
  start)
    cd /sigdb && nohup ./run >/dev/null 2>&1 &
    ;;
  stop)
    pkill -f "./AgtSigdb -m"
    ;;
  status)
    if pgrep -f "./AgtSigdb -m" >/dev/null 2>&1; then
      echo "sigdb em execucao"; exit 0
    else
      echo "sigdb parado"; exit 3
    fi
    ;;
  restart)
    $0 stop; sleep 2; $0 start
    ;;
  *)
    echo "Uso: $0 {start|stop|status|restart}"; exit 1
    ;;
esac
