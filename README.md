Prezada Figura, bom dia.

Mantemos a justificativa do fechamento anterior. A solicitação original não trazia a referência das REQs de liberação de acesso (REQ000144955097 e REQ000144249814, informadas somente agora, na reabertura) e também não trazia a relação dos NFS a serem montados, com endpoint de origem, mount point de destino e tipo. Sem esses dados, não havia como configurar a esteira.

Analisamos as REQs informadas:

WO0000080516700: liberou o IP de backup 192.168.233.69 no export Isilon .../CEPTIBR/SIEXC.
WO0000081109164: resultou na montagem dos 4 NFS do tipo VM (sigdb/sicql, sigdb/sitec, sicql_bovespa e upload_prd) via 192.168.227.59.

Essas liberações cobrem apenas os compartilhamentos que já estão montados hoje. Para os novos itens do DE/PARA (hyperprd12, hyperprd56, 10.252.168.196 e nfsdcp), não identificamos liberação de acesso nessas REQs. Cada export possui sua própria lista de clientes, portanto a liberação de um não vale para outro.

A esteira apenas monta o que já está provisionado e liberado para o IP principal e para o IP de backup do servidor. Sem a ACL, a montagem falha por timeout ou permissão negada, como já ocorreu com o storage 10.116.88.160.

Para darmos andamento, precisamos que seja informado, por NFS novo:

Endpoint de origem (produção) e endpoint a ser montado em DES.
Mount point de destino.
Tipo (ISILON ou VM), incluindo os compartilhamentos repetidos.
REQ ou registro que liberou cada export para o IP principal e para o IP de backup do servidor de DES. Caso não exista, a liberação deve ser solicitada ao time de Armazenamento pelo InfraFácil, e assim que concluída a demanda retorna para a esteira.
