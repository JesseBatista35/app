
-sh-4.2$ oc rsh -n $NS -c sigec-csc-frontend-tqs $POD sh -c 'getent hosts sigec-csc.esteiras.tqs.caixa; curl -skI https://sigec-csc.esteiras.tqs.caixa/csc-api/ | head -15'
10.116.180.23   sigec-csc.esteiras.tqs.caixa
HTTP/1.1 200 OK
Date: Tue, 24 Nov 2026 13:29:10 GMT
Server: JBoss-EAP/7
Accept-Language: pt-BR,pt;q=0.9,en-US;q=0.8,en;q=0.7
X-Powered-By: Undertow/1
Accept-Encoding: gzip, deflate
Access-Control-Allow-Headers: *
Access-Control-Expose-Headers: X-Total-Count
Accept-Ranges: bytes
Access-Control-Allow-Origin: *
Last-Modified: Thu, 29 Oct 2026 12:41:18 GMT
Access-Control-Allow-Credentials: true
Content-Type: text/html; charset=UTF-8
Content-Length: 1468
Access-Control-Allow-Methods: GET, HEAD, OPTIONS, POST, DELETE, PUT
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ NS=sigec-tqs
-sh-4.2$ POD=sigec-csc-frontend-tqs-83-rvzvp
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc logs -n $NS $POD -c sigec-csc-frontend-tqs --since=168h | grep -v kube-probe \
>   | grep -E 'request_time [0-9.]+ 504 |request_time [0-9]{3,}\.' | tail -20
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ nslookup 10.116.180.23
** server can't find 23.180.116.10.in-addr.arpa.: NXDOMAIN

-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$

Skip to main content
Azure DevOps
projetos
/
Caixa
/
Pipelines
/
Releases
Search


Caixa

Overview

Boards

Repos

Pipelines
Pipelines
Environments
Releases
Library
Task groups
Deployment groups
Portal Infra

Test Plans

Artifacts
Project settings
sigec-csc

New
SIGEC-csc-frontend-okd4
Edit

Create release

Releases
Deployments
Analytics

All releases


Row 5

Row 5

Row 5

Row 5

Row 2

Row 2

No pipelines match your search

Select a release pipeline to view its releases

16 pipelines found

Row 6

Row 2

29 pipelines found

Select a release pipeline to view its releases

18 pipelines found

Select a release pipeline to view its releases

7 pipelines found

Select a release pipeline to view its releases

4 pipelines found

Row 4

Row 5


Skip to main content
Azure DevOps
projetos
/
Caixa
/
Pipelines
/
Releases
Search


Caixa

Overview

Boards

Repos

Pipelines
Pipelines
Environments
Releases
Library
Task groups
Deployment groups
Portal Infra

Test Plans

Artifacts
Project settings
sigec-csc

New
SIGEC-CSC
Edit

Create release

Releases
Deployments
Analytics

All releases


Row 5

Row 5

Row 5

Row 2

Row 2

No pipelines match your search

Select a release pipeline to view its releases

16 pipelines found

Row 6

Row 2

29 pipelines found

Select a release pipeline to view its releases

18 pipelines found

Select a release pipeline to view its releases

7 pipelines found

Select a release pipeline to view its releases

4 pipelines found

Row 4

Row 5

Row 2




entoa qual proejto que é forntoendo ou csc?



