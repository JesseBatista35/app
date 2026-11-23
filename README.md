
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc login --token=sha256~93rEc0glXen2hmUCI9fh4BPECRiXlrexk_XOYaKSjSU --server=https://api.produtos4.caixa:6443
Logged into "https://api.produtos4.caixa:6443" as "p585600@corp.caixa.gov.br" using the token provided.

You have access to 269 projects, the list has been suppressed. You can list all projects with 'oc projects'

Using project "build-images-ads".
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get build -l buildconfig=sisgf-frontend
NAME                 TYPE     FROM     STATUS     STARTED       DURATION
sisgf-frontend-415   Source   Binary   Complete   3 days ago    20s
sisgf-frontend-416   Source   Binary   Complete   3 hours ago   22s
-sh-4.2$
-sh-4.2$
-sh-4.2$


nao tem build travada
