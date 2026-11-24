
-sh-4.2$
-sh-4.2$
-sh-4.2$ H=/opt/jbcs-httpd24-2.4/httpd
-sh-4.2$ grep -RniE '^\s*(Timeout|ProxyTimeout)\b|timeout=' $H/conf $H/conf.d 2>/dev/null
/opt/jbcs-httpd24-2.4/httpd/conf/.httpd.conf.20200103220147.root:67:Timeout 120
/opt/jbcs-httpd24-2.4/httpd/conf/httpd.conf:67:Timeout 120
/opt/jbcs-httpd24-2.4/httpd/conf/.httpd.conf.20200121110100.a412811:67:Timeout 120
/opt/jbcs-httpd24-2.4/httpd/conf/.httpd.conf.20200122090157.a412811:67:Timeout 120
/opt/jbcs-httpd24-2.4/httpd/conf/.httpd.conf.20200122090140.a412811:67:Timeout 120
/opt/jbcs-httpd24-2.4/httpd/conf/.httpd.conf.20200529100542.a568234:67:Timeout 120
-sh-4.2$
-sh-4.2$
-sh-4.2$ grep -Rln 'sigec-csc' $H/conf $H/conf.d 2>/dev/null
-sh-4.2$
-sh-4.2$
-sh-4.2$ grep -niE '^\s*Include' $H/conf/httpd.conf $H/conf/httpd_eap_71_esteiraagil.conf
/opt/jbcs-httpd24-2.4/httpd/conf/httpd.conf:115:Include conf.modules.d/*.conf
/opt/jbcs-httpd24-2.4/httpd/conf/httpd.conf:860:IncludeOptional conf.d/*.conf
/opt/jbcs-httpd24-2.4/httpd/conf/httpd_eap_71_esteiraagil.conf:58:Include /opt/jbcs-httpd24-2.4/httpd/conf/httpd.conf
/opt/jbcs-httpd24-2.4/httpd/conf/httpd_eap_71_esteiraagil.conf:95:IncludeOptional sites-enabled/eap_71_esteiraagil/*.conf
-sh-4.2$
-sh-4.2$
-sh-4.2$ grep -Rln --exclude-dir=logs 'sigec-csc' $H 2>/dev/null
/opt/jbcs-httpd24-2.4/httpd/sites-available/httpd-eap71-tqs-sigec-csc.conf
/opt/jbcs-httpd24-2.4/httpd/sites-enabled/eap_71_esteiraagil/httpd-eap71-tqs-sigec-csc.conf
/opt/jbcs-httpd24-2.4/httpd/sites-enabled/esteiraagil/httpd-eap71-tqs-sigec-csc.conf
-sh-4.2$
