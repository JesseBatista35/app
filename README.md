   oc exec sigsj-alvara-des-702-m5bvt -- curl -s localhost:8080/q/health


      oc get pods -w | grep sigsj-alvara-des
   oc exec <pod-novo> -- curl -s localhost:8080/q/health      # após uns 30s de pod rodando
   oc describe pod <pod-novo> | sed -n '/Last State/,/Restart Count/p;/Events/,$p'
   oc logs <pod-novo> --previous                               # se reiniciar
