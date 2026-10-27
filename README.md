NS=sigcb-tqs
APP=sigcb-backend-tqs

# 1. Estado do backend
oc get pods -n $NS -o wide | grep -i backend
oc get dc,deploy -n $NS | grep -i backend
oc rollout history dc/$APP -n $NS          # houve deploy em 26/10?

# 2. Endpoints: se vazio, explica o 503
oc get svc -n $NS | grep -i backend
oc get endpoints $APP -n $NS -o wide
oc describe svc $APP -n $NS                 # conferir Selector e TargetPort vs labels/porta do pod

# 3. Route(s): host, service alvo, porta, duplicidade
oc get route -n $NS -o wide | grep -i backend
oc get route -A | grep sigcb-backend-tqs    # outra Route com o mesmo host em outro ns?

# 4. Por que não está pronto
oc describe pod <pod-backend> -n $NS        # readiness/liveness, init containers, eventos
oc logs <pod-backend> -n $NS --all-containers --tail=200
oc get events -n $NS --sort-by=.lastTimestamp | tail -40
oc describe quota -n $NS



# De dentro do pod do frontend (mesma rede do cluster)
oc rsh -n $NS <pod-frontend-tqs>
curl -i -X OPTIONS http://$APP:<porta>/sigcb/beneficiario/beneficiarios?idBeneficiario=1100375 \
  -H "Origin: https://sigcb-frontend-tqs.apps.nprd.caixa" \
  -H "Access-Control-Request-Method: GET" \
  -H "Access-Control-Request-Headers: authorization"
