<img width="1888" height="913" alt="image" src="https://github.com/user-attachments/assets/b00924c0-9b29-40e0-bbdb-38954dc0155e" />


ele estava com o secret_cert-jksJBOS habilitdao e dava esse erro


<img width="1194" height="700" alt="image" src="https://github.com/user-attachments/assets/3eca26e1-7251-404b-835d-ea3bc6b7ff88" />


eu habilietei o multipla conforme esta em DES

SO QUE AGORA TA DAN ESSE ERRO


2026-10-13T18:45:19.5708654Z ##[section]Starting: Adicionando Multiplas Secrets
2026-10-13T18:45:19.5749035Z ==============================================================================
2026-10-13T18:45:19.5749141Z Task         : Bash
2026-10-13T18:45:19.5749189Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-13T18:45:19.5749271Z Version      : 3.227.0
2026-10-13T18:45:19.5749316Z Author       : Microsoft Corporation
2026-10-13T18:45:19.5749541Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-13T18:45:19.5749627Z ==============================================================================
2026-10-13T18:45:20.5022860Z Generating script.
2026-10-13T18:45:20.5033457Z ========================== Starting Command Output ===========================
2026-10-13T18:45:20.5040673Z [command]/bin/bash /opt/ads-agent/_work/_temp/65cff972-17d1-4c0a-b4e0-6304cf6664b3.sh
2026-10-13T18:45:20.5137370Z Variavel de ambiente com o certificado = CACERTIFICATE_SECUREFILEPATH=/opt/ads-agent/_work/_temp/cacerts_sinfs_intra_tqs2
2026-10-13T18:45:20.5141842Z Encontrado certificado = cacerts_sinfs_intra_tqs2 com o PATH /opt/ads-agent/_work/_temp/cacerts_sinfs_intra_tqs2
2026-10-13T18:45:20.5142397Z nome do arquivo final = cacerts_sinfs_intra_tqs2
2026-10-13T18:45:20.5158498Z nome da Secret Name = cacerts-sinfs-intra-tqs2
2026-10-13T18:45:20.5158842Z LOCALIZANDO SECRET OKD
2026-10-13T18:45:20.7373523Z NAME                       TYPE      DATA      AGE
2026-10-13T18:45:20.7374222Z cacerts-sinfs-intra-tqs2   Opaque    1         3m35s
2026-10-13T18:45:20.7410116Z EXCLUINDO SECRET OKD
2026-10-13T18:45:20.9851185Z secret "cacerts-sinfs-intra-tqs2" deleted
2026-10-13T18:45:20.9921268Z CRIANDO SECRET OKD
2026-10-13T18:45:21.1926791Z secret/cacerts-sinfs-intra-tqs2 created
2026-10-13T18:45:21.1964839Z oc create secret generic cacerts-sinfs-intra-tqs2 --from-file=cacerts_sinfs_intra_tqs2 -n sinfs-tqs
2026-10-13T18:45:21.1965322Z SET VOLUME COM NOVA SECRET
2026-10-13T18:45:21.4331116Z warning: volume "cacerts-sinfs-intra-tqs2" did not previously exist and was not overriden. A new volume with this name has been created instead.error: deploymentconfigs/sinfs-tqs volume mount '/opt/jboss/standalone/configuration/cacerts_sinfs_intra_tqs2' already exists for container 'sinfs-tqs'
2026-10-13T18:45:21.4400423Z ##[error]Bash exited with code '1'.
2026-10-13T18:45:21.4411513Z ##[section]Finishing: Adicionando Multiplas Secrets


EM DES PASSA
