oc get secret bt-client-secret-siifx-api-aplicacao-des -o jsonpath='{.data.BT_CLIENT_ID}' | base64 -d; echo
