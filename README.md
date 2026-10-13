for ns in sinfs-des sinfs-tqs; do
  echo "== $ns"; oc get secret bt-client-secret-$ns -n $ns -o jsonpath='{.data.BT_CLIENT_ID}' | base64 -d; echo
done
