Livia, os valores de proxy de DES/TQS não valem para PRD. O HTTP_PROXY/HTTPS_PROXY de DES aponta para o proxy de DES, e o NO_PROXY tem o IP do banco de DES.

Na Mudança, solicitem a inclusão das variáveis _ENV.HTTP_PROXY, _ENV.HTTPS_PROXY e _ENV.NO_PROXY na library de PRD (SIPGC-API-SEGURANCA-PRD), informando que os valores devem ser os de PRD: o proxy de produção, e no NO_PROXY o IP do SQL Server de PRD no lugar do de DES.

Eu não tenho acesso a PRD, então não consigo conferir nem informar o valor do proxy de lá. Vale confirmar o endereço com a equipe de PRD ou de Infra e deixar na Mudança.

Aproveitem para conferir se as libraries do vault de PRD (BT-VAULT e BT-VAULT-SECRET) já foram criadas via REQ TE191, e se a regra de IP de origem do client BeyondTrust de PRD está liberada. Em TQS o deploy ficou travado por isso.
