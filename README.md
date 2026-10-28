#!/bin/bash
#  AgtSigdb -m<alias-desse-host> -h<ip-do-destino> -i<ip-desse-servidor>
LD_LIBRARY_PATH=/usr/lib
export LD_LIBRARY_PATH

umask 000
cd /sigdb

# evita instancias duplicadas (init.d / service --status-all / systemd)
if pgrep -f "AgtSigdb -mtr7261lx651" >/dev/null 2>&1; then
  exit 0
fi

# foreground (compativel com systemd) e sem herdar stdout/stderr de quem chamou
exec ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111 >>/sigdb/AgtSigdb.out 2>&1
