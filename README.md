
-sh-4.2$
-sh-4.2$ oc get instrumentation -n sispi-des -o yaml | grep -E 'creationTimestamp|resourceVersion|image:|generation'
      instrumentation.opentelemetry.io/default-auto-instrumentation-apache-httpd-image: ghcr.io/open-telemetry/opentelemetry-operator/autoinstrumentation-apache-httpd:1.0.4
      instrumentation.opentelemetry.io/default-auto-instrumentation-dotnet-image: ghcr.io/open-telemetry/opentelemetry-operator/autoinstrumentation-dotnet:1.2.0
      instrumentation.opentelemetry.io/default-auto-instrumentation-go-image: ghcr.io/open-telemetry/opentelemetry-go-instrumentation/autoinstrumentation-go:v0.22.1
      instrumentation.opentelemetry.io/default-auto-instrumentation-java-image: ghcr.io/open-telemetry/opentelemetry-operator/autoinstrumentation-java:1.33.6
      instrumentation.opentelemetry.io/default-auto-instrumentation-nginx-image: ghcr.io/open-telemetry/opentelemetry-operator/autoinstrumentation-apache-httpd:1.0.4
      instrumentation.opentelemetry.io/default-auto-instrumentation-nodejs-image: ghcr.io/open-telemetry/opentelemetry-operator/autoinstrumentation-nodejs:0.63.0
      instrumentation.opentelemetry.io/default-auto-instrumentation-python-image: ghcr.io/open-telemetry/opentelemetry-operator/autoinstrumentation-python:0.58b0
    creationTimestamp: 2024-12-20T18:56:28Z
    generation: 27
            f:instrumentation.opentelemetry.io/default-auto-instrumentation-java-image: {}
            f:image: {}
    resourceVersion: "1382498377"
      image: ghcr.io/open-telemetry/opentelemetry-operator/autoinstrumentation-apache-httpd:1.0.4
      image: ghcr.io/open-telemetry/opentelemetry-operator/autoinstrumentation-dotnet:1.2.0
      image: ghcr.io/open-telemetry/opentelemetry-go-instrumentation/autoinstrumentation-go:v0.17.0-alpha
      image: default-route-openshift-image-registry.apps.produtos4.caixa/openshift/autoinstrumentation-java:2.12.0
      image: ghcr.io/open-telemetry/opentelemetry-operator/autoinstrumentation-apache-httpd:1.0.4
      image: ghcr.io/open-telemetry/opentelemetry-operator/autoinstrumentation-nodejs:0.53.0
      image: ghcr.io/open-telemetry/opentelemetry-operator/autoinstrumentation-python:0.48b0
  resourceVersion: ""
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pod $POD -n sispi-des -o jsonpath='{range .spec.initContainers[*]}{.name}{"  "}{.image}{"\n"}{end}'
secrets-agent-sidecar  default-route-openshift-image-registry.apps.produtos4.caixa/openshift/secrets-agent:v23.3.2
secrets-check  default-route-openshift-image-registry.apps.produtos4.caixa/openshift/ubi:9.3-1552
dynatrace-operator  public.ecr.aws/dynatrace/dynatrace-operator:v1.11.0
opentelemetry-auto-instrumentation-java  default-route-openshift-image-registry.apps.produtos4.caixa/openshift/autoinstrumentation-java:2.12.0
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc adm top pod $POD -n sispi-des --containers
POD                                        NAME                             CPU(cores)   MEMORY(bytes)
sispi-qrcode-api-validador-des-297-6jjtp   sispi-qrcode-api-validador-des   19m          0Mi
sispi-qrcode-api-validador-des-297-6jjtp   POD                              0m           0Mi
sispi-qrcode-api-validador-des-297-6jjtp   istio-proxy                      3m           165Mi
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc logs sispi-dict-batch-polling-des-735-rkrxh -n sispi-des -c sispi-dict-batch-polling-des --previous | tail -20
2026-10-27 12:01:00,130 INFO  [br.gov.caixa.spi.dict.v2.ejb.RelatoInfracaoEjb] (EJB default - 71) [CORRELATION-ID:ea5c68f0-3bd0-4f29-9181-1ea514add196] [BATCH] [RELATOSINFRACAO] [ATUALIZACAO] Pooling buscarRelatosDeInfracao Finalizado em 57ms
2026-10-27 12:01:00,171 INFO  [br.gov.caixa.spi.dict.ejb.EventoDevolucaoInternaEjb] (EJB default - 98) [CORRELATION-ID:0febb01d-1b4b-4a39-b7be-6307bcbbd704] [BATCH] [EVENTO-DEVOLUCAO-ABERTAS-INTERNAS] Nenhuma devolu??o INTERNA com status OPEN encontrada
2026-10-27 12:01:00,171 INFO  [br.gov.caixa.spi.dict.scheduler.DevolucoesInternas] (EJB default - 98) [CORRELATION-ID:0febb01d-1b4b-4a39-b7be-6307bcbbd704] [DEVOLUCOES_MED][BATCH][ABERTAS_INTERNAS] Finaliza processo para resolver as devolucoes abertas internas
2026-10-27 12:01:00,183 INFO  [br.gov.caixa.spi.dict.scheduler.RelatosInfracaoEjb] (EJB default - 71) [CORRELATION-ID:ea5c68f0-3bd0-4f29-9181-1ea514add196] [POLLING][RELATOSINFRACAO][BATCH][ATUALIZACAO][FINALIZADO] Polling dos relatos de infra??o. Busca dos ?ltimos relatos atualizados.. Duracao:182 ms. Pr?xima data/hora base 2026-10-27T15:01:00.057 (UTC)
2026-10-27 12:01:00,198 INFO  [br.gov.caixa.spi.dict.ejb.recon.ReconciliacaoEventosEjb] (EJB default - 87) [CORRELATION-ID:5941b738-0653-4ee8-aa00-0f472f1ccd13] [POLLING][RECONCILIACAO_EVENTOS][BATCH][CPF] Demorou 135 ms para atualizar os eventos da reconciliacao. Iteracao 1 Data base 2026-10-27T11:49:00.501
2026-10-27 12:01:00,202 INFO  [br.gov.caixa.spi.dict.ejb.recon.ReconciliacaoEventosEjb] (EJB default - 87) [CORRELATION-ID:5941b738-0653-4ee8-aa00-0f472f1ccd13] [POLLING][RECONCILIACAO_EVENTOS][BATCH][INICIANDO][CPF] Finalizado polling da reconciliacao por eventos. Demorou 145
2026-10-27 12:01:00,204 INFO  [br.gov.caixa.spi.dict.ejb.EventoFecharLiquidados] (EJB default - 93) [CORRELATION-ID:b7180e89-fab8-451e-a5c6-6e2eb5222d92] [BATCH][FECHAR-LIQUIDADAS] Nenhuma devolucao liquidada externa encontrada
2026-10-27 12:01:00,204 INFO  [br.gov.caixa.spi.dict.scheduler.FecharLiquidadosScheduler] (EJB default - 93) [CORRELATION-ID:b7180e89-fab8-451e-a5c6-6e2eb5222d92] [BATCH][FECHAR-LIQUIDADAS] Finaliza processo para fechar devolucoes liquidadas.
2026-10-27 12:01:00,223 INFO  [br.gov.caixa.spi.dict.ejb.recon.ReconciliacaoEventosEjb] (EJB default - 99) [CORRELATION-ID:f03b1dad-c581-4596-9265-6e29fd03e59d] [POLLING][RECONCILIACAO_EVENTOS][BATCH][EVP] Demorou 191 ms para atualizar os eventos da reconciliacao. Iteracao 1 Data base 2026-10-27T11:55:03.216
2026-10-27 12:01:00,224 INFO  [br.gov.caixa.spi.dict.ejb.recon.ReconciliacaoEventosEjb] (EJB default - 91) [CORRELATION-ID:1f0314df-0d90-4eff-a357-45e7a3bde8ec] [POLLING][RECONCILIACAO_EVENTOS][BATCH][CNPJ] Demorou 150 ms para atualizar os eventos da reconciliacao. Iteracao 1 Data base 2026-10-27T11:55:03.216
2026-10-27 12:01:00,229 INFO  [br.gov.caixa.spi.dict.ejb.recon.ReconciliacaoEventosEjb] (EJB default - 99) [CORRELATION-ID:f03b1dad-c581-4596-9265-6e29fd03e59d] [POLLING][RECONCILIACAO_EVENTOS][BATCH][INICIANDO][EVP] Finalizado polling da reconciliacao por eventos. Demorou 201
2026-10-27 12:01:00,234 INFO  [br.gov.caixa.spi.dict.ejb.recon.ReconciliacaoEventosEjb] (EJB default - 91) [CORRELATION-ID:1f0314df-0d90-4eff-a357-45e7a3bde8ec] [POLLING][RECONCILIACAO_EVENTOS][BATCH][INICIANDO][CNPJ] Finalizado polling da reconciliacao por eventos. Demorou 178
2026-10-27 12:01:00,241 INFO  [br.gov.caixa.spi.dict.ejb.recon.ReconciliacaoEventosEjb] (EJB default - 84) [CORRELATION-ID:32ed346a-fee8-423c-b863-c6f2d5c18f35] [POLLING][RECONCILIACAO_EVENTOS][BATCH][PHONE] Demorou 182 ms para atualizar os eventos da reconciliacao. Iteracao 1 Data base 2026-10-27T11:49:00.56
2026-10-27 12:01:00,248 INFO  [br.gov.caixa.spi.dict.ejb.recon.ReconciliacaoEventosEjb] (EJB default - 84) [CORRELATION-ID:32ed346a-fee8-423c-b863-c6f2d5c18f35] [POLLING][RECONCILIACAO_EVENTOS][BATCH][INICIANDO][PHONE] Finalizado polling da reconciliacao por eventos. Demorou 192
2026-10-27 12:01:00,305 INFO  [br.gov.caixa.spi.dict.ejb.EventoDevolucaoPixAutomatico] (EJB default - 79) [CORRELATION-ID:d18bda40-c9c1-4d9c-ad51-e3209b134f16] [BATCH] [EVENTO-DEVOLUCAO-PIX-AUTOMATICO] Devolucoes Pix Automatico encontradas na base Caixa: 0
2026-10-27 12:01:00,305 INFO  [br.gov.caixa.spi.dict.ejb.EventoDevolucaoPixAutomatico] (EJB default - 79) [CORRELATION-ID:d18bda40-c9c1-4d9c-ad51-e3209b134f16] [BATCH] [EVENTO-DEVOLUCAO-PIX-AUTOMATICO] Nenhuma devolucao com status Pix Automatico encontrada
2026-10-27 12:01:00,305 INFO  [br.gov.caixa.spi.dict.scheduler.DevolucoesCriadasAutomaticoSchedule] (EJB default - 79) [CORRELATION-ID:d18bda40-c9c1-4d9c-ad51-e3209b134f16] [BATCH][EVENTOSDEVOLUCAO][FECHAR] Finalizando o processo de resolver as devolucoes Pix Automatico
2026-10-27 12:01:00,462 INFO  [br.gov.caixa.spi.dict.ejb.EventoDevolucaoAbertaAutomatico] (EJB default - 94) [CORRELATION-ID:e6053048-8d4b-4ead-b547-3694f11839ac] [BATCH] [EVENTO-DEVOLUCAO-ABERTAS-AUTOMATICO] Nenhuma devolu??o com status ABERTA_PIX_AUTOMATICO encontrada
2026-10-27 12:01:00,462 INFO  [br.gov.caixa.spi.dict.scheduler.DevolucoesAbertasAutomaticoSchedule] (EJB default - 94) [CORRELATION-ID:e6053048-8d4b-4ead-b547-3694f11839ac] [DEVOLUCOES_MED][BATCH][EVENTO-DEVOLUCAO-ABERTAS-AUTOMATICO] Finalizando o processo de resolver as devolucoes abertas automaticas
2026-10-27 12:01:02,297 INFO  [br.gov.caixa.spi.dict.v2.ejb.RelatoInfracaoEjb] (EJB default - 64) [CORRELATION-ID:834f53ca-0003-4985-9450-04b8ea8625c5] FORAM ENCONTRADO 1 RELATOS SEM RESULTADO
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc patch dc/sispi-qrcode-api-validador-des -n sispi-des --type=json \
>     -p '[{"op":"remove","path":"/spec/template/metadata/annotations/instrumentation.opentelemetry.io~1inject-java"}]'
deploymentconfig.apps.openshift.io/sispi-qrcode-api-validador-des patched
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc set resources dc/sispi-qrcode-api-validador-des -n sispi-des -c sispi-qrcode-api-validador-des --requests=cpu=500m
deploymentconfig.apps.openshift.io/sispi-qrcode-api-validador-des resource requirements updated
-sh-4.2$
-sh-4.2$
-sh-4.2$ c set probe dc/sispi-qrcode-api-validador-des -n sispi-des -c sispi-qrcode-api-validador-des --liveness --initial-delay-seconds=240
-sh: c: comando não encontrado
-sh-4.2$   oc set probe dc/sispi-qrcode-api-validador-des -n sispi-des -c sispi-qrcode-api-validador-des --liveness --initial-delay-seconds=240
deploymentconfig.apps.openshift.io/sispi-qrcode-api-validador-des probes updated
-sh-4.2$
-sh-4.2$
-sh-4.2$
