
To see projects on another server, pass '--server=<server>'.
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc login --token=sha256~BFy4C3vzu4f166H7GoukPclblJJx3-cbkHlQRJHN5zo --server=https://api.nprd.caixa:6443
Logged into "https://api.nprd.caixa:6443" as "p585600@corp.caixa.gov.br" using the token provided.

You have access to 997 projects, the list has been suppressed. You can list all projects with 'oc projects'

Using project "sispi-des".
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc project sigcb-tqs
Now using project "sigcb-tqs" on server "https://api.nprd.caixa:6443".
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pods -n sigcb-tqs | grep backend
sigcb-backend-tqs-182-deploy     0/1       Completed   0                 116d
sigcb-backend-tqs-183-deploy     0/1       Completed   0                 4m45s
sigcb-backend-tqs-183-gnqxx      1/1       Running     0                 4m42s
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get endpoints sigcb-backend-tqs -n sigcb-tqs  # tem que listar IP:8080
NAME                ENDPOINTS          AGE
sigcb-backend-tqs   25.1.22.180:8080   2y66d
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get events -n sigcb-tqs --sort-by=.lastTimestamp | grep -iE "182|FailedMount|FailedCreatePodSandBox|FailedAttach"
F1027 15:18:44.321776   43672 sorter.go:306] Field {.lastTimestamp} in *unstructured.Unstructured is an unsortable type: interface, err: unsortable interface: interface
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc describe pod <pod-182> -n sigcb-tqs   # se ainda existir
-sh: pod-182: Arquivo ou diretório não encontrado
-sh-4.2$
