Pessoal, obrigado pelos retornos! Consolidando os próximos passos:

📌 Próximos passos – fábrica

1. SIGSJ-intranet – remover o datasource
Confirmei no pacote do intranet (EAR, WARs e libs) que não há nenhuma referência a datasource ou Oracle. No SIGSJ-intranet-config (master), podem remover:
• do jboss/standalone-full-ha.xml, o bloco do datasource SIGSJ04;
• do jboss/jboss-deployments, a linha do ojdbc8.
Com isso o intranet não depende mais de variáveis de banco.

2. SIGSJ-internet – senha do SIGSJ04 em TQS
No JBoss 7.4 da esteira, o datasource usa usuário e senha direto (não usa security-domain como no JBoss 5). O SIGSJ04_PASSWORD precisa ter a senha real do usuário de TQS, marcada como secreta. Conseguem passar ou confirmar com o DBA?

3. Log4j – arquivos XML do legado
As aplicações leem a configuração de log de um XML externo em /log_jboss/config-log4j/ (sigsj_intranet.xml, sigsj_ws_boleto.xml e o equivalente do internet), que não existe nas VMs novas. Precisamos que nos enviem esses XMLs dos servidores legados. Com eles, ajustamos a configuração para que a esteira crie esses arquivos nas VMs a cada deploy.

4. SIGSJ-internet – SIROT
Quando o SIROT for embutido no build (como no boleto e no intranet), nos avisem para removermos o jar externo e o alias JNDI.

5. _ENV.URL_STATICS (intranet)
Hoje está com o valor www.teste.com. Podem confirmar o valor correto?

📌 Próximos passos – esteira

1. Rodar novamente as releases de TQS do intranet e do internet após os ajustes acima e validar a subida.
2. Log4j: com os XMLs em mãos, preparar a configuração nos repositórios de config para criação automática dos arquivos nas VMs (boleto, intranet e internet).
3. URLs customizadas: seguir com as solicitações (certificado, VIP, balanceamento e DNS) para o intranet, o internet e também o boleto, conforme confirmado.
4. Proxy: o JVM_PROXY_HOST pode ficar como proxydes.caixa, não existe proxytqs.caixa no DNS.

Qualquer dúvida, fico à disposição!
