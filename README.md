Prezados(as),

Informamos que o compartilhamento NFS fs_sisib (nprdnfs01.ad.caixa, 50 GB), criado pela equipe de Armazenamento nesta WO, foi configurado no ambiente DES (OKD, namespace sisib-des) para o módulo sisib-arquivos-de-quebra, conforme solicitado:

PV: sisib-arquivos-de-quebra-data-des (50Gi, RWX, Retain)
PVC: sisib-arquivos-de-quebra-data-des, status Bound

Na release, o pod do módulo foi criado e a aplicação foi iniciada. Porém o job validarArquivoJob (Spring Batch) termina com falha por ausência de parâmetro obrigatório:

ArquivoInvalidoException: PARAMETRO_OBRIGATORIO | linha 0 | Informe o parametro arquivo

A falha é da aplicação e não tem relação com o NFS. Além disso, a aplicação executa um processamento batch que é finalizado ao término da execução. Publicada como Deployment, ela é reiniciada continuamente pelo OKD, e o rollout não conclui.

Para seguir, a equipe de desenvolvimento do SISIB deve abrir nova requisição para:

Definir como o parâmetro arquivo será informado ao job.
Avaliar o modelo de execução do módulo, como Job/CronJob ou disparo por agendador, em vez de Deployment contínuo.

Ponto de atenção: a equipe de Armazenamento informou que os IPs da partição mainframe DSP1 (192.168.231.11, .12 e .15) não foram incluídos no compartilhamento, por pertencerem à rede de backup antiga. Assim, a comunicação com o mainframe e a conversão EBCDIC→ASCII ainda não estão disponíveis. Caso essa integração seja necessária, a área solicitante deve obter os IPs da DSP1 na nova rede de backup NPRD (10.188.0.0/16) e solicitar a inclusão à equipe de Armazenamento.

Diante do exposto, encerramos esta WO.

Atenciosamente,
Esteira DevOps NPRD
