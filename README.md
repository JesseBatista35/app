ls -d /var/opt/SUNWappserver*/domains/das01 /opt/SUNWas8/domains/das01 2>/dev/null

grep -i 'AS_DEF_DOMAINS_PATH' /opt/SUNWas8/config/asenv.conf

ps -ef | grep -i das01 | grep -v grep
ps -ef | grep -i appservDAS | grep -v grep

tail -200 $DOM/logs/server.log
ls -l $DOM/config/ | grep -i -E 'lock|pid'
grep -n 'admin-listener' $DOM/config/domain.xml
df -h $DOM /tmp /var

