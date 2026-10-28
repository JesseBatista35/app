ps -ef --forest | grep -iE "Agent\.(Listener|Worker)|ads-agent" | grep -v grep
sudo systemctl list-units --all | grep -i vsts
ls -lt /opt/ads-agent/_diag | head -5
tail -50 $(ls -t /opt/ads-agent/_diag/Worker_*.log | head -1)
