
-sh-4.2$
-sh-4.2$ oc exec sigsj-alvara-des-703-mmnmn -- curl -s localhost:8080/q/health/ready
{
    "status": "DOWN",
    "checks": [
        {
            "name": "Database connections health check",
            "status": "UP",
            "data": {
                "<default>": "UP"
            }
        },
        {
            "name": "CNJ indisponível",
            "status": "DOWN"
        },
        {
            "name": "SmallRye Reactive Messaging - readiness check",
            "status": "UP"
        }
    ]
}-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec sigsj-alvara-des-703-mmnmn -- curl -s localhost:8080/q/health/live
{
    "status": "UP",
    "checks": [
        {
            "name": "SmallRye Reactive Messaging - liveness check",
            "status": "UP"
        }
    ]
}-sh-4.2$ oc logs sigsj-alvara-des-703-mmnmn | grep -iE 'cnj|perfis|health' -A3
-sh-4.2$
-sh-4.2$





beleza entao vamos fechar respondetno tudo que ele questionou e mandar o que ele precisa corrgir
