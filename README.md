Em continuidade ao REQ000146430103 e REQ000146376304 onde foi solicitada a criação de NFS compartilhado para o ambiente TQS para o SICCV Batch 
Informo que o host 10.188.6.225 não se encontra visível na rede. Favor verificar a configuração da VM. No momento, não há ação de redes.
Segue parecer da equipe da CETEL no REQ000146585048 para verificação:

===========
13/10/2026 11:52:20 ; (P908440)
À
TELEDATA/CETEL/REDES,
- Informo que o host 10.188.6.225 não se encontra visível na rede. Favor verificar a configuração da VM. No momento, não há ação de redes.
Att,
Magnus dos Santos Silva
Analista de Datacenter - Redes
TELEDATA/CETEL/REDES
===========


Solicitar Armazenamento
----------------------------------------------------
Solicitante: c052958
Centro de Custo: CESOB
Opção NAS: Sistema
Nome Sistema: siccv
Ambiente: TQS
VM da Esteira
Plataforma Armazenamento: OPEN
Tipo de Disco: NAS
Compartilhamento NOVO
Volumetria: 50GB
Custo Mensal: R$ 9,23
Custo Anual: R$ 110,67
----------------------------------------------------
Ponto de Montagem: /siccv
Tipo de Compartilhamento: NFS
Vai se Comunicar com Mainframe: NÃO

---------------------------------
HOSTS ESTEIRA
---------------------------------
Módulo: siccv-batch
Ip Real: 10.116.202.23
Ip de Backup: 10.188.6.225
Hostname: caddeapllx2821.agil.nprd.caixa.gov.br
----------------------------------------------------

Histórico de Informações de Trabalho da Ordem de Trabalho
ID da Ordem de Trabalho	 WO0000081801601
Criado em	 06/10/2026 10:40:11
Criado por	 P981778
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezado(a),

Realizada a configuração do compartilhamento NFS na esteira do SICCV-batch (TQS):

Ajustado o grupo de variáveis SICCV-batch-tqs, que estava apontando para o export Isilon de DES. Agora aponta para o compartilhamento criado nesta WO:
Endpoint: hypernprd12.ad.caixa:/fs_siccv
Ponto de montagem: /SICCV
A release foi reexecutada e a automação processou a configuração corretamente.

A montagem, porém, não foi concluída por falha de comunicação de rede, fora do escopo desta equipe. A interface de backup do servidor caddeapllx2821 (ens224 – 10.188.6.225) não recebe resposta ARP de nenhum IP do storage na rede 10.188.0.0/19.

Ação necessária: abrir requisição para a CETEL solicitando a verificação do portgroup/VLAN da interface de backup do servidor. Segue abaixo o texto sugerido para a abertura.

Depois que a CETEL corrigir, basta reexecutar a release do SICCV-batch em TQS. Nenhum ajuste adicional na esteira é necessário.

Encerramos esta WO.

Atte.
Esteira DevOps DES/TQS NPRD

Texto sugerido para a nova REQ (CETEL)

Assunto: Servidor caddeapllx2821 sem comunicação na rede de backup (10.188.0.0/19)

A VM caddeapllx2821.agil.nprd.caixa.gov.br (SICCV-batch, TQS) está sem comunicação de camada 2 na rede de backup.

Interface de backup: ens224, IP 10.188.6.225/19, MAC 00:50:56:82:a5:1d, estado UP
Destino: storage hypernprd12.ad.caixa (10.188.0.11/.13/.14/.16/.17/.18), mesma sub-rede, sem gateway

Evidências:

$ ip route get 10.188.0.14
10.188.0.14 dev ens224 src 10.188.6.225

$ ip neigh show dev ens224
10.188.0.14 FAILED
10.188.0.18 FAILED
10.188.0.16 FAILED
10.188.0.13 FAILED
10.188.0.11 FAILED
10.188.0.17 FAILED

$ arping -c3 -I ens224 10.188.0.14
Enviadas 3 sondas (3 broadcast(s))
Recebida(s) 0 resposta(s)

Solicitação: verificar se a vNIC ens224 está no portgroup/VLAN correto da rede de backup e se a VLAN está presente no host ESXi onde a VM está alocada.

Impacto: impede a montagem do NFS hypernprd12.ad.caixa:/fs_siccv (WO0000081801601) no servidor.


Thiago Silva
Analista
CTIS / CESTI Esteira DEVOPS DES TQS NPRD
ID da Ordem de Trabalho	 WO0000081801601
Criado em	 06/10/2026 09:22:09
Criado por	 P768728
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezado(a),

Informamos que sua solicitação foi recebida.

Nosso SLA para atendimento é de até 24h úteis, analisaremos a solicitação para nos certificarmos que o atendimento está dentro do escopo de atuação da nossa equipe.

Caso seja identificado que o atendimento não corresponde ao nosso escopo, a solicitação será redirecionada à equipe responsável.

Novas informações e atualizações serão registradas diretamente nesta WO.

Atte.

Esteira Devops DES TQS NPRD
ID da Ordem de Trabalho	 WO0000081801601
Criado em	 05/10/2026 12:34:07
Criado por	 P722542
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezados,

Realizada a criação do NFS conforme solicitado.

Seguem informações para montagem:
FQDN: hypernprd12.ad.caixa - 10.188.0.0/16
PATH: /fs_siccv

Segue evidência:

 ID                     : 370
 Name                   : fs_siccv
 Capacity               : 50.000GB
 Description            : WO0000081801601
 Available Capacity     : 49.999GB
 Used Capacity Ratio(%) : 0.00

 Share Permission ID  Access Name   Access Type  Share Name
 -------------------  ------------  -----------  ----------
 7189                 10.188.6.225  Read Write   /fs_siccv

At.te,
Vinicius Pires
SONDA/CESTI53/ARMAZENAMENTO
ID da Ordem de Trabalho	 WO0000081801601
Criado em	 05/10/2026 12:14:09
Criado por	 P583155
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezado(a)
Acusamos o recebimento desta WO.
- Informamos que sua solicitação entrou em fila de atendimento.
- Esta demanda será atendida em breve
- Informações futuras serão adicionadas a esta WO.

Att
CESTI53
ID da Ordem de Trabalho	 WO0000081801601
Criado em	 05/10/2026 11:54:01
Criado por	 P776093
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Demanda inicial sem viés de falha, erro, degradação ou esgotamento de infraestrutura, serviço, máquina, armazenamento, rotina ou situação que não esteja na iminência de tornar-se incidente. Previsto atendimento em até 72 horas. [CENTRAL-SID]
ID da Ordem de Trabalho	 WO0000081801601
Criado em	 05/10/2026 07:06:31
Criado por	 Remedy Application Service
Origem de Comunicação	 E-mail
Exibir Acesso	 Interno
Notas	 Este ticket foi criado a partir do sistema de solicitação de serviço.
Impresso por P585600 em Terça-feira, 13/10/2026 13:41:38







Solicitamos a criação de NFS compartilhado para o ambiente TQS para o SICCV Batch e efetuar a sua configuração na library do SICCV Batch de TQS tendo em vista que o NFS configurado trata-se do ambiente de DES

https://devops.caixa/projetos/Caixa/_library?itemType=VariableGroups&view=VariableGroupView&variableGroupId=19518&path=SICCV-batch-tqs




Histórico de Informações de Trabalho da Ordem de Trabalho
ID da Ordem de Trabalho	 WO0000081788379
Criado em	 02/10/2026 15:54:57
Criado por	 P585600
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 À CAIXA

Prezados

Analisada a demanda. A library SICCV-batch-tqs aponta para o export NFS /ifs/CADSVISISD4/SERVIDORES/CEPTISP/SICCV, que pertence ao ambiente de DES. Verificado no storage que não existe export NFS de TQS para o SICCV. Verificado também que o servidor de TQS (caddeapllx2821 – 10.116.202.23) não possui interface na rede de backup/storage, por onde é feito o acesso ao NFS.

A criação de novo compartilhamento NFS é atribuição da equipe de Armazenamento e não é atendida por esta fila. Deve ser solicitada pelo próprio demandante via InfraFácil,

Orientações de preenchimento na Wiki: https://wikifacil.caixa/article/armazenamento/nas

Atenção: não utilizar a opção "Inclusão de IP" no compartilhamento existente, pois isso daria ao TQS acesso ao NFS de DES.

Após o atendimento da requisição de Armazenamento, a mesma req vem para a Esteiras DES/TQS informando o path do novo export, para atualização da variável NFS_ENDPOINT_ISILON na library SICCV-batch-tqs e montagem no servidor.



Atenciosamente,

Jessé Mouta Pereira Batista
Analista
CTIS / CESTI Esteira DEVOPS DES TQS NPRD
ID da Ordem de Trabalho	 WO0000081788379
Criado em	 02/10/2026 12:26:03
Criado por	 P730708
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Demanda inicial sem viés de falha, erro, degradação ou
esgotamento de infraestrutura, serviço, máquina, armazenamento,
rotina ou situação que não esteja na iminência de tornar-se
incidente. Previsto atendimento em até 24 horas úteis.

[CENTRAL-SID]
ID da Ordem de Trabalho	 WO0000081788379
Criado em	 02/10/2026 11:58:52
Criado por	 P558217
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezado(a),



Informamos que sua solicitação foi recebida.  



Nosso SLA para atendimento é de até 24h úteis, analisaremos a solicitação para nos certificarmos que o atendimento está dentro do escopo de atuação da nossa equipe.



Caso seja identificado que o atendimento não corresponde ao nosso escopo, a solicitação será redirecionada à equipe responsável.



Novas informações e atualizações serão registradas diretamente nesta WO.



Atte.



Esteira Devops DES TQS NPRD
ID da Ordem de Trabalho	 WO0000081788379
Criado em	 02/10/2026 11:50:36
Criado por	 Remedy Application Service
Origem de Comunicação	 E-mail
Exibir Acesso	 Interno
Notas	 Este ticket foi criado a partir do sistema de solicitação de serviço.
Impresso por P585600 em Terça-feira, 13/10/2026 13:42:13



