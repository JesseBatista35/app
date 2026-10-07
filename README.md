-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ cd /opt/ads-agent/esteira-jboss-vm
-sh-4.2$
-sh-4.2$ diff roles/zabbix/tasks/.criaconsolidado.yml.20261006131048.a567498 roles/zabbix/tasks/criaconsolidado.yml
523d522
<                   ambiente     = '{{ sistema_ambiente | upper }}',
-sh-4.2$ grep -rn "db_ip\|db_user\|db_name\|db_porta" roles/zabbix/ group_vars/all group_vars/nprd* 2>/dev/null | grep -v '/\.'
roles/zabbix/defaults/main.yml:19:db_ip: 10.244.74.86
roles/zabbix/defaults/main.yml:20:db_porta: 5432
roles/zabbix/defaults/main.yml:22:db_name: monitordb001
roles/zabbix/defaults/main.yml:23:db_user: monitdbadm
roles/zabbix/tasks/criaconsolidado.yml:41:        login_host: "{{ db_ip }}"
roles/zabbix/tasks/criaconsolidado.yml:42:        login_port: "{{ db_porta }}"
roles/zabbix/tasks/criaconsolidado.yml:43:        login_user: "{{ db_user }}"
roles/zabbix/tasks/criaconsolidado.yml:45:        db: "{{ db_name }}"
roles/zabbix/tasks/criaconsolidado.yml:58:        login_host: "{{ db_ip }}"
roles/zabbix/tasks/criaconsolidado.yml:59:        login_port: "{{ db_porta }}"
roles/zabbix/tasks/criaconsolidado.yml:60:        login_user: "{{ db_user }}"
roles/zabbix/tasks/criaconsolidado.yml:62:        db: "{{ db_name }}"
roles/zabbix/tasks/criaconsolidado.yml:118:        login_host: "{{ db_ip }}"
roles/zabbix/tasks/criaconsolidado.yml:119:        login_port: "{{ db_porta }}"
roles/zabbix/tasks/criaconsolidado.yml:120:        login_user: "{{ db_user }}"
roles/zabbix/tasks/criaconsolidado.yml:122:        db: "{{ db_name }}"
roles/zabbix/tasks/criaconsolidado.yml:511:         login_host: "{{ db_ip }}"
roles/zabbix/tasks/criaconsolidado.yml:512:         login_port: "{{ db_porta }}"
roles/zabbix/tasks/criaconsolidado.yml:513:         login_user: "{{ db_user }}"
roles/zabbix/tasks/criaconsolidado.yml:515:         db: "{{ db_name }}"
roles/zabbix/tasks/criaconsolidado.yml:533:        login_host: "{{ db_ip }}"
roles/zabbix/tasks/criaconsolidado.yml:534:        login_port: "{{ db_porta }}"
roles/zabbix/tasks/criaconsolidado.yml:535:        login_user: "{{ db_user }}"
roles/zabbix/tasks/criaconsolidado.yml:537:        db: "{{ db_name }}"
roles/zabbix/tasks/criaconsolidado.yml:559:        login_host: "{{ db_ip }}"
roles/zabbix/tasks/criaconsolidado.yml:560:        login_port: "{{ db_porta }}"
roles/zabbix/tasks/criaconsolidado.yml:561:        login_user: "{{ db_user }}"
roles/zabbix/tasks/criaconsolidado.yml:563:        db: "{{ db_name }}"
group_vars/all:116:cmdb_username: USR_CETADAUT2
-sh-4.2$
-sh-4.2$
-sh-4.2$ find . -newermt "2026-10-05" -type f ! -path "./.git/*" -ls
331403887    4 -rw-r--r--   1 root     root          811 Out  6 13:15 ./roles/zabbix/defaults/main.yml
339742255   28 -rw-r--r--   1 root     root        25021 Out  6 13:12 ./roles/zabbix/tasks/criaconsolidado.yml
339740623   28 -rw-r--r--   1 root     root        25088 Out  6 13:12 ./roles/zabbix/tasks/.criaconsolidado.yml.20261006131048.a567498
-sh-4.2$ ^C
-sh-4.2$ ^C
-sh-4.2$
