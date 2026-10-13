
sh-5.1$ command terminated with exit code 137
-sh-4.2$ oc get pods -n sihdg-des
NAME                            READY     STATUS      RESTARTS   AGE
sihdg-angular18-des-36-deploy   0/1       Completed   0          4d20h
sihdg-angular18-des-37-8kcqk    2/2       Running     0          3d9h
sihdg-angular18-des-37-deploy   0/1       Completed   0          3d9h
sihdg-backend-des-329-deploy    0/1       Completed   0          84d
sihdg-backend-des-330-6pl4m     1/1       Running     0          38d
sihdg-backend-des-330-deploy    0/1       Completed   0          38d
sihdg-frontend-des-195-deploy   0/1       Completed   0          165d
sihdg-frontend-des-196-6kk65    2/2       Running     0          147d
sihdg-frontend-des-196-deploy   0/1       Completed   0          147d
sihdg-jboss8-des-115-deploy     0/1       Completed   0          5d18h
sihdg-jboss8-des-116-deploy     0/1       Completed   0          5d
sihdg-jboss8-des-116-mq4ct      1/1       Running     0          5d
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ ^C
-sh-4.2$ oc rsh -n sihdg-des -c <container> sihdg-jboss8-des-116-mq4ct curl -s -o /dev/null -w "%{http_code}\n" http://localhost:8080/sihdg-api/health/ready
-sh: container: Arquivo ou diretório não encontrado
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc rsh -n sihdg-des -c sihdg-des sihdg-jboss8-des-116-mq4ct curl -s -o /dev/null -w "%{http_code}\n" http://localhost:8080/sihdg-api/health/ready
Error from server (BadRequest): container sihdg-des is not valid for pod sihdg-jboss8-des-116-mq4ct
-sh-4.2$
