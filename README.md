[p585600@sspdeapllx0039 ~]$
[p585600@sspdeapllx0039 ~]$
[p585600@sspdeapllx0039 ~]$
[p585600@sspdeapllx0039 ~]$ for f in b2b.properties config.properties release.properties; do echo "==== $f ===="; sed -E 's#(senha|password|pwd|secret)[[:space:]]*=.*#\1=***#I' /apl/sigsj/properties/$f; done
==== b2b.properties ====
# Parametros especificos para o consumo do B2B no canal Intranet #
intranet.clote.url.lista = http://10.116.89.232:5033/GSJ_LOTE_LISTA
#intranet.clote.url.lista = https://sigsj.b2b.des.caixa.gov.br/GSJ_LOTE_LISTA
intranet.clote.url.download.v2 = http://10.116.89.232:5033/GSJ_LOTE_DOWNLOAD_v2
#intranet.clote.url.download.v2 = http://sigsj.b2b.des.corerj.caixa/GSJ_LOTE_DOWNLOAD_v2
intranet.clote.url.upload = http://10.116.89.232:5033/GSJ_LOTE_UPLOAD
intranet.clote.url.upload.v2 = http://10.116.89.232:5033/GSJ_LOTE_UPLOAD_v2?LOTE_FILENAME=
intranet.clote.url.download = http://10.116.89.232:5033/GSJ_LOTE_DOWNLOAD



#intranet.clote.url.upload = http://10.116.89.232:5033/GSJ_LOTE_UPLOAD
#intranet.clote.url.lista = http://10.116.89.232:5033/GSJ_LOTE_LISTA
#intranet.clote.url.download = http://10.116.89.232:5033/GSJ_LOTE_DOWNLOAD


#Parametros de conex�o com p B2B para a funcionalidade Carregamento Lote, para o canal Internet

internet.clote.url.upload = http://10.116.89.232:5033/GSJ_LOTE_UPLOAD
internet.clote.url.upload.v2 = http://10.116.89.232:5033/GSJ_LOTE_UPLOAD_v2?LOTE_FILENAME=
internet.clote.url.lista = https://sigsj.b2b.des.caixa.gov.br/GSJ_LOTE_LISTA
internet.clote.url.download = https://sigsj.b2b.des.caixa.gov.br/GSJ_LOTE_DOWNLOAD
internet.clote.url.download.v2 = http://10.116.89.232:5033/GSJ_LOTE_DOWNLOAD_v2


timeout.b2b = 90

==== config.properties ====
sigsj.release = 1.13.0
#sigsj.convivencia.url = http://sigsj-convivencia-des-esteiras.nprd2.caixa/convivencia/v1
sigsj.convivencia.url = https://sigsj-convivencia-des.apps.nprd.caixa/convivencia/v1
sigsj.ambiente = DES
simtr.url = http://simtr-api-intranet-des.apps.nprd.caixa/

==== release.properties ====
sigsj.release = 1.13.0

[p585600@sspdeapllx0039 ~]$
[p585600@sspdeapllx0039 ~]$
[p585600@sspdeapllx0039 ~]$
