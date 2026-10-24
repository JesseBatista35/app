2026-10-24T14:44:45.5521942Z ##[debug]Evaluating condition for step: 'Verificando Status do Deployment'
2026-10-24T14:44:45.5522387Z ##[debug]Evaluating: succeeded()
2026-10-24T14:44:45.5522832Z ##[debug]Evaluating succeeded:
2026-10-24T14:44:45.5523113Z ##[debug]=> True
2026-10-24T14:44:45.5523295Z ##[debug]Result: True
2026-10-24T14:44:45.5523475Z ##[section]Starting: Verificando Status do Deployment
2026-10-24T14:44:45.5527243Z ==============================================================================
2026-10-24T14:44:45.5527379Z Task         : Bash
2026-10-24T14:44:45.5527456Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-24T14:44:45.5527580Z Version      : 3.227.0
2026-10-24T14:44:45.5527656Z Author       : Microsoft Corporation
2026-10-24T14:44:45.5527749Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-24T14:44:45.5527889Z ==============================================================================
2026-10-24T14:44:45.6101507Z ##[debug]Using node path: /opt/ads-agent/externals/node16/bin/node
2026-10-24T14:44:45.6336908Z ##[debug]Agent environment resources - Disk: / Available 63372.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 21.80%
2026-10-24T14:44:45.6878501Z ##[debug]agent.TempDirectory=/opt/ads-agent/_work/_temp
2026-10-24T14:44:45.6893234Z ##[debug]loading inputs and endpoints
2026-10-24T14:44:45.6898067Z ##[debug]loading INPUT_TARGETTYPE
2026-10-24T14:44:45.6902693Z ##[debug]loading INPUT_FILEPATH
2026-10-24T14:44:45.6904011Z ##[debug]loading INPUT_SCRIPT
2026-10-24T14:44:45.6904692Z ##[debug]loading INPUT_WORKINGDIRECTORY
2026-10-24T14:44:45.6905205Z ##[debug]loading INPUT_FAILONSTDERR
2026-10-24T14:44:45.6906228Z ##[debug]loading ENDPOINT_AUTH_SYSTEMVSSCONNECTION
2026-10-24T14:44:45.6906898Z ##[debug]loading ENDPOINT_AUTH_SCHEME_SYSTEMVSSCONNECTION
2026-10-24T14:44:45.6909235Z ##[debug]loading ENDPOINT_AUTH_PARAMETER_SYSTEMVSSCONNECTION_ACCESSTOKEN
2026-10-24T14:44:45.6915106Z ##[debug]loading SECRET_TOKEN_CRQ
2026-10-24T14:44:45.6916285Z ##[debug]loading SECRET_SCOWDB01
2026-10-24T14:44:45.6917792Z ##[debug]loading SECRET_OKD_TOKEN_KAFKA
2026-10-24T14:44:45.6919713Z ##[debug]loading SECRET_BT_SECRETS_PATH
2026-10-24T14:44:45.6922481Z ##[debug]loading SECRET_PW_ISILON
2026-10-24T14:44:45.6923624Z ##[debug]loading SECRET_PW_ALOCAIP
2026-10-24T14:44:45.6924194Z ##[debug]loading SECRET_OKD_4_TOKEN
2026-10-24T14:44:45.6924944Z ##[debug]loading SECRET_AZPAT
2026-10-24T14:44:45.6925565Z ##[debug]loading SECRET_PASSWORD_CGC
2026-10-24T14:44:45.6926145Z ##[debug]loading SECRET_GRAYLOG_PASSWORD
2026-10-24T14:44:45.6926696Z ##[debug]loading SECRET_OKD_TOKEN_REGISTRY
2026-10-24T14:44:45.6927292Z ##[debug]loading SECRET_FORTIFY_PASS
2026-10-24T14:44:45.6928978Z ##[debug]loading SECRET_FORTIFY_APITOKEN
2026-10-24T14:44:45.6929415Z ##[debug]loading SECRET_ALOCAIP_SENHA
2026-10-24T14:44:45.6929914Z ##[debug]loaded 22
2026-10-24T14:44:45.6936405Z ##[debug]Agent.ProxyUrl=undefined
2026-10-24T14:44:45.6936836Z ##[debug]Agent.CAInfo=undefined
2026-10-24T14:44:45.6937162Z ##[debug]Agent.ClientCert=undefined
2026-10-24T14:44:45.6937392Z ##[debug]Agent.SkipCertValidation=True
2026-10-24T14:44:45.6954384Z ##[debug]check path : /opt/ads-agent/_work/_tasks/Bash_6c731c3c-3c68-459a-a5c9-bde6e6595b5b/3.227.0/task.json
2026-10-24T14:44:45.6956333Z ##[debug]adding resource file: /opt/ads-agent/_work/_tasks/Bash_6c731c3c-3c68-459a-a5c9-bde6e6595b5b/3.227.0/task.json
2026-10-24T14:44:45.6956619Z ##[debug]system.culture=en-US
2026-10-24T14:44:45.6965576Z ##[debug]failOnStderr=false
2026-10-24T14:44:45.6967676Z ##[debug]workingDirectory=/opt/ads-agent/_work/r934/a
2026-10-24T14:44:45.6967930Z ##[debug]check path : /opt/ads-agent/_work/r934/a
2026-10-24T14:44:45.6968734Z ##[debug]targetType=inline
2026-10-24T14:44:45.6968969Z ##[debug]bashEnvValue=undefined
2026-10-24T14:44:45.6969609Z ##[debug]script=if [[ -n "$SITE" && "$SITE" =~ (okd4|ocp|openshift) ]];
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
2026-10-24T14:44:45.6982194Z Generating script.
2026-10-24T14:44:45.6984394Z ##[debug]which 'bash'
2026-10-24T14:44:45.6990653Z ##[debug]found: '/usr/bin/bash'
2026-10-24T14:44:45.6991161Z ##[debug]Agent.Version=3.236.1
2026-10-24T14:44:45.6991410Z ##[debug]agent.tempDirectory=/opt/ads-agent/_work/_temp
2026-10-24T14:44:45.6991664Z ##[debug]check path : /opt/ads-agent/_work/_temp
2026-10-24T14:44:45.6995197Z ========================== Starting Command Output ===========================
2026-10-24T14:44:45.6996852Z ##[debug]which '/usr/bin/bash'
2026-10-24T14:44:45.6998040Z ##[debug]found: '/usr/bin/bash'
2026-10-24T14:44:45.6998909Z ##[debug]/usr/bin/bash arg: /opt/ads-agent/_work/_temp/5724b2d7-207c-4cfe-b493-9569cc6bc2de.sh
2026-10-24T14:44:45.7001845Z ##[debug]exec tool: /usr/bin/bash
2026-10-24T14:44:45.7002084Z ##[debug]arguments:
2026-10-24T14:44:45.7002325Z ##[debug]   /opt/ads-agent/_work/_temp/5724b2d7-207c-4cfe-b493-9569cc6bc2de.sh
2026-10-24T14:44:45.7004810Z [command]/usr/bin/bash /opt/ads-agent/_work/_temp/5724b2d7-207c-4cfe-b493-9569cc6bc2de.sh
2026-10-24T14:44:45.7962573Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-10-24T14:44:47.6749151Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-10-24T14:44:47.7400609Z Waiting for rollout to finish: 1 old replicas are pending termination...
2026-10-24T14:44:50.6345678Z ##[debug]Agent environment resources - Disk: / Available 63379.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 19.51%
2026-10-24T14:44:55.6354565Z ##[debug]Agent environment resources - Disk: / Available 63379.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 17.61%
2026-10-24T14:45:00.6367839Z ##[debug]Agent environment resources - Disk: / Available 63379.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 16.07%
2026-10-24T14:45:05.6381161Z ##[debug]Agent environment resources - Disk: / Available 63499.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 14.78%
2026-10-24T14:45:10.6382428Z ##[debug]Agent environment resources - Disk: / Available 63497.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 13.67%
2026-10-24T14:45:15.6395802Z ##[debug]Agent environment resources - Disk: / Available 63499.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 12.73%
2026-10-24T14:45:20.6429938Z ##[debug]Agent environment resources - Disk: / Available 63499.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 11.92%
2026-10-24T14:45:25.6434298Z ##[debug]Agent environment resources - Disk: / Available 63497.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 11.19%
2026-10-24T14:45:30.6442551Z ##[debug]Agent environment resources - Disk: / Available 63489.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 10.57%
2026-10-24T14:45:35.6470095Z ##[debug]Agent environment resources - Disk: / Available 63489.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 10.03%
2026-10-24T14:45:40.6477370Z ##[debug]Agent environment resources - Disk: / Available 63486.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 9.55%
2026-10-24T14:45:45.6560846Z ##[debug]Agent environment resources - Disk: / Available 63485.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 9.08%
2026-10-24T14:45:50.6569810Z ##[debug]Agent environment resources - Disk: / Available 63475.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 8.67%
2026-10-24T14:45:55.6570874Z ##[debug]Agent environment resources - Disk: / Available 63478.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 8.29%
2026-10-24T14:46:00.6571859Z ##[debug]Agent environment resources - Disk: / Available 63480.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 7.95%
2026-10-24T14:46:05.6573548Z ##[debug]Agent environment resources - Disk: / Available 63480.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 7.63%
2026-10-24T14:46:10.6583089Z ##[debug]Agent environment resources - Disk: / Available 63477.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 7.33%
2026-10-24T14:46:15.6594250Z ##[debug]Agent environment resources - Disk: / Available 63480.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 7.07%
2026-10-24T14:46:20.6602031Z ##[debug]Agent environment resources - Disk: / Available 63480.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 6.81%
2026-10-24T14:46:25.6609241Z ##[debug]Agent environment resources - Disk: / Available 63480.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 6.58%
2026-10-24T14:46:30.6621697Z ##[debug]Agent environment resources - Disk: / Available 63478.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 6.36%
2026-10-24T14:46:35.6622070Z ##[debug]Agent environment resources - Disk: / Available 63471.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 6.16%
2026-10-24T14:46:40.6627993Z ##[debug]Agent environment resources - Disk: / Available 63463.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 5.97%
2026-10-24T14:46:45.6643336Z ##[debug]Agent environment resources - Disk: / Available 63463.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 5.79%
2026-10-24T14:46:50.6651496Z ##[debug]Agent environment resources - Disk: / Available 63460.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 5.62%
2026-10-24T14:46:55.6650628Z ##[debug]Agent environment resources - Disk: / Available 63463.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 5.46%
2026-10-24T14:47:00.6659790Z ##[debug]Agent environment resources - Disk: / Available 63454.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 5.31%
2026-10-24T14:47:05.6667541Z ##[debug]Agent environment resources - Disk: / Available 63459.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 5.17%
2026-10-24T14:47:10.6675651Z ##[debug]Agent environment resources - Disk: / Available 63446.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 5.04%
2026-10-24T14:47:15.6687050Z ##[debug]Agent environment resources - Disk: / Available 63447.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 4.90%
2026-10-24T14:47:20.6694693Z ##[debug]Agent environment resources - Disk: / Available 63447.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 4.79%
2026-10-24T14:47:25.6709258Z ##[debug]Agent environment resources - Disk: / Available 63463.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 4.67%
2026-10-24T14:47:30.6716154Z ##[debug]Agent environment resources - Disk: / Available 63462.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 4.56%
2026-10-24T14:47:35.6724243Z ##[debug]Agent environment resources - Disk: / Available 63463.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 4.46%
2026-10-24T14:47:40.6733688Z ##[debug]Agent environment resources - Disk: / Available 63463.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 4.36%
2026-10-24T14:47:45.6743756Z ##[debug]Agent environment resources - Disk: / Available 63463.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 4.26%
2026-10-24T14:47:50.6752879Z ##[debug]Agent environment resources - Disk: / Available 63463.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 4.17%
2026-10-24T14:47:55.6769019Z ##[debug]Agent environment resources - Disk: / Available 63460.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 4.09%
2026-10-24T14:48:00.6774663Z ##[debug]Agent environment resources - Disk: / Available 63451.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 4.01%
2026-10-24T14:48:05.6787926Z ##[debug]Agent environment resources - Disk: / Available 63453.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.93%
2026-10-24T14:48:10.6790700Z ##[debug]Agent environment resources - Disk: / Available 63450.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.85%
2026-10-24T14:48:15.6805506Z ##[debug]Agent environment resources - Disk: / Available 63449.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.77%
2026-10-24T14:48:20.6812763Z ##[debug]Agent environment resources - Disk: / Available 63451.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.71%
2026-10-24T14:48:25.6823816Z ##[debug]Agent environment resources - Disk: / Available 63451.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.64%
2026-10-24T14:48:30.6839627Z ##[debug]Agent environment resources - Disk: / Available 63449.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.58%
2026-10-24T14:48:35.6850156Z ##[debug]Agent environment resources - Disk: / Available 63438.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.51%
2026-10-24T14:48:40.6855297Z ##[debug]Agent environment resources - Disk: / Available 63437.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.45%
2026-10-24T14:48:45.6865908Z ##[debug]Agent environment resources - Disk: / Available 63439.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.39%
2026-10-24T14:48:50.6877107Z ##[debug]Agent environment resources - Disk: / Available 63438.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.34%
2026-10-24T14:48:55.6882976Z ##[debug]Agent environment resources - Disk: / Available 63439.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.28%
2026-10-24T14:49:00.6896895Z ##[debug]Agent environment resources - Disk: / Available 63436.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.23%
2026-10-24T14:49:05.6909774Z ##[debug]Agent environment resources - Disk: / Available 63439.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.18%
2026-10-24T14:49:10.6916264Z ##[debug]Agent environment resources - Disk: / Available 63437.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.13%
2026-10-24T14:49:15.6924824Z ##[debug]Agent environment resources - Disk: / Available 63438.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.08%
2026-10-24T14:49:20.6936422Z ##[debug]Agent environment resources - Disk: / Available 63439.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 3.04%
2026-10-24T14:49:25.6944534Z ##[debug]Agent environment resources - Disk: / Available 63439.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.99%
2026-10-24T14:49:30.6965338Z ##[debug]Agent environment resources - Disk: / Available 63430.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.95%
2026-10-24T14:49:35.6964834Z ##[debug]Agent environment resources - Disk: / Available 63427.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.91%
2026-10-24T14:49:40.6977804Z ##[debug]Agent environment resources - Disk: / Available 63428.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.87%
2026-10-24T14:49:45.6979809Z ##[debug]Agent environment resources - Disk: / Available 63425.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.83%
2026-10-24T14:49:50.6989255Z ##[debug]Agent environment resources - Disk: / Available 63424.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.79%
2026-10-24T14:49:55.6997924Z ##[debug]Agent environment resources - Disk: / Available 63425.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.75%
2026-10-24T14:50:00.7008534Z ##[debug]Agent environment resources - Disk: / Available 63425.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.72%
2026-10-24T14:50:05.7015892Z ##[debug]Agent environment resources - Disk: / Available 63415.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.68%
2026-10-24T14:50:10.7025776Z ##[debug]Agent environment resources - Disk: / Available 63416.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.65%
2026-10-24T14:50:15.7034429Z ##[debug]Agent environment resources - Disk: / Available 63417.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.61%
2026-10-24T14:50:20.7041846Z ##[debug]Agent environment resources - Disk: / Available 63413.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.58%
2026-10-24T14:50:25.7046048Z ##[debug]Agent environment resources - Disk: / Available 63416.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.55%
2026-10-24T14:50:30.7058591Z ##[debug]Agent environment resources - Disk: / Available 63428.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.52%
2026-10-24T14:50:35.7065192Z ##[debug]Agent environment resources - Disk: / Available 63427.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.49%
2026-10-24T14:50:40.7077286Z ##[debug]Agent environment resources - Disk: / Available 63427.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 2.46%
2026-10-24T14:50:45.5572526Z ##[debug]Started cancellation of executing script
2026-10-24T14:50:45.5579907Z ##[debug]Exit code null received from tool '/usr/bin/bash'
2026-10-24T14:50:53.0631534Z ##[error]The task has timed out.
2026-10-24T14:50:53.0632442Z ##[section]Finishing: Verificando Status do Deployment



2026-10-24T14:50:53.0657513Z ##[debug]Evaluating condition for step: 'Logs da Aplicação'
2026-10-24T14:50:53.0658200Z ##[debug]Evaluating: always()
2026-10-24T14:50:53.0658348Z ##[debug]Evaluating always:
2026-10-24T14:50:53.0659225Z ##[debug]=> True
2026-10-24T14:50:53.0659436Z ##[debug]Result: True
2026-10-24T14:50:53.0659616Z ##[section]Starting: Logs da Aplicação
2026-10-24T14:50:53.0662705Z ==============================================================================
2026-10-24T14:50:53.0662788Z Task         : Bash
2026-10-24T14:50:53.0662831Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-24T14:50:53.0662905Z Version      : 3.227.0
2026-10-24T14:50:53.0662949Z Author       : Microsoft Corporation
2026-10-24T14:50:53.0663098Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-24T14:50:53.0663183Z ==============================================================================
2026-10-24T14:50:53.1192234Z ##[debug]Using node path: /opt/ads-agent/externals/node16/bin/node
2026-10-24T14:50:53.1981330Z ##[debug]agent.TempDirectory=/opt/ads-agent/_work/_temp
2026-10-24T14:50:53.1990952Z ##[debug]loading inputs and endpoints
2026-10-24T14:50:53.1998767Z ##[debug]loading INPUT_TARGETTYPE
2026-10-24T14:50:53.2006273Z ##[debug]loading INPUT_FILEPATH
2026-10-24T14:50:53.2007393Z ##[debug]loading INPUT_SCRIPT
2026-10-24T14:50:53.2008058Z ##[debug]loading INPUT_WORKINGDIRECTORY
2026-10-24T14:50:53.2008667Z ##[debug]loading INPUT_FAILONSTDERR
2026-10-24T14:50:53.2009351Z ##[debug]loading ENDPOINT_AUTH_SYSTEMVSSCONNECTION
2026-10-24T14:50:53.2010361Z ##[debug]loading ENDPOINT_AUTH_SCHEME_SYSTEMVSSCONNECTION
2026-10-24T14:50:53.2012436Z ##[debug]loading ENDPOINT_AUTH_PARAMETER_SYSTEMVSSCONNECTION_ACCESSTOKEN
2026-10-24T14:50:53.2017717Z ##[debug]loading SECRET_TOKEN_CRQ
2026-10-24T14:50:53.2019234Z ##[debug]loading SECRET_SCOWDB01
2026-10-24T14:50:53.2020705Z ##[debug]loading SECRET_OKD_TOKEN_KAFKA
2026-10-24T14:50:53.2022533Z ##[debug]loading SECRET_BT_SECRETS_PATH
2026-10-24T14:50:53.2024407Z ##[debug]loading SECRET_PW_ISILON
2026-10-24T14:50:53.2025463Z ##[debug]loading SECRET_PW_ALOCAIP
2026-10-24T14:50:53.2026288Z ##[debug]loading SECRET_OKD_4_TOKEN
2026-10-24T14:50:53.2026906Z ##[debug]loading SECRET_AZPAT
2026-10-24T14:50:53.2027593Z ##[debug]loading SECRET_PASSWORD_CGC
2026-10-24T14:50:53.2029929Z ##[debug]loading SECRET_GRAYLOG_PASSWORD
2026-10-24T14:50:53.2030173Z ##[debug]loading SECRET_OKD_TOKEN_REGISTRY
2026-10-24T14:50:53.2030416Z ##[debug]loading SECRET_FORTIFY_PASS
2026-10-24T14:50:53.2031267Z ##[debug]loading SECRET_FORTIFY_APITOKEN
2026-10-24T14:50:53.2032172Z ##[debug]loading SECRET_ALOCAIP_SENHA
2026-10-24T14:50:53.2032465Z ##[debug]loaded 22
2026-10-24T14:50:53.2037197Z ##[debug]Agent.ProxyUrl=undefined
2026-10-24T14:50:53.2037538Z ##[debug]Agent.CAInfo=undefined
2026-10-24T14:50:53.2037897Z ##[debug]Agent.ClientCert=undefined
2026-10-24T14:50:53.2038217Z ##[debug]Agent.SkipCertValidation=True
2026-10-24T14:50:53.2052342Z ##[debug]check path : /opt/ads-agent/_work/_tasks/Bash_6c731c3c-3c68-459a-a5c9-bde6e6595b5b/3.227.0/task.json
2026-10-24T14:50:53.2054588Z ##[debug]adding resource file: /opt/ads-agent/_work/_tasks/Bash_6c731c3c-3c68-459a-a5c9-bde6e6595b5b/3.227.0/task.json
2026-10-24T14:50:53.2054871Z ##[debug]system.culture=en-US
2026-10-24T14:50:53.2062428Z ##[debug]failOnStderr=false
2026-10-24T14:50:53.2064197Z ##[debug]workingDirectory=/opt/ads-agent/_work/r934/a
2026-10-24T14:50:53.2064454Z ##[debug]check path : /opt/ads-agent/_work/r934/a
2026-10-24T14:50:53.2065028Z ##[debug]targetType=inline
2026-10-24T14:50:53.2065261Z ##[debug]bashEnvValue=undefined
2026-10-24T14:50:53.2066070Z ##[debug]script=#!/bin/bash
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
2026-10-24T14:50:53.2074228Z Generating script.
2026-10-24T14:50:53.2076083Z ##[debug]which 'bash'
2026-10-24T14:50:53.2081373Z ##[debug]found: '/usr/bin/bash'
2026-10-24T14:50:53.2081895Z ##[debug]Agent.Version=3.236.1
2026-10-24T14:50:53.2082148Z ##[debug]agent.tempDirectory=/opt/ads-agent/_work/_temp
2026-10-24T14:50:53.2082406Z ##[debug]check path : /opt/ads-agent/_work/_temp
2026-10-24T14:50:53.2084992Z ========================== Starting Command Output ===========================
2026-10-24T14:50:53.2086158Z ##[debug]which '/usr/bin/bash'
2026-10-24T14:50:53.2087052Z ##[debug]found: '/usr/bin/bash'
2026-10-24T14:50:53.2087817Z ##[debug]/usr/bin/bash arg: /opt/ads-agent/_work/_temp/f8b42f3e-9e90-45e8-89b2-2edd54961eae.sh
2026-10-24T14:50:53.2090029Z ##[debug]exec tool: /usr/bin/bash
2026-10-24T14:50:53.2090264Z ##[debug]arguments:
2026-10-24T14:50:53.2090506Z ##[debug]   /opt/ads-agent/_work/_temp/f8b42f3e-9e90-45e8-89b2-2edd54961eae.sh
2026-10-24T14:50:53.2092122Z [command]/usr/bin/bash /opt/ads-agent/_work/_temp/f8b42f3e-9e90-45e8-89b2-2edd54961eae.sh
2026-10-24T14:50:53.2165313Z + shopt -s expand_aliases
2026-10-24T14:50:53.2165527Z + [[ -n okd4_nprd ]]
2026-10-24T14:50:53.2165633Z + [[ okd4_nprd =~ ocp ]]
2026-10-24T14:50:53.2165771Z + [[ -n okd4_nprd ]]
2026-10-24T14:50:53.2165885Z + [[ okd4_nprd =~ (okd4|openshift) ]]
2026-10-24T14:50:53.2166039Z + app=sicow-conres-okd-des
2026-10-24T14:50:53.2166147Z + oc version
2026-10-24T14:50:53.2817607Z Client Version: v4.2.0-alpha.0-1394-g45460a5
2026-10-24T14:50:53.2817895Z Server Version: 4.12.0-0.okd-2023-04-16-041331
2026-10-24T14:50:53.2818094Z Kubernetes Version: v1.25.0-2824+27e744f55d2e99-dirty
2026-10-24T14:50:53.2853062Z ++ oc get pod -l name=sicow-conres-okd-des -n sicow-des -o 'jsonpath={range .items[*]}{.metadata.name}{"\n"}' --sort-by=.metadata.creationTimestamp
2026-10-24T14:50:53.2857367Z ++ tac
2026-10-24T14:50:53.2861884Z ++ head -n1
2026-10-24T14:50:53.2862204Z ++ grep -v '^$'
2026-10-24T14:50:53.3663814Z + last_pod=sicow-conres-okd-des-28-598q7
2026-10-24T14:50:53.3664153Z + echo 'Logs do POD: sicow-conres-okd-des-28-598q7'
2026-10-24T14:50:53.3664395Z + oc logs sicow-conres-okd-des-28-598q7 -c sicow-conres-okd-des -n sicow-des
2026-10-24T14:50:53.3664584Z Logs do POD: sicow-conres-okd-des-28-598q7
2026-10-24T14:50:53.4610678Z =========================================================================
2026-10-24T14:50:53.4612935Z 
2026-10-24T14:50:53.4613262Z   JBoss Bootstrap Environment
2026-10-24T14:50:53.4613352Z 
2026-10-24T14:50:53.4615293Z   JBOSS_HOME: /opt/jboss
2026-10-24T14:50:53.4615671Z 
2026-10-24T14:50:53.4616247Z   JAVA: /usr/lib/jvm/java-1.8.0-openjdk-1.8.0.372.b07-1.el7_9.x86_64/jre/bin/java
2026-10-24T14:50:53.4616345Z 
2026-10-24T14:50:53.4618037Z   JAVA_OPTS:  -verbose:gc -Xloggc:"/opt/jboss/standalone/log/gc.log" -XX:+PrintGCDetails -XX:+PrintGCDateStamps -XX:+UseGCLogFileRotation -XX:NumberOfGCLogFiles=5 -XX:GCLogFileSize=3M -XX:-TraceClassUnloading -Xms1024m -Xmx1024m -XX:MetaspaceSize=96m -XX:MaxMetaspaceSize=512m -Djava.net.preferIPv4Stack=true -Djboss.modules.system.pkgs=org.jboss.byteman -Djava.awt.headless=true -Djavax.net.ssl.trustStore=/opt/jboss/standalone/configuration/caixa-truststore-acteste-nprd.jks -Djavax.net.ssl.trustStorePassword=changeit -Dhttps.proxyHost=proxydes.caixa -Dhttps.proxyPort=80 -Dhttp.proxyHost=proxydes.caixa -Dhttp.proxyPort=80 -Dhttp.nonProxyHosts=*.caixa -Djboss.modules.policy-permissions=true -server -XX:+ExplicitGCInvokesConcurrent -XX:+UseG1GC -XX:MaxGCPauseMillis=500 -Xbootclasspath/p:/opt/jboss/modules/system/layers/base/org/wildfly/common/main/wildfly-common-1.5.4.Final-redhat-00001.jar -Xbootclasspath/p:/opt/jboss/modules/system/layers/base/org/jboss/logmanager/main/jboss-logmanager-2.1.18.Final-redhat-00001.jar -Djboss.modules.system.pkgs=org.jboss.byteman,org.jboss.logmanager -Djava.util.logging.manager=org.jboss.logmanager.LogManager -javaagent:/opt/jmx_exporter/jmx_prometheus.jar=8778:/opt/jmx_exporter/jmx_prometheus.yaml -javaagent:/opt/jboss/standalone/deployments/applicationinsights-agent-3.7.1.jar -Djava.net.useSystemProxies=false -Dhttp.proxyHost=proxydes.caixa -Dhttp.proxyPort=80 -Dhttps.proxyHost=proxydes.caixa -Dhttps.proxyPort=80 -Dhttp.nonProxyHosts=localhost\|127.0.0.1\|*.caixa 
2026-10-24T14:50:53.4619314Z 
2026-10-24T14:50:53.4619454Z =========================================================================
2026-10-24T14:50:53.4619524Z 
2026-10-24T14:50:53.4619897Z OpenJDK 64-Bit Server VM warning: If the number of processors is expected to increase from one, then you should configure the number of parallel GC threads appropriately using -XX:ParallelGCThreads=N
2026-10-24T14:50:53.4620546Z 2026-10-24 11:50:12.062-03:00 WARN  i.o.s.a.ResourceConfiguration - Found reference to io.opentelemetry.sdk.autoconfigure.internal.EnvironmentResourceProvider in otel.java.enabled.resource.providers. Please update to io.opentelemetry.sdk.autoconfigure.EnvironmentResourceProvider. Support for the old provider name will be removed after 1.49.0.
2026-10-24T14:50:53.4621004Z 2026-10-24 11:50:30.153-03:00 INFO  c.m.applicationinsights.agent - Application Insights Java Agent 3.7.1 started successfully (PID 171, JVM running for 32.76 s)
2026-10-24T14:50:53.4621393Z 2026-10-24 11:50:30.155-03:00 INFO  c.m.applicationinsights.agent - Java version: 1.8.0_372, vendor: Red Hat, Inc., home: /usr/lib/jvm/java-1.8.0-openjdk-1.8.0.372.b07-1.el7_9.x86_64/jre
2026-10-24T14:50:53.4621704Z [0m11:50:31,552 INFO  [org.jboss.modules] (main) JBoss Modules version 1.12.0.Final-redhat-00001
2026-10-24T14:50:53.4621960Z [0m[0m11:50:32,917 INFO  [org.jboss.msc] (main) JBoss MSC version 1.4.12.Final-redhat-00001
2026-10-24T14:50:53.4622211Z [0m[0m11:50:33,042 INFO  [org.jboss.threads] (main) JBoss Threads version 2.4.0.Final-redhat-00001
2026-10-24T14:50:53.4622520Z [0m[0m11:50:33,640 INFO  [org.jboss.as] (MSC service thread 1-2) WFLYSRV0049: JBoss EAP 7.4.11.GA (WildFly Core 15.0.26.Final-redhat-00001) starting
2026-10-24T14:50:53.4622987Z [0m[0m11:50:33,957 INFO  [org.jboss.vfs] (MSC service thread 1-1) VFS000002: Failed to clean existing content for temp file provider of type temp. Enable DEBUG level log to find what caused this
2026-10-24T14:50:53.4623577Z [0m[33m11:50:34,816 WARN  [org.jboss.as.controller] (Controller Boot Thread) WFLYCTL0456: System property "user.timezone" is already set in the <system-properties> section of the configuration file. The value set in the command line will be overridden by that value.
2026-10-24T14:50:53.4623984Z [0m[0m11:50:38,118 INFO  [org.wildfly.security] (ServerService Thread Pool -- 31) ELY00001: WildFly Elytron version 1.15.16.Final-redhat-00001
2026-10-24T14:50:53.4624345Z [0m[0m11:50:39,022 INFO  [org.jboss.as.controller.management-deprecated] (ServerService Thread Pool -- 16) WFLYCTL0033: Extension 'security' is deprecated and may not be supported in future versions
2026-10-24T14:50:53.4624948Z [0m[0m11:50:40,628 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'security-realm' in the resource at address '/core-service=management/management-interface=native-interface' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-10-24T14:50:53.4625663Z [0m[0m11:50:40,630 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'security-realm' in the resource at address '/core-service=management/management-interface=http-interface' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-10-24T14:50:53.4626358Z [0m[0m11:50:40,725 INFO  [org.jboss.as.controller.management-deprecated] (ServerService Thread Pool -- 34) WFLYCTL0028: Attribute 'security-realm' in the resource at address '/subsystem=undertow/server=default-server/https-listener=https' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-10-24T14:50:53.4626921Z [0m[0m11:50:41,534 INFO  [org.jboss.as.repository] (ServerService Thread Pool -- 8) WFLYDR0001: Content added at location /opt/jboss/standalone/data/content/43/10e3eda419b2f2c7d4fb432f9cf7908f535920/content
2026-10-24T14:50:53.4627410Z [0m[0m11:50:42,046 INFO  [org.jboss.as.repository] (ServerService Thread Pool -- 8) WFLYDR0001: Content added at location /opt/jboss/standalone/data/content/8f/a714485f427852e3aa59ff367a6b9db506f167/content
2026-10-24T14:50:53.4628391Z [0m[31m11:50:42,215 ERROR [org.jboss.as.controller.management-operation] (Controller Boot Thread) WFLYCTL0013: Operation ("add") failed - address: ([("core-service" => "vault")]): org.jboss.as.server.services.security.VaultReaderException: WFLYSRV0076: Error initializing vault --  org.jboss.security.vault.SecurityVaultException: java.lang.RuntimeException: PBOX00140: Unable to get keystore (/opt/jboss/standalone/configuration/vault-sicow-des.keystore)
2026-10-24T14:50:53.4628870Z 	at org.jboss.as.server.services.security.VaultReaderImpl.createVault(RuntimeVaultReader.java:159)
2026-10-24T14:50:53.4629139Z 	at org.jboss.as.server.services.security.RuntimeVaultReader.createVault(RuntimeVaultReader.java:100)
2026-10-24T14:50:53.4629447Z 	at org.jboss.as.server.services.security.VaultAddHandler.performRuntime(VaultAddHandler.java:96)
2026-10-24T14:50:53.4629765Z 	at org.jboss.as.controller.AbstractAddStepHandler.performRuntime(AbstractAddStepHandler.java:343)
2026-10-24T14:50:53.4630070Z 	at org.jboss.as.controller.AbstractAddStepHandler$1.execute(AbstractAddStepHandler.java:164)
2026-10-24T14:50:53.4630277Z 	at org.jboss.as.controller.AbstractOperationContext.executeStep(AbstractOperationContext.java:1047)
2026-10-24T14:50:53.4630497Z 	at org.jboss.as.controller.AbstractOperationContext.processStages(AbstractOperationContext.java:779)
2026-10-24T14:50:53.4630711Z 	at org.jboss.as.controller.AbstractOperationContext.executeOperation(AbstractOperationContext.java:468)
2026-10-24T14:50:53.4630925Z 	at org.jboss.as.controller.OperationContextImpl.executeOperation(OperationContextImpl.java:1431)
2026-10-24T14:50:53.4631119Z 	at org.jboss.as.controller.ModelControllerImpl.boot(ModelControllerImpl.java:559)
2026-10-24T14:50:53.4631317Z 	at org.jboss.as.controller.AbstractControllerService.boot(AbstractControllerService.java:546)
2026-10-24T14:50:53.4631516Z 	at org.jboss.as.controller.AbstractControllerService.boot(AbstractControllerService.java:508)
2026-10-24T14:50:53.4631705Z 	at org.jboss.as.server.ServerService.boot(ServerService.java:464)
2026-10-24T14:50:53.4631872Z 	at org.jboss.as.server.ServerService.boot(ServerService.java:417)
2026-10-24T14:50:53.4632050Z 	at org.jboss.as.controller.AbstractControllerService$1.run(AbstractControllerService.java:447)
2026-10-24T14:50:53.4632224Z 	at java.lang.Thread.run(Thread.java:750)
2026-10-24T14:50:53.4632579Z Caused by: org.jboss.security.vault.SecurityVaultException: java.lang.RuntimeException: PBOX00140: Unable to get keystore (/opt/jboss/standalone/configuration/vault-sicow-des.keystore)
2026-10-24T14:50:53.4633001Z 	at org.picketbox.plugins.vault.PicketBoxSecurityVault.init(PicketBoxSecurityVault.java:210)
2026-10-24T14:50:53.4633289Z 	at org.jboss.as.server.services.security.VaultReaderImpl.createVault(RuntimeVaultReader.java:157)
2026-10-24T14:50:53.4633499Z 	... 15 more
2026-10-24T14:50:53.4633873Z Caused by: java.lang.RuntimeException: PBOX00140: Unable to get keystore (/opt/jboss/standalone/configuration/vault-sicow-des.keystore)
2026-10-24T14:50:53.4634176Z 	at org.picketbox.plugins.vault.PicketBoxSecurityVault.getKeyStore(PicketBoxSecurityVault.java:691)
2026-10-24T14:50:53.4634441Z 	at org.picketbox.plugins.vault.PicketBoxSecurityVault.init(PicketBoxSecurityVault.java:205)
2026-10-24T14:50:53.4634673Z 	... 16 more
2026-10-24T14:50:53.4634922Z Caused by: java.io.FileNotFoundException: /opt/jboss/standalone/configuration/vault-sicow-des.keystore (No such file or directory)
2026-10-24T14:50:53.4635099Z 	at java.io.FileInputStream.open0(Native Method)
2026-10-24T14:50:53.4635248Z 	at java.io.FileInputStream.open(FileInputStream.java:195)
2026-10-24T14:50:53.4635414Z 	at java.io.FileInputStream.<init>(FileInputStream.java:138)
2026-10-24T14:50:53.4635585Z 	at org.picketbox.util.KeyStoreUtil.getKeyStore(KeyStoreUtil.java:150)
2026-10-24T14:50:53.4635778Z 	at org.picketbox.plugins.vault.PicketBoxSecurityVault.getKeyStore(PicketBoxSecurityVault.java:688)
2026-10-24T14:50:53.4635975Z 	... 17 more
2026-10-24T14:50:53.4636016Z 
2026-10-24T14:50:53.4636383Z [0m[31m11:50:42,226 FATAL [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0056: Server boot has failed in an unrecoverable manner; exiting. See previous messages for details.
2026-10-24T14:50:53.4636753Z [0m[0m11:50:42,417 INFO  [org.jboss.as] (MSC service thread 1-1) WFLYSRV0050: JBoss EAP 7.4.11.GA (WildFly Core 15.0.26.Final-redhat-00001) stopped in 176ms
2026-10-24T14:50:53.4653272Z ##[debug]Exit code 0 received from tool '/usr/bin/bash'
2026-10-24T14:50:53.4657176Z ##[debug]STDIO streams have closed for tool '/usr/bin/bash'
2026-10-24T14:50:53.4661854Z ##[debug]task result: Succeeded
2026-10-24T14:50:53.4663839Z ##[debug]Processed: ##vso[task.complete result=Succeeded;done=true;]
2026-10-24T14:50:53.4694977Z ##[section]Finishing: Logs da Aplicação

