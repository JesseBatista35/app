cp -r /opt/app-root/src/sidcx-host/. /opt/app-root/src/
nginx && curl -s -o /dev/null -w '%{http_code}\n' http://localhost:8080/
