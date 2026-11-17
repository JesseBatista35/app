[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$ curl -vk --resolve siemp.des.caixa:443:10.116.180.9 https://siemp.des.caixa/siemp_java/
* Added siemp.des.caixa:443:10.116.180.9 to DNS cache
* Hostname siemp.des.caixa was found in DNS cache
*   Trying 10.116.180.9:443...
* Connected to siemp.des.caixa (10.116.180.9) port 443 (#0)
* ALPN, offering h2
* ALPN, offering http/1.1
*  CAfile: /etc/pki/tls/certs/ca-bundle.crt
* TLSv1.0 (OUT), TLS header, Certificate Status (22):
* TLSv1.3 (OUT), TLS handshake, Client hello (1):
* TLSv1.2 (IN), TLS header, Certificate Status (22):
* TLSv1.3 (IN), TLS handshake, Server hello (2):
* TLSv1.2 (OUT), TLS header, Finished (20):
* TLSv1.3 (OUT), TLS change cipher, Change cipher spec (1):
* TLSv1.2 (OUT), TLS header, Certificate Status (22):
* TLSv1.3 (OUT), TLS handshake, Client hello (1):
* TLSv1.2 (IN), TLS header, Finished (20):
* TLSv1.2 (IN), TLS header, Certificate Status (22):
* TLSv1.3 (IN), TLS handshake, Server hello (2):
* TLSv1.2 (IN), TLS header, Unknown (23):
* TLSv1.3 (IN), TLS handshake, Encrypted Extensions (8):
* TLSv1.3 (IN), TLS handshake, Certificate (11):
* TLSv1.2 (IN), TLS header, Unknown (23):
* TLSv1.3 (IN), TLS handshake, CERT verify (15):
* TLSv1.3 (IN), TLS handshake, Finished (20):
* TLSv1.2 (OUT), TLS header, Unknown (23):
* TLSv1.3 (OUT), TLS handshake, Finished (20):
* SSL connection using TLSv1.3 / TLS_AES_256_GCM_SHA384
* ALPN, server accepted to use http/1.1
* Server certificate:
*  subject: C=BR; O=Caixa Economica Federal; CN=siemp.des.caixa
*  start date: Nov  9 20:31:26 2026 GMT
*  expire date: Nov  9 20:41:26 2031 GMT
*  issuer: C=BR; O=Caixa Economica Federal; CN=AC Icptestes Sub
*  SSL certificate verify result: self-signed certificate in certificate chain (19), continuing anyway.
* TLSv1.2 (OUT), TLS header, Unknown (23):
> GET /siemp_java/ HTTP/1.1
> Host: siemp.des.caixa
> User-Agent: curl/7.76.1
> Accept: */*
>
* TLSv1.2 (IN), TLS header, Unknown (23):
* Mark bundle as not supporting multiuse
< HTTP/1.1 404 Not Found
< Date: Tue, 17 Nov 2026 20:14:28 GMT
< Server: Apache
< Content-Length: 74
< Content-Type: text/html; charset=UTF-8
<
* Connection #0 to host siemp.des.caixa left intact
<html><head><title>Error</title></head><body>404 - Not Found</body></html>[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$ df -h /tmp
Sist. Arq.                       Tam. Usado Disp. Uso% Montado em
/dev/mapper/VG_PRINCIPAL-LV_TMP  960M   57M  904M   6% /tmp
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
