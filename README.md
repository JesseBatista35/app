systemctl list-units --type=service | grep -i -E "jboss|eap|sigec"
systemctl status <nome-do-serviço> --no-pager -l
journalctl -u <nome-do-serviço> --since "11:55" --no-pager | tail -80
ss -ltnp | grep -E "9990|8080|8443"
ls -ld /opt/*sigec* /opt/jboss* 2>/dev/null
