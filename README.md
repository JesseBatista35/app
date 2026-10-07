cat -n roles/zabbix/defaults/main.yml | sed -E 's/(db_password:).*/\1 ****/'
ls -la --time-style=full-iso roles/zabbix/defaults/

grep -rn "db_ip\|db_password" roles/zabbix/defaults/.main* 2>/dev/null | sed -E 's/(db_password:).*/\1 ****/'

grep -rn "db_ip\|db_password" roles/zabbix/defaults/.main* 2>/dev/null | sed -E 's/(db_password:).*/\1 ****/'
