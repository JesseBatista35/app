2026-10-24T15:15:56.4561525Z ##[debug]Evaluating condition for step: 'Verificando Status do Deployment'
2026-10-24T15:15:56.4561933Z ##[debug]Evaluating: succeeded()
2026-10-24T15:15:56.4562150Z ##[debug]Evaluating succeeded:
2026-10-24T15:15:56.4562415Z ##[debug]=> True
2026-10-24T15:15:56.4562579Z ##[debug]Result: True
2026-10-24T15:15:56.4562855Z ##[section]Starting: Verificando Status do Deployment
2026-10-24T15:15:56.4565806Z ==============================================================================
2026-10-24T15:15:56.4565894Z Task         : Bash
2026-10-24T15:15:56.4565938Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-24T15:15:56.4566010Z Version      : 3.227.0
2026-10-24T15:15:56.4566055Z Author       : Microsoft Corporation
2026-10-24T15:15:56.4566108Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-24T15:15:56.4566189Z ==============================================================================
2026-10-24T15:15:56.5115634Z ##[debug]Using node path: /opt/ads-agent/externals/node16/bin/node
2026-10-24T15:15:56.5797090Z ##[debug]agent.TempDirectory=/opt/ads-agent/_work/_temp
2026-10-24T15:15:56.5805016Z ##[debug]loading inputs and endpoints
2026-10-24T15:15:56.5812242Z ##[debug]loading INPUT_TARGETTYPE
2026-10-24T15:15:56.5819969Z ##[debug]loading INPUT_FILEPATH
2026-10-24T15:15:56.5820739Z ##[debug]loading INPUT_SCRIPT
2026-10-24T15:15:56.5821788Z ##[debug]loading INPUT_WORKINGDIRECTORY
2026-10-24T15:15:56.5822051Z ##[debug]loading INPUT_FAILONSTDERR
2026-10-24T15:15:56.5822394Z ##[debug]loading ENDPOINT_AUTH_SYSTEMVSSCONNECTION
2026-10-24T15:15:56.5823298Z ##[debug]loading ENDPOINT_AUTH_SCHEME_SYSTEMVSSCONNECTION
2026-10-24T15:15:56.5825284Z ##[debug]loading ENDPOINT_AUTH_PARAMETER_SYSTEMVSSCONNECTION_ACCESSTOKEN
2026-10-24T15:15:56.5831320Z ##[debug]loading SECRET_TOKEN_CRQ
2026-10-24T15:15:56.5831823Z ##[debug]loading SECRET_GRAYLOG_PASSWORD
2026-10-24T15:15:56.5833628Z ##[debug]loading SECRET_FORTIFY_APITOKEN
2026-10-24T15:15:56.5835714Z ##[debug]loading SECRET_PW_ISILON
2026-10-24T15:15:56.5836944Z ##[debug]loading SECRET_ALOCAIP_SENHA
2026-10-24T15:15:56.5838142Z ##[debug]loading SECRET_SCOWDB01
2026-10-24T15:15:56.5838775Z ##[debug]loading SECRET_PW_ALOCAIP
2026-10-24T15:15:56.5839328Z ##[debug]loading SECRET_OKD_TOKEN_KAFKA
2026-10-24T15:15:56.5839949Z ##[debug]loading SECRET_FORTIFY_PASS
2026-10-24T15:15:56.5840602Z ##[debug]loading SECRET_PASSWORD_CGC
2026-10-24T15:15:56.5841156Z ##[debug]loading SECRET_AZPAT
2026-10-24T15:15:56.5841691Z ##[debug]loading SECRET_BT_SECRETS_PATH
2026-10-24T15:15:56.5843243Z ##[debug]loading SECRET_OKD_TOKEN_REGISTRY
2026-10-24T15:15:56.5843800Z ##[debug]loading SECRET_OKD_4_TOKEN
2026-10-24T15:15:56.5844351Z ##[debug]loaded 22
2026-10-24T15:15:56.5848975Z ##[debug]Agent.ProxyUrl=undefined
2026-10-24T15:15:56.5849386Z ##[debug]Agent.CAInfo=undefined
2026-10-24T15:15:56.5849719Z ##[debug]Agent.ClientCert=undefined
2026-10-24T15:15:56.5849952Z ##[debug]Agent.SkipCertValidation=True
2026-10-24T15:15:56.5865076Z ##[debug]check path : /opt/ads-agent/_work/_tasks/Bash_6c731c3c-3c68-459a-a5c9-bde6e6595b5b/3.227.0/task.json
2026-10-24T15:15:56.5866821Z ##[debug]adding resource file: /opt/ads-agent/_work/_tasks/Bash_6c731c3c-3c68-459a-a5c9-bde6e6595b5b/3.227.0/task.json
2026-10-24T15:15:56.5867188Z ##[debug]system.culture=en-US
2026-10-24T15:15:56.5874601Z ##[debug]failOnStderr=false
2026-10-24T15:15:56.5876133Z ##[debug]workingDirectory=/opt/ads-agent/_work/r934/a
2026-10-24T15:15:56.5876403Z ##[debug]check path : /opt/ads-agent/_work/r934/a
2026-10-24T15:15:56.5876943Z ##[debug]targetType=inline
2026-10-24T15:15:56.5877177Z ##[debug]bashEnvValue=undefined
2026-10-24T15:15:56.5877845Z ##[debug]script=if [[ -n "$SITE" && "$SITE" =~ (okd4|ocp|openshift) ]];
then
  app="sicow-conres-okd-des"
else
  app="sicow-conres-okd-des-esteiras"
fi

oc rollout status deploymentconfig/"$app"  --request-timeout=600 -n sicow-des
if [ "$?" -ne "0" ]; then
  echo "A aplicação não foi iniciada com sucesso!"
  echo "Os logs da aplicação estão disponíveis na próxima task: Logs da Aplicação"
  exit 1
fi
2026-10-24T15:15:56.5886676Z Generating script.
2026-10-24T15:15:56.5888187Z ##[debug]which 'bash'
2026-10-24T15:15:56.5893588Z ##[debug]found: '/usr/bin/bash'
2026-10-24T15:15:56.5894040Z ##[debug]Agent.Version=3.236.1
2026-10-24T15:15:56.5894291Z ##[debug]agent.tempDirectory=/opt/ads-agent/_work/_temp
2026-10-24T15:15:56.5894541Z ##[debug]check path : /opt/ads-agent/_work/_temp
2026-10-24T15:15:56.5896838Z ========================== Starting Command Output ===========================
2026-10-24T15:15:56.5897968Z ##[debug]which '/usr/bin/bash'
2026-10-24T15:15:56.5898817Z ##[debug]found: '/usr/bin/bash'
2026-10-24T15:15:56.5899369Z ##[debug]/usr/bin/bash arg: /opt/ads-agent/_work/_temp/4214c91a-2538-45cb-9813-d1da1f74600e.sh
2026-10-24T15:15:56.5901769Z ##[debug]exec tool: /usr/bin/bash
2026-10-24T15:15:56.5902008Z ##[debug]arguments:
2026-10-24T15:15:56.5902262Z ##[debug]   /opt/ads-agent/_work/_temp/4214c91a-2538-45cb-9813-d1da1f74600e.sh
2026-10-24T15:15:56.5904065Z [command]/usr/bin/bash /opt/ads-agent/_work/_temp/4214c91a-2538-45cb-9813-d1da1f74600e.sh
2026-10-24T15:15:56.6812373Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-10-24T15:15:58.8476029Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-10-24T15:15:58.9243540Z Waiting for rollout to finish: 1 old replicas are pending termination...
2026-10-24T15:16:00.9612295Z ##[debug]Agent environment resources - Disk: / Available 63467.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 17.60%
2026-10-24T15:16:05.9620275Z ##[debug]Agent environment resources - Disk: / Available 63469.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 15.91%
2026-10-24T15:16:10.9622103Z ##[debug]Agent environment resources - Disk: / Available 63469.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 14.50%
2026-10-24T15:16:15.9641786Z ##[debug]Agent environment resources - Disk: / Available 63458.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 13.33%
2026-10-24T15:16:20.9648649Z ##[debug]Agent environment resources - Disk: / Available 63461.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 12.35%
2026-10-24T15:16:25.9657855Z ##[debug]Agent environment resources - Disk: / Available 63461.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 11.49%
2026-10-24T15:16:30.9669714Z ##[debug]Agent environment resources - Disk: / Available 63453.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 10.74%
2026-10-24T15:16:35.9719607Z ##[debug]Agent environment resources - Disk: / Available 63468.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 10.10%
2026-10-24T15:16:40.9720169Z ##[debug]Agent environment resources - Disk: / Available 63469.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 9.53%
2026-10-24T15:16:45.9726224Z ##[debug]Agent environment resources - Disk: / Available 63467.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 9.02%
2026-10-24T15:16:50.9734620Z ##[debug]Agent environment resources - Disk: / Available 63467.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 8.57%
2026-10-24T15:16:55.9749314Z ##[debug]Agent environment resources - Disk: / Available 63467.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 8.17%
2026-10-24T15:17:00.9754054Z ##[debug]Agent environment resources - Disk: / Available 63467.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 7.79%
2026-10-24T15:17:05.9764113Z ##[debug]Agent environment resources - Disk: / Available 63467.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 7.45%
2026-10-24T15:17:10.9770445Z ##[debug]Agent environment resources - Disk: / Available 63467.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 7.14%
2026-10-24T15:17:15.9771499Z ##[debug]Agent environment resources - Disk: / Available 63464.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 6.87%
2026-10-24T15:17:20.9774459Z ##[debug]Agent environment resources - Disk: / Available 63456.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 6.59%
2026-10-24T15:17:25.9781315Z ##[debug]Agent environment resources - Disk: / Available 63457.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 6.36%
2026-10-24T15:17:30.9789833Z ##[debug]Agent environment resources - Disk: / Available 63457.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 6.13%
2026-10-24T15:17:35.9799833Z ##[debug]Agent environment resources - Disk: / Available 63459.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 5.92%
2026-10-24T15:17:40.9806116Z ##[debug]Agent environment resources - Disk: / Available 63450.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 5.72%
2026-10-24T15:17:45.9819774Z ##[debug]Agent environment resources - Disk: / Available 63447.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 5.55%
2026-10-24T15:17:50.9826856Z ##[debug]Agent environment resources - Disk: / Available 63446.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 5.38%
2026-10-24T15:17:55.9836612Z ##[debug]Agent environment resources - Disk: / Available 63446.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 5.21%
2026-10-24T15:18:00.9848026Z ##[debug]Agent environment resources - Disk: / Available 63439.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 5.06%
2026-10-24T15:18:05.9850120Z ##[debug]Agent environment resources - Disk: / Available 63439.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 4.92%
2026-10-24T15:18:10.9859025Z ##[debug]Agent environment resources - Disk: / Available 63441.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 4.78%
2026-10-24T15:18:15.9864294Z ##[debug]Agent environment resources - Disk: / Available 63438.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 4.66%
2026-10-24T15:18:20.9874279Z ##[debug]Agent environment resources - Disk: / Available 63437.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 4.54%
2026-10-24T15:18:25.9887467Z ##[debug]Agent environment resources - Disk: / Available 63437.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 4.42%
2026-10-24T15:18:30.9894955Z ##[debug]Agent environment resources - Disk: / Available 63431.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 4.31%
2026-10-24T15:18:35.9901653Z ##[debug]Agent environment resources - Disk: / Available 63430.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 4.21%
2026-10-24T15:18:40.9907782Z ##[debug]Agent environment resources - Disk: / Available 63431.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 4.11%
2026-10-24T15:18:45.9971616Z ##[debug]Agent environment resources - Disk: / Available 63430.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 4.02%
2026-10-24T15:18:50.9964248Z ##[debug]Agent environment resources - Disk: / Available 63430.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.93%
2026-10-24T15:18:55.9978487Z ##[debug]Agent environment resources - Disk: / Available 63428.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.84%
2026-10-24T15:19:00.9982972Z ##[debug]Agent environment resources - Disk: / Available 63420.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.76%
2026-10-24T15:19:05.9989150Z ##[debug]Agent environment resources - Disk: / Available 63422.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.68%
2026-10-24T15:19:10.9991168Z ##[debug]Agent environment resources - Disk: / Available 63422.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.61%
2026-10-24T15:19:15.9999418Z ##[debug]Agent environment resources - Disk: / Available 63422.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.54%
2026-10-24T15:19:21.0005426Z ##[debug]Agent environment resources - Disk: / Available 63420.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.47%
2026-10-24T15:19:26.0013205Z ##[debug]Agent environment resources - Disk: / Available 63422.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.40%
2026-10-24T15:19:31.0018138Z ##[debug]Agent environment resources - Disk: / Available 63412.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.34%
2026-10-24T15:19:36.0028213Z ##[debug]Agent environment resources - Disk: / Available 63412.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.28%
2026-10-24T15:19:41.0032845Z ##[debug]Agent environment resources - Disk: / Available 63427.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.22%
2026-10-24T15:19:46.0042832Z ##[debug]Agent environment resources - Disk: / Available 63427.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.16%
2026-10-24T15:19:51.0051963Z ##[debug]Agent environment resources - Disk: / Available 63435.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.11%
2026-10-24T15:19:56.0054126Z ##[debug]Agent environment resources - Disk: / Available 63433.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.06%
2026-10-24T15:20:01.0061282Z ##[debug]Agent environment resources - Disk: / Available 63434.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.01%
2026-10-24T15:20:06.0065427Z ##[debug]Agent environment resources - Disk: / Available 63426.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.96%
2026-10-24T15:20:11.0078966Z ##[debug]Agent environment resources - Disk: / Available 63425.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.91%
2026-10-24T15:20:16.0079006Z ##[debug]Agent environment resources - Disk: / Available 63424.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.86%
2026-10-24T15:20:21.0086243Z ##[debug]Agent environment resources - Disk: / Available 63424.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.82%
2026-10-24T15:20:26.0091194Z ##[debug]Agent environment resources - Disk: / Available 63415.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.78%
2026-10-24T15:20:31.0095060Z ##[debug]Agent environment resources - Disk: / Available 63416.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.74%
2026-10-24T15:20:36.0106361Z ##[debug]Agent environment resources - Disk: / Available 63413.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.70%
2026-10-24T15:20:41.0113784Z ##[debug]Agent environment resources - Disk: / Available 63414.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.66%
2026-10-24T15:20:46.0119430Z ##[debug]Agent environment resources - Disk: / Available 63414.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.62%
2026-10-24T15:20:51.0124831Z ##[debug]Agent environment resources - Disk: / Available 63414.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.58%
2026-10-24T15:20:56.0130881Z ##[debug]Agent environment resources - Disk: / Available 63417.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.55%
2026-10-24T15:21:01.0136005Z ##[debug]Agent environment resources - Disk: / Available 63410.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.52%
2026-10-24T15:21:06.0140984Z ##[debug]Agent environment resources - Disk: / Available 63410.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.49%
2026-10-24T15:21:11.0140627Z ##[debug]Agent environment resources - Disk: / Available 63406.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.45%
2026-10-24T15:21:16.0141075Z ##[debug]Agent environment resources - Disk: / Available 63405.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.42%
2026-10-24T15:21:21.0140364Z ##[debug]Agent environment resources - Disk: / Available 63406.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.39%
2026-10-24T15:21:26.0140080Z ##[debug]Agent environment resources - Disk: / Available 63395.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.36%
2026-10-24T15:21:31.0143196Z ##[debug]Agent environment resources - Disk: / Available 63365.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.33%
2026-10-24T15:21:36.0155529Z ##[debug]Agent environment resources - Disk: / Available 63365.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.31%
2026-10-24T15:21:41.0161179Z ##[debug]Agent environment resources - Disk: / Available 63365.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.28%
2026-10-24T15:21:46.0167119Z ##[debug]Agent environment resources - Disk: / Available 63364.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.25%
2026-10-24T15:21:51.0173033Z ##[debug]Agent environment resources - Disk: / Available 63366.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.22%
2026-10-24T15:21:56.0186784Z ##[debug]Agent environment resources - Disk: / Available 63366.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.20%
2026-10-24T15:21:56.4615642Z ##[debug]Started cancellation of executing script
2026-10-24T15:21:56.4619880Z ##[debug]Exit code null received from tool '/usr/bin/bash'
2026-10-24T15:22:03.9663761Z ##[error]The task has timed out.
2026-10-24T15:22:03.9664723Z ##[section]Finishing: Verificando Status do Deployment



2026-10-24T15:22:03.9685644Z ##[debug]Evaluating condition for step: 'Logs da Aplicação'
2026-10-24T15:22:03.9686398Z ##[debug]Evaluating: always()
2026-10-24T15:22:03.9686562Z ##[debug]Evaluating always:
2026-10-24T15:22:03.9687445Z ##[debug]=> True
2026-10-24T15:22:03.9687652Z ##[debug]Result: True
2026-10-24T15:22:03.9687826Z ##[section]Starting: Logs da Aplicação
2026-10-24T15:22:03.9691084Z ==============================================================================
2026-10-24T15:22:03.9691160Z Task         : Bash
2026-10-24T15:22:03.9691203Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-24T15:22:03.9691276Z Version      : 3.227.0
2026-10-24T15:22:03.9691319Z Author       : Microsoft Corporation
2026-10-24T15:22:03.9691371Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-24T15:22:03.9691451Z ==============================================================================
2026-10-24T15:22:04.0313412Z ##[debug]Using node path: /opt/ads-agent/externals/node16/bin/node
2026-10-24T15:22:04.1011690Z ##[debug]agent.TempDirectory=/opt/ads-agent/_work/_temp
2026-10-24T15:22:04.1019153Z ##[debug]loading inputs and endpoints
2026-10-24T15:22:04.1026833Z ##[debug]loading INPUT_TARGETTYPE
2026-10-24T15:22:04.1034806Z ##[debug]loading INPUT_FILEPATH
2026-10-24T15:22:04.1035793Z ##[debug]loading INPUT_SCRIPT
2026-10-24T15:22:04.1036644Z ##[debug]loading INPUT_WORKINGDIRECTORY
2026-10-24T15:22:04.1037216Z ##[debug]loading INPUT_FAILONSTDERR
2026-10-24T15:22:04.1038040Z ##[debug]loading ENDPOINT_AUTH_SYSTEMVSSCONNECTION
2026-10-24T15:22:04.1038603Z ##[debug]loading ENDPOINT_AUTH_SCHEME_SYSTEMVSSCONNECTION
2026-10-24T15:22:04.1040577Z ##[debug]loading ENDPOINT_AUTH_PARAMETER_SYSTEMVSSCONNECTION_ACCESSTOKEN
2026-10-24T15:22:04.1047192Z ##[debug]loading SECRET_TOKEN_CRQ
2026-10-24T15:22:04.1048232Z ##[debug]loading SECRET_GRAYLOG_PASSWORD
2026-10-24T15:22:04.1050453Z ##[debug]loading SECRET_FORTIFY_APITOKEN
2026-10-24T15:22:04.1051767Z ##[debug]loading SECRET_PW_ISILON
2026-10-24T15:22:04.1054450Z ##[debug]loading SECRET_ALOCAIP_SENHA
2026-10-24T15:22:04.1054760Z ##[debug]loading SECRET_SCOWDB01
2026-10-24T15:22:04.1055464Z ##[debug]loading SECRET_PW_ALOCAIP
2026-10-24T15:22:04.1055768Z ##[debug]loading SECRET_OKD_TOKEN_KAFKA
2026-10-24T15:22:04.1056286Z ##[debug]loading SECRET_FORTIFY_PASS
2026-10-24T15:22:04.1056966Z ##[debug]loading SECRET_PASSWORD_CGC
2026-10-24T15:22:04.1057548Z ##[debug]loading SECRET_AZPAT
2026-10-24T15:22:04.1058134Z ##[debug]loading SECRET_BT_SECRETS_PATH
2026-10-24T15:22:04.1059452Z ##[debug]loading SECRET_OKD_TOKEN_REGISTRY
2026-10-24T15:22:04.1059953Z ##[debug]loading SECRET_OKD_4_TOKEN
2026-10-24T15:22:04.1060467Z ##[debug]loaded 22
2026-10-24T15:22:04.1065510Z ##[debug]Agent.ProxyUrl=undefined
2026-10-24T15:22:04.1065859Z ##[debug]Agent.CAInfo=undefined
2026-10-24T15:22:04.1066151Z ##[debug]Agent.ClientCert=undefined
2026-10-24T15:22:04.1066411Z ##[debug]Agent.SkipCertValidation=True
2026-10-24T15:22:04.1081167Z ##[debug]check path : /opt/ads-agent/_work/_tasks/Bash_6c731c3c-3c68-459a-a5c9-bde6e6595b5b/3.227.0/task.json
2026-10-24T15:22:04.1083649Z ##[debug]adding resource file: /opt/ads-agent/_work/_tasks/Bash_6c731c3c-3c68-459a-a5c9-bde6e6595b5b/3.227.0/task.json
2026-10-24T15:22:04.1083985Z ##[debug]system.culture=en-US
2026-10-24T15:22:04.1091517Z ##[debug]failOnStderr=false
2026-10-24T15:22:04.1092826Z ##[debug]workingDirectory=/opt/ads-agent/_work/r934/a
2026-10-24T15:22:04.1093151Z ##[debug]check path : /opt/ads-agent/_work/r934/a
2026-10-24T15:22:04.1094016Z ##[debug]targetType=inline
2026-10-24T15:22:04.1094481Z ##[debug]bashEnvValue=undefined
2026-10-24T15:22:04.1095477Z ##[debug]script=#!/bin/bash
set -o errexit
set -o pipefail
set -x

shopt -s expand_aliases

if [[ -n "$SITE" && "okd4_nprd" =~ "ocp" ]]
then
  app="sicow-conres-okd-des"

  arquivo="/usr/local/bin/oc-v4.13"
  if [ -e "$arquivo" ]; then 
    alias oc="$arquivo"
  fi
elif [[ -n "$SITE" && "$SITE" =~ (okd4|openshift) ]];
then
app="sicow-conres-okd-des"
else
  app="sicow-conres-okd-des-esteiras"
fi

oc version

last_pod=$(oc get pod -l name="$app" -n sicow-des -o jsonpath='{range .items[*]}{.metadata.name}{"\n"}' --sort-by=.metadata.creationTimestamp  | tac | grep -v '^$' | head -n1)

echo "Logs do POD: $last_pod"
oc logs $last_pod -c "$app" -n sicow-des
2026-10-24T15:22:04.1102872Z Generating script.
2026-10-24T15:22:04.1104711Z ##[debug]which 'bash'
2026-10-24T15:22:04.1111634Z ##[debug]found: '/usr/bin/bash'
2026-10-24T15:22:04.1111905Z ##[debug]Agent.Version=3.236.1
2026-10-24T15:22:04.1112203Z ##[debug]agent.tempDirectory=/opt/ads-agent/_work/_temp
2026-10-24T15:22:04.1112511Z ##[debug]check path : /opt/ads-agent/_work/_temp
2026-10-24T15:22:04.1114838Z ========================== Starting Command Output ===========================
2026-10-24T15:22:04.1115474Z ##[debug]which '/usr/bin/bash'
2026-10-24T15:22:04.1115996Z ##[debug]found: '/usr/bin/bash'
2026-10-24T15:22:04.1116705Z ##[debug]/usr/bin/bash arg: /opt/ads-agent/_work/_temp/af48e13e-fc39-4e16-9337-5025786e583f.sh
2026-10-24T15:22:04.1118431Z ##[debug]exec tool: /usr/bin/bash
2026-10-24T15:22:04.1118931Z ##[debug]arguments:
2026-10-24T15:22:04.1119390Z ##[debug]   /opt/ads-agent/_work/_temp/af48e13e-fc39-4e16-9337-5025786e583f.sh
2026-10-24T15:22:04.1120877Z [command]/usr/bin/bash /opt/ads-agent/_work/_temp/af48e13e-fc39-4e16-9337-5025786e583f.sh
2026-10-24T15:22:04.1193385Z + shopt -s expand_aliases
2026-10-24T15:22:04.1193625Z + [[ -n okd4_nprd ]]
2026-10-24T15:22:04.1193731Z + [[ okd4_nprd =~ ocp ]]
2026-10-24T15:22:04.1193897Z + [[ -n okd4_nprd ]]
2026-10-24T15:22:04.1194038Z + [[ okd4_nprd =~ (okd4|openshift) ]]
2026-10-24T15:22:04.1194223Z + app=sicow-conres-okd-des
2026-10-24T15:22:04.1194359Z + oc version
2026-10-24T15:22:04.1947944Z Client Version: v4.2.0-alpha.0-1394-g45460a5
2026-10-24T15:22:04.1948242Z Server Version: 4.12.0-0.okd-2023-04-16-041331
2026-10-24T15:22:04.1948467Z Kubernetes Version: v1.25.0-2824+27e744f55d2e99-dirty
2026-10-24T15:22:04.1976866Z ++ oc get pod -l name=sicow-conres-okd-des -n sicow-des -o 'jsonpath={range .items[*]}{.metadata.name}{"\n"}' --sort-by=.metadata.creationTimestamp
2026-10-24T15:22:04.1977106Z ++ tac
2026-10-24T15:22:04.1978021Z ++ grep -v '^$'
2026-10-24T15:22:04.1978941Z ++ head -n1
2026-10-24T15:22:04.2786093Z + last_pod=sicow-conres-okd-des-29-48wkr
2026-10-24T15:22:04.2786455Z + echo 'Logs do POD: sicow-conres-okd-des-29-48wkr'
2026-10-24T15:22:04.2786698Z + oc logs sicow-conres-okd-des-29-48wkr -c sicow-conres-okd-des -n sicow-des
2026-10-24T15:22:04.2786922Z Logs do POD: sicow-conres-okd-des-29-48wkr
2026-10-24T15:22:04.3653609Z =========================================================================
2026-10-24T15:22:04.3653754Z 
2026-10-24T15:22:04.3654581Z   JBoss Bootstrap Environment
2026-10-24T15:22:04.3654633Z 
2026-10-24T15:22:04.3654802Z   JBOSS_HOME: /opt/jboss
2026-10-24T15:22:04.3654846Z 
2026-10-24T15:22:04.3655320Z   JAVA: /usr/lib/jvm/java-1.8.0-openjdk-1.8.0.372.b07-1.el7_9.x86_64/jre/bin/java
2026-10-24T15:22:04.3655437Z 
2026-10-24T15:22:04.3657088Z   JAVA_OPTS:  -verbose:gc -Xloggc:"/opt/jboss/standalone/log/gc.log" -XX:+PrintGCDetails -XX:+PrintGCDateStamps -XX:+UseGCLogFileRotation -XX:NumberOfGCLogFiles=5 -XX:GCLogFileSize=3M -XX:-TraceClassUnloading -Xms1024m -Xmx1024m -XX:MetaspaceSize=96m -XX:MaxMetaspaceSize=512m -Djava.net.preferIPv4Stack=true -Djboss.modules.system.pkgs=org.jboss.byteman -Djava.awt.headless=true -Djavax.net.ssl.trustStore=/opt/jboss/standalone/configuration/caixa-truststore-acteste-nprd.jks -Djavax.net.ssl.trustStorePassword=changeit -Dhttps.proxyHost=proxydes.caixa -Dhttps.proxyPort=80 -Dhttp.proxyHost=proxydes.caixa -Dhttp.proxyPort=80 -Dhttp.nonProxyHosts=*.caixa -Djboss.modules.policy-permissions=true -server -XX:+ExplicitGCInvokesConcurrent -XX:+UseG1GC -XX:MaxGCPauseMillis=500 -Xbootclasspath/p:/opt/jboss/modules/system/layers/base/org/wildfly/common/main/wildfly-common-1.5.4.Final-redhat-00001.jar -Xbootclasspath/p:/opt/jboss/modules/system/layers/base/org/jboss/logmanager/main/jboss-logmanager-2.1.18.Final-redhat-00001.jar -Djboss.modules.system.pkgs=org.jboss.byteman,org.jboss.logmanager -Djava.util.logging.manager=org.jboss.logmanager.LogManager -javaagent:/opt/jmx_exporter/jmx_prometheus.jar=8778:/opt/jmx_exporter/jmx_prometheus.yaml -javaagent:/opt/jboss/standalone/deployments/applicationinsights-agent-3.7.1.jar -Djava.net.useSystemProxies=false -Dhttp.proxyHost=proxydes.caixa -Dhttp.proxyPort=80 -Dhttps.proxyHost=proxydes.caixa -Dhttps.proxyPort=80 -Dhttp.nonProxyHosts=localhost\|127.0.0.1\|*.caixa 
2026-10-24T15:22:04.3658362Z 
2026-10-24T15:22:04.3658512Z =========================================================================
2026-10-24T15:22:04.3658584Z 
2026-10-24T15:22:04.3658939Z OpenJDK 64-Bit Server VM warning: If the number of processors is expected to increase from one, then you should configure the number of parallel GC threads appropriately using -XX:ParallelGCThreads=N
2026-10-24T15:22:04.3659530Z 2026-10-24 12:21:28.149-03:00 WARN  i.o.s.a.ResourceConfiguration - Found reference to io.opentelemetry.sdk.autoconfigure.internal.EnvironmentResourceProvider in otel.java.enabled.resource.providers. Please update to io.opentelemetry.sdk.autoconfigure.EnvironmentResourceProvider. Support for the old provider name will be removed after 1.49.0.
2026-10-24T15:22:04.3660078Z 2026-10-24 12:21:46.154-03:00 INFO  c.m.applicationinsights.agent - Application Insights Java Agent 3.7.1 started successfully (PID 171, JVM running for 32.692 s)
2026-10-24T15:22:04.3660485Z 2026-10-24 12:21:46.156-03:00 INFO  c.m.applicationinsights.agent - Java version: 1.8.0_372, vendor: Red Hat, Inc., home: /usr/lib/jvm/java-1.8.0-openjdk-1.8.0.372.b07-1.el7_9.x86_64/jre
2026-10-24T15:22:04.3660823Z [0m12:21:47,640 INFO  [org.jboss.modules] (main) JBoss Modules version 1.12.0.Final-redhat-00001
2026-10-24T15:22:04.3661102Z [0m[0m12:21:48,822 INFO  [org.jboss.msc] (main) JBoss MSC version 1.4.12.Final-redhat-00001
2026-10-24T15:22:04.3661383Z [0m[0m12:21:48,938 INFO  [org.jboss.threads] (main) JBoss Threads version 2.4.0.Final-redhat-00001
2026-10-24T15:22:04.3661719Z [0m[0m12:21:49,453 INFO  [org.jboss.as] (MSC service thread 1-2) WFLYSRV0049: JBoss EAP 7.4.11.GA (WildFly Core 15.0.26.Final-redhat-00001) starting
2026-10-24T15:22:04.3662076Z [0m[0m12:21:49,732 INFO  [org.jboss.vfs] (MSC service thread 1-2) VFS000002: Failed to clean existing content for temp file provider of type temp. Enable DEBUG level log to find what caused this
2026-10-24T15:22:04.3662550Z [0m[33m12:21:50,528 WARN  [org.jboss.as.controller] (Controller Boot Thread) WFLYCTL0456: System property "user.timezone" is already set in the <system-properties> section of the configuration file. The value set in the command line will be overridden by that value.
2026-10-24T15:22:04.3663071Z [0m[0m12:21:52,948 INFO  [org.wildfly.security] (ServerService Thread Pool -- 31) ELY00001: WildFly Elytron version 1.15.16.Final-redhat-00001
2026-10-24T15:22:04.3663466Z [0m[0m12:21:53,821 INFO  [org.jboss.as.controller.management-deprecated] (ServerService Thread Pool -- 23) WFLYCTL0033: Extension 'security' is deprecated and may not be supported in future versions
2026-10-24T15:22:04.3664146Z [0m[0m12:21:55,549 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'security-realm' in the resource at address '/core-service=management/management-interface=native-interface' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-10-24T15:22:04.3664863Z [0m[0m12:21:55,551 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'security-realm' in the resource at address '/core-service=management/management-interface=http-interface' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-10-24T15:22:04.3666043Z [0m[0m12:21:55,719 INFO  [org.jboss.as.controller.management-deprecated] (ServerService Thread Pool -- 8) WFLYCTL0028: Attribute 'security-realm' in the resource at address '/subsystem=undertow/server=default-server/https-listener=https' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-10-24T15:22:04.3666662Z [0m[0m12:21:56,461 INFO  [org.jboss.as.repository] (ServerService Thread Pool -- 27) WFLYDR0001: Content added at location /opt/jboss/standalone/data/content/43/10e3eda419b2f2c7d4fb432f9cf7908f535920/content
2026-10-24T15:22:04.3667094Z [0m[0m12:21:57,029 INFO  [org.jboss.as.repository] (ServerService Thread Pool -- 27) WFLYDR0001: Content added at location /opt/jboss/standalone/data/content/8f/a714485f427852e3aa59ff367a6b9db506f167/content
2026-10-24T15:22:04.3667757Z [0m[31m12:21:57,135 ERROR [org.jboss.as.controller.management-operation] (Controller Boot Thread) WFLYCTL0013: Operation ("add") failed - address: ([("core-service" => "vault")]): org.jboss.as.server.services.security.VaultReaderException: WFLYSRV0076: Error initializing vault --  org.jboss.security.vault.SecurityVaultException: java.lang.RuntimeException: PBOX00140: Unable to get keystore (/opt/jboss/standalone/configuration/vault-sicow-des.keystore)
2026-10-24T15:22:04.3668216Z 	at org.jboss.as.server.services.security.VaultReaderImpl.createVault(RuntimeVaultReader.java:159)
2026-10-24T15:22:04.3668467Z 	at org.jboss.as.server.services.security.RuntimeVaultReader.createVault(RuntimeVaultReader.java:100)
2026-10-24T15:22:04.3668706Z 	at org.jboss.as.server.services.security.VaultAddHandler.performRuntime(VaultAddHandler.java:96)
2026-10-24T15:22:04.3668945Z 	at org.jboss.as.controller.AbstractAddStepHandler.performRuntime(AbstractAddStepHandler.java:343)
2026-10-24T15:22:04.3669180Z 	at org.jboss.as.controller.AbstractAddStepHandler$1.execute(AbstractAddStepHandler.java:164)
2026-10-24T15:22:04.3669384Z 	at org.jboss.as.controller.AbstractOperationContext.executeStep(AbstractOperationContext.java:1047)
2026-10-24T15:22:04.3669630Z 	at org.jboss.as.controller.AbstractOperationContext.processStages(AbstractOperationContext.java:779)
2026-10-24T15:22:04.3669872Z 	at org.jboss.as.controller.AbstractOperationContext.executeOperation(AbstractOperationContext.java:468)
2026-10-24T15:22:04.3670111Z 	at org.jboss.as.controller.OperationContextImpl.executeOperation(OperationContextImpl.java:1431)
2026-10-24T15:22:04.3670336Z 	at org.jboss.as.controller.ModelControllerImpl.boot(ModelControllerImpl.java:559)
2026-10-24T15:22:04.3670561Z 	at org.jboss.as.controller.AbstractControllerService.boot(AbstractControllerService.java:546)
2026-10-24T15:22:04.3670785Z 	at org.jboss.as.controller.AbstractControllerService.boot(AbstractControllerService.java:508)
2026-10-24T15:22:04.3670999Z 	at org.jboss.as.server.ServerService.boot(ServerService.java:464)
2026-10-24T15:22:04.3671196Z 	at org.jboss.as.server.ServerService.boot(ServerService.java:417)
2026-10-24T15:22:04.3671377Z 	at org.jboss.as.controller.AbstractControllerService$1.run(AbstractControllerService.java:447)
2026-10-24T15:22:04.3671578Z 	at java.lang.Thread.run(Thread.java:750)
2026-10-24T15:22:04.3671946Z Caused by: org.jboss.security.vault.SecurityVaultException: java.lang.RuntimeException: PBOX00140: Unable to get keystore (/opt/jboss/standalone/configuration/vault-sicow-des.keystore)
2026-10-24T15:22:04.3672335Z 	at org.picketbox.plugins.vault.PicketBoxSecurityVault.init(PicketBoxSecurityVault.java:210)
2026-10-24T15:22:04.3672649Z 	at org.jboss.as.server.services.security.VaultReaderImpl.createVault(RuntimeVaultReader.java:157)
2026-10-24T15:22:04.3672840Z 	... 15 more
2026-10-24T15:22:04.3673126Z Caused by: java.lang.RuntimeException: PBOX00140: Unable to get keystore (/opt/jboss/standalone/configuration/vault-sicow-des.keystore)
2026-10-24T15:22:04.3673361Z 	at org.picketbox.plugins.vault.PicketBoxSecurityVault.getKeyStore(PicketBoxSecurityVault.java:691)
2026-10-24T15:22:04.3673591Z 	at org.picketbox.plugins.vault.PicketBoxSecurityVault.init(PicketBoxSecurityVault.java:205)
2026-10-24T15:22:04.3673780Z 	... 16 more
2026-10-24T15:22:04.3674053Z Caused by: java.io.FileNotFoundException: /opt/jboss/standalone/configuration/vault-sicow-des.keystore (No such file or directory)
2026-10-24T15:22:04.3674247Z 	at java.io.FileInputStream.open0(Native Method)
2026-10-24T15:22:04.3674419Z 	at java.io.FileInputStream.open(FileInputStream.java:195)
2026-10-24T15:22:04.3674606Z 	at java.io.FileInputStream.<init>(FileInputStream.java:138)
2026-10-24T15:22:04.3674802Z 	at org.picketbox.util.KeyStoreUtil.getKeyStore(KeyStoreUtil.java:150)
2026-10-24T15:22:04.3675015Z 	at org.picketbox.plugins.vault.PicketBoxSecurityVault.getKeyStore(PicketBoxSecurityVault.java:688)
2026-10-24T15:22:04.3675191Z 	... 17 more
2026-10-24T15:22:04.3675233Z 
2026-10-24T15:22:04.3675549Z [0m[31m12:21:57,152 FATAL [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0056: Server boot has failed in an unrecoverable manner; exiting. See previous messages for details.
2026-10-24T15:22:04.3675971Z [0m[0m12:21:57,338 INFO  [org.jboss.as] (MSC service thread 1-2) WFLYSRV0050: JBoss EAP 7.4.11.GA (WildFly Core 15.0.26.Final-redhat-00001) stopped in 111ms
2026-10-24T15:22:04.3692808Z ##[debug]Exit code 0 received from tool '/usr/bin/bash'
2026-10-24T15:22:04.3695632Z ##[debug]STDIO streams have closed for tool '/usr/bin/bash'
2026-10-24T15:22:04.3700871Z ##[debug]task result: Succeeded
2026-10-24T15:22:04.3701819Z ##[debug]Processed: ##vso[task.complete result=Succeeded;done=true;]
2026-10-24T15:22:04.3732438Z ##[section]Finishing: Logs da Aplicação



falhou novamente
