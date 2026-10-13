- REQ000144955097
- REQ000144249814


Analisar 

ERRO NO BUILD ESTEIRA SIEXC

Link esteira do SIEXC:
https://devops.caixa/projetos/Caixa/_git/SIEXC-web-aplicacao-config

Adicionei os endpoint e mount points dos NFS anexados à library de DES do SIEXC e o build falhou. Por favor realizar a montagem adequada e rodar o build com sucesso

Log do erro em anexo
Documento com instruções das montagens que foram adicionadas em anexo. Favor não remover nenhum ponto de montagem do SIEXC.

Link da release com erro:
https://devops.caixa/projetos/Caixa/_releaseProgress?releaseId=502739&environmentId=2335617&itemType=VariableGroups&_a=release-environment-logs


Histórico de Informações de Trabalho da Ordem de Trabalho
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 24/07/2026 13:42:14
Criado por	 P725476
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 A

CESOB,

1. Feito ajuste do valor de IP do NFS configurado visto na esteira o NFS é montado a partir do IP de backup e não do IP de serviço. Segue evidências abaixo:

[p725476@caddeapllx2193 ~]$ df -h |egrep -i "nfsctcnprd.ctc.caixa|192.168.227.59"
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC  5,0G  493M  4,6G  10% /siexc
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC  5,0G  493M  4,6G  10% /integracoes/SIEXC
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC     16G   39M   16G   1% /integracoes/SIAPC
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF  7,0G  5,1G  1,9G  73% /integracoes/SIISF
192.168.227.59:/export/sigdb/sicql                              5,0G  2,0G  3,1G  40% /opt/sigdb
192.168.227.59:/export/sigdb/sitec                               97M  8,5M   89M   9% /opt/sigdb/sitec
192.168.227.59:/export/sicql_bovespa                             97M  5,3M   92M   6% /opt/jboss/bovespa
192.168.227.59:/export/upload_prd                                97M  5,3M   92M   6% /upload
[p725476@caddeapllx2193 ~]$

2. Segue evidências da release executada com sucesso.

https://devops.caixa/projetos/Caixa/_releaseProgress?_a=release-environment-logs&releaseId=505328&environmentId=2347073

Roger Costa Machado
Analista de Suporte Multiplataforma DES/TQS CTIS
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 23/07/2026 18:23:43
Criado por	 P694128
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 À ESTEIRAS DEVOPS NPRD,

Segue para verificação conforme nota anterior
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 23/07/2026 18:11:34
Criado por	 P719768
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezados,

Para que a equipe de Armazenamento possa localizar e validar corretamente o compartilhamento NFS no storage, é necessário o envio do path completo (caminho interno do Isilon/FQDN do export), e não apenas o caminho de exportação apresentado à aplicação.

Como exemplo, a informação necessária deve seguir o formato abaixo:

/ifs/CADSVISISD4/SERVIDORES/CETAD/SIIGA_SIAPI_DESID


Os caminhos informados até o momento:

/export/sigdb/sicql /export/sigdb/sitec /export/sicql_bovespa /export/upload_prd

Eles correspondem aos exports NFS disponibilizados aos clientes e não permitem identificar, de forma inequívoca, o diretório interno do storage.

Solicitamos, portanto, o envio do path completo, conforme exemplo acima, para que possamos dar continuidade ao atendimento e realizar as verificações necessárias.

Atenciosamente,
Armazenamento Sonda.
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 23/07/2026 15:13:14
Criado por	 P768728
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 A equipe

Armazenamento,

Sobre o FQDN/path interno do NFS no storage 10.116.88.160: essa informação não está disponível para o time de Esteiras/DevOps NPRD, pois se trata de configuração interna do storage, vinculada à FREI original de alocação de espaço em Isilon.

Solicitamos que a equipe de Armazenamento consulte esse dado diretamente em seus registros de export, associados ao IP 10.116.88.160 e aos paths informados nas notas dos dias 20/07 as 16:58 e 22/07 as 10:36

Reiteramos que a demanda está em espera de retorno desde 20/07 e solicitamos priorização considerando o SLA já mencionado.

Desde já agradecemos a compreensão.

Atte.

Esteira Devops  - NPRD
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 23/07/2026 15:10:52
Criado por	 C160402
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Repassando informações da mensagem desta REQ 20/7/2026 16:58:35 ; (P585600) que replica as informações do documento PDF com as intruções:

À CAIXA

Prezados

Em resposta à solicitação, seguem os paths NFS confirmados conforme anexo original de abertura da demanda:

SICQL
Path do NFS (Storage 10.116.88.160): /export/sigdb/sicql
Ponto de montagem na esteira: /opt/sigdb


SITEC
Path do NFS (Storage 10.116.88.160): /export/sigdb/sitec
Ponto de montagem na esteira: /opt/sigdb/sitec


BOVESPA
Path do NFS (Storage 10.116.88.160): /export/sicql_bovespa
Ponto de montagem na esteira: /opt/jboss/bovespa

ARQUIVOS
Path do NFS (Storage 10.116.88.160): /export/upload_prd
Ponto de montagem na esteira: /upload


IPs dos servidores de aplicação da esteira:

DES: 10.116.199.181
TQS: 10.116.201.141

IPs de rede de backup:
DES: 192.168.233.69
TQS: 192.168.242.137

Conforme o FREI original, é necessário liberar tanto os IPs de aplicação quanto os IPs de backup dos servidores acima para que a montagem seja efetiva.
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 23/07/2026 11:55:41
Criado por	 P768728
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Reiteramos que está faltando as informações de path (FQDN), sem as informações necessárias não é possível localizar o NFS em questão.
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 22/07/2026 17:09:07
Criado por	 P626562
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Reiteramos que está faltando as informações de path (FQDN), sem as informações necessárias não é possível localizar o NFS em questão.
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 22/07/2026 10:36:32
Criado por	 P585600
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 À ARMAZENAMENTO

Prezados,

Reforçando informações já enviadas nesta WO em 20/07 às 16h16 e 16h58, que parecem não ter sido consideradas nas respostas seguintes:

Os paths de montagem e IPs (aplicação e backup) já foram fornecidos anteriormente nesta mesma WO. Segue novamente, para facilitar:

Paths conforme FREI original:

/export/sigdb/sicql -> /opt/sigdb /export/sigdb/sitec -> /opt/sigdb/sitec /export/sicql_bovespa -> /opt/jboss/bovespa /export/upload_prd -> /upload

IPs de aplicação: DES 10.116.199.181 | TQS 10.116.201.141
IPs de backup: DES 192.168.233.69 | TQS 192.168.242.137

Sobre o FQDN/path interno do NFS no storage 10.116.88.160: essa informação não está disponível para o time de Esteiras/DevOps, pois se trata de configuração interna do storage, vinculada à FREI original de alocação de espaço em Isilon. Solicitamos que a equipe de Armazenamento consulte esse dado diretamente em seus próprios registros de export, associados ao IP 10.116.88.160 e aos paths acima informados.

Reiteramos que a demanda está em espera de retorno desde 20/07 e solicitamos priorização considerando o SLA já mencionado.

Atenciosamente,

Jessé Mouta Pereira Batista
CTIS/CESTI - Esteira DEVOPS DES TQS NPRD
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 22/07/2026 09:58:19
Criado por	 P768728
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 A CAIXA,

Gentileza considerar a aplicação do SLA de 24 horas para este atendimento a partir deste momento, visto que a demanda foi direcionada à nossa fila já com o prazo expirado.

Desde já agradecemos a compreensão.

Atte.

Esteira Devops DES e TQS - NPRD
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 21/07/2026 16:07:11
Criado por	 P573005
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 1. Os endereços IPs foram informados na nota de 20/07 - 16h58

2. Necessário informar a equipe de armazenamento o FQDN do NFS montado nos servidores, conforme solicitado na nota 20/07 - 16h37.
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 21/07/2026 14:58:54
Criado por	 P768728
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 A Equipe

Multi Suporte S.O

Conforme nota adicionada pelo nosso analista NPRD no dia 20/07 as 16:16 nós não possuímos as informações do IP de Backup.

Encaminhamos essa WO para atendimento conforme orientação passada pela equipe de Armazenamento para que possam disponibilizar as informações dos IPs de Backup.

Atte.

Esteira Devops NPRD
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 21/07/2026 14:13:05
Criado por	 P669476
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 À
Esteira DES TQS,

Segue demanda para avaliação e tratamento.

Atenciosamente,
André Hebert dos Santos
Preposto
CTIS/CESTI/ESTEIRA - APLICAÇÃO/DEVOPS
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 21/07/2026 11:02:41
Criado por	 P580900
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Ambiente de esteiras, segue para atendimento.
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 21/07/2026 10:26:26
Criado por	 P768728
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 A Equipe

Multi Suporte S.O

Segue WO conforme solicitado na nota anterior.

Atte.

Esteira Devops DES TQS  - NPRD
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 20/07/2026 18:56:59
Criado por	 P637135
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 À
CTIS/CESTI/Esteiras - DEVOPS DES TQS NPRD

Prezados, qual é o path NFS em questão e quais são os IPs da rede de backup que precisam de permissão

Arquivos anexados a demanda não informam o NFS do Storage, sem essa informação Armazenamento não consegue apoiar no atendimento.

RE-Lembrando: "/export/sigdb/sicql" não é o path NFS do Storage.

Caso não tenham essa informação por gentileza encaminhar demanda para Multi - Suporte a Sistemas Operacionais.

Obrigado.

Att,
CESTI53.
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 20/07/2026 16:58:35
Criado por	 P585600
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 À CAIXA

Prezados

Em resposta à solicitação, seguem os paths NFS confirmados conforme anexo original de abertura da demanda:

SICQL
Path do NFS (Storage 10.116.88.160): /export/sigdb/sicql
Ponto de montagem na esteira: /opt/sigdb


SITEC
Path do NFS (Storage 10.116.88.160): /export/sigdb/sitec
Ponto de montagem na esteira: /opt/sigdb/sitec


BOVESPA
Path do NFS (Storage 10.116.88.160): /export/sicql_bovespa
Ponto de montagem na esteira: /opt/jboss/bovespa

ARQUIVOS
Path do NFS (Storage 10.116.88.160): /export/upload_prd
Ponto de montagem na esteira: /upload


IPs dos servidores de aplicação da esteira:

DES: 10.116.199.181
TQS: 10.116.201.141

IPs de rede de backup:
DES: 192.168.233.69
TQS: 192.168.242.137

Conforme o FREI original, é necessário liberar tanto os IPs de aplicação quanto os IPs de backup dos servidores acima para que a montagem seja efetiva.
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 20/07/2026 16:37:05
Criado por	 P637135
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 À
CTIS/CESTI/Esteiras - DEVOPS DES TQS NPRD

Prezados, qual é o path NFS em questão e quais são os IPs da rede de backup que precisam de permissão

Lembrando: /export/sigdb/sicql não é o path NFS do Storage.

Obrigado.

Att,
CESTI53.
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 20/07/2026 16:31:20
Criado por	 C160402
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 À Armazenamento.

Prezados(as),

Como consta no documento de montagem presente nesta REQ, é necessário liberação para os IPs do servidores de DES e TQS da esteira. Podem verificar por lá, mas repito aqui:

Servidor da aplicação SIEXC: 10.116.199.181 (DES)
Servidor da aplicação SIEXC: 10.116.201.141 (TQS)

Importante liberar também nos servidores de backup de cada uma das instâncias. Ja temos uma liberação de exemplo como indicado pelo Jessé na mensagem dele.

Esses NFSs se comunicam com o mainframe (uso do SIGDB), caso seja necessário alguma liberação neste sentido também, peço por favor que incluam no planejamento das liberações.

Grato.

Atenciosamente,
Figura Carrijo Viana Figur
Analista Junior
CESOB - Comunicade Câmbio e Tesouraria
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 20/07/2026 16:16:03
Criado por	 P585600
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 À Armazenamento

Prezados,

Em atendimento à solicitação de montagem dos novos compartilhamentos NFS na esteira do sistema SIEXC (ambiente DES), informo o que foi realizado e o ponto pendente que requer atuação da equipe de Armazenamento.

Após o ajuste, a esteira passou a processar corretamente o tipo de compartilhamento e avançou até a etapa efetiva de montagem no servidor.


Ponto pendente — acesso ao storage 10.116.88.160:
Na etapa de montagem, o servidor de destino não concede acesso ao host de origem. Testes de conectividade realizados diretamente na VM confirmam o cenário:

Tentativa de mount manual retorna: mount.nfs: failed to prepare mount: Operation not permitted
Teste de conexão nas portas 2049 e 111 (NFS/portmapper): sem resposta do destino
Comandos rpcinfo -p e showmount -e para o destino: sem retorno

Servidor de origem (cliente NFS): caddeapllx2193.agil.nprd.caixa.gov.br
IPs do servidor de origem:

10.116.199.181 (interface ens192)
192.168.233.69 (interface ens224)

Storage de destino: 10.116.88.160
Exports solicitados:

/export/sigdb/sicql
/export/sigdb/sitec
/export/sicql_bovespa
/export/upload_prd

Solicito a verificação se o(s) IP(s) do servidor de origem estão autorizados na lista de clientes (ACL) desses exports no storage 10.116.88.160, e a liberação necessária para viabilizar o acesso.
Como referência, este mesmo servidor já monta com sucesso outros 3 compartilhamentos hospedados em nfsctcnprd.ctc.caixa (Isilon), utilizando o IP 10.116.199.181.


Encaminho para a equipe de Armazenamento para análise e liberação do acesso solicitado.

Atenciosamente,

Jessé Mouta Pereira Batista
Analista
CTIS / CESTI Esteira DEVOPS DES TQS NPRD
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 20/07/2026 12:22:39
Criado por	 P730708
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Demanda inicial sem viés de falha, erro, degradação ou
esgotamento de infraestrutura, serviço, máquina, armazenamento,
rotina ou situação que não esteja na iminência de tornar-se
incidente. Previsto atendimento em até 24 horas úteis.

[CENTRAL-SID]
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 20/07/2026 12:07:20
Criado por	 P768728
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezado(a),

Informamos que sua solicitação foi recebida.

Nosso SLA para atendimento é de até 24h úteis, analisaremos a solicitação para nos certificarmos que o atendimento está dentro do escopo de atuação da nossa equipe.

Caso seja identificado que o atendimento não corresponde ao nosso escopo, a solicitação será redirecionada à equipe responsável.

Novas informações e atualizações serão registradas diretamente nesta WO.

Atte.

CTIS / CESTI Esteira DEVOPS DES TQS NPRD
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 20/07/2026 11:44:09
Criado por	 C160402
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Anexo do Registro de Solicitação.
ID da Ordem de Trabalho	 WO0000081109164
Criado em	 20/07/2026 11:44:08
Criado por	 Remedy Application Service
Origem de Comunicação	 E-mail
Exibir Acesso	 Interno
Notas	 Este ticket foi criado a partir do sistema de solicitação de serviço.
Impresso por P585600 em Terça-feira, 13/10/2026 11:39:29




Adição de IP ao NFS /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC

Favor verificar, 
Solicitação de Armazenamento
****************************************************
SOLICITANTE: c160402
CENTRO DE CUSTO: CESOB
OPÇÃO NAS: Sistema
NOME SISTEMA: siexc
AMBIENTE: DES
PLATAFORMA SISTEMA: VM da Esteira
PLATAFORMA ARMAZENAMENTO: OPEN
TIPO DE DISCO: NAS
COMPARTILHAMENTO NOVO
VOLUMETRIA: 5GB
CUSTO MENSAL: R$ 0,93
CUSTO ANUAL: R$ 11,07
HOSTNAMES:
MÓDULO: siexc-web-aplicacao
IP REAL: 10.116.199.181
IP BACKUP: 192.168.233.69
HOSTNAME: caddeapllx2193.agil.nprd.caixa.gov.br


VM esteiras ágeis
PONTO DE MONTAGEM: /producao
TIPO DE COMPARTILHAMENTO: NFS
VAI COMUNICAR COM MAINFRAME: SIM
Transformação de Caracteres? (EBC/DIC para ASCII)E: SIM
VERSÃO DO NFS: 3
PARTIÇÕES MAINFRAME A COMPARTILHAR:  | D1DF - IPS: 192.168.231.41 | RJD1 - IPS: 192.168.235.108 , 192.168.235.109 , 192.168.235.110 |

****************************************************


Histórico de Informações de Trabalho da Ordem de Trabalho
ID da Ordem de Trabalho	 WO0000080516700
Criado em	 23/05/2026 14:25:38
Criado por	 P569415
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Com o encerramento da demanda final 8609, encerramos também esse atendimento
ID da Ordem de Trabalho	 WO0000080516700
Criado em	 21/05/2026 21:14:35
Criado por	 P637135
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Aberta a WO0000080518609 para Esteiras fazer a montagem
ID da Ordem de Trabalho	 WO0000080516700
Criado em	 21/05/2026 20:16:28
Criado por	 P626562
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 IPs adicionados, segue evidências.

FQDN de acesso:
nfsctcnprd.ctc.caixa - 192.168.224.0/19

ID: 432
                  Zone: SERVIDORES
                 Paths: /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
           Description: Description: CEPTIBR - SIEXC - WO71449297 - WO71606707 - WO77260890 -
               Clients: 192.168.226.250, 192.168.229.62, 192.168.230.163, 192.168.230.164, 192.168.231.41, 192.168.233.69, 192.168.235.108, 192.168.235.109, 192.168.235.110
          Root Clients: 192.168.226.250, 192.168.229.62, 192.168.230.163, 192.168.230.164, 192.168.231.41, 192.168.233.69, 192.168.235.108, 192.168.235.109, 192.168.235.110
     Read Only Clients: -
    Read Write Clients: 192.168.226.250, 192.168.229.62, 192.168.230.163, 192.168.230.164, 192.168.231.41, 192.168.233.69, 192.168.235.108, 192.168.235.109, 192.168.235.110
Thu May 21 20:15:04 -03 2026




Atenciosamente,
Armazenamento Sonda.
ID da Ordem de Trabalho	 WO0000080516700
Criado em	 21/05/2026 19:01:39
Criado por	 C159842
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Demanda autorizada conforme deliberado pela CESTI33. Att, CESTI91
ID da Ordem de Trabalho	 WO0000080516700
Criado em	 21/05/2026 17:59:55
Criado por	 P637135
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 [PAUTA CESTI]
Número: WO0000080516700
Ação: Adição de IP ao NFS /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
Risco: Baixo
Impacto: Não
Ambiente: NPRD
Segmento: Infraestrutura
Sistema: Open
Destaque: Não
Site: DTC
Corte: 22/05/2026 02:00
Janela: 21/05/2026 20:00 - 22/05/2026 02:00
Prioridade: Baixa
ID da Ordem de Trabalho	 WO0000080516700
Criado em	 21/05/2026 17:59:12
Criado por	 P637135
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 [SELO DE CONFORMIDADE  - SCR91001]
Este registro foi avaliado sob os aspectos dos prazos, da qualidade, da documentação do atendimento e do processo, e da conformidade procedimental e técnica visando resguardar a execução, a validação e eventual retorno.
ID da Ordem de Trabalho	 WO0000080516700
Criado em	 21/05/2026 17:45:35
Criado por	 C103881
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Autorizamos a execução da atividade (inclusão de IP conforme nota anterior)

Att
CESTI33
ID da Ordem de Trabalho	 WO0000080516700
Criado em	 21/05/2026 17:06:16
Criado por	 P719768
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Conforme evidência abaixo o NFS já existe em ambiente NPRD com praticamente todos os IPs informados na WO inclusos.

SERVIDORES
                 Paths: /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
           Description: Description: CEPTIBR - SIEXC - WO71449297 - WO71606707 - WO77260890 -
               Clients: 192.168.226.250, 192.168.229.62, 192.168.230.163, 192.168.230.164, 192.168.231.41, 192.168.235.108
          Root Clients: 192.168.226.250, 192.168.229.62, 192.168.230.163, 192.168.230.164, 192.168.231.41, 192.168.235.108
     Read Only Clients: -
    Read Write Clients: 192.168.226.250, 192.168.229.62, 192.168.230.163, 192.168.230.164, 192.168.231.41, 192.168.235.108
Thu May 21 16:35:22 -03 2026

Dessa forma seguimos com o plano de ação para incluir os IPs relacionados que ainda não fazem parte desse NFS, são eles:

192.168.233.69,192.168.235.109,192.168.235.110





WO0000080516700 - Adição de IP ao NFS
---------------------------------------------------------------------------------------------------------------------
AÇÃO: Incluir IP de backup ao NFS
---------------------------------------------------------------------------------------------------------------------
JUSTIFICATIVA: Conceder acesso ao IPs: 192.168.233.69,192.168.235.109,192.168.235.110

---------------------------------------------------------------------------------------------------------------------
SITE (CTC OU DTC) - CTC
---------------------------------------------------------------------------------------------------------------------
AMBIENTE (Bancário, Negocial, Social, NPRD, HMP, Departamental):
---------------------------------------------------------------------------------------------------------------------
RISCO: Baixo  
---------------------------------------------------------------------------------------------------------------------
IMPACTO: SIM (   ) NÃO ( X )
---------------------------------------------------------------------------------------------------------------------  
ITEM OU ITENS DE CONFIGURAÇÃO (IC):
---------------------------------------------------------------------------------------------------------------------
PLANO DE EXECUÇÃO: SIM ( X ) NÃO (   )
---------------------------------------------------------------------------------------------------------------------
VALIDAÇÃO: SIM ( X ) NÃO (   )
---------------------------------------------------------------------------------------------------------------------
RETORNO: SIM ( X ) NÃO (   )
---------------------------------------------------------------------------------------------------------------------



Plano de ação:

0) A demanda Altera o Ambiente?
Sim (X)
Não ( )

1) Avaliação de Risco:
Baixo (x )
Médio ( )
Alto ( )

2) Plano de Execução:
Passo 1: Procedimento a ser executado no CADSVISISD4;
Passo 2: Acesse a console: 10.122.148.76;
Passo 3: Executar o comando abaixo:


Listar os IPs existentes ao NFS
isi nfs exports list --zone=SERVIDORES --path=/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC -v |head -n 8;date

Adicionar o IP 10.122.22.106 ao NFS:
isi nfs exports modify --add-clients=192.168.233.69,192.168.235.109,192.168.235.110  --add-root-clients=192.168.233.69,192.168.235.109,192.168.235.110 --add-read-write-clients=192.168.233.69,192.168.235.109,192.168.235.110 --zone=SERVIDORES --id=432


Evidenciar o IP incluído:
isi nfs exports list --zone=SERVIDORES --path=/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC -v |head -n 8;date

Informar FQDN de acesso:
nfsctcnprd.ctc.caixa - 192.168.224.0/19



Atenciosamente,
Armazenamento Sonda.
ID da Ordem de Trabalho	 WO0000080516700
Criado em	 21/05/2026 16:24:07
Criado por	 P556543
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Demanda inicial sem viés de falha, erro, degradação ou esgotamento de infraestrutura, serviço, máquina, armazenamento, rotina ou situação que não esteja na iminência de tornar-se incidente. Previsto atendimento em até 72 horas.[CENTRAL-SID]
ID da Ordem de Trabalho	 WO0000080516700
Criado em	 21/05/2026 16:22:34
Criado por	 P637135
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezado(a)
Acusamos o recebimento desta WO.
1. Informamos que sua solicitação entrou em fila de atendimento.
2. Trata-se de uma atividade de complexidade baixa e será atendida o mais breve
possível.
3. Esta demanda será apresentada para deliberação na reunião de Overview?
( ) SIM ( ) NÃO
4. Em complemento as informações, destaca-se que: Será realizado o planejamento para deliberação em breve.
5. Informações futuras serão adicionadas a esta WO.
Qualquer dúvida, estamos à disposição
Preposto Armazenamento
CTIS / CESTI / Armazenamento CESTI53.
ID da Ordem de Trabalho	 WO0000080516700
Criado em	 21/05/2026 15:49:41
Criado por	 Remedy Application Service
Origem de Comunicação	 E-mail
Exibir Acesso	 Interno
Notas	 Este ticket foi criado a partir do sistema de solicitação de serviço.
Impresso por P585600 em Terça-feira, 13/10/2026 11:40:12
