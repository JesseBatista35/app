Paulo, boa tarde!

✅ SIEMP: já está no ar no JBoss 7.4 (DES).

Pacote: siemp-ear-14.37.0.6.ear
Server-group: siemp (servidor siemp_node1_lx465, cbrdeapllx465)
Status: enabled

❓ SIEMP-EMPRESAS (empresas-1.2.3-b15.ear): antes de subir, preciso confirmar em qual server-group ele deve rodar.

No 7.4, cada grupo tem um balanceador próprio:

siemp → mod_cluster_siemp
sifec-intranet → mod_cluster_sifec, que atende o migracaosifec.des.caixa

Nos logs, o SIFEC chama o /empresas-web pelo migracaosifec.des.caixa. Por isso, se ele subir no grupo do SIEMP, o link dentro do SIFEC não vai encontrar a aplicação.

No ambiente antigo, o EMPRESAS rodava junto com o SIEMP ou junto com o SIFEC? Ele é acessado só pelo menu do SIFEC ou tem uma URL própria pelo SIEMP?

Minha sugestão é subir no sifec-intranet. Com a sua confirmação, eu faço o deploy na hora.
