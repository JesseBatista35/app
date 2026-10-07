Sandra, boa tarde! Peço desculpas pela confusão de antes. Eu estava tratando outra demanda de NFS em paralelo (de outro sistema) e acabei misturando as duas na nossa conversa. A pergunta sobre a sigla SICCV-batch não tem relação com o SIHDG, então pode desconsiderar.

Sobre o SIHDG, os ajustes foram aplicados em DES e o release foi executado. Segue em anexo o print do terminal do OKD com os dois NFS montados:

/sihdg_des: nprdnfs01.ad.caixa:/ifs/cpwsprd01/nprd/fs_sihdg_sinaf (SINAF, 50G)
/sihdg_des_pwc: hypernprd56.ad.caixa:/fs_sihdg (PowerCenter, 50G)

A propriedade SIHDG-path.arquivo.sinaf está apontando para /sihdg_des/Arquivos_SINAF/, e a pasta Arquivos_SINAF já foi criada (vazia).

Ponto em aberto do lado de vocês: como o /sihdg_des agora é o storage novo, os arquivos que estavam no storage antigo continuam em /sihdg_des_pwc e precisam ser copiados para /sihdg_des/Arquivos_SINAF para a aplicação conseguir lê-los. Você consegue combinar quem faz essa cópia?
