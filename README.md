 oc get pvc sisib-arquivos-de-quebra-data-des
NAME                                STATUS    VOLUME                              CAPACITY   ACCESS MODES   STORAGECLASS   AGE
sisib-arquivos-de-quebra-data-des   Bound     sisib-arquivos-de-quebra-data-des   50Gi       RWX                           21m
[p981778@cadsvaprlx067 ~]$ oc describe pvc sisib-arquivos-de-quebra-data-des
Name:          sisib-arquivos-de-quebra-data-des
Namespace:     sisib-des
StorageClass:
Status:        Bound
Volume:        sisib-arquivos-de-quebra-data-des
Labels:        <none>
Annotations:   pv.kubernetes.io/bind-completed=yes
Finalizers:    [kubernetes.io/pvc-protection]
Capacity:      50Gi
Access Modes:  RWX
VolumeMode:    Filesystem
[p981778@cadsvaprlx067 ~]$ oc get pv | grep sisib
sisib-arquivos-de-quebra-data-des                       50Gi       RWX            Retain           Bound         sisib-des/sisib-arquivos-de-quebra-data-des                                                                             22m
sisib-backend-data-des                                  5Gi        RWX            Retain           Bound         sisib-des/sisib-backend-data-des                                                                                        3y11d
sisib-batch-bacen-data-des                              5Gi        RWX            Retain           Bound         sisib-des/sisib-batch-bacen-data-des                                                                                    372d
sisib-oficio-data-des                                   1Gi        RWX            Retain           Bound         sisib-des/sisib-oficio-data-des                                                                                         363d
sisib-quebra-sigilo-data-des                            5Gi        RWX            Retain           Bound         sisib-des/sisib-quebra-sigilo-data-des                                                                                  2y67d
sisib-sisbajud-backend-data-des                         5Gi        RWX            Retain           Bound         sisib-des/sisib-sisbajud-backend-data-des                                                                               21d
sisib-sisbajud-backend-data-tqs                         5Gi        RWX            Retain           Bound         sisib-tqs/sisib-sisbajud-backend-data-tqs                                                                               43h
[p981778@cadsvaprlx067 ~]$


me ajuda a fechar a nota foi motnado conforme solicitado, o pod ano sobe pois tem um erro, neessario abrir u ma req para que a euipe possar relaizar o ajuste
