
-sh-4.2$
-sh-4.2$
-sh-4.2$ ls -l $H/sites-enabled/eap_71_esteiraagil/httpd-eap71-tqs-sigec-csc.conf \
>       $H/sites-enabled/esteiraagil/httpd-eap71-tqs-sigec-csc.conf
lrwxrwxrwx 1 apache apache 74 Jul 14  2020 /opt/jbcs-httpd24-2.4/httpd/sites-enabled/eap_71_esteiraagil/httpd-eap71-tqs-sigec-csc.conf -> /opt/jbcs-httpd24-2.4/httpd/sites-available/httpd-eap71-tqs-sigec-csc.conf
lrwxrwxrwx 1 apache apache 74 Jul 14  2020 /opt/jbcs-httpd24-2.4/httpd/sites-enabled/esteiraagil/httpd-eap71-tqs-sigec-csc.conf -> /opt/jbcs-httpd24-2.4/httpd/sites-available/httpd-eap71-tqs-sigec-csc.conf
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ cat $H/sites-available/httpd-eap71-tqs-sigec-csc.conf
# VIP: 10.116.180.23
<VirtualHost *:80>
  ServerName  sigec-csc.esteiras.tqs.caixa

#   ErrorDocument 503 http://sigec-csc.esteiras.tqs.caixa/error
#
  ProxyErrorOverride Off
  ProxyRequests Off
  RewriteEngine On
  RewriteRule ^/$ /csc-api [R]

  ProxyPass   ^/csc-api/ balancer://sigec-csc/csc-api/  stickysession=JSESSIONID|jsessionid  nofailover=On
  ProxyPassReverse ^/csc-api/ balancer://sigec-csc/csc-api/

  <Location /balancer-manager>
          SetHandler balancer-manager
          Require all granted
  </Location>

   <Location /errors>
     Require all granted
     Options All MultiViews
  </Location>

  <Location /styles>
     Require all granted
     Options All MultiViews
  </Location>

  <Location /scripts>
     Require all granted
     Options All MultiViews
 </Location>

  <Location /fonts>
     Require all granted
     Options All MultiViews
 </Location>

  <Location /images>
     Require all granted
     Options All MultiViews
 </Location>

  CustomLog /logs/apache2/sigec-csc/sigec-csc.esteiras.tqs.caixa-access.log combined
  ErrorLog /logs/apache2/sigec-csc/sigec-csc.esteiras.tqs.caixa-error.log
</VirtualHost>
-sh-4.2$
