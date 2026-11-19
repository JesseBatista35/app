[root@sspdeapllx0039 lib]# B=/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet
[root@sspdeapllx0039 lib]# grep -rniE "8111|farm|connector.*host|siper.*host|10\.116\.89\." $B/deploy $B/deployapp $B/tmp /apl/sigsj 2>/dev/null | grep -viE "password|senha|\.so" | head -20
Binary file /opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/tmp/a382g2o-c29mdx-mwb397on-1-mwb39p2q-9w/sigsj_internet-war-2.73.0.10.war/WEB-INF/classes/br/gov/caixa/sigsj/internet/mb/CarregamentoLoteIdAgrupadorMB.class matches
/apl/sigsj/properties/b2b.properties:2:intranet.clote.url.lista = http://10.116.89.232:5033/GSJ_LOTE_LISTA
/apl/sigsj/properties/b2b.properties:4:intranet.clote.url.download.v2 = http://10.116.89.232:5033/GSJ_LOTE_DOWNLOAD_v2
/apl/sigsj/properties/b2b.properties:6:intranet.clote.url.upload = http://10.116.89.232:5033/GSJ_LOTE_UPLOAD
/apl/sigsj/properties/b2b.properties:7:intranet.clote.url.upload.v2 = http://10.116.89.232:5033/GSJ_LOTE_UPLOAD_v2?LOTE_FILENAME=
/apl/sigsj/properties/b2b.properties:8:intranet.clote.url.download = http://10.116.89.232:5033/GSJ_LOTE_DOWNLOAD
/apl/sigsj/properties/b2b.properties:12:#intranet.clote.url.upload = http://10.116.89.232:5033/GSJ_LOTE_UPLOAD
/apl/sigsj/properties/b2b.properties:13:#intranet.clote.url.lista = http://10.116.89.232:5033/GSJ_LOTE_LISTA
/apl/sigsj/properties/b2b.properties:14:#intranet.clote.url.download = http://10.116.89.232:5033/GSJ_LOTE_DOWNLOAD
/apl/sigsj/properties/b2b.properties:19:internet.clote.url.upload = http://10.116.89.232:5033/GSJ_LOTE_UPLOAD
/apl/sigsj/properties/b2b.properties:20:internet.clote.url.upload.v2 = http://10.116.89.232:5033/GSJ_LOTE_UPLOAD_v2?LOTE_FILENAME=
/apl/sigsj/properties/b2b.properties:23:internet.clote.url.download.v2 = http://10.116.89.232:5033/GSJ_LOTE_DOWNLOAD_v2
Binary file /apl/sigsj/DES.GSJ.MZ.BBM1.WP196.D261005.S000010.N1.txt matches
/apl/sigsj/tmpupload/temp.CRA00032603_26MAR2026 v1.txt:1820:0200  0000000000000     00000000                                                                                                                                                                                                                                                                              CRA0003030400420000015470669090000052665448111000000000071369000000000071369002026032711542475202603270000                                                     N0304N1402NSN                                                                                                                                                                                                                                                                      
/apl/sigsj/tmpupload/temp.CRA00032603_26MAR2026 v1.txt:3858:0200  0000000000000     00000000                                                                                                                                                                                                                                                                              CRA0003050100420000015328111090000052115439721000000000037578000000000037578002026032711542475202603270000                                                     N0501N1402NSN                                                                                                                                                                                                                                                                      
/apl/sigsj/tmpupload/temp.CRA00032603_26MAR2026 v1.txt:4307:0200  0000000000000     00000000                                                                                                                                                                                                                                                                              CRA0003055200420000015138256090000052254811107000000000071009000000000071009002026032711542475202603270000                                                     N0552N1402NSN                                                                                                                                                                                                                                                                      
/apl/sigsj/tmpupload/temp.CRA00032603_26MAR2026 v1.txt:4308:0200  0000000000000     00000000                                                                                                                                                                                                                                                                              CRA0003055200420000015140331090000052334811111000000000035159000000000035159002026032711542475202603270000                                                     N0552N1402NSN                                                                                                                                                                                                                                                                      
/apl/sigsj/tmpupload/temp.CRA00032603_26MAR2026 v1.txt:4309:0200  0000000000000     00000000                                                                                                                                                                                                                                                                              CRA0003055200420000015141516090000052514811128000000000003222000000000003222002026032711542475202603270000                                                     N0552N1402NSN                                                                                                                                                                                                                                                                      
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#


[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]# timeout 5 bash -c "cat < /dev/null > /dev/tcp/10.116.89.101/8111" && echo "ABRIU 10.116.89.101:8111" || echo "SEM CONEXAO 10.116.89.101:8111"
SEM CONEXAO 10.116.89.101:8111
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#


