oc exec sigsj-alvara-des-703-mmnmn -- curl -s localhost:8080/q/health/ready
oc exec sigsj-alvara-des-703-mmnmn -- curl -s localhost:8080/q/health/live
oc logs sigsj-alvara-des-703-mmnmn | grep -iE 'cnj|perfis|health' -A3
