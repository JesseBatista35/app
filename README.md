DOM=/opt/SUNWas8/domains/das01

tail -100 $DOM/logs/server.log
ls -l $DOM/config/ | egrep -i 'lock|pid'
egrep -n 'admin-listener' $DOM/config/domain.xml

# onde o processo está parado (deve mostrar read em stdin se a hipótese estiver certa)
pstack 7248 | head -50
pfiles 7248 | head -20

# derrubar o processo pendurado (só o 7248, não o imqbroker)
sudo -u sjsas8 kill 7248
# se não sair em ~30s:
sudo -u sjsas8 kill -9 7248

# remover lock/pid antigo, se o ls acima mostrou algum
# subir de novo, com o passwordfile (que deve conter AS_ADMIN_PASSWORD e AS_ADMIN_MASTERPASSWORD)
sudo -u sjsas8 /opt/SUNWas8/bin/asadmin start-domain --user ASadmin \
  --passwordfile /opt/SUNWas8/config/passwordfile.conf das01

  
