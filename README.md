
-sh-4.2$
-sh-4.2$ oc label pod sispi-med-gestao-des-22-ckdkt -n sispi-des maistra.io/expose-route-
pod/sispi-med-gestao-des-22-ckdkt labeled
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc patch dc sispi-med-gestao-des -n sispi-des --type json \
>   -p '[{"op":"remove","path":"/spec/template/metadata/labels/maistra.io~1expose-route"}]'
deploymentconfig.apps.openshift.io/sispi-med-gestao-des patched
-sh-4.2$
-sh-4.2$
-sh-4.2$
