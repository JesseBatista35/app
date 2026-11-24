2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get route --all-namespaces 2>/dev/null | grep -i sigec-csc
sigec-des                            sigec-csc-frontend-des                                         sigec-csc-frontend-des.apps.nprd.caixa                                                                                                            sigec-csc-frontend-des                                         web               edge/Redirect          None
sigec-hmp                            sigec-csc-frontend-hmp                                         sigec-csc-frontend-hmp.apps.nprd.caixa                                                                                                            sigec-csc-frontend-hmp                                         web               edge/Redirect          None
sigec-tqs                            sigec-csc-frontend-tqs                                         sigec-csc-frontend-tqs.apps.nprd.caixa                                                                                                            sigec-csc-frontend-tqs                                         web               edge/Redirect          None
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc projects | grep -i sigec
    sigec-des
    sigec-hmp
    sigec-tqs
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ NS=sigec-tqs
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get route sigec-csc-frontend-tqs -n $NS -o yaml | grep -iE 'timeout|host:'
    haproxy.router.openshift.io/timeout: 10m
          f:haproxy.router.openshift.io/timeout: {}
        f:host: {}
  host: sigec-csc-frontend-tqs.apps.nprd.caixa
    host: sigec-csc-frontend-tqs.apps.nprd.caixa
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pods -n $NS -o wide | grep -i csc
sigec-csc-frontend-tqs-82-deploy   0/1       Completed   0                5d19h     25.2.26.174   ceadecldlx056.nprd.caixa   <none>           <none>
sigec-csc-frontend-tqs-83-deploy   0/1       Completed   0                4d20h     25.3.26.140   ceadecldlx057.nprd.caixa   <none>           <none>
sigec-csc-frontend-tqs-83-rvzvp    2/2       Running     0                4d20h     25.1.8.61     ceadecldlx027.nprd.caixa   <none>           <none>
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ POD=sigec-csc-frontend-tqs-83-rvzvp
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc rsh -n $NS $POD sh -c 'ps -ef | head -20; echo ---; grep -Rni "proxy_pass\|proxy_.*timeout\|server_tokens" /etc/nginx /opt/app-root/etc 2>/dev/null; echo ---; env | grep -iE "url|api|backend|proxy"'
Defaulting container name to sigec-csc-frontend-tqs.
Use 'oc describe pod/sigec-csc-frontend-tqs-83-rvzvp -n sigec-tqs' to see all of the containers in this pod.
UID          PID    PPID  C STIME TTY          TIME CMD
default        1       0  0 Nov19 ?        00:00:00 nginx: master process nginx -g daemon off;
default       23       1  0 Nov19 ?        00:00:09 nginx: worker process
default       24       1  0 Nov19 ?        00:00:05 nginx: worker process
default       25       1  0 Nov19 ?        00:00:00 nginx: worker process
default       26       1  0 Nov19 ?        00:00:00 nginx: worker process
default       27       1  0 Nov19 ?        00:00:00 nginx: worker process
default       28       1  0 Nov19 ?        00:00:00 nginx: worker process
default       29       1  0 Nov19 ?        00:00:00 nginx: worker process
default       30       1  0 Nov19 ?        00:00:00 nginx: worker process
default       31       1  0 Nov19 ?        00:00:00 nginx: worker process
default       32       1  0 Nov19 ?        00:00:00 nginx: worker process
default       33       1  0 Nov19 ?        00:00:00 nginx: worker process
default       34       1  0 Nov19 ?        00:00:00 nginx: worker process
default       35       1  0 Nov19 ?        00:00:00 nginx: worker process
default       36       1  0 Nov19 ?        00:00:00 nginx: worker process
default       37       1  0 Nov19 ?        00:00:00 nginx: worker process
default       38       1  0 Nov19 ?        00:00:00 nginx: worker process
default       39       1  0 Nov19 ?        00:00:00 nginx: worker process
default       40       1  0 Nov19 ?        00:00:00 nginx: worker process
---
/etc/nginx/nginx.conf.default:60:        #    proxy_pass   http://127.0.0.1;
/opt/app-root/etc/nginx.default.d/sigec-nginx.conf:3:        proxy_connect_timeout 600s;
/opt/app-root/etc/nginx.default.d/sigec-nginx.conf:4:        proxy_send_timeout 600s;
/opt/app-root/etc/nginx.default.d/sigec-nginx.conf:5:        proxy_read_timeout 600s;
/opt/app-root/etc/nginx.default.d/sigec-nginx.conf:10:        proxy_pass https://sigec-csc.esteiras.tqs.caixa/csc-api;
/opt/app-root/etc/nginx.default.d/sigec-nginx.conf:12:        server_tokens off;
---
BASE_URL_REST_SIGEC_CSC=https://sigec-csc.esteiras.tqs.caixa/csc-api
STI_SCRIPTS_URL=image:///usr/libexec/s2i
DESCRIPTION=Nginx is a web server and a reverse proxy server for HTTP, SMTP, POP3 and IMAP protocols, with a strong focus on high concurrency, performance and low memory usage. The container image provides a containerized packaging of the nginx 1.18 daemon. The image can be used as a base image for other applications based on nginx 1.18 web server. Nginx server image can be extended using source-to-image tool.
URL_SSO=https://login.tqs.caixa/auth
KEYCLOAK_CONFIG_URL=https://login.tqs.caixa/auth
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
