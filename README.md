Login Cluster

View raw log

Starting: Login Cluster
==============================================================================
Task         : Bash
Description  : Run a Bash script on macOS, Linux, or Windows
Version      : 3.227.0
Author       : Microsoft Corporation
Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
==============================================================================
Generating script.
========================== Starting Command Output ===========================
/usr/bin/bash /opt/ads-agent/_work/_temp/85b8ad5c-4ce1-4a3c-a52a-fa661bad7290.sh
+ echo ''
+ egrep -q '^(okd4|ocp)'
+ oc login https://cloudnprd2.caixa --insecure-skip-tls-verify=true --token=***
error: dial tcp 10.116.180.18:443: i/o timeout - verify you have provided the correct host and port and that the server is currently running.
##[error]Bash exited with code '1'.
Finishing: Login Cluster

da dan opau para fazer long no cluster agora

