
-sh-4.2$
-sh-4.2$ ip route get 10.244.61.74
10.244.61.74 via 10.116.192.1 dev ens192 src 10.116.197.11
    cache
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ exit
logout
Connection to 10.116.197.11 closed.
[p585600@cadsvitrlx100 ~]$ ssh 10.116.196.254
The authenticity of host '10.116.196.254 (10.116.196.254)' can't be established.
ED25519 key fingerprint is SHA256:uxZ/jUZ4Sv+8Jp/eM9c2XB/xaEeHFw/rbyZ0BHrUWgc.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:174: 10.116.197.11
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '10.116.196.254' (ED25519) to the list of known hosts.
p585600@10.116.196.254's password:
Creating home directory for p585600.
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ timeout 5 bash -c '</dev/tcp/10.244.61.74/2049' && echo OK || echo FALHOU
FALHOU
-sh-4.2$
