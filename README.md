Verificar o CI quebrando no passo de deploy https://github.com/caixagithub/silce-gestao-operacional/actions/runs/39463354047.


Skip to content
GitHub Enterprise
Users managed by Caixa Economica Federal
caixagithub
silce-gestao-operacional
Repository navigation
Code
Issues
Pull requests
1
 (1)
Actions
Projects
Wiki
Security and quality
3
 (3)
Insights
Settings
CI/CD Workflow (develop)
develop_caixagithub/silce-gestao-operacional_develop_39603505605.38 #38
All jobs
Run details
Annotations
1 error and 1 warning
CI_DES / ArgoCD_Deploy / ArgoCD_Deploy (DES)
failed 1 hour ago in 12m 17s
Search logs
10s
0s
1s
0s
0s
0s
0s
0s
0s
0s
0s
0s
0s
1m 9s
0s
8s
0s
0s
0s
4s
0s
1s
0s
0s
0s
21s
5s
0s
0s
1s
10m 8s
1s
Run caixagithub/DevSecOps-Actions/.github/integrations/argocd/logs@main
  with:
    ARGOCD_SERVER: https://openshift-gitops-server-openshift-gitops.apps.aroidpprd.brazilsouth.aroapp.io
    ARGOCD_APP: caixagithub/silce-gestao-operacional
    AMBIENTE: DES
    IMAGE_TAG: 39603505605
    HEALTH_CHECK_WAS_SUCCESSFUL: false
  env:
    APIM_VERSIONAPI: 
    APIM_displaynameAPI: 
    APIM_PATH: 
    APIM_SWAGGERPATH: 
    APIM_TAGSAPI: 
    APIM_POLICIESALLOPERATIONSPATH: 
    AZ_INSTALL_STATUS: ms_repo_ok
    AZ_VERSION: latest
    INSTALL_PREREQUISITES: true
    AZ_LATEST_VERSION: 2.91.0
    environment: des
    repository_suffix: infranprd
    REPO: silce-gestao-operacional
    JOB_ID: 166063
    ARGOCD_AUTH_TOKEN: ***
Formate ARGO REPOSITORY
0s
Run echo "REPO_NAME=$(echo 'caixagithub/silce-gestao-operacional' | cut -d'/' -f2)" >> $GITHUB_ENV
    echo "REPO_NAME=$(echo 'caixagithub/silce-gestao-operacional' | cut -d'/' -f2)" >> $GITHUB_ENV
    echo "INPUT_IMAGE_TAG: '39603505605'"
    echo "AMBIENTE_LOWER=$(echo 'DES' | tr '[:upper:]' '[:lower:]')" >> $GITHUB_ENV
    shell: /usr/bin/bash --noprofile --norc -e -o pipefail {0}
    env:
      APIM_VERSIONAPI: 
      APIM_displaynameAPI: 
      APIM_PATH: 
      APIM_SWAGGERPATH: 
      APIM_TAGSAPI: 
      APIM_POLICIESALLOPERATIONSPATH: 
      AZ_INSTALL_STATUS: ms_repo_ok
      AZ_VERSION: latest
      INSTALL_PREREQUISITES: true
      AZ_LATEST_VERSION: 2.91.0
      environment: des
      repository_suffix: infranprd
      REPO: silce-gestao-operacional
      JOB_ID: 166063
      ARGOCD_AUTH_TOKEN: ***
  INPUT_IMAGE_TAG: '39603505605'
Coletando logs dos pods
0s
Run RESOURCE_TREE_URL="https://openshift-gitops-server-openshift-gitops.apps.aroidpprd.brazilsouth.aroapp.io/api/v1/applications/silce-gestao-operacional-des/resource-tree?appNamespace=openshift-gitops"
    RESOURCE_TREE_URL="https://openshift-gitops-server-openshift-gitops.apps.aroidpprd.brazilsouth.aroapp.io/api/v1/applications/silce-gestao-operacional-des/resource-tree?appNamespace=openshift-gitops"
    echo "Fazendo requisição para: ${RESOURCE_TREE_URL}"
    
    RESOURCE_TREE_JSON=$(curl -s -H "Authorization: ***" "${RESOURCE_TREE_URL}")
    if [ $? -ne 0 ]; then
      echo "Erro ao fazer requisição para o resource-tree"
      exit 1
    fi
    
    echo "Resource-tree obtido com sucesso"
    
    echo "Filtrando pods e encontrando o mais recente..."
    
    LATEST_POD=$(echo "$RESOURCE_TREE_JSON" | jq -r '
      .nodes // [] |
      map(select(.kind == "Pod" and .createdAt != null)) |
      sort_by(.createdAt) |
      last |
      .name // empty
    ')
    
    if [ -z "$LATEST_POD" ]; then
      echo "Nenhum pod encontrado ou JSON não contém dados esperados"
      exit 0
    fi
    
    echo "Pod mais recente encontrado: ${LATEST_POD}"
    
    LOGS_URL="https://openshift-gitops-server-openshift-gitops.apps.aroidpprd.brazilsouth.aroapp.io/api/v1/applications/silce-gestao-operacional-des/logs?appNamespace=openshift-gitops&container=silce-gestao-operacional-des&namespace=silce-gestao-operacional&follow=false&podName=${LATEST_POD}&tailLines=1000&sinceSeconds=0"
    echo "URL dos logs: ${LOGS_URL}"
    
    LOGS_RESPONSE=$(curl -s -H "Authorization: ***" "${LOGS_URL}")
    
    if [ $? -ne 0 ]; then
      echo "Erro ao obter logs do pod"
      exit 1
    fi
    
    echo "Logs obtidos com sucesso"
    echo "Logs do pod ${LATEST_POD}:"
    echo "================================================"
    
    echo "Exibindo os Logs:"
    echo "$LOGS_RESPONSE" | jq -r '.result.content'
    
    echo "================================================"
    echo "Script executado com sucesso!"
    echo "Pod utilizado: ${LATEST_POD}"
    
0s
0s
0s
0s
0s
0s
0s
0s
0s
1s
0s

2026-10-21T13:12:53.372Z	info	service@v0.127.0/service.go:199	Setting up own telemetry...	{"resource": {}}
2026-10-21T13:12:53.373Z	info	builders/builders.go:26	Development component. May change in the future.	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "traces"}
2026-10-21T13:12:53.373Z	info	builders/builders.go:26	Development component. May change in the future.	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "logs"}
2026-10-21T13:12:53.373Z	info	builders/builders.go:26	Development component. May change in the future.	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics"}
2026-10-21T13:12:53.370Z	warn	envprovider@v1.33.0/provider.go:61	Configuration references unset environment variable	{"resource": {}, "name": "APP_INSIGHTS_CONNECTION_STRING"}
2026-10-21T13:12:53.374Z	info	service@v0.127.0/service.go:266	Starting otelcol-contrib...	{"resource": {}, "Version": "0.127.0", "NumCPU": 4}
2026-10-21T13:12:53.374Z	info	extensions/extensions.go:41	Starting extensions...	{"resource": {}}
2026-10-21T13:12:53.374Z	info	extensions/extensions.go:45	Extension is starting...	{"resource": {}, "otelcol.component.id": "pprof", "otelcol.component.kind": "extension"}
2026-10-21T13:12:53.374Z	info	pprofextension@v0.127.0/pprofextension.go:61	Starting net/http/pprof server	{"resource": {}, "otelcol.component.id": "pprof", "otelcol.component.kind": "extension", "config": {"TCPAddr":{"Endpoint":":1888","DialerConfig":{"Timeout":0}},"BlockProfileFraction":0,"MutexProfileFraction":0,"SaveToFile":""}}
2026-10-21T13:12:53.374Z	info	extensions/extensions.go:62	Extension started.	{"resource": {}, "otelcol.component.id": "pprof", "otelcol.component.kind": "extension"}
2026-10-21T13:12:53.374Z	info	extensions/extensions.go:45	Extension is starting...	{"resource": {}, "otelcol.component.id": "health_check", "otelcol.component.kind": "extension"}
2026-10-21T13:12:53.374Z	info	healthcheckextension@v0.127.0/healthcheckextension.go:32	Starting health_check extension	{"resource": {}, "otelcol.component.id": "health_check", "otelcol.component.kind": "extension", "config": {"Endpoint":":13133","TLSSetting":null,"CORS":null,"Auth":null,"MaxRequestBodySize":0,"IncludeMetadata":false,"ResponseHeaders":null,"CompressionAlgorithms":null,"ReadTimeout":0,"ReadHeaderTimeout":0,"WriteTimeout":0,"IdleTimeout":0,"Middlewares":null,"Path":"/","ResponseBody":null,"CheckCollectorPipeline":{"Enabled":false,"Interval":"5m","ExporterFailureThreshold":5}}}
2026-10-21T13:12:53.375Z	info	extensions/extensions.go:62	Extension started.	{"resource": {}, "otelcol.component.id": "health_check", "otelcol.component.kind": "extension"}
2026-10-21T13:12:53.375Z	info	extensions/extensions.go:45	Extension is starting...	{"resource": {}, "otelcol.component.id": "zpages", "otelcol.component.kind": "extension"}
2026-10-21T13:12:53.375Z	info	zpagesextension@v0.127.0/zpagesextension.go:56	Registered zPages span processor on tracer provider	{"resource": {}, "otelcol.component.id": "zpages", "otelcol.component.kind": "extension"}
2026-10-21T13:12:53.375Z	info	zpagesextension@v0.127.0/zpagesextension.go:71	Registered Host's zPages	{"resource": {}, "otelcol.component.id": "zpages", "otelcol.component.kind": "extension"}
2026-10-21T13:12:53.375Z	info	zpagesextension@v0.127.0/zpagesextension.go:83	Starting zPages extension	{"resource": {}, "otelcol.component.id": "zpages", "otelcol.component.kind": "extension", "config": {"Endpoint":":55679","TLSSetting":null,"CORS":null,"Auth":null,"MaxRequestBodySize":0,"IncludeMetadata":false,"ResponseHeaders":null,"CompressionAlgorithms":null,"ReadTimeout":0,"ReadHeaderTimeout":0,"WriteTimeout":0,"IdleTimeout":0,"Middlewares":null,"Expvar":{"Enabled":false}}}
2026-10-21T13:12:53.375Z	info	extensions/extensions.go:62	Extension started.	{"resource": {}, "otelcol.component.id": "zpages", "otelcol.component.kind": "extension"}
2026-10-21T13:12:53.375Z	info	otlpreceiver@v0.127.0/otlp.go:116	Starting GRPC server	{"resource": {}, "otelcol.component.id": "otlp", "otelcol.component.kind": "receiver", "endpoint": "0.0.0.0:4317"}
2026-10-21T13:12:53.376Z	info	healthcheck/handler.go:132	Health Check state change	{"resource": {}, "otelcol.component.id": "health_check", "otelcol.component.kind": "extension", "status": "ready"}
2026-10-21T13:12:53.376Z	info	service@v0.127.0/service.go:289	Everything is ready. Begin running and processing data.	{"resource": {}}
2026-10-21T13:13:36.568Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:14:36.562Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:15:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:16:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:17:36.562Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:18:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:19:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:20:36.562Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:21:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:22:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:23:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:24:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:25:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:26:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:27:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:28:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:29:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:30:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:31:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:32:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:33:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:34:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:35:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:36:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 80}
2026-10-21T13:37:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 84}
2026-10-21T13:38:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 96}
2026-10-21T13:39:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 96}
2026-10-21T13:40:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 96}
2026-10-21T13:41:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 96}
2026-10-21T13:42:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 96}
2026-10-21T13:43:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 96}
2026-10-21T13:44:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 96}
2026-10-21T13:45:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 96}
2026-10-21T13:46:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 96}
2026-10-21T13:47:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 100}
2026-10-21T13:48:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 100}
2026-10-21T13:49:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 100}
2026-10-21T13:50:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 100}
2026-10-21T13:51:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 100}
2026-10-21T13:52:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 100}
2026-10-21T13:53:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 100}
2026-10-21T13:54:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 100}
2026-10-21T13:55:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 100}
2026-10-21T13:56:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 100}
2026-10-21T13:57:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 104}
2026-10-21T13:58:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 104}
2026-10-21T13:59:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 104}
2026-10-21T14:00:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 104}
2026-10-21T14:01:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 104}
2026-10-21T14:02:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 104}
2026-10-21T14:03:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 104}
2026-10-21T14:04:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 104}
2026-10-21T14:05:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 104}
2026-10-21T14:06:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 104}
2026-10-21T14:07:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 108}
2026-10-21T14:08:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 108}
2026-10-21T14:09:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 108}
2026-10-21T14:10:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 112}
2026-10-21T14:11:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 116}
2026-10-21T14:12:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:13:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:14:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:15:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:16:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:17:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:18:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:19:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:20:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:21:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:22:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:23:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:24:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:25:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:26:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:27:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:28:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:29:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:30:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:31:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:32:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:33:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:34:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:35:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:36:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:37:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:38:36.563Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:39:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:40:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:41:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:42:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:43:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:44:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:45:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:46:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:47:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:48:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:49:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:50:36.560Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:51:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}
2026-10-21T14:52:36.561Z	info	Metrics	{"resource": {}, "otelcol.component.id": "debug", "otelcol.component.kind": "exporter", "otelcol.signal": "metrics", "resource metrics": 1, "metrics": 21, "data points": 120}


