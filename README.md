Oi, Sandra! Sobre a montagem do NFS do SICCV-batch em TQS (WO0000081801601): a configuração do lado da esteira está concluída, mas a montagem não funciona por um problema de rede no servidor, que precisa ser corrigido pela CETEL. Por isso preciso que você abra uma nova REQ para a CETEL, com o texto abaixo.

Resumo: o servidor caddeapllx2821 tem uma interface de rede dedicada ao backup/armazenamento (ens224, IP 10.188.6.225), mas ela não consegue se comunicar com o storage hypernprd12.ad.caixa. Sem isso, o NFS /fs_siccv não monta em /SICCV.

O que já foi validado:

O IP de backup está cadastrado no IPAM (CADBKBKPLX186, "IP BACKUP ARMAZENAMENTO siccv-batch - tqs").
A interface está ativa (UP) e configurada com 10.188.6.225/19.
A esteira executou a montagem e o erro retornado foi mount.nfs: No route to host.
O erro está na rede da VM, não na esteira nem no export do storage.

Texto para abrir a REQ para a CETEL:

Servidor caddeapllx2821 (TQS, IP de acesso 10.116.202.23): a interface de backup ens224 (IP 10.188.6.225/19, cadastrado no IPAM como CADBKBKPLX186, rede REDE_BACKUP-NPRD) não tem comunicação com o storage hypernprd12.ad.caixa (10.188.0.11, .13, .14, .16, .17 e .18).

Evidências:

arping -I ens224 -c 3 10.188.0.11 envia 3 sondas e recebe 0 respostas.
ip neigh show dev ens224 mostra todos os IPs do storage em FAILED.
O ping retorna "Host de destino inalcançável".
O mount.nfs retorna "No route to host".

Solicitamos verificar o portgroup/VLAN da vNIC no VMware e a conectividade da rede REDE_BACKUP-NPRD com a rede do storage. Objetivo: montar hypernprd12.ad.caixa:/fs_siccv em /SICCV.
