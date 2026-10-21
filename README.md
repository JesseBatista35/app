
Using project "sisei-des".
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pods -n sigsj-des -l name=sigsj-alvara-des
NAME                         READY     STATUS    RESTARTS   AGE
sigsj-alvara-des-702-m5bvt   1/1       Running   0          25m
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc project sigsj-des
Now using project "sigsj-des" on server "https://api.nprd.caixa:6443".
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pods
NAME                                             READY     STATUS      RESTARTS         AGE
sigsj-alvara-des-701-deploy                      0/1       Completed   0                19h
sigsj-alvara-des-702-deploy                      0/1       Completed   0                25m
sigsj-alvara-des-702-m5bvt                       1/1       Running     0                25m
sigsj-alvara-sandbox-des-147-deploy              0/1       Completed   0                6d21h
sigsj-alvara-sandbox-des-147-tjscn               1/1       Running     0                6d21h
sigsj-api-des-79-deploy                          0/1       Completed   0                15d
sigsj-api-des-80-8nqfb                           1/1       Running     2 (12d ago)      15d
sigsj-api-des-80-deploy                          0/1       Completed   0                15d
sigsj-api-rpv-backend-des-30-deploy              0/1       Completed   0                5d21h
sigsj-api-rpv-backend-des-31-deploy              0/1       Completed   0                3h15m
sigsj-api-rpv-backend-des-31-fdh8k               1/1       Running     0                3h15m
sigsj-assincrono-des-23-deploy                   0/1       Completed   0                3h32m
sigsj-assincrono-des-24-deploy                   0/1       Completed   0                3h16m
sigsj-assincrono-des-24-wzg76                    1/1       Running     0                3h16m
sigsj-backend-area-cliente-des-207-deploy        0/1       Completed   0                5d21h
sigsj-backend-area-cliente-des-208-2ph9w         1/1       Running     0                4h22m
sigsj-backend-area-cliente-des-208-deploy        0/1       Completed   0                4h23m
sigsj-backend-area-gestora-des-79-deploy         0/1       Completed   0                13d
sigsj-backend-area-gestora-des-80-deploy         0/1       Completed   0                7d20h
sigsj-backend-area-gestora-des-80-h64tv          1/1       Running     0                7d20h
sigsj-backend-des-19-5zfdz                       1/1       Running     190 (17m ago)    309d
sigsj-backend-plataforma-des-27-deploy           0/1       Completed   0                47h
sigsj-backend-plataforma-des-28-deploy           0/1       Completed   0                23h
sigsj-backend-plataforma-des-28-s7hg4            1/1       Running     0                23h
sigsj-backend-privado-des-214-deploy             0/1       Completed   0                7d4h
sigsj-backend-privado-des-215-ck2qx              1/1       Running     0                7d3h
sigsj-backend-privado-des-215-deploy             0/1       Completed   0                7d3h
sigsj-backend-publico-des-235-deploy             0/1       Completed   0                32d
sigsj-backend-publico-des-236-5sqwb              1/1       Running     0                26h
sigsj-backend-publico-des-236-deploy             0/1       Completed   0                26h
sigsj-backend-publico-rc-des-10-deploy           0/1       Completed   0                20d
sigsj-backend-publico-rc-des-10-h9bqq            1/1       Running     0                20d
sigsj-backend-publico-rc-des-9-deploy            0/1       Completed   0                42d
sigsj-backend-report-des-1-jds47                 1/1       Running     0                378d
sigsj-cadastro-des-31-deploy                     0/1       Completed   0                20d
sigsj-cadastro-des-32-deploy                     0/1       Completed   0                20d
sigsj-cadastro-des-32-xqmjh                      1/1       Running     0                20d
sigsj-cadastro-sandbox-des-4-deploy              0/1       Completed   0                26h
sigsj-cadastro-sandbox-des-5-bhf87               1/1       Running     0                26h
sigsj-cadastro-sandbox-des-5-deploy              0/1       Completed   0                26h
sigsj-convivencia-des-280-deploy                 0/1       Completed   0                26d
sigsj-convivencia-des-281-deploy                 0/1       Completed   0                25d
sigsj-convivencia-des-281-fq8nn                  1/1       Running     33 (7h50m ago)   25d
sigsj-deposito-des-325-deploy                    0/1       Completed   0                6d21h
sigsj-deposito-des-326-deploy                    0/1       Completed   0                26h
sigsj-deposito-des-326-ln4pq                     1/1       Running     0                26h
sigsj-deposito-rc-des-45-deploy                  0/1       Completed   0                20d
sigsj-deposito-rc-des-46-deploy                  0/1       Completed   0                7d21h
sigsj-deposito-rc-des-46-ptbw5                   1/1       Running     0                7d21h
sigsj-deposito-sandbox-des-134-deploy            0/1       Completed   0                27d
sigsj-deposito-sandbox-des-135-4msmj             1/1       Running     0                26d
sigsj-deposito-sandbox-des-135-deploy            0/1       Completed   0                26d
sigsj-destinacao-des-134-deploy                  0/1       Completed   0                28d
sigsj-destinacao-des-135-deploy                  0/1       Completed   0                26d
sigsj-destinacao-des-135-l8r9m                   1/1       Running     0                26d
sigsj-dev-back-des-96-deploy                     0/1       Completed   0                21h
sigsj-dev-back-des-97-2vdd8                      1/1       Running     0                21h
sigsj-dev-back-des-97-deploy                     0/1       Completed   0                21h
sigsj-dev-front-des-38-deploy                    0/1       Completed   0                45h
sigsj-dev-front-des-39-2hjzz                     2/2       Running     0                21h
sigsj-dev-front-des-39-deploy                    0/1       Completed   0                21h
sigsj-dromos-alvara-des-57-5cw62                 1/1       Running     14 (7d5h ago)    434d
sigsj-dromos-des-27-deploy                       0/1       Completed   0                376d
sigsj-dromos-des-27-hw2t5                        1/1       Running     168 (15h ago)    376d
sigsj-frontend-11-des-1-deploy                   0/1       Completed   0                75d
sigsj-frontend-11-des-1-wlgd5                    2/2       Running     0                75d
sigsj-frontend-area-cliente-des-50-pjrkc         2/2       Running     0                414d
sigsj-frontend-area-gestora-des-40-deploy        0/1       Completed   0                21d
sigsj-frontend-area-gestora-des-41-deploy        0/1       Completed   0                21d
sigsj-frontend-area-gestora-des-41-g69mf         2/2       Running     0                21d
sigsj-frontend-des-492-deploy                    0/1       Completed   0                34d
sigsj-frontend-des-493-deploy                    0/1       Completed   0                33d
sigsj-frontend-des-494-deploy                    0/1       Completed   0                33d
sigsj-frontend-des-495-deploy                    0/1       Completed   0                33d
sigsj-frontend-des-496-deploy                    0/1       Completed   0                33d
sigsj-frontend-des-497-deploy                    0/1       Completed   0                33d
sigsj-frontend-des-498-deploy                    0/1       Completed   0                33d
sigsj-frontend-des-499-deploy                    0/1       Completed   0                33d
sigsj-frontend-des-500-deploy                    0/1       Completed   0                32d
sigsj-frontend-des-501-deploy                    0/1       Completed   0                23d
sigsj-frontend-des-502-deploy                    0/1       Completed   0                20d
sigsj-frontend-des-503-deploy                    0/1       Completed   0                20d
sigsj-frontend-des-504-deploy                    0/1       Completed   0                19d
sigsj-frontend-des-505-deploy                    0/1       Completed   0                14d
sigsj-frontend-des-506-deploy                    0/1       Completed   0                14d
sigsj-frontend-des-507-deploy                    0/1       Completed   0                13d
sigsj-frontend-des-508-deploy                    0/1       Completed   0                12d
sigsj-frontend-des-509-deploy                    0/1       Completed   0                6d22h
sigsj-frontend-des-510-deploy                    0/1       Completed   0                47h
sigsj-frontend-des-511-deploy                    0/1       Completed   0                47h
sigsj-frontend-des-512-8qzqv                     2/2       Running     0                26h
sigsj-frontend-des-512-deploy                    0/1       Completed   0                26h
sigsj-frontend-precatorio-des-160-deploy         0/1       Completed   0                39d
sigsj-frontend-precatorio-des-161-deploy         0/1       Completed   0                14d
sigsj-frontend-precatorio-des-161-zjw7x          2/2       Running     0                14d
sigsj-frontend-rc-des-24-deploy                  0/1       Completed   0                5d3h
sigsj-frontend-rc-des-25-deploy                  0/1       Completed   0                5d2h
sigsj-frontend-rc-des-25-gltfz                   2/2       Running     0                5d2h
sigsj-frontend-sandbox-des-15-deploy             0/1       Completed   0                236d
sigsj-frontend-sandbox-des-16-2q774              2/2       Running     0                68d
sigsj-frontend-sandbox-des-16-deploy             0/1       Completed   0                68d
sigsj-integracao-rest-soap-des-13-deploy         0/1       Completed   0                55d
sigsj-integracao-rest-soap-des-14-deploy         0/1       Completed   0                53d
sigsj-integracao-rest-soap-des-14-kb746          1/1       Running     0                53d
sigsj-intranet-back-levantamento-des-30-deploy   0/1       Completed   0                2d3h
sigsj-intranet-back-levantamento-des-31-4hspp    1/1       Running     0                162m
sigsj-intranet-back-levantamento-des-31-deploy   0/1       Completed   0                162m
sigsj-intranet-front-lvnto-des-12-deploy         0/1       Completed   0                47h
sigsj-intranet-front-lvnto-des-13-deploy         0/1       Completed   0                162m
sigsj-intranet-front-lvnto-des-13-g78zt          2/2       Running     0                162m
sigsj-notificacao-des-263-deploy                 0/1       Completed   0                5d3h
sigsj-notificacao-des-264-6d728                  1/1       Running     0                28h
sigsj-notificacao-des-264-deploy                 0/1       Completed   0                28h
sigsj-plataforma-microfront-des-11-deploy        0/1       Completed   0                153d
sigsj-plataforma-microfront-des-12-deploy        0/1       Completed   0                135d
sigsj-plataforma-microfront-des-12-pjlx7         2/2       Running     0                135d
sigsj-saldo-des-327-deploy                       0/1       Completed   0                5d21h
sigsj-saldo-des-328-deploy                       0/1       Completed   0                5d
sigsj-saldo-des-328-plmnl                        1/1       Running     0                5d
sigsj-saldo-sandbox-des-18-deploy                0/1       Completed   0                50d
sigsj-saldo-sandbox-des-19-deploy                0/1       Completed   0                7d23h
sigsj-saldo-sandbox-des-19-xz7fr                 1/1       Running     0                7d23h
sigsj-super-app-des-19-deploy                    0/1       Completed   0                42d
sigsj-super-app-des-20-deploy                    0/1       Completed   0                22d
sigsj-super-app-des-20-fvfzg                     1/1       Running     0                22d
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc logs sigsj-alvara-des-693-gnfhp -c sigsj-alvara-des -n sigsj-des --previous
Error from server (NotFound): pods "sigsj-alvara-des-693-gnfhp" not found
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get events -n sigsj-des --sort-by=.lastTimestamp | grep -i alvara
F1021 14:11:35.170772   61363 sorter.go:306] Field {.lastTimestamp} in *unstructured.Unstructured is an unsortable type: interface, err: unsortable interface: interface
-sh-4.2$
