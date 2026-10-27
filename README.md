Ambiente: SIDMF – DES – sspdeaplux0100 (SJSAS 8.2 EE, domínio das01, target dsv01)

Solicitação: undeploy da aplicação sidmf no target dsv01.

Análise realizada:

O DAS (das01) estava travado na inicialização (“starting”, porta 14848 fechada) após uma tentativa de start às 16:18, com erro SEC8001 ao inicializar o SunPKCS11. O processo travado foi finalizado e o DAS subiu normalmente (“Application server startup complete”).
Com o DAS no ar, os comandos asadmin continuaram falhando com java.security.cert.CertificateExpiredException: NotAfter: Sun Dec 07 2025.
Causa raiz: o certificado administrativo s1as do domínio das01, autoassinado e gerado em 07/12/2015 com validade de 10 anos, venceu em 07/12/2025. Por isso o asadmin não consegue estabelecer a conexão SSL com o DAS, e o undeploy é bloqueado.
O DAS também não alcança as instâncias dsv01 a dsv11 (EEADM0302).

Situação atual: DAS das01 em execução. Os arquivos NSS do domínio permanecem como estavam, com backup em ~sjsas8/bkp_nss_20261027/. O undeploy não foi realizado.

Pendência / encaminhamento: regerar o certificado s1as no NSS do domínio (/opt/SUNWas8/domains/das01/config) com o certutil, remover o ~sjsas8/.asadmintruststore, reiniciar o DAS e sincronizar os node agents. O procedimento exige a master password do domínio das01, que não está disponível para a equipe CESTI. A demanda deve ser direcionada à equipe responsável pela administração do SJSAS8/SIGOV que detém essa senha. Concluída a troca do certificado, o undeploy pode ser executado normalmente.
