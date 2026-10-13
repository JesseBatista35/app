Oi, Figura! Tudo bem? Não localizei na REQ o anexo com a relação dos NFS novos, só o documento de montagem antigo (os 4 NFS do 10.116.88.160 que já estão montados). Já vou cadastrar na library de DES o que você mandou por escrito. Pode me mandar a lista completa dos NFS novos, com o endpoint e o mount point de cada um? Se puder, já indique se algum é o mesmo export em mais de um mount point.

Vou rodar a release com a recriação da VM assim que cadastrar tudo.

O que cadastrar agora na library SIEXC-web-aplicacao-des

Variável	Valor
NFS_ENDPOINT_VM_5	192.168.227.59:/export/sicql_bovespa
NFS_MOUNT_POINT_VM_5	/SIEXC_SWIFT
NFS_ENDPOINT_ISILON_5	nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
NFS_MOUNT_POINT_ISILON_5	/siexc_incoming
