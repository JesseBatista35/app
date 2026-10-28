Bom dia!

O compartilhamento foi criado pela equipe de Armazenamento, e na nossa parte (Esteira) configuramos apenas a montagem NFS no OKD para o módulo sisib-arquivos-de-quebra. O acesso ao share SMB pela estação é tratado pela equipe de Armazenamento.

Pela evidência registrada, o servidor nprdsmb01.ad.caixa está na rede de backup NPRD (10.188.0.0/16), que normalmente não é acessível a partir das estações de trabalho. Também não consta a liberação de permissão do share fs_sisib_smb para as matrículas responsáveis.

Para confirmar, você pode rodar no PowerShell:
Test-NetConnection nprdsmb01.ad.caixa -Port 445

Recomendo abrir nova requisição para a equipe de Armazenamento, citando a REQ000146870898 / WO0000082112572, solicitando a liberação de acesso SMB ao share \\nprdsmb01.ad.caixa\fs_sisib_smb a partir da estação, com permissão para c161778 e c131457. Inclua o print do erro apresentado e o resultado do teste acima.
