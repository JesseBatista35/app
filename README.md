Favor verificar, pois não está sendo possível prosseguir com as releases no módulo SIIFX-api-aplicacao, ambiente de DES devido erro anexo. Segue também o caminho da Release:

SIIFX-api-aplicacao

https://devops.caixa/projetos/Caixa/_releaseProgress?_a=release-environment-logs&releaseId=540301&environmentId=2510562


2026-10-14T13:02:14.8781082Z ##[section]Starting: Verificando Status do Deployment
2026-10-14T13:02:14.8784058Z ==============================================================================
2026-10-14T13:02:14.8784146Z Task         : Bash
2026-10-14T13:02:14.8784194Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-14T13:02:14.8784267Z Version      : 3.227.0
2026-10-14T13:02:14.8784314Z Author       : Microsoft Corporation
2026-10-14T13:02:14.8784368Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-14T13:02:14.8784452Z ==============================================================================
2026-10-14T13:02:15.0065799Z Generating script.
2026-10-14T13:02:15.0081313Z ========================== Starting Command Output ===========================
2026-10-14T13:02:15.0091063Z [command]/usr/bin/bash /opt/ads-agent/_work/_temp/b1a60a67-ffe2-413e-9c35-f00dae24de89.sh
2026-10-14T13:02:15.1020177Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-10-14T13:02:15.6569623Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-10-14T13:02:15.7069910Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-10-14T13:02:47.6854273Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-10-14T13:02:47.7768736Z Waiting for rollout to finish: 0 of 1 updated replicas are available...
2026-10-14T13:08:22.3887468Z ##[error]The task has timed out.
2026-10-14T13:08:22.3888493Z ##[section]Finishing: Verificando Status do Deployment


2026-10-14T13:08:22.3910728Z ##[section]Starting: Logs da Aplicação
2026-10-14T13:08:22.3913717Z ==============================================================================
2026-10-14T13:08:22.3913798Z Task         : Bash
2026-10-14T13:08:22.3913845Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-14T13:08:22.3913929Z Version      : 3.227.0
2026-10-14T13:08:22.3913978Z Author       : Microsoft Corporation
2026-10-14T13:08:22.3914033Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-14T13:08:22.3914120Z ==============================================================================
2026-10-14T13:08:22.5181640Z Generating script.
2026-10-14T13:08:22.5192118Z ========================== Starting Command Output ===========================
2026-10-14T13:08:22.5198956Z [command]/usr/bin/bash /opt/ads-agent/_work/_temp/2d2b3f5d-64ab-494a-a51c-290d71ac855a.sh
2026-10-14T13:08:22.5258980Z + shopt -s expand_aliases
2026-10-14T13:08:22.5259135Z + [[ -n okd4_nprd ]]
2026-10-14T13:08:22.5259302Z + [[ okd4_nprd =~ ocp ]]
2026-10-14T13:08:22.5259444Z + [[ -n okd4_nprd ]]
2026-10-14T13:08:22.5259609Z + [[ okd4_nprd =~ (okd4|openshift) ]]
2026-10-14T13:08:22.5259783Z + app=siifx-api-aplicacao-des
2026-10-14T13:08:22.5259902Z + oc version
2026-10-14T13:08:22.5864852Z Client Version: v4.2.0-alpha.0-1394-g45460a5
2026-10-14T13:08:22.5865138Z Server Version: 4.12.0-0.okd-2023-04-16-041331
2026-10-14T13:08:22.5865344Z Kubernetes Version: v1.25.0-2824+27e744f55d2e99-dirty
2026-10-14T13:08:22.5894631Z ++ oc get pod -l name=siifx-api-aplicacao-des -n siifx-des -o 'jsonpath={range .items[*]}{.metadata.name}{"\n"}' --sort-by=.metadata.creationTimestamp
2026-10-14T13:08:22.5895103Z ++ tac
2026-10-14T13:08:22.5896607Z ++ grep -v '^$'
2026-10-14T13:08:22.5896727Z ++ head -n1
2026-10-14T13:08:22.6631066Z + last_pod=siifx-api-aplicacao-des-2896-p97pn
2026-10-14T13:08:22.6631370Z + echo 'Logs do POD: siifx-api-aplicacao-des-2896-p97pn'
2026-10-14T13:08:22.6631616Z + oc logs siifx-api-aplicacao-des-2896-p97pn -c siifx-api-aplicacao-des -n siifx-des
2026-10-14T13:08:22.6631847Z Logs do POD: siifx-api-aplicacao-des-2896-p97pn
2026-10-14T13:08:22.7389841Z Error from server (BadRequest): container "siifx-api-aplicacao-des" in pod "siifx-api-aplicacao-des-2896-p97pn" is waiting to start: PodInitializing
2026-10-14T13:08:22.7437854Z ##[error]Bash exited with code '1'.
2026-10-14T13:08:22.7470830Z ##[section]Finishing: Logs da Aplicação
