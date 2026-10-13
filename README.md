Peço desculpas pela confusão na nossa resposta anterior. Solicitamos informações de produção (endpoints de origem de PRD) que não são necessárias, já que as esteiras DES/TQS não atuam em produção. Entendido que os NFS de PRD só entram quando a library de PRD for preparada, e que em DES todos os exports já estão liberados para os servidores da esteira. Esses pedidos estão retirados.

Vamos dar andamento à análise do erro da release 502739 com os endpoints e mount points adicionados na library de DES, sem remover nenhum ponto de montagem existente.

Um ponto de atenção: nos exemplos enviados, NFS_ENDPOINT_ISILON e NFS_MOUNT_POINT_ISILON aparecem sem sufixo, e essas variáveis já existem na library apontando para /integracoes/SIEXC. Por favor, confirme se as novas foram criadas com sufixo (por exemplo _ISILON_5), para não sobrescrever as atuais.
