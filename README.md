Prezados(as),

Informamos que o compartilhamento NFS fs_sisib (nprdnfs01.ad.caixa, 50 GB), criado pela equipe de Armazenamento nesta WO, foi configurado no ambiente DES (OKD, namespace sisib-des) para o módulo sisib-arquivos-de-quebra, conforme solicitado:

PV: sisib-arquivos-de-quebra-data-des (50Gi, RWX, Retain)
PVC: sisib-arquivos-de-quebra-data-des, status Bound

O pod do módulo ainda não sobe por causa de um erro na inicialização da aplicação: [descrever o erro]. Esse ajuste não faz parte do escopo de montagem do NFS atendido nesta WO. Para tratá-lo, é necessário abrir uma nova requisição direcionada à equipe [equipe responsável], anexando o log do pod.

Ponto de atenção: a equipe de Armazenamento informou que os IPs da partição mainframe DSP1 (192.168.231.11, .12 e .15) não foram incluídos no compartilhamento, por pertencerem à rede de backup antiga. Assim, a comunicação com o mainframe e a conversão EBCDIC→ASCII ainda não estão disponíveis. Caso essa integração seja necessária, a área solicitante deve obter os IPs da DSP1 na nova rede de backup NPRD (10.188.0.0/16) e solicitar a inclusão à equipe de Armazenamento.

Diante do exposto, encerramos esta WO.

Atenciosamente,
Esteira DevOps NPRD
