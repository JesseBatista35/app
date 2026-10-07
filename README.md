-sh-4.2$ cd roles/zabbix/defaults
-sh-4.2$
-sh-4.2$
-sh-4.2$ diff <(sed -E 's/(_password:|_token:).*/\1 ****/' .main.yml.20240704180752.p947976) \
-sh: erro de sintaxe próximo do `token' não esperado `('
-sh-4.2$      <(sed -E 's/(_password:|_token:).*/\1 ****/' main.yml)
-sh: erro de sintaxe próximo do `token' não esperado `('
-sh-4.2$
-sh-4.2$
-sh-4.2$ cd roles/zabbix/defaults
-sh: cd: roles/zabbix/defaults: Arquivo ou diretório não encontrado
-sh-4.2$
-sh-4.2$ # Diferenças além da senha
-sh-4.2$ diff <(sed -E 's/(_password:|_token:).*/\1 ****/' .main.yml.20240704180752.p947976) \
-sh: erro de sintaxe próximo do `token' não esperado `('
-sh-4.2$      <(sed -E 's/(_password:|_token:).*/\1 ****/' main.yml)
-sh: erro de sintaxe próximo do `token' não esperado `('
-sh-4.2$
-sh-4.2$ # A senha mudou? (compara só o hash)
-sh-4.2$ for f in .main.yml.2024*; do echo "$f $(grep '^db_password:' $f | md5sum)"; done
.main.yml.20240520140539.p947976 fcd6faf8414b57fed681ec622c565526  -
.main.yml.20240626100637.p947976 fcd6faf8414b57fed681ec622c565526  -
.main.yml.20240704180752.p947976 fcd6faf8414b57fed681ec622c565526  -
-sh-4.2$ echo "main.yml $(grep '^db_password:' main.yml | md5sum)"
main.yml fcd6faf8414b57fed681ec622c565526  -
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
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
-sh-4.2$
