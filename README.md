



oc get pods -n sispi-des -l deploymentconfig=sispi-qrcode-api-validador-des -o wide
oc get rc -n sispi-des | grep sispi-qrcode-api-validador

POD=<nome-do-pod>

oc logs $POD -n sispi-des -c sispi-qrcode-api-validador-des --previous | tail -300
# se der "previous terminated container not found", tire o --previous

oc get pod $POD -n sispi-des -o jsonpath='{.status.containerStatuses[?(@.name=="sispi-qrcode-api-validador-des")].lastState}{"\n"}'

oc exec $POD -n sispi-des -c sispi-qrcode-api-validador-des -- ls -l /deployments/



-sh-4.2$ oc get pods
NAME                                                      READY     STATUS             RESTARTS          AGE
sispi-agendar-pix-internos-des-7-deploy                   0/1       Completed          0                 60d
sispi-agendar-pix-internos-des-8-deploy                   0/1       Completed          0                 59d
sispi-agendar-pix-internos-des-8-tgzh4                    2/2       Running            0                 59d
sispi-agrupador-frontend-des-148-deploy                   0/1       Completed          0                 67d
sispi-agrupador-frontend-des-149-deploy                   0/1       Completed          0                 3d22h
sispi-agrupador-frontend-des-149-hckpn                    3/3       Running            2 (3d22h ago)     3d22h
sispi-api-consulta-chave-parceiros-des-75-deploy          0/1       Completed          0                 82d
sispi-api-consulta-chave-parceiros-des-76-deploy          0/1       Completed          0                 72d
sispi-api-consulta-chave-parceiros-des-76-jq4rs           1/2       CrashLoopBackOff   806 (2m46s ago)   72d
sispi-api-consulta-situacao-transacao-des-56-deploy       0/1       Completed          0                 126d
sispi-api-consulta-situacao-transacao-des-57-deploy       0/1       Completed          0                 89d
sispi-api-consulta-situacao-transacao-des-57-gwqq8        2/2       Running            0                 89d
sispi-api-dados-pix-interno-des-5-dkzcl                   2/2       Running            79 (13d ago)      112d
sispi-api-extrato-pix-des-242-deploy                      0/1       Completed          0                 3d9h
sispi-api-extrato-pix-des-243-6bvgt                       2/2       Running            0                 3d9h
sispi-api-extrato-pix-des-243-deploy                      0/1       Completed          0                 3d9h
sispi-api-fabrica-ids-des-36-deploy                       0/1       Completed          0                 122d
sispi-api-fabrica-ids-des-37-cv5d8                        2/2       Running            0                 68d
sispi-api-fabrica-ids-des-37-deploy                       0/1       Completed          0                 68d
sispi-api-fabrica-ids-des-37-sjr6x                        2/2       Running            0                 4d13h
sispi-api-feriados-des-3-zwxxv                            2/2       Running            9 (25d ago)       129d
sispi-api-gestao-documento-des-10-deploy                  0/1       Completed          0                 18m
sispi-api-gestao-documento-des-10-f45nr                   2/2       Running            0                 18m
sispi-api-gestao-documento-des-9-deploy                   0/1       Completed          0                 19h
sispi-api-notificacao-des-486-deploy                      0/1       Completed          0                 25h
sispi-api-notificacao-des-487-deploy                      0/1       Completed          0                 22h
sispi-api-notificacao-des-487-kfsfk                       2/2       Running            11 (153m ago)     22h
sispi-api-open-finance-des-38-deploy                      0/1       Completed          0                 26d
sispi-api-open-finance-des-39-deploy                      0/1       Completed          0                 26d
sispi-api-open-finance-des-39-tfn6g                       2/2       Running            0                 18d
sispi-api-participantes-pix-des-52-deploy                 0/1       Completed          0                 61d
sispi-api-participantes-pix-des-53-b2d75                  2/2       Running            0                 25d
sispi-api-participantes-pix-des-53-deploy                 0/1       Completed          0                 25d
sispi-api-pix-envio-interno-des-142-deploy                0/1       Completed          0                 53d
sispi-api-pix-envio-interno-des-143-deploy                0/1       Completed          0                 53d
sispi-api-pix-envio-interno-des-143-r7ndx                 2/2       Running            17 (3d21h ago)    53d
sispi-api-proxy-sso-des-86-bwfn9                          2/2       Running            0                 129d
sispi-api-rco-des-139-deploy                              0/1       Completed          0                 24d
sispi-api-rco-des-139-wfrmm                               2/2       Running            0                 24d
sispi-api-tarifacao-des-52-pk9gl                          2/2       Running            0                 7d
sispi-api-valida-pix-des-42-7dqzq                         2/2       Running            0                 129d
sispi-atendimento-bff-des-116-deploy                      0/1       Completed          0                 6d23h
sispi-atendimento-bff-des-117-66lvb                       2/2       Running            0                 6d23h
sispi-atendimento-bff-des-117-deploy                      0/1       Completed          0                 6d23h
sispi-atendimento-bff-des-117-pw7np                       2/2       Running            0                 6d23h
sispi-atendimento-bff-des-117-t859s                       2/2       Running            0                 6d23h
sispi-atendimento-bff-des-117-wpdlb                       2/2       Running            0                 6d23h
sispi-atendimento-frontend-des-140-deploy                 0/1       Completed          0                 4d
sispi-atendimento-frontend-des-141-deploy                 0/1       Completed          0                 19h
sispi-atendimento-frontend-des-141-m8sjt                  3/3       Running            2 (19h ago)       19h
sispi-backend-antifraude-des-89-deploy                    0/1       Completed          0                 39d
sispi-backend-antifraude-des-90-deploy                    0/1       Completed          0                 38d
sispi-backend-antifraude-des-90-trj2k                     2/2       Running            0                 4d
sispi-backend-batch-contabil-des-499-deploy               0/1       Completed          0                 48d
sispi-backend-batch-contabil-des-500-deploy               0/1       Completed          0                 34d
sispi-backend-batch-contabil-des-500-g7ptd                2/2       Running            6 (30h ago)       34d
sispi-backend-batch-dimp-des-34-deploy                    0/1       Completed          0                 95d
sispi-backend-batch-dimp-des-35-deploy                    0/1       Completed          0                 91d
sispi-backend-batch-dimp-des-35-gpjvs                     2/2       Running            0                 91d
sispi-backend-batch-efinanceira-des-66-z6c87              2/2       Running            0                 129d
sispi-backend-recebimento-des-394-deploy                  0/1       Completed          0                 3d23h
sispi-backend-recebimento-des-395-deploy                  0/1       Completed          0                 3d23h
sispi-backend-recebimento-des-395-h4rnk                   2/2       Running            0                 3d23h
sispi-backend-recebimento-secundario-des-453-deploy       0/1       Completed          0                 3d23h
sispi-backend-recebimento-secundario-des-454-8gxnb        2/2       Running            0                 3d22h
sispi-backend-recebimento-secundario-des-454-deploy       0/1       Completed          0                 3d22h
sispi-backend-retorno-des-497-deploy                      0/1       Completed          0                 22h
sispi-backend-retorno-des-498-deploy                      0/1       Completed          0                 21h
sispi-backend-retorno-des-498-nqcc2                       2/2       Running            0                 21h
sispi-backend-retorno-secundario-des-350-deploy           0/1       Completed          0                 4d
sispi-backend-retorno-secundario-des-351-deploy           0/1       Completed          0                 4d
sispi-backend-retorno-secundario-des-351-xvkh4            2/2       Running            0                 4d
sispi-batch-busca-pendencia-des-117-deploy                0/1       Completed          0                 10d
sispi-batch-busca-pendencia-des-118-5cwr9                 1/2       CrashLoopBackOff   664 (2m45s ago)   4d23h
sispi-batch-busca-pendencia-des-118-deploy                0/1       Completed          0                 4d23h
sispi-batch-extrato-relatorio-des-82-deploy               0/1       Completed          0                 17d
sispi-batch-extrato-relatorio-des-83-deploy               0/1       Completed          0                 17d
sispi-batch-extrato-relatorio-des-83-wcdwt                2/2       Running            0                 17d
sispi-batch-qrcode-certificados-des-47-khc4p              2/2       Running            2 (61d ago)       129d
sispi-batch-relatorio-operacional-des-35-deploy           0/1       Completed          0                 94d
sispi-batch-relatorio-operacional-des-36-deploy           0/1       Completed          0                 91d
sispi-batch-relatorio-operacional-des-36-r4fsj            2/2       Running            0                 91d
sispi-batch-resolve-pendencia-des-106-deploy              0/1       Completed          0                 10d
sispi-batch-resolve-pendencia-des-107-deploy              0/1       Completed          0                 4d22h
sispi-batch-resolve-pendencia-des-107-t8qwb               2/2       Running            1 (30h ago)       4d22h
sispi-batch-tratamento-bloqueio-antifraude-des-12-7d7qc   2/2       Running            0                 129d
sispi-container-backend-des-1035-deploy                   0/1       Completed          0                 3d19h
sispi-container-backend-des-1036-deploy                   0/1       Completed          0                 3d16h
sispi-container-backend-des-1036-gscmg                    2/2       Running            3 (3d16h ago)     3d16h
sispi-container-dict-des-874-deploy                       0/1       Completed          0                 3d20h
sispi-container-dict-des-875-deploy                       0/1       Completed          0                 18h
sispi-container-dict-des-875-kg4x9                        2/2       Running            0                 18h
sispi-container-frontend-des-634-deploy                   0/1       Completed          0                 2d12h
sispi-container-frontend-des-635-deploy                   0/1       Completed          0                 2d12h
sispi-container-frontend-des-635-g2cs7                    3/3       Running            2 (2d12h ago)     2d12h
sispi-dict-api-des-29-deploy                              0/1       Completed          0                 55d
sispi-dict-api-des-30-deploy                              0/1       Completed          0                 55d
sispi-dict-api-des-30-hbg4k                               2/2       Running            0                 19m
sispi-dict-api-med-des-159-deploy                         0/1       Completed          0                 3d17h
sispi-dict-api-med-des-160-deploy                         0/1       Completed          0                 3d17h
sispi-dict-api-med-des-160-fktrr                          2/2       Running            0                 3d17h
sispi-dict-balde-chaves-des-32-deploy                     0/1       Completed          0                 27d
sispi-dict-balde-chaves-des-33-deploy                     0/1       Completed          0                 7d20h
sispi-dict-balde-chaves-des-33-kf8j5                      2/2       Running            0                 7d20h
sispi-dict-batch-polling-des-734-deploy                   0/1       Completed          0                 23h
sispi-dict-batch-polling-des-735-deploy                   0/1       Completed          0                 22h
sispi-dict-batch-polling-des-735-rkrxh                    1/2       CrashLoopBackOff   329 (2m7s ago)    22h
sispi-dict-consulta-chaves-des-37-deploy                  0/1       Completed          0                 4d20h
sispi-dict-consulta-chaves-des-38-deploy                  0/1       Completed          0                 20h
sispi-dict-consulta-chaves-des-38-r8ftd                   2/2       Running            0                 83m
sispi-dict-consulta-estatisticas-des-58-deploy            0/1       Completed          0                 4d19h
sispi-dict-consulta-estatisticas-des-59-deploy            0/1       Completed          0                 3d21h
sispi-dict-consulta-estatisticas-des-59-f2h4x             2/2       Running            0                 3d21h
sispi-dict-gestao-chaves-des-54-deploy                    0/1       Completed          0                 52d
sispi-dict-gestao-chaves-des-55-95pmc                     2/2       Running            0                 52d
sispi-dict-gestao-chaves-des-55-deploy                    0/1       Completed          0                 52d
sispi-dict-lista-restrita-des-75-deploy                   0/1       Completed          0                 5d20h
sispi-dict-lista-restrita-des-76-d85td                    1/2       CrashLoopBackOff   378 (3m46s ago)   3d19h
sispi-dict-lista-restrita-des-76-deploy                   0/1       Completed          0                 3d19h
sispi-dict-polling-des-114-deploy                         0/1       Completed          0                 3d18h
sispi-dict-polling-des-115-deploy                         0/1       Completed          0                 3d18h
sispi-dict-polling-des-115-gmcmr                          2/2       Running            0                 3d18h
sispi-dict-processar-antifraude-des-22-deploy             0/1       Completed          0                 3d20h
sispi-dict-processar-antifraude-des-23-deploy             0/1       Completed          0                 85m
sispi-dict-processar-antifraude-des-23-szpwt              2/2       Running            0                 85m
sispi-dict-processar-arquivo-des-17-deploy                0/1       Completed          0                 77d
sispi-dict-processar-arquivo-des-18-deploy                0/1       Completed          0                 77d
sispi-dict-validacao-posse-des-10-deploy                  0/1       Completed          0                 3d19h
sispi-dict-validacao-posse-des-10-pkg72                   2/2       Running            0                 3d19h
sispi-dict-validacao-posse-des-9-deploy                   0/1       Completed          0                 6d1h
sispi-dict-verifica-chaves-batch-des-38-deploy            0/1       Completed          0                 126d
sispi-dict-verifica-chaves-batch-des-38-g5t6l             2/2       Running            0                 126d
sispi-dict-verifica-chaves-des-74-deploy                  0/1       Completed          0                 84d
sispi-dict-verifica-chaves-des-75-deploy                  0/1       Completed          0                 69d
sispi-dict-verifica-chaves-des-75-v95cx                   2/2       Running            0                 69d
sispi-disparador-eventos-des-1-cc5pl                      2/2       Running            0                 20d
sispi-disparador-eventos-des-1-deploy                     0/1       Completed          0                 20d
sispi-envio-notif-intra-bacen-des-125-deploy              0/1       Completed          0                 52d
sispi-envio-notif-intra-bacen-des-126-2d7xg               2/2       Running            15 (21h ago)      26d
sispi-envio-notif-intra-bacen-des-126-deploy              0/1       Completed          0                 26d
sispi-med-auditoria-des-29-deploy                         0/1       Completed          0                 94d
sispi-med-auditoria-des-30-deploy                         0/1       Completed          0                 82d
sispi-med-auditoria-des-30-x5zjs                          2/2       Running            0                 82d
sispi-med-gestao-des-21-deploy                            0/1       Completed          0                 19h
sispi-med-gestao-des-22-ckdkt                             2/2       Running            0                 18h
sispi-med-gestao-des-22-deploy                            0/1       Completed          0                 18h
sispi-med-orquestrador-des-10-deploy                      0/1       Completed          0                 48d
sispi-med-orquestrador-des-11-deploy                      0/1       Completed          0                 18d
sispi-med-polling-des-13-deploy                           0/1       Completed          0                 55d
sispi-med-polling-des-14-deploy                           0/1       Completed          0                 18d
sispi-parametrizacoes-pix-des-43-j9kzn                    2/2       Running            0                 129d
sispi-pix-api-onboarding-des-93-6krnb                     2/2       Running            2 (35d ago)       129d
sispi-pix-gestao-des-640-deploy                           0/1       Completed          0                 4d
sispi-pix-gestao-des-641-4chkc                            2/2       Running            0                 4d
sispi-pix-gestao-des-641-deploy                           0/1       Completed          0                 4d
sispi-pix-gestao-dict-des-304-deploy                      0/1       Completed          0                 5d20h
sispi-pix-gestao-dict-des-305-72r7g                       2/2       Running            0                 21h
sispi-pix-gestao-dict-des-305-deploy                      0/1       Completed          0                 21h
sispi-pix-med-des-393-deploy                              0/1       Completed          0                 3d17h
sispi-pix-med-des-394-bpttm                               2/2       Running            12 (43m ago)      3d16h
sispi-pix-med-des-394-deploy                              0/1       Completed          0                 3d16h
sispi-pocrosa-orchestrator-des-24-deploy                  0/1       Completed          0                 21d
sispi-pocrosa-orchestrator-des-25-deploy                  0/1       Completed          0                 20d
sispi-pocrosa-orchestrator-des-25-k47mf                   2/2       Running            2 (5d13h ago)     20d
sispi-processar-ans-iga-des-70-deploy                     0/1       Completed          0                 48d
sispi-processar-ans-iga-des-71-5k6qc                      2/2       Running            2 (21h ago)       4d18h
sispi-processar-ans-iga-des-71-deploy                     0/1       Completed          0                 6d21h
sispi-processar-fila-secundario-des-44-4lbxh              1/2       Running            2 (7d10h ago)     129d
sispi-processar-health-check-des-37-fgf7f                 2/2       Running            39 (3d2h ago)     129d
sispi-processar-health-check-des-37-zqt6z                 2/2       Running            23 (4d ago)       126d
sispi-processar-mensagem-contabil-des-111-deploy          0/1       Completed          0                 3d19h
sispi-processar-mensagem-contabil-des-112-deploy          0/1       Completed          0                 3d19h
sispi-processar-mensagem-contabil-des-112-tnxf5           2/2       Running            0                 3d19h
sispi-processar-notif-intra-bacen-des-87-deploy           0/1       Completed          0                 59d
sispi-processar-notif-intra-bacen-des-88-deploy           0/1       Completed          0                 26d
sispi-processar-notif-intra-bacen-des-88-pffwm            2/2       Running            9 (21h ago)       26d
sispi-processar-pix-automatico-des-268-deploy             0/1       Completed          0                 4d
sispi-processar-pix-automatico-des-269-2ddzs              2/2       Running            1 (30h ago)       4d
sispi-processar-pix-automatico-des-269-deploy             0/1       Completed          0                 4d
sispi-processar-pix-externo-des-57-deploy                 0/1       Completed          0                 3d15h
sispi-processar-pix-externo-des-58-deploy                 0/1       Completed          0                 25h
sispi-processar-pix-externo-des-58-tc5vx                  2/2       Running            1 (21h ago)       25h
sispi-processar-pix-internos-des-618-deploy               0/1       Completed          0                 15m
sispi-processar-pix-internos-des-618-wj8ms                1/2       Running            4 (56s ago)       10m
sispi-processar-pix-internos-des-619-deploy               1/1       Running            0                 8m16s
sispi-processar-pix-internos-des-619-wbkgr                1/2       Running            3 (51s ago)       8m12s
sispi-processar-pix-internos-primario-des-240-deploy      0/1       Completed          0                 81m
sispi-processar-pix-internos-primario-des-240-ttxvx       2/2       Running            0                 81m
sispi-processar-pix-internos-primario-des-243-deploy      1/1       Running            0                 4m28s
sispi-processar-pix-internos-primario-des-243-sj99v       1/2       Running            0                 4m23s
sispi-processar-recebimento-des-1-deploy                  0/1       Completed          0                 29d
sispi-processar-recebimento-des-2-deploy                  0/1       Completed          0                 28d
sispi-processar-recebimento-pix-auto-des-59-ftmjp         2/2       Running            70 (21h ago)      129d
sispi-processar-recebimento-sec-des-50-deploy             0/1       Completed          0                 28d
sispi-processar-recebimento-sec-des-51-deploy             0/1       Completed          0                 27d
sispi-processar-resolve-pendencia-des-246-deploy          0/1       Completed          0                 4d22h
sispi-processar-resolve-pendencia-des-247-deploy          0/1       Completed          0                 4d22h
sispi-processar-resolve-pendencia-des-247-n6ssg           2/2       Running            0                 4d22h
sispi-processar-solicitacao-historico-des-138-deploy      0/1       Completed          0                 4d
sispi-processar-solicitacao-historico-des-139-deploy      0/1       Completed          0                 4d
sispi-processar-solicitacao-historico-des-139-gmn4r       2/2       Running            0                 4d
sispi-processar-solicitacao-notificacao-des-159-deploy    0/1       Completed          0                 53d
sispi-processar-solicitacao-notificacao-des-160-6ndpn     1/2       Running            70 (5m9s ago)     4h32m
sispi-processar-solicitacao-notificacao-des-160-deploy    0/1       Completed          0                 18d
sispi-processar-solicitacao-push-des-68-deploy            0/1       Completed          0                 122d
sispi-processar-solicitacao-push-des-69-ccqt7             2/2       Running            0                 20d
sispi-processar-solicitacao-push-des-69-deploy            0/1       Completed          0                 122d
sispi-processar-tempo-envio-intra-bacen-des-19-9sblj      2/2       Running            1 (101d ago)      129d
sispi-processar-tratamento-padrao-siatr-des-165-deploy    0/1       Completed          0                 105d
sispi-processar-tratamento-padrao-siatr-des-166-deploy    0/1       Completed          0                 97d
sispi-processar-tratamento-padrao-siatr-des-166-mq5mk     2/2       Running            0                 97d
sispi-qrcode-api-consultas-des-452-deploy                 0/1       Completed          0                 6d2h
sispi-qrcode-api-consultas-des-453-deploy                 0/1       Completed          0                 6d2h
sispi-qrcode-api-consultas-des-453-qd9c7                  2/2       Running            1 (13h ago)       6d2h
sispi-qrcode-api-credenciamento-des-442-deploy            0/1       Completed          0                 13d
sispi-qrcode-api-credenciamento-des-443-cmq9r             2/2       Running            0                 13d
sispi-qrcode-api-credenciamento-des-443-deploy            0/1       Completed          0                 13d
sispi-qrcode-api-dinamico-des-383-deploy                  0/1       Completed          0                 6d21h
sispi-qrcode-api-dinamico-des-384-4vhh9                   2/2       Running            13 (3d21h ago)    6d1h
sispi-qrcode-api-dinamico-des-384-deploy                  0/1       Completed          0                 6d1h
sispi-qrcode-api-dinamico-lote-des-177-deploy             0/1       Completed          0                 12d
sispi-qrcode-api-dinamico-lote-des-178-deploy             0/1       Completed          0                 6d22h
sispi-qrcode-api-dinamico-lote-des-178-s72gc              2/2       Running            6 (23h ago)       4d23h
sispi-qrcode-api-estatico-des-74-w5jqt                    2/2       Running            0                 129d
sispi-qrcode-api-externo-des-214-deploy                   0/1       Completed          0                 54d
sispi-qrcode-api-externo-des-215-deploy                   0/1       Completed          0                 54d
sispi-qrcode-api-externo-des-215-wkc56                    2/2       Running            2 (2d1h ago)      54d
sispi-qrcode-api-prelocation-des-111-csgf6                2/2       Running            0                 129d
sispi-qrcode-api-validador-des-296-deploy                 0/1       Completed          0                 12d
sispi-qrcode-api-validador-des-297-6jjtp                  1/2       Running            1 (21s ago)       2m51s
sispi-qrcode-api-validador-des-297-deploy                 0/1       Completed          0                 6d19h
sispi-qrcode-api-validador-des-308-deploy                 0/1       Error              0                 120m
sispi-qrcode-api-validador-des-309-deploy                 0/1       Error              0                 47m
sispi-qrcode-api-webhook-des-93-deploy                    0/1       Completed          0                 98d
sispi-qrcode-api-webhook-des-93-dpk5n                     2/2       Running            607 (20h ago)     98d
sispi-qrcode-clientid-exclusivo-des-10-deploy             0/1       Completed          0                 83d
sispi-qrcode-clientid-exclusivo-des-10-mwlln              2/2       Running            0                 83d
sispi-qrcode-clientid-exclusivo-des-9-deploy              0/1       Completed          0                 83d
sispi-qrcode-envia-notificacao-des-16-deploy              0/1       Completed          0                 83d
sispi-qrcode-envia-notificacao-des-17-deploy              0/1       Completed          0                 83d
sispi-qrcode-envia-notificacao-des-17-q77xt               2/2       Running            0                 83d
sispi-qrcode-frontend-des-304-deploy                      0/1       Completed          0                 65m
sispi-qrcode-frontend-des-305-deploy                      0/1       Completed          0                 61m
sispi-qrcode-frontend-des-305-r4tmj                       3/3       Running            2 (61m ago)       61m
sispi-qrcode-migracao-dn-des-24-deploy                    0/1       Completed          0                 40d
sispi-qrcode-migracao-dn-des-25-deploy                    0/1       Completed          0                 40d
sispi-qualidade-roteador-des-33-xjc4f                     2/2       Running            0                 129d
sispi-reenvio-notificacao-des-74-gbf89                    1/2       Running            0                 129d
sispi-resolve-pendencia-notif-intra-bacen-des-67-deploy   0/1       Completed          0                 101d
sispi-resolve-pendencia-notif-intra-bacen-des-68-5ftll    2/2       Running            0                 91d
sispi-resolve-pendencia-notif-intra-bacen-des-68-deploy   0/1       Completed          0                 91d
-sh-4.2$
