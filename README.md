No 473:

bash
grep -a -A40 "IJ031084" $LOG | grep -aE "Caused by|ORA-|IO Error|Listener" | tail -10

No CLI do 471, teste a conexão:

/host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473/subsystem=datasources/data-source="jdbc/OracleSiccrDS":test-connection-in-pool

Se esse segundo comando der erro de “not found”, me mande a saída deste, para eu ver o nome exato:

/profile=full-ha-sifec-intranet/subsystem=datasources:read-children-names(child-type=data-source)
