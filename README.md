
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$ ls -la /opt/app-root/src/sidcx-host | head
grep -rn "root\|index" /etc/nginx/nginx.conf /opt/app-root/etc/nginx.d/ /opt/app-root/etc/nginx.default.d/ 2>/dev/null
total 1676
drwxr-xr-x. 2 default root   4096 Oct 20 12:31 .
drwxr-xr-x. 1 default root     36 Oct 20 12:32 ..
-rw-r--r--. 1 default root   3280 Oct 20 12:31 3rdpartylicenses.txt
-rw-r--r--. 1 default root  39908 Oct 20 12:31 CAIXAStd-Bold.woff
-rw-r--r--. 1 default root  32136 Oct 20 12:31 CAIXAStd-Bold.woff2
-rw-r--r--. 1 default root  40424 Oct 20 12:31 CAIXAStd-BoldItalic.woff
-rw-r--r--. 1 default root  32532 Oct 20 12:31 CAIXAStd-BoldItalic.woff2
-rw-r--r--. 1 default root  38832 Oct 20 12:31 CAIXAStd-Regular.woff
-rw-r--r--. 1 default root  31248 Oct 20 12:31 CAIXAStd-Regular.woff2
/etc/nginx/nginx.conf:34:    include /opt/app-root/etc/nginx.d/*.conf;
/etc/nginx/nginx.conf:40:        root         /opt/app-root/src;
/etc/nginx/nginx.conf:44:        include /opt/app-root/etc/nginx.default.d/*.conf;
/etc/nginx/nginx.conf:59:          try_files $uri $uri/ /index.html =404;
/opt/app-root/etc/nginx.default.d/sidcx-nginx.conf:3:# Rotas do single-spa (ex.: /spa/...) sao resolvidas no browser; devolve o index.html.
/opt/app-root/etc/nginx.default.d/sidcx-nginx.conf:4:error_page 404 =200 /index.html;
/opt/app-root/etc/nginx.default.d/sidcx-nginx.conf:6:# O index.html referencia o bundle atual; nao pode ficar em cache.
/opt/app-root/etc/nginx.default.d/sidcx-nginx.conf:7:location = /index.html {
sh-5.1$
sh-5.1$
sh-5.1$
