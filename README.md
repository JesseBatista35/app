[section]******************************************************************************
[section]Starting: Deploy Config no JBOSS
[section]******************************************************************************
==============================================================================
Task         : Bash
Description  : Run a Bash script on macOS, Linux, or Windows
Version      : 3.227.0
Author       : Microsoft Corporation
Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
==============================================================================
Generating script.
========================== Starting Command Output ===========================
[command]/bin/bash /opt/ads-agent/_work/_temp/cf187bec-d87c-43a1-9f6a-5eea7697d9c8.sh
/opt/ads-agent/_work/_temp/cf187bec-d87c-43a1-9f6a-5eea7697d9c8.sh: line 2: quantidade_vm: comando não encontrado
/opt/ads-agent/_work/_temp/cf187bec-d87c-43a1-9f6a-5eea7697d9c8.sh: line 2: USE_WMQ: comando não encontrado

PLAY [local] *******************************************************************

PLAY [Configurando o DNS] ******************************************************

PLAY [local] *******************************************************************

PLAY [Verificando serviços] ****************************************************

PLAY [Configuração LDAP] *******************************************************
[WARNING]: Found variable using reserved name: when

PLAY [jboss] *******************************************************************

PLAY [Stack Jboss] *************************************************************
Wednesday 28 October 2026  12:23:45 -0300 (0:00:00.362)       0:00:00.362 ***** 

TASK [Verifica ser o Jboss já foi instalado] ***********************************
[DEPRECATION WARNING]: Distribution rhel 9.3 on host 
caddeapllx2651.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, 
but is using /usr/bin/python for backward compatibility with prior Ansible 
releases. A future Ansible release will default to using the discovered 
platform python for this host. See https://docs.ansible.com/ansible/2.9/referen
ce_appendices/interpreter_discovery.html for more information. This feature 
will be removed in version 2.12. Deprecation warnings can be disabled by 
setting deprecation_warnings=False in ansible.cfg.
ok: [caddeapllx2651.agil.nprd.caixa.gov.br]

PLAY [jboss] *******************************************************************
Wednesday 28 October 2026  12:23:46 -0300 (0:00:00.539)       0:00:00.901 ***** 

TASK [Verifica se o arquivo nfs_config.json existe] ****************************
ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
Wednesday 28 October 2026  12:23:46 -0300 (0:00:00.467)       0:00:01.369 ***** 
included: /opt/ads-agent/_work/r19131/a/esteira-jboss-vm-v2/roles/nfs/tasks/get_nfs.yml for caddeapllx2651.agil.nprd.caixa.gov.br
Wednesday 28 October 2026  12:23:46 -0300 (0:00:00.053)       0:00:01.422 ***** 

TASK [nfs : Criar variáveis] ***************************************************
ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
Wednesday 28 October 2026  12:23:47 -0300 (0:00:00.064)       0:00:01.487 ***** 

TASK [nfs : Coletar variáveis de ambiente] *************************************
ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
Wednesday 28 October 2026  12:23:47 -0300 (0:00:00.536)       0:00:02.024 ***** 

TASK [nfs : Exibir resultado em JSON] ******************************************
ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
    "nfs_vars_json": {
        "changed": false, 
        "cmd": "cat /opt/ads-agent/_work/r19131/a/nfs_config.json", 
        "delta": "0:00:00.044513", 
        "end": "2026-10-28 12:23:47.563614", 
        "failed": false, 
        "rc": 0, 
        "start": "2026-10-28 12:23:47.519101", 
        "stderr": "", 
        "stderr_lines": [], 
        "stdout": "[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT_VM\": \"/siccp\"}]", 
        "stdout_lines": [
            "[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT_VM\": \"/siccp\"}]"
        ]
    }
}
Wednesday 28 October 2026  12:23:47 -0300 (0:00:00.074)       0:00:02.099 ***** 

TASK [nfs : Criar variáveis] ***************************************************
ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
Wednesday 28 October 2026  12:23:47 -0300 (0:00:00.066)       0:00:02.165 ***** 

TASK [nfs : execute montagem script] *******************************************
changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
Wednesday 28 October 2026  12:23:48 -0300 (0:00:00.727)       0:00:02.893 ***** 

TASK [nfs : ansible.builtin.debug] *********************************************
ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
    "changed": false, 
    "msg": {
        "changed": true, 
        "cmd": [
            "python", 
            "/opt/ads-agent/_work/r19131/a/esteira-jboss-vm-v2/roles/nfs/files/nfs.py", 
            "montagem", 
            "siccp-intra", 
            "des", 
            "ctc_nprd", 
            "/opt/ads-agent/_work/r19131/a/esteira-jboss-vm-v2", 
            "C&t@d02", 
            "***", 
            "s736651@corp.caixa.gov.br", 
            "***", 
            "[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT_VM\": \"/siccp\"}]"
        ], 
        "delta": "0:00:00.356145", 
        "end": "2026-10-28 12:23:48.427555", 
        "failed": false, 
        "rc": 0, 
        "start": "2026-10-28 12:23:48.071410", 
        "stderr": "", 
        "stderr_lines": [], 
        "stdout": "[{u'NFS_MOUNT_POINT_VM': u'/siccp', u'NFS_ENDPOINT_VM': u'hypernprd12.ad.caixa:/fs_siccp'}]\nNome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           \n------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------\nhypernprd12.ad.caixa                /fs_siccp                           /siccp                              VM                                  hypernprd12.ad.caixa                des                                \nnfs_path=/siccp\nnfs_src=hypernprd12.ad.caixa:/fs_siccp\nhypernprd12.ad.caixa                /fs_siccp                           /siccp                              VM                                  hypernprd12.ad.caixa                des                          ...
        "stdout_lines": [
            "[{u'NFS_MOUNT_POINT_VM': u'/siccp', u'NFS_ENDPOINT_VM': u'hypernprd12.ad.caixa:/fs_siccp'}]", 
            "Nome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           ", 
            "------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------", 
            "hypernprd12.ad.caixa                /fs_siccp                           /siccp                              VM                                  hypernprd12.ad.caixa                des                                ", 
            "nfs_path=/siccp", 
            "nfs_src=hypernprd12.ad.caixa:/fs_siccp", 
            "hypernprd12.ad.caixa                /fs_siccp                           /siccp                              VM                                  hypernprd12.ad.caixa                des                                "
        ]
    }
}
Wednesday 28 October 2026  12:23:48 -0300 (0:00:00.068)       0:00:02.961 ***** 

TASK [nfs : execute clean json] ************************************************
changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
Wednesday 28 October 2026  12:23:48 -0300 (0:00:00.268)       0:00:03.229 ***** 

TASK [nfs : result_new_string_json] ********************************************
ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
    "msg": {
        "changed": true, 
        "cmd": "echo '[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT_VM\": \"/siccp\"}]' | sed 's/NFS_ENDPOINT_ISILON[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_ISILON[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_HUAWEI[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_HUAWEI[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_VM[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_VM[^\"]*/NFS_MOUNT_POINT/g'", 
        "delta": "0:00:00.004117", 
        "end": "2026-10-28 12:23:48.768640", 
        "failed": false, 
        "rc": 0, 
        "start": "2026-10-28 12:23:48.764523", 
        "stderr": "", 
        "stderr_lines": [], 
        "stdout": "[{\"NFS_ENDPOINT\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT\": \"/siccp\"}]", 
        "stdout_lines": [
            "[{\"NFS_ENDPOINT\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT\": \"/siccp\"}]"
        ]
    }
}
Wednesday 28 October 2026  12:23:48 -0300 (0:00:00.064)       0:00:03.294 ***** 

TASK [nfs : Parse JSON data] ***************************************************
ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
Wednesday 28 October 2026  12:23:48 -0300 (0:00:00.063)       0:00:03.358 ***** 

TASK [nfs : result_new_json] ***************************************************
ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
    "msg": [
        {
            "NFS_ENDPOINT": "hypernprd12.ad.caixa:/fs_siccp", 
            "NFS_MOUNT_POINT": "/siccp"
        }
    ]
}
Wednesday 28 October 2026  12:23:48 -0300 (0:00:00.063)       0:00:03.422 ***** 
included: /opt/ads-agent/_work/r19131/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2651.agil.nprd.caixa.gov.br
Wednesday 28 October 2026  12:23:49 -0300 (0:00:00.070)       0:00:03.492 ***** 

TASK [nfs : Parse JSON data] ***************************************************
ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
Wednesday 28 October 2026  12:23:49 -0300 (0:00:00.061)       0:00:03.554 ***** 

TASK [nfs : debug] *************************************************************
ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
    "msg": {
        "NFS_ENDPOINT": "hypernprd12.ad.caixa:/fs_siccp", 
        "NFS_MOUNT_POINT": "/siccp"
    }
}
Wednesday 28 October 2026  12:23:49 -0300 (0:00:00.061)       0:00:03.615 ***** 

TASK [nfs : debug] *************************************************************
ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
    "msg": "/siccp"
}
Wednesday 28 October 2026  12:23:49 -0300 (0:00:00.083)       0:00:03.699 ***** 

TASK [nfs : debug] *************************************************************
ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
    "msg": "hypernprd12.ad.caixa:/fs_siccp"
}
Wednesday 28 October 2026  12:23:49 -0300 (0:00:00.061)       0:00:03.760 ***** 

TASK [nfs : Verificando as variaveis] ******************************************
ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
    "changed": false, 
    "msg": "All assertions passed"
}
Wednesday 28 October 2026  12:23:49 -0300 (0:00:00.065)       0:00:03.825 ***** 

TASK [nfs : Instalando o NFS Client] *******************************************
ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
Wednesday 28 October 2026  12:23:53 -0300 (0:00:03.849)       0:00:07.674 ***** 

TASK [nfs : Install networker lgtoclnt_url] ************************************
[WARNING]: Consider using the yum, dnf or zypper module rather than running
'rpm'.  If you need to use command because yum, dnf or zypper is insufficient
you can add 'warn: false' to this command task or set 'command_warnings=False'
in ansible.cfg to get rid of this message.
fatal: [caddeapllx2651.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.617019", "end": "2026-10-28 12:23:54.087731", "msg": "non-zero return code", "rc": 1, "start": "2026-10-28 12:23:53.470712", "stderr": "aviso: /var/tmp/rpm-tmp.6ReAD8: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.6ReAD8: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying... ...
...ignoring
Wednesday 28 October 2026  12:23:54 -0300 (0:00:00.873)       0:00:08.548 ***** 

TASK [nfs : Install networker lgtonmda_url] ************************************
fatal: [caddeapllx2651.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.546044", "end": "2026-10-28 12:23:54.893067", "msg": "non-zero return code", "rc": 1, "start": "2026-10-28 12:23:54.347023", "stderr": "aviso: /var/tmp/rpm-tmp.fQpOWr: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.fQpOWr: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying... ...
...ignoring
Wednesday 28 October 2026  12:23:54 -0300 (0:00:00.806)       0:00:09.354 ***** 

TASK [nfs : Remove pacote jbcs-httpd] ******************************************
changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
Wednesday 28 October 2026  12:23:55 -0300 (0:00:00.434)       0:00:09.789 ***** 

TASK [nfs : Create a symbolic link] ********************************************
changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
Wednesday 28 October 2026  12:23:55 -0300 (0:00:00.263)       0:00:10.053 ***** 

TASK [nfs : Networker | Start networker] ***************************************
ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
Wednesday 28 October 2026  12:23:56 -0300 (0:00:00.964)       0:00:11.017 ***** 

TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
Wednesday 28 October 2026  12:23:56 -0300 (0:00:00.277)       0:00:11.295 ***** 

TASK [nfs : Networker | Restart networker] *************************************
changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
Wednesday 28 October 2026  12:24:07 -0300 (0:00:10.487)       0:00:21.783 ***** 

TASK [nfs : Montando volume remoto] ********************************************
ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
Wednesday 28 October 2026  12:24:07 -0300 (0:00:00.440)       0:00:22.223 ***** 

PLAY [jboss] *******************************************************************

PLAY [jboss] *******************************************************************
Wednesday 28 October 2026  12:24:07 -0300 (0:00:00.054)       0:00:22.278 ***** 

TASK [Gathering Facts] *********************************************************
ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
Wednesday 28 October 2026  12:24:08 -0300 (0:00:00.673)       0:00:22.951 ***** 
