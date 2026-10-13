Prezado(a),

Conforme solicitado em demanda, o atendimento foi realizado.

A falha de comunicação do IP 10.188.6.225 ocorria porque a interface de backup do servidor caddeapllx2821 (SICCV-batch, TQS) estava conectada ao port group da rede 192.168.224.0/19 (VL3697), enquanto o storage hypernprd12.ad.caixa está na rede BACKUP-NPRD (10.188.0.0/16).

A esteira corrigiu a rede de backup do servidor e o parâmetro correspondente na release do SICCV-batch em TQS, evitando a reversão em novas execuções. A release foi reexecutada com sucesso, com reprovisionamento do servidor, e o NFS hypernprd12.ad.caixa:/fs_siccv (50 GB) encontra-se montado em /SICCV.

Não há ação pendente para a equipe de Redes.

Atenciosamente,
Jessé Mouta Pereira Batista
Analista
CTIS / CESTI Esteira DEVOPS DES TQS NPRD
