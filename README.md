cd roles/zabbix/defaults

# Diferenças além da senha
diff <(sed -E 's/(_password:|_token:).*/\1 ****/' .main.yml.20240704180752.p947976) \
     <(sed -E 's/(_password:|_token:).*/\1 ****/' main.yml)

# A senha mudou? (compara só o hash)
for f in .main.yml.2024*; do echo "$f $(grep '^db_password:' $f | md5sum)"; done
echo "main.yml $(grep '^db_password:' main.yml | md5sum)"

for f in main.yml .main.yml.20240704180752.p947976; do
  echo "== $f"
  PGPASSWORD="$(awk '/^db_password:/{print $2}' $f | tr -d '"'"'")" \
    psql -h 10.244.74.86 -p 5432 -U monitdbadm -d monitordb001 -c 'select 1' 2>&1 | tail -1
done
