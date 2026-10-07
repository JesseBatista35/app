# appcd /opt/ads-agent/esteira-jboss-vm

# 1. O que a a567498 mudou
diff roles/zabbix/tasks/.criaconsolidado.yml.20261006131048.a567498 roles/zabbix/tasks/criaconsolidado.yml

# 2. Onde ficam host, usuário e banco
grep -rn "db_ip\|db_user\|db_name\|db_porta" roles/zabbix/ group_vars/all group_vars/nprd* 2>/dev/null | grep -v '/\.'

# 3. Outros arquivos alterados desde 05/10
find . -newermt "2026-10-05" -type f ! -path "./.git/*" -ls
