No 473:

bash
grep -a -A40 "IJ031084" $LOG | grep -aE "Caused by|ORA-|IO Error|Listener" | tail -10

No CLI do 471, teste a conexão:

/host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473/subsystem=datasources/data-source="jdbc/OracleSiccrDS":test-connection-in-pool

Se esse segundo comando der erro de “not found”, me mande a saída deste, para eu ver o nome exato:

/profile=full-ha-sifec-intranet/subsystem=datasources:read-children-names(child-type=data-source)





[domain@localhost:9999 /] /host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473/subsystem=datasources/data-source="jdbc/OracleSiccrDS":test-connection-in-pool
{
    "outcome" => "success",
    "result" => [true]
}

[domain@localhost:9999 /]



    "outcome" => "success",
    "result" => [
        "ExampleDS",
        "java:/jdbc/OracleDataguardDS_caixa",
        "java:/jdbc/OracleSiccrDS_docker",
        "java:/jdbc/OracleSiccrTributarioDS",
        "jdbc/DB2SiarcDS",
        "jdbc/DB2SiccrDS",
        "jdbc/DB2SiempDS",
        "jdbc/DB2SigecDS",
        "jdbc/Db2SiccrDS_OLD",
        "jdbc/IdmsSiapxDS",
        "jdbc/OracleBndesDS",
        "jdbc/OracleSiccrDS",
        "jdbc/OracleSicdtDS",
        "jdbc/OracleSifesDS",
        "jdbc/OracleSiganDS",
        "jdbc/OracleSipgeDS",
        "jdbc/OracleSirurDS",
        "jdbc/SybaseSibanDS",
        "jdbc/SybaseSibanDS_ORIGINAL",
        "jdbc/SybaseSiempDS",
        "jdbc/SybaseSifbnDS",
        "jdbc/SybaseSifbnDS02",
        "jdbc/SybaseSifbnDS_ORIGINAL",
        "jdbc/SybaseSifbnDS_ori",
        "jdbc/SybaseSiganDS",
        "jdbc/SybaseSiricDS"
    ]
}

[domain@localhost:9999 /]




[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]# grep -a -A40 "IJ031084" $LOG | grep -aE "Caused by|ORA-|IO Error|Listener" | tail -10
        at org.jboss.jca.core.connectionmanager.pool.mcp.SemaphoreConcurrentLinkedDequeManagedConnectionPool.createConnectionEventListener(SemaphoreConcurrentLinkedDequeManagedConnectionPool.java:1363)
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#

