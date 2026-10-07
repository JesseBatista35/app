cd /opt/ads-agent/esteira-jboss-vm
find . -newermt "2026-10-01" -type f ! -path "./.git/*" -exec ls -l --time-style=full-iso {} \;


find . -name ".*.2026*" -type f -exec ls -l --time-style=full-iso {} \;

git status --short
git diff --stat

grep -E '^db_(ip|porta|name|user|password):' roles/zabbix/defaults/main.yml | md5sum
grep '^db_password:' roles/zabbix/defaults/main.yml | md5sum

md5sum roles/zabbix/defaults/main.yml roles/zabbix/tasks/*.yml stack_monitoracao.yml site.yml
