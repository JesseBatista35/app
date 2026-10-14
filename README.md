
Verificamos a montagem do NFS do SIMCN-backend nos ambientes DES e TQS (OKD4 NPRD):

O export nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/UP_SIMCN está montado corretamente em /simcn nos pods de DES (namespace simcn-des) e TQS (namespace simcn-tqs).
A montagem é feita pelos nós do cluster OKD4. O servidor ceadecldlx022 (10.116.208.42) não participa dela, e o IP 25.128.181.35 é o IP interno do service da aplicação, sem relação com o NFS.
O caminho upload/des/simcn não existe no export. Os diretórios da aplicação (conciliacao, cacheJson, relatoriosLegados) estão na raiz do volume.

Pontos identificados (fora do escopo da esteira):

Permissão: a aplicação roda com o uid 185, e os subdiretórios do export pertencem a 30000115:20000957 com permissão 775. Por isso a gravação retorna Permission denied.
Compartilhamento entre ambientes: DES e TQS apontam para o mesmo export (UP_SIMCN), e por isso os arquivos dos dois ambientes se misturam.

Ação necessária: a equipe do sistema deve abrir solicitação ao time de Armazenamento para:

conceder leitura e escrita ao uid 185 no export UP_SIMCN e em seus subdiretórios;
avaliar a separação do export por ambiente (ex.: UP_SIMCN/des e UP_SIMCN/tqs), se desejado.

Após o atendimento pelo Armazenamento, caso haja alteração de caminho, basta abrir nova solicitação à esteira para ajustarmos as variáveis PATH_NFS e STORAGE_PATH e recriarmos os volumes.
