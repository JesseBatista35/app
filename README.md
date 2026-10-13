oc get secret bt-client-secret-sinfs-tqs -n sinfs-tqs -o jsonpath='{.data.BT_CLIENT_SECRET}' | base64 -d; echo
