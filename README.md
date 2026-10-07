/opt/ads-agent/ansible/bin/python -c "
import psycopg2,re
p=re.search(r'^db_password:\s*[\"\x27]?([^\"\x27\n]+)',open('main.yml').read(),re.M).group(1).strip()
try:
  psycopg2.connect(host='10.244.74.86',port=5432,user='monitdbadm',dbname='monitordb001',password=p,sslmode='require',connect_timeout=10); print('OK')
except Exception as e: print(e)
"
