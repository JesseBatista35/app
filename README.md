A release falha no custom.sh da aplicação (repositório SIOPI-ws-config), na montagem NFS do Azure Blob Storage stgsiopivendasonline em /arquivos-recebidos.

Criamos o ponto de montagem no servidor, mas o private endpoint do Blob (10.244.61.74) não é alcançável a partir da rede NPRD. Testamos também no servidor anterior da aplicação, com o mesmo resultado.

Pedimos que a equipe confirme se essa montagem é necessária em DES. Se não for, remova ou condicione o bloco no custom.sh para o ambiente. Se for, nos informe para encaminharmos a liberação de rede ao time de Nuvem. Recomendamos ainda incluir mkdir -p e timeout no mount para que falhas de rede não interrompam o deploy.
