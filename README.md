oc label pod sispi-med-gestao-des-22-ckdkt -n sispi-des maistra.io/expose-route-
oc patch dc sispi-med-gestao-des -n sispi-des --type json \
  -p '[{"op":"remove","path":"/spec/template/metadata/labels/maistra.io~1expose-route"}]'
