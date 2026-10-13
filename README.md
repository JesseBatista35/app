Mas eu não entendi Jesse Mouta Pereira Batista, pois coloquei as indicações dos NFS, exemplo:
 
DES

NFS_ENDPOINT_VM_5 = 192.168.227.59:/export/sicql_bovespa

NFS_MOUNT_POINT_VM_5 = /SIEXC_SWIFT


DES

NFS_ENDPOINT_ISILON = nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC	

NFS_MOUNT_POINT_ISILON = /siexc_incoming
 
O que eu não entendi é sobre a necessidade dos NFS de PRD. Não podemos conectar nada de PRD em DES, então nos preocuparemos com PRD apenas quando a library de PRD começar a ser preparada para montagem.
 
em DES, todos os NFS já estão liberados para os servidores de DES da esteira
 
