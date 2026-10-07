
-sh-4.2$
-sh-4.2$ oc project sihdg-des
Now using project "sihdg-des" on server "https://api.nprd.caixa:6443".
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pods
NAME                            READY     STATUS      RESTARTS   AGE
sihdg-angular18-des-33-deploy   0/1       Completed   0          25h
sihdg-angular18-des-34-deploy   0/1       Completed   0          4h52m
sihdg-angular18-des-34-rrzz8    2/2       Running     0          4h52m
sihdg-backend-des-329-deploy    0/1       Completed   0          79d
sihdg-backend-des-330-6pl4m     1/1       Running     0          33d
sihdg-backend-des-330-deploy    0/1       Completed   0          33d
sihdg-frontend-des-195-deploy   0/1       Completed   0          160d
sihdg-frontend-des-196-6kk65    2/2       Running     0          142d
sihdg-frontend-des-196-deploy   0/1       Completed   0          142d
sihdg-jboss8-des-112-deploy     0/1       Completed   0          52m
sihdg-jboss8-des-113-6hhvc      1/1       Running     0          5m6s
sihdg-jboss8-des-113-deploy     0/1       Completed   0          5m10s
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc rsh sihdg-jboss8-des-113-6hhvc
sh-5.1$ df -h | grep sihdg
nprdnfs01.ad.caixa:/ifs/cpwsprd01/nprd/fs_sihdg_sinaf   50G     0   50G   0% /sihdg_sinaf
hypernprd56.ad.caixa:/fs_sihdg                          50G     0   50G   0% /sihdg_des_pwc
sh-5.1$
sh-5.1$
sh-5.1$
