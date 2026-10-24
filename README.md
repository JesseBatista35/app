oc get pods -n sicow-des | grep conres-okd
oc logs <pod-conres-atual> -n sicow-des | grep -E "OPVDX001|WFLYCTL0362|ModuleNotFound|WFLYUT0021|WFLYSRV0010|WFLYSRV0025|WFLYSRV0026|veio sem valor|Login failed|scowdb01" | head -30
