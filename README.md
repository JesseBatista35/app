Pessoal, obrigado pelos retornos!

Concluímos a análise do lado da esteira. Segue o que verificamos e o que fica com cada time a partir de agora.

🔎 O que foi analisado pela esteira
• SIGSJ-boleto (TQS): implantado e validado. Contexto /boletoService no ar, sem erros de deploy.
• SIGSJ-internet (TQS): implantado. Contexto /sigsj_internet no ar e EAR implantado.
• SIGSJ-intranet (TQS): implantado e respondendo em /sigsj_intranet. Validamos o pacote completo (EAR, WARs e libs) e confirmamos que o intranet não utiliza datasource nem Oracle, como o Marcio informou.
• Proxy: o proxytqs.caixa não existe no DNS. O JVM_PROXY_HOST pode permanecer como proxydes.caixa.
• Log4j: as três aplicações leem a configuração de log de um XML externo em /log_jboss/config-log4j/, que existia nos servidores legados e não existe nas VMs novas.

📌 Próximos passos – fábrica
1. SIGSJ-intranet-config (master): remover o bloco do datasource SIGSJ04 do jboss/standalone-full-ha.xml e a linha do ojdbc8 do jboss/jboss-deployments. Com isso, o intranet deixa de depender de variáveis de banco.
2. SIGSJ-internet: preencher o SIGSJ04_PASSWORD (TQS) com a senha real do usuário do banco, marcada como secreta. No JBoss 7.4 o datasource usa usuário e senha direto, sem o security-domain do JBoss 5.
3. Log4j: nos enviar os XMLs dos servidores legados (sigsj_intranet.xml, sigsj_ws_boleto.xml e o equivalente do internet).
4. SIGSJ-internet: quando o SIROT for embutido no build, nos avisar para removermos o jar externo e o alias JNDI.
5. Intranet: confirmar o valor correto da variável _ENV.URL_STATICS (hoje está www.teste.com).

📌 Próximos passos – esteira
1. Após os ajustes acima, rodar novamente as releases de TQS do intranet e do internet e validar a subida.
2. Com os XMLs do log4j em mãos, configurar nos repositórios de config a criação automática desses arquivos nas VMs a cada deploy.
3. Seguir com as solicitações das URLs customizadas (certificado, VIP, balanceamento e DNS) para o intranet, o internet e o boleto.

Nossa parte da análise está concluída. Agora aguardamos os ajustes de vocês para seguirmos com as releases. Qualquer dúvida, fico à disposição!
