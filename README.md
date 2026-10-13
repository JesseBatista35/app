
-sh-4.2$
-sh-4.2$ oc get dc/sinfs-des -n sinfs-des -o jsonpath='{.spec.template.spec.initContainers[0].envFrom}{"\n"}'

-sh-4.2$
-sh-4.2$
-sh-4.2$ for ns in sinfs-des sinfs-tqs; do
>   echo "== $ns"; oc get secret bt-client-secret-$ns -n $ns -o jsonpath='{.data.BT_CLIENT_ID}' | base64 -d; echo
> done
== sinfs-des
3d9ed850-192e-4709-82e4-ff4a2e53268d
== sinfs-tqs
4c3c08e8-336e-4fa1-9919-e5f9f730f865
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
