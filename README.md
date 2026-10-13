À equipe de Virtualização,

Prezados,

Em atendimento ao parecer da CETEL nesta REQ (host 10.188.6.225 não visível na rede), foi verificado no servidor caddeapllx2821.agil.nprd.caixa.gov.br (SICCV-batch, TQS) que a interface de backup ens224 (Network adapter 2, MAC 00:50:56:82:a5:1d), com IP 10.188.6.225/16 da rede BACKUP-NPRD (10.188.0.0/16), está conectada ao port group tn-NPRD|NPRD_BKP-ap|VL3697-ep (rede 192.168.224.0/19). A captura de tráfego na interface confirma apenas tráfego dessa faixa, por isso o IP não é visto na rede.

Solicitamos alterar o port group da vNIC ens224 da VM caddeapllx2821 para tn-BACKUP|BACKUP-NPRD-ap|BACKUP-NPRD-ep, rede de acesso ao storage hypernprd12.ad.caixa (10.188.0.16). A configuração de IP no sistema operacional já foi ajustada pela esteira e não requer alteração.

Após o ajuste, a esteira reexecutará a release do SICCV-batch em TQS para concluir a montagem do NFS hypernprd12.ad.caixa:/fs_siccv (WO0000081801601).

Atenciosamente,
Jessé Mouta Pereira Batista
Analista
CTIS / CESTI Esteira DEVOPS DES TQS NPRD****
