Sandra, o healthcheck já está habilitado e funcionando: em DES o pod sihdg-jboss8-des-116 responde 200 em /sihdg-api/health/ready, com a mesma aplicação e as mesmas probes. Em TQS (pod sihdg-jboss8-tqs-37-6llp9, imagem 3.18.0.1) as probes dão 404/503 porque o sihdg-api.war não inicializa: SecurityConfig e CacheConfig falham com Connect timed out em 10.116.29.201:31153, e o OKD reinicia o container a cada falha de liveness. A rota existe no projeto. A causa é a conectividade com o banco, que está em tratamento com a Infra/Plataforma OKD (egress do namespace sihdg-tqs, CRQ000001499711). Pedimos manter a WO aberta até a conectividade ser corrigida.


Fábio, boa tarde. Pedimos a reabertura da WO0000081857473. O fechamento indicou que a rota de healthcheck não existe na aplicação, mas a análise mostra que a causa é outra.

Evidências

Em DES, o pod sihdg-jboss8-des-116-mq4ct responde 200 em /sihdg-api/health/ready. A rota existe no projeto e as probes de readiness e liveness já estão habilitadas, com o mesmo path em TQS.
Em TQS, no pod sihdg-jboss8-tqs-37-6llp9 (imagem 3.18.0.1), o log mostra o sihdg-3.18.0.1.ear finalizado com erros (started (with errors)). Os componentes SecurityConfig e CacheConfig não sobem por Connect timed out em 10.116.29.201:31153.
Com o sihdg-api.war fora do ar, /sihdg-api/ e o healthcheck do servidor (:9990/health/ready) respondem 503, e /sihdg-api/health/ready responde 404.
A liveness probe falha, o OKD mata o container e ele reinicia em loop (4 restarts em 8 minutos).

Causa
O 404 do healthcheck é consequência da aplicação não conseguir conexão com o banco. A falha de conectividade está em tratamento com a Infra/Plataforma OKD: o tráfego dos pods do namespace sihdg-tqs não sai com o egress IP 10.116.221.46, que é o IP liberado na regra de firewall da CRQ000001499711. A Redes validou por captura que a regra funciona quando o tráfego sai com esse IP.

Pedido
Manter a WO aberta, sem nova tentativa de deploy, até a conectividade com o banco ser corrigida. Quando houver retorno da Infra, o teste será repetido e a WO atualizada.
