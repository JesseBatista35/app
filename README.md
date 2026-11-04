Prezados,
AMBIENTE TGE

Após configurar/atualizar a library do projeto siifx-caixinhas-api-aplicacao e tentar efetuar release em TGE ocorre o erro abaixo: 
Verificando Status do Deployment - The task has timed out.
https://devops.caixa/projetos/Caixa/_releaseProgress?_a=release-environment-logs&releaseId=550368&environmentId=2557888

Não foi possível conferir no OKD, pois não foi localizado pod para esteira TGE.

Segue em anexo prints.

2026-11-04T14:09:59.5685668Z ##[section]Starting: Verificando Status do Deployment
2026-11-04T14:09:59.5689172Z ==============================================================================
2026-11-04T14:09:59.5689257Z Task         : Bash
2026-11-04T14:09:59.5689318Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-11-04T14:09:59.5689381Z Version      : 3.227.0
2026-11-04T14:09:59.5689439Z Author       : Microsoft Corporation
2026-11-04T14:09:59.5689586Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-11-04T14:09:59.5689662Z ==============================================================================
2026-11-04T14:09:59.6933953Z Generating script.
2026-11-04T14:09:59.6946688Z ========================== Starting Command Output ===========================
2026-11-04T14:09:59.6953972Z [command]/usr/bin/bash /opt/ads-agent/_work/_temp/4c0ef59e-3e18-49b6-be6e-4b9860e51f14.sh
2026-11-04T14:09:59.7797329Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-11-04T14:10:01.1215595Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-11-04T14:10:01.1982295Z Waiting for rollout to finish: 1 old replicas are pending termination...
2026-11-04T14:14:08.5156954Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-11-04T14:14:08.5375184Z Waiting for rollout to finish: 1 old replicas are pending termination...
2026-11-04T14:16:07.0812180Z ##[error]The task has timed out.
2026-11-04T14:16:07.0813200Z ##[section]Finishing: Verificando Status do Deployment



2026-11-04T14:16:07.0831811Z ##[section]Starting: Logs da Aplicação
2026-11-04T14:16:07.0834799Z ==============================================================================
2026-11-04T14:16:07.0834878Z Task         : Bash
2026-11-04T14:16:07.0834924Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-11-04T14:16:07.0834997Z Version      : 3.227.0
2026-11-04T14:16:07.0835043Z Author       : Microsoft Corporation
2026-11-04T14:16:07.0835097Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-11-04T14:16:07.0835193Z ==============================================================================
2026-11-04T14:16:07.2527982Z Generating script.
2026-11-04T14:16:07.2539903Z ========================== Starting Command Output ===========================
2026-11-04T14:16:07.2546928Z [command]/usr/bin/bash /opt/ads-agent/_work/_temp/5fe2b2f4-8010-4cad-a1bc-8c406e6a82bd.sh
2026-11-04T14:16:07.2606051Z + shopt -s expand_aliases
2026-11-04T14:16:07.2607761Z + [[ -n okd4_nprd ]]
2026-11-04T14:16:07.2607921Z + [[ okd4_nprd =~ ocp ]]
2026-11-04T14:16:07.2608054Z + [[ -n okd4_nprd ]]
2026-11-04T14:16:07.2608163Z + [[ okd4_nprd =~ (okd4|openshift) ]]
2026-11-04T14:16:07.2608333Z + app=siifx-caixinhas-api-aplicacao-des
2026-11-04T14:16:07.2608438Z + oc version
2026-11-04T14:16:07.3336893Z Client Version: v4.2.0-alpha.0-1394-g45460a5
2026-11-04T14:16:07.3337141Z Server Version: 4.12.0-0.okd-2023-04-16-041331
2026-11-04T14:16:07.3337329Z Kubernetes Version: v1.25.0-2824+27e744f55d2e99-dirty
2026-11-04T14:16:07.3364905Z ++ oc get pod -l name=siifx-caixinhas-api-aplicacao-des -n siifx-des -o 'jsonpath={range .items[*]}{.metadata.name}{"\n"}' --sort-by=.metadata.creationTimestamp
2026-11-04T14:16:07.3366072Z ++ tac
2026-11-04T14:16:07.3367148Z ++ grep -v '^$'
2026-11-04T14:16:07.3367415Z ++ head -n1
2026-11-04T14:16:07.4328220Z + last_pod=siifx-caixinhas-api-aplicacao-des-113-7bsd2
2026-11-04T14:16:07.4328600Z + echo 'Logs do POD: siifx-caixinhas-api-aplicacao-des-113-7bsd2'
2026-11-04T14:16:07.4328850Z + oc logs siifx-caixinhas-api-aplicacao-des-113-7bsd2 -c siifx-caixinhas-api-aplicacao-des -n siifx-des
2026-11-04T14:16:07.4329100Z Logs do POD: siifx-caixinhas-api-aplicacao-des-113-7bsd2
2026-11-04T14:16:07.5100158Z Error from server (BadRequest): container "siifx-caixinhas-api-aplicacao-des" in pod "siifx-caixinhas-api-aplicacao-des-113-7bsd2" is waiting to start: PodInitializing
2026-11-04T14:16:07.5167204Z ##[error]Bash exited with code '1'.
2026-11-04T14:16:07.5182321Z ##[section]Finishing: Logs da Aplicação
