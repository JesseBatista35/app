NS=sigec-tqs
POD=sigec-csc-frontend-tqs-83-rvzvp

# 1. requisições reais com 504 ou que demoraram >= 100s (sem probes)
oc logs -n $NS $POD -c sigec-csc-frontend-tqs --since=168h | grep -v kube-probe \
  | grep -E 'request_time [0-9.]+ 504 |request_time [0-9]{3,}\.' | tail -20

# 2. o 10.116.180.23 é VM ou VIP?
nslookup 10.116.180.23
