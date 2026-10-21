ls -la /opt/app-root/src/sidcx-host | head
grep -rn "root\|index" /etc/nginx/nginx.conf /opt/app-root/etc/nginx.d/ /opt/app-root/etc/nginx.default.d/ 2>/dev/null
