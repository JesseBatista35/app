
REQs das liberaçõe dos IPss:
- REQ000144955097
- REQ000144249814


Montagem NFS nos servidores da esteira do SIEXC
Servidor da aplicação SIEXC: 10.116.199.181 (DES)
Servidor da aplicação SIEXC: 10.116.201.141 (TQS)
MONTAR TAMBÉM NOS IPs DE BACKUP!
NFS: 10.116.88.160
OS SEGUINTES DIRETÓRIOS DEVEM SER MONTADOS NOS SERVIDORES DA ESTEIRA:
SICQL
SITEC
Path do NFS: /export/sigdb/sicql
Ponto de montagem nos servidores da esteira: /opt/sigdb
Path do NFS: /export/sigdb/sitec
Ponto de montagem nos servidores da esteira: /opt/sigdb/sitec
BOVESPA
Path do NFS: /export/sicql_bovespa
Ponto de montagem nos servidores da esteira: /opt/jboss/bovespa
ARQUIVOS
Path do NFS: /export/upload_prd
Ponto de montagem nos servidores da esteira: /upload
OBSERVAÇÕES IMPORTANTES
ATENÇÃO: Os NFS acima, diretórios e subdiretórios já existem. O que solicitamos é a liberação de
leitura e escrita nos NFS para os IPs dos servidores da esteira do SIEXC, para que o acesso seja
permitido e montagem seja efetiva.
Comunicação com Mainframe
Os NFS acima se comunicam com o mainframe, por isso seguem as informações sobre as partições que serão
compartilhadas e a necessidade de transformação de caracteres (EBCDIC para ASCII):
VAI COMUNICAR COM MAINFRAME: SIM
Transformação de Caracteres? (EBC/DIC para ASCII)E: SIM
VERSÃO DO NFS: 3
PARTIÇÕES MAINFRAME A COMPARTILHAR:
| D1DF - IPS: 192.168.231.41 |
| RJD1 - IPS: 192.168.235.108 , 192.168.235.109 , 192.168.235.110 |
