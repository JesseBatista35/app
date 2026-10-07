-sh-4.2$ ^C
-sh-4.2$ cat -n roles/zabbix/defaults/main.yml | sed -E 's/(db_password:).*/\1 ****/'
     1  zabbix_log_file_size: 1
     2  zabbix_timeout: 30
     3  zabbix_version: 6.0.23-release1
     4  #Cria grupo/host api zabbix
     5  zabbix_username: api_esteira
     6  zabbix_password: C3m07Z2bb1x2dx
     7  zabbix_token: "1865f89361c9d98b36600ec269f5930bdc66cef246042d05293473235a14d7af"
     8  zabbix_url: https://monitoracao.az.cloud.caixa/zabbixapi/api_jsonrpc.php
     9  zabbix_hostname: "{{ inventory_hostname.split('.')[0] }}"
    10  zabbix_ip: "{{ hostvars[inventory_hostname]['ansible_host'] }}"
    11  zabbix_proxy: "Proxy-Cloud-cadsvaprlx402"
    12  zabbix_host: 10.122.157.167
    13  versao: "1.1.11"
    14  datahora: "{{ now(utc=false,fmt='%Y-%m-%d %H:%M:%S') }}"
    15  tipo_sistema: "ansible"
    16  fonte: "esteiras"
    17  #Consulta e atuliza dados no postgresql
    18  db_tabela: btrad_tb_sistemas
    19  db_ip: 10.244.74.86
    20  db_porta: 5432
    21  db_esquema: mon
    22  db_name: monitordb001
    23  db_user: monitdbadm
    24  db_password: ****
    25
-sh-4.2$
-sh-4.2$
-sh-4.2$ ls -la --time-style=full-iso roles/zabbix/defaults/
total 16
drwxr-xr-x 2 root root 142 2026-10-06 13:15:31.139269268 -0300 .
drwxr-xr-x 6 root root  68 2024-05-14 09:39:53.000000000 -0300 ..
-rw-r--r-- 1 root root 811 2026-10-06 13:15:31.036270585 -0300 main.yml
-rw-r--r-- 1 root root 578 2024-05-20 14:47:13.615227053 -0300 .main.yml.20240520140539.p947976
-rw-r--r-- 1 root root 695 2024-06-26 10:37:13.383954714 -0300 .main.yml.20240626100637.p947976
-rw-r--r-- 1 root root 769 2024-07-04 18:43:28.926146609 -0300 .main.yml.20240704180752.p947976
-sh-4.2$
-sh-4.2$
-sh-4.2$ grep -rn "db_ip\|db_password" roles/zabbix/defaults/.main* 2>/dev/null | sed -E 's/(db_password:).*/\1 ****/'
roles/zabbix/defaults/.main.yml.20240520140539.p947976:13:db_ip: 10.244.74.86
roles/zabbix/defaults/.main.yml.20240520140539.p947976:18:db_password: ****
roles/zabbix/defaults/.main.yml.20240626100637.p947976:15:db_ip: 10.244.74.86
roles/zabbix/defaults/.main.yml.20240626100637.p947976:20:db_password: ****
roles/zabbix/defaults/.main.yml.20240704180752.p947976:17:db_ip: 10.244.74.86
roles/zabbix/defaults/.main.yml.20240704180752.p947976:22:db_password: ****
-sh-4.2$
-sh-4.2$
-sh-4.2$ grep -rn "db_ip\|db_password" roles/zabbix/defaults/.main* 2>/dev/null | sed -E 's/(db_password:).*/\1 ****/'
roles/zabbix/defaults/.main.yml.20240520140539.p947976:13:db_ip: 10.244.74.86
roles/zabbix/defaults/.main.yml.20240520140539.p947976:18:db_password: ****
roles/zabbix/defaults/.main.yml.20240626100637.p947976:15:db_ip: 10.244.74.86
roles/zabbix/defaults/.main.yml.20240626100637.p947976:20:db_password: ****
roles/zabbix/defaults/.main.yml.20240704180752.p947976:17:db_ip: 10.244.74.86
roles/zabbix/defaults/.main.yml.20240704180752.p947976:22:db_password: ****
-sh-4.2$
-sh-4.2$
-sh-4.2$
