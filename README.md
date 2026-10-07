
-sh-4.2$ for f in main.yml .main.yml.20240704180752.p947976; do
>   echo "== $f"
>   PGPASSWORD="$(awk '/^db_password:/{print $2}' $f | tr -d '"'"'")" \
>     psql -h 10.244.74.86 -p 5432 -U monitdbadm -d monitordb001 -c 'select 1' 2>&1 | tail -1
> done
== main.yml
-sh: psql: comando não encontrado
== .main.yml.20240704180752.p947976
-sh: psql: comando não encontrado
-sh-4.2$
-sh-4.2$ ^C
-sh-4.2$ /opt/ads-agent/ansible/bin/python -c "
> import psycopg2,re
> p=re.search(r'^db_password:\s*[\"\x27]?([^\"\x27\n]+)',open('main.yml').read(),re.M).group(1).strip()
> try:
>   psycopg2.connect(host='10.244.74.86',port=5432,user='monitdbadm',dbname='monitordb001',password=p,sslmode='require',connect_timeout=10); print('OK')
> except Exception as e: print(e)
> "
/opt/ads-agent/ansible/lib/python2.7/site-packages/psycopg2/__init__.py:144: UserWarning: The psycopg2 wheel package will be renamed from release 2.8; in order to keep installing from binary please use "pip install psycopg2-binary" instead. For details see: <http://initd.org/psycopg/docs/install.html#binary-install-from-pypi>.
  """)
FATAL:  password authentication failed for user "monitdbadm"

-sh-4.2$
