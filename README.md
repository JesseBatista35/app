deployment-info --name=SIEMP

ssh p585600@10.116.97.52
sudo sh -c 'tail -f /opt/jboss/jboss-eap/hc/servers/*/log/server.log' | grep -iE --line-buffered "empresas|WFLYSRV0010|WFLYSRV0021|faltam|WELD-001408|Registered web context"
