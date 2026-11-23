ssh 10.116.202.45
sudo su -

# ultimas linhas do log da aplicacao
tail -60 /log_jboss/sigsj_internet/sigsj_internet.log

# so os erros do seu teste de agora
grep -nE "ERROR|Exception|Caused by|ORA-|SenhasSIIBC|SIROT|SIPER|getResponse|Connection" /log_jboss/sigsj_internet/sigsj_internet.log | tail -40
