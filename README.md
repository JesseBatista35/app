Prezados,

Realizada a inclusão dos certificados DigiCert Global Root G2 e DigiCert Global G2 TLS RSA SHA256 2020 CA1 no truststore do SISEI, ambiente de Desenvolvimento (DES), para as aplicações SISEI-mgi e SISEI-mgi-sip.

Ações executadas:
1. Os dois certificados foram acrescentados ao bundle sisei_nprd_082026.crt, mantendo todos os 20 certificados existentes (total de 22). O arquivo foi atualizado no Secure Files da Library e referenciado na task "Download secure file" das releases SISEI-mgi e SISEI-mgi-sip.
2. Executadas as releases de DES de SISEI-mgi e SISEI-mgi-sip. A secret sisei-nprd-082026 (namespace sisei-des) foi atualizada com o novo bundle.
3. Na validação, verificou-se que o PHP das aplicações (/etc/php.d/99-custom.ini, parâmetros curl.cainfo e openssl.cafile) lê o arquivo /opt/app-root/src/sisei_nprd.crt, originado da secret sisei-nprd, e não o sisei_nprd_082026.crt. O conteúdo das duas secrets era idêntico antes da alteração.
4. Feito backup da secret sisei-nprd. A secret foi atualizada com o mesmo bundle de 22 certificados, e os deployments sisei-mgi-des e sisei-mgi-sip-des foram reiniciados.
5. Validado nos novos pods que o arquivo utilizado pelo PHP (sisei_nprd.crt) contém os 22 certificados, incluindo os dois certificados DigiCert solicitados.

Observações:
- Em TQS, a task "Download secure file" também passou a referenciar o arquivo atualizado, pois o secure file é compartilhado entre os stages. Não foi executada release em TQS. A alteração terá efeito somente na próxima release desse ambiente.
- Recomendação à equipe do SISEI: ajustar na origem a configuração do 99-custom.ini (ConfigMaps config-custom-sisei-mgi e config-custom-sisei-mgi-sip, recriados pela release) para apontar para /opt/app-root/src/sisei_nprd_082026.crt, arquivo gerenciado pela esteira. Hoje o PHP utiliza o sisei_nprd.crt, que vem de uma secret mantida manualmente, fora da release.
- O bundle contém certificados duplicados e dois certificados de servidor expirados em 11/08/2026 (cas.staging.iti.br e assinatura-api.staging.iti.br). Isso não afeta o funcionamento, mas recomenda-se uma revisão do arquivo pela equipe responsável.

Solicitamos que a equipe valide a comunicação da aplicação com o serviço que utiliza certificado DigiCert. Em caso de nova ocorrência, favor reabrir a demanda.
