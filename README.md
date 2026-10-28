sudo grep -E "Accepted|session opened|Disconnected|Connection closed" /var/log/secure | grep "Oct 28" | tail -30

ps -ef --forest | grep -E "Agent\.(Listener|Worker)|ansible-playbook|ssh .*caddeapllx2651" | grep -v grep
df -h /opt/ads-agent
ls -la ~/.ansible/cp/ 2>/dev/null      # socket ControlPersist travado do usuário do agente

