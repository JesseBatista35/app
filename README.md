oc debug dc/sidcx-host-des -c sidcx-host-des -n sidcx-des -- ls -laR /opt/app-root/src | head -50
oc debug dc/sidcx-host-des -c sidcx-host-des -n sidcx-des -- find /opt/app-root/src -maxdepth 4 -name index.html


oc debug dc/sidcx-host-des -c sidcx-host-des -n sidcx-des
# dentro do shell:
ls -la /opt/app-root/src; find / -name index.html 2>/dev/null | grep -v /usr/share
