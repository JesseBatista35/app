Pessoal, boa tarde!

O SICOW-conres-okd (DES) foi regularizado. A aplicação sobe sem erros (contexto /sicow-conres) e o acesso pelo portal carrega o módulo CONRES normalmente.

Causas e ajustes realizados:

standalone.conf: removido um $ indevido na linha do JBOSS_MODULES_SYSTEM_PKGS, que gerava o erro =org.jboss.byteman: command not found.
standalone-okd.xml: o arquivo era o template padrão do JBoss, sem a configuração do SICOW. Foi refeito no padrão do SICOW-penhor-okd, com datasource sicow-ds, vault, security domain do SIUSR via SIUSR_END_POINT, system-properties (URL do portal, URLs dos módulos, SICLI e SIISO) e log também no console.
Falha no deploy do .war (código): o endpoint OcorrenciaConresWS expunha o método público setSistemaDao(SistemaWSDAO) como operação SOAP, o que causava IllegalAnnotationsException (o JAXB não consegue serializar o EntityManager). O setter foi anotado com @WebMethod(exclude = true).
Vault: incluídos na release o download do vault-sicow-des.keystore e a task VAULT_OKD, e criado o configmap vault-sicow-conres-okd com o VAULT.dat, como no Penhor.
Library SICOW-CONRES-OKD-DES: corrigidas MAIL_EXPRESSO_HOST, SICOWPORTALURL e JKS_FILE, incluídas as URLs dos módulos (SICOW*_WAR) e vinculado o grupo SICOW-BT-VAULT-SECRET-DES.

Os ajustes de código e de módulos (OcorrenciaConresWS.java, jboss-modules, cli-offline.sh) estão na branch Cesti-teste. É necessário que o desenvolvimento faça o merge (PR) na branch oficial e gere nova tag.

Pendência (time SICOW/DBA): o usuário scowdb01 continua com falha de autenticação no banco cowdb001 (10.116.92.41:5116), assim como no portal e no Penhor. Até a senha do vault (VAULT::SICOW::SCOWDB01::1) ser corrigida, as telas que consultam o banco retornam erro ou vêm vazias.
