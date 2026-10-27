Causa raiz: A aplicação sispi-med-gestao-des (namespace sispi-des, cluster pixnprd4) é exposta pelo Service Mesh (Gateway/VirtualService), cuja rota pública fica no namespace istio-system. Havia também uma Route criada manualmente no namespace sispi-des com o mesmo host. Por ser mais antiga, ela reivindicava o host, e a rota correta do istio-system ficava rejeitada (HostAlreadyClaimed). O tráfego seguia direto para o pod, fora da malha, e era bloqueado pela NetworkPolicy do Service Mesh. Com isso, retornava HTTP 503, apesar de a aplicação estar no ar e saudável.

Correção: Removida a Route manual do namespace sispi-des (backup preservado). A rota do istio-system passou a Admitted, no mesmo padrão das demais aplicações do SISPI. Um novo deploy foi executado e a Route manual não foi recriada pela release.

Validação: https://sispi-med-gestao-des.apps.pixnprd4.caixa/q/health/ready retorna HTTP 200. O acesso à raiz da URL sem token retorna 403, que é comportamento esperado da aplicação (validação de token habilitada). A validação funcional deve ser feita pela equipe em um endpoint da API, com token válido.

Orientação: Para sistemas no Service Mesh, não criar Routes diretamente no namespace da aplicação. A exposição deve ser feita somente via Gateway/VirtualService.

Observação: sispi-med-auditoria-des

Durante a análise foi identificado o mesmo conflito de rota no sispi-med-auditoria-des: uma Route manual no namespace sispi-des impedia a admissão da rota do istio-system. O mesmo ajuste foi aplicado, e a rota do Service Mesh agora está admitida.

Porém, após o novo deploy (pod sispi-med-auditoria-des-31), a aplicação apresenta outro problema, sem relação com a rota:

Readiness DOWN: o health check “Database connections health check” falha com Acquisition timeout while waiting for new connection. A aplicação não consegue obter conexão com o banco de dados.
No startup: o Hibernate registra Unable to obtain isolated JDBC connection e Could not retrieve the database version.
Liveness: falhas com HTTP 500.
Agente APM: o Elastic APM falha ao iniciar (Could not access Unsafe class: sun.misc.Unsafe.defineClass), indicando incompatibilidade entre a versão do agente e a versão do Java da imagem. Não impede a subida da aplicação.

Solicitamos que a equipe responsável abra uma nova REQ para tratar a conectividade do sispi-med-auditoria-des com o banco de dados. É necessário verificar, por parte da aplicação, a URL do datasource, as credenciais e a liberação de firewall entre o namespace sispi-des e o banco. Também deve ser avaliada a atualização ou remoção do agente Elastic APM.
