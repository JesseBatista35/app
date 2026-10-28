oc get pods -n sigsj-des -l name=sigsj-frontend-rc-des
oc describe pod sigsj-frontend-rc-des-28-fxnxf -n sigsj-des | tail -30
oc logs sigsj-frontend-rc-des-28-fxnxf -n sigsj-des --previous

# ver onde o bundle ficou dentro da imagem
oc debug dc/sigsj-frontend-rc-des -n sigsj-des -- sh -c 'ls -la /opt/app-root/src; find /opt/app-root/src -maxdepth 3 -name "main*.js"'

