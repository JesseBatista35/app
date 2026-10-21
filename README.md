
2026-10-21T18:46:24.7815146Z ##[section]Starting: Logs da Aplicação
2026-10-21T18:46:24.7818742Z ==============================================================================
2026-10-21T18:46:24.7818856Z Task         : Bash
2026-10-21T18:46:24.7818900Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-21T18:46:24.7818971Z Version      : 3.227.0
2026-10-21T18:46:24.7819050Z Author       : Microsoft Corporation
2026-10-21T18:46:24.7819099Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-21T18:46:24.7819172Z ==============================================================================
2026-10-21T18:46:25.1977172Z Generating script.
2026-10-21T18:46:25.1978037Z ========================== Starting Command Output ===========================
2026-10-21T18:46:25.1979627Z [command]/usr/bin/bash /opt/ads-agent/_work/_temp/3523b24a-50b8-4f24-8b7c-9a793d5d8035.sh
2026-10-21T18:46:25.1979813Z + shopt -s expand_aliases
2026-10-21T18:46:25.1979940Z + [[ -n okd4_nprd ]]
2026-10-21T18:46:25.1980093Z + [[ okd4_nprd =~ ocp ]]
2026-10-21T18:46:25.1980224Z + [[ -n okd4_nprd ]]
2026-10-21T18:46:25.1980331Z + [[ okd4_nprd =~ (okd4|openshift) ]]
2026-10-21T18:46:25.1980461Z + app=sidcx-host-des
2026-10-21T18:46:25.1980563Z + oc version
2026-10-21T18:46:25.1980727Z Client Version: v4.2.0-alpha.0-1394-g45460a5
2026-10-21T18:46:25.1981196Z Server Version: 4.12.0-0.okd-2023-04-16-041331
2026-10-21T18:46:25.1981384Z Kubernetes Version: v1.25.0-2824+27e744f55d2e99-dirty
2026-10-21T18:46:25.1981658Z ++ oc get pod -l name=sidcx-host-des -n sidcx-des -o 'jsonpath={range .items[*]}{.metadata.name}{"\n"}' --sort-by=.metadata.creationTimestamp
2026-10-21T18:46:25.1981814Z ++ tac
2026-10-21T18:46:25.1981929Z ++ grep -v '^$'
2026-10-21T18:46:25.1982028Z ++ head -n1
2026-10-21T18:46:25.1982173Z + last_pod=sidcx-host-des-3-pm266
2026-10-21T18:46:25.1982341Z + echo 'Logs do POD: sidcx-host-des-3-pm266'
2026-10-21T18:46:25.1982517Z + oc logs sidcx-host-des-3-pm266 -c sidcx-host-des -n sidcx-des
2026-10-21T18:46:25.1982691Z Logs do POD: sidcx-host-des-3-pm266
2026-10-21T18:46:25.1982993Z 2026/10/21 15:46:08 [error] 27#27: *1 directory index of "/opt/app-root/src/" is forbidden, client: 25.1.20.1, server: _, request: "GET / HTTP/1.1", host: "25.1.20.40:8080"
2026-10-21T18:46:25.1983508Z [21/Oct/2026:15:46:08 -0300] 25.1.20.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1792608368.407 request_time 0.000 403 146 - kube-probe/1.25 -
2026-10-21T18:46:25.1983898Z 2026/10/21 15:46:18 [error] 29#29: *2 directory index of "/opt/app-root/src/" is forbidden, client: 25.1.20.1, server: _, request: "GET / HTTP/1.1", host: "25.1.20.40:8080"
2026-10-21T18:46:25.1984310Z 2026/10/21 15:46:18 [error] 28#28: *3 directory index of "/opt/app-root/src/" is forbidden, client: 25.1.20.1, server: _, request: "GET / HTTP/1.1", host: "25.1.20.40:8080"
2026-10-21T18:46:25.1984663Z [21/Oct/2026:15:46:18 -0300] 25.1.20.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1792608378.406 request_time 0.000 403 146 - kube-probe/1.25 -
2026-10-21T18:46:25.1985008Z [21/Oct/2026:15:46:18 -0300] 25.1.20.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1792608378.406 request_time 0.000 403 146 - kube-probe/1.25 -
2026-10-21T18:46:25.1987009Z ##[section]Finishing: Logs da Aplicação


[21/Oct/2026:16:30:58 -0300] 127.0.0.1 - - - _ to: -: GET /stub_status HTTP/1.1 upstream_response_time - msec 1792611058.793 request_time 0.000 200 97 - NGINX-Prometheus-Exporter/v -
2026/10/21 16:31:15 [error] 24#24: *2 directory index of "/opt/app-root/src/" is forbidden, client: 25.3.14.1, server: _, request: "GET / HTTP/1.1", host: "25.3.14.160:8080"
[21/Oct/2026:16:31:15 -0300] 25.3.14.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1792611075.751 request_time 0.000 403 146 - kube-probe/1.25 -
2026/10/21 16:31:25 [error] 26#26: *4 directory index of "/opt/app-root/src/" is forbidden, client: 25.3.14.1, server: _, request: "GET / HTTP/1.1", host: "25.3.14.160:8080"
2026/10/21 16:31:25 [error] 25#25: *3 directory index of "/opt/app-root/src/" is forbidden, client: 25.3.14.1, server: _, request: "GET / HTTP/1.1", host: "25.3.14.160:8080"
[21/Oct/2026:16:31:25 -0300] 25.3.14.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1792611085.751 request_time 0.000 403 146 - kube-probe/1.25 -
[21/Oct/2026:16:31:25 -0300] 25.3.14.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1792611085.751 request_time 0.000 403 146 - kube-probe/1.25 -
2026/10/21 16:31:35 [error] 27#27: *5 directory index of "/opt/app-root/src/" is forbidden, client: 25.3.14.1, server: _, request: "GET / HTTP/1.1", host: "25.3.14.160:8080"
2026/10/21 16:31:35 [error] 28#28: *6 directory index of "/opt/app-root/src/" is forbidden, client: 25.3.14.1, server: _, request: "GET / HTTP/1.1", host: "25.3.14.160:8080"
[21/Oct/2026:16:31:35 -0300] 25.3.14.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1792611095.751 request_time 0.000 403 146 - kube-probe/1.25 -
[21/Oct/2026:16:31:35 -0300] 25.3.14.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1792611095.751 request_time 0.000 403 146 - kube-probe/1.25 -
2026/10/21 16:31:35 [error] 29#29: *7 directory index of "/opt/app-root/src/" is forbidden, client: 25.3.14.1, server: _, request: "GET / HTTP/1.1", host: "25.3.14.160:8080"
[21/Oct/2026:16:31:35 -0300] 25.3.14.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1792611095.752 request_time 0.000 403 146 - kube-probe/1.25 -
