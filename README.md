Avaliar e corrigir erro  "503 Service Unavailable" e de "CORS" no https://sigcb-frontend-tqs.apps.nprd.caixa/,  que ocorre desde segunda-feira, 26/10/2026,  ao executar quaisquer tentativas de comunicação entre front e backend. Conforme detalhamento em REQ.

<img width="1204" height="611" alt="image" src="https://github.com/user-attachments/assets/96d020c2-f97c-4eee-9431-c3331f5ba737" />


<img width="1219" height="521" alt="image" src="https://github.com/user-attachments/assets/ea395fab-dda2-460f-bb94-8c5b5333e281" />


<img width="1224" height="511" alt="image" src="https://github.com/user-attachments/assets/5ae0c519-dd40-4ff7-9c50-65b7b852728c" />

<img width="561" height="864" alt="image" src="https://github.com/user-attachments/assets/045c4396-304a-46bb-9904-f5b18c9301f8" />


<img width="1868" height="677" alt="image" src="https://github.com/user-attachments/assets/808bf137-c8e6-4636-b71d-62d997e6570a" />


2026-10-22T13:33:52.4715587Z ##[section]Starting: Logs da Aplicação
2026-10-22T13:33:52.4718838Z ==============================================================================
2026-10-22T13:33:52.4718925Z Task         : Bash
2026-10-22T13:33:52.4718966Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-22T13:33:52.4719027Z Version      : 3.227.0
2026-10-22T13:33:52.4719078Z Author       : Microsoft Corporation
2026-10-22T13:33:52.4719208Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-22T13:33:52.4719275Z ==============================================================================
2026-10-22T13:33:53.2473880Z Generating script.
2026-10-22T13:33:53.2484790Z ========================== Starting Command Output ===========================
2026-10-22T13:33:53.2496604Z [command]/bin/bash /opt/ads-agent/_work/_temp/5e645b46-d246-4cee-90c9-96d0f8ea000e.sh
2026-10-22T13:33:53.2541391Z + shopt -s expand_aliases
2026-10-22T13:33:53.2542977Z + [[ -n okd4_nprd ]]
2026-10-22T13:33:53.2543143Z + [[ okd4_nprd =~ ocp ]]
2026-10-22T13:33:53.2543281Z + [[ -n okd4_nprd ]]
2026-10-22T13:33:53.2543383Z + [[ okd4_nprd =~ (okd4|openshift) ]]
2026-10-22T13:33:53.2543515Z + app=sigcb-frontend-des
2026-10-22T13:33:53.2545572Z + oc version
2026-10-22T13:33:53.4200960Z oc v3.11.0+0cbc58b
2026-10-22T13:33:53.4201138Z kubernetes v1.11.0+d4cacc0
2026-10-22T13:33:53.4201423Z features: Basic-Auth GSSAPI Kerberos SPNEGO
2026-10-22T13:33:53.4301639Z 
2026-10-22T13:33:53.4301944Z Server https://api.nprd.caixa:6443
2026-10-22T13:33:53.4302152Z kubernetes v1.25.0-2824+27e744f55d2e99-dirty
2026-10-22T13:33:53.4343168Z ++ oc get pod -l name=sigcb-frontend-des -n sigcb-des -o 'jsonpath={range .items[*]}{.metadata.name}{"\n"}' --sort-by=.metadata.creationTimestamp
2026-10-22T13:33:53.4344637Z ++ tac
2026-10-22T13:33:53.4345206Z ++ grep -v '^$'
2026-10-22T13:33:53.4346302Z ++ head -n1
2026-10-22T13:33:53.7047621Z + last_pod=sigcb-frontend-des-1332-nllvm
2026-10-22T13:33:53.7048013Z + echo 'Logs do POD: sigcb-frontend-des-1332-nllvm'
2026-10-22T13:33:53.7048325Z + oc logs sigcb-frontend-des-1332-nllvm -c sigcb-frontend-des -n sigcb-des
2026-10-22T13:33:53.7048615Z Logs do POD: sigcb-frontend-des-1332-nllvm
2026-10-22T13:33:54.0379802Z [22/Oct/2026:10:33:20 -0300] 127.0.0.1 - - - _ to: -: GET /stub_status HTTP/1.1 upstream_response_time - msec 1792676000.063 request_time 0.000 200 97 - NGINX-Prometheus-Exporter/v -
2026-10-22T13:33:54.0380308Z [22/Oct/2026:10:33:37 -0300] 25.3.6.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1792676017.185 request_time 0.000 200 1593 - kube-probe/1.25 -
2026-10-22T13:33:54.0380641Z [22/Oct/2026:10:33:47 -0300] 25.3.6.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1792676027.185 request_time 0.000 200 1593 - kube-probe/1.25 -
2026-10-22T13:33:54.0380972Z [22/Oct/2026:10:33:47 -0300] 25.3.6.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1792676027.186 request_time 0.000 200 1593 - kube-probe/1.25 -
2026-10-22T13:33:54.0472702Z ##[section]Finishing: Logs da Aplicação


sigcb-frontend-tqs-218-kbjvc
Running


[13/Oct/2026:17:29:14 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923354.548 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:29:14 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923354.548 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:29:24 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923364.549 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:29:24 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923364.549 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:29:34 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923374.549 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:29:34 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923374.549 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:29:44 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923384.548 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:29:44 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923384.548 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:29:54 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923394.548 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:29:54 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923394.548 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:30:04 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923404.549 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:30:04 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923404.549 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:30:14 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923414.548 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:30:14 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923414.548 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:30:24 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923424.549 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:30:24 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923424.549 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:30:34 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923434.548 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:30:34 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923434.548 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:30:44 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923444.548 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:30:44 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923444.548 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:30:54 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923454.548 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:30:54 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923454.548 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:31:04 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923464.549 request_time 0.000 200 1593 - kube-probe/1.25 -
[13/Oct/2026:17:31:04 -0300] 25.1.22.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1791923464.549 request_time 0.000 200 1593 - kube-probe/1.25
