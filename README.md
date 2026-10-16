oc rsh -c sihdg-angular18-tqs sihdg-angular18-tqs-28-xw6jj sh -c 'cat /proc/1/cmdline | tr "\0" " "; echo; ls -la /deployments 2>/dev/null'
oc get secret caixa-truststore-acteste-nprd -n sihdg-tqs
