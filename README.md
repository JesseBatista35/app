
[p585600@caddeapllx2651 ~]$ ps -ef --forest | grep -iE "Agent\.(Listener|Worker)|ads-agent" | grep -v grep
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo systemctl list-units --all | grep -i vsts
[p585600@caddeapllx2651 ~]$ ls -lt /opt/ads-agent/_diag | head -5
ls: não foi possível acessar '/opt/ads-agent/_diag': Arquivo ou diretório inexistente
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ tail -50 $(ls -t /opt/ads-agent/_diag/Worker_*.log | head -1)
ls: não foi possível acessar '/opt/ads-agent/_diag/Worker_*.log': Arquivo ou diretório inexistente

