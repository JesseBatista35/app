oc get dc/sinfs-tqs -n sinfs-tqs -o yaml > dc-sinfs-tqs-backup.yaml
oc set volume dc/sinfs-tqs -n sinfs-tqs --remove --name=accaixa-v4


2026-10-13 18:54:39,399 INFO Getting secrets just once, POLLING_WAIT_BETWEEN_REQUESTS_MINUTES was not configured
2026-10-13 18:54:39,399 INFO (8afa725c-c737-11f1-a4d7-0a5819030fac) APP VERSION: 2.1.0
2026-10-13 18:54:39,399 INFO (8afa725c-c737-11f1-a4d7-0a5819030fac) Starting Execution...8afa725c-c737-11f1-a4d7-0a5819030fac
2026-10-13 18:54:39,399 INFO (8afa725c-c737-11f1-a4d7-0a5819030fac) You are using: <,> as List delimiter
2026-10-13 18:54:39,399 WARNING (8afa725c-c737-11f1-a4d7-0a5819030fac) InsecureRequestWarning: Unverified HTTPS request is being made to host https://sicsn.caixa/BeyondTrust/api/public/v3'. Adding certificate verification isstrongly advised. See: https://urllib3.readthedocs.io/en/1.26.x/advanced-usage.html#ssl-warnings
2026-10-13 18:54:39,399 INFO (8afa725c-c737-11f1-a4d7-0a5819030fac) Certificate was not configured
2026-10-13 18:54:39,403 DEBUG (8afa725c-c737-11f1-a4d7-0a5819030fac) How long to wait for the server to connect and send data before giving up: connection timeout: 30 seconds, request timeout 30 seconds
2026-10-13 18:54:39,403 WARNING (8afa725c-c737-11f1-a4d7-0a5819030fac) verify_ca=false is insecure, it instructs the caller to not verify the certificate authority when making API calls.
2026-10-13 18:54:39,463 INFO (8afa725c-c737-11f1-a4d7-0a5819030fac) Calling sign_app_in endpoint: https://sicsn.caixa/BeyondTrust/api/public/v3
2026-10-13 18:54:39,504 DEBUG (8afa725c-c737-11f1-a4d7-0a5819030fac) Running get_secret method in SecretsSafe class
2026-10-13 18:54:39,505 INFO (8afa725c-c737-11f1-a4d7-0a5819030fac) **************** secret path: SINFS_TQS/JCICSDIRECT *****************
2026-10-13 18:54:39,510 DEBUG (8afa725c-c737-11f1-a4d7-0a5819030fac) Calling get_secret_by_path endpoint: /secrets-safe/secrets?path=SINFS_TQS&separator=%2F&version=3.1&title=JCICSDIRECT
2026-10-13 18:54:39,511 DEBUG (8afa725c-c737-11f1-a4d7-0a5819030fac) GET request to URL: https://sicsn.caixa/BeyondTrust/api/public/v3/secrets-safe/secrets?path=SINFS_TQS&separator=%2F&version=3.1&title=JCICSDIRECT
2026-10-13 18:54:39,587 DEBUG (8afa725c-c737-11f1-a4d7-0a5819030fac) Running get_secret method in SecretsSafe class
2026-10-13 18:54:39,587 INFO (8afa725c-c737-11f1-a4d7-0a5819030fac) **************** secret path: SINFS_TQS/SSO_SENHA *****************
2026-10-13 18:54:39,588 DEBUG (8afa725c-c737-11f1-a4d7-0a5819030fac) Calling get_secret_by_path endpoint: /secrets-safe/secrets?path=SINFS_TQS&separator=%2F&version=3.1&title=SSO_SENHA
2026-10-13 18:54:39,588 DEBUG (8afa725c-c737-11f1-a4d7-0a5819030fac) GET request to URL: https://sicsn.caixa/BeyondTrust/api/public/v3/secrets-safe/secrets?path=SINFS_TQS&separator=%2F&version=3.1&title=SSO_SENHA
2026-10-13 18:54:39,646 DEBUG (8afa725c-c737-11f1-a4d7-0a5819030fac) Running get_secret method in SecretsSafe class
2026-10-13 18:54:39,646 INFO (8afa725c-c737-11f1-a4d7-0a5819030fac) **************** secret path: SINFS_TQS/TGNFSNFDV_SENHA *****************
2026-10-13 18:54:39,647 DEBUG (8afa725c-c737-11f1-a4d7-0a5819030fac) Calling get_secret_by_path endpoint: /secrets-safe/secrets?path=SINFS_TQS&separator=%2F&version=3.1&title=TGNFSNFDV_SENHA
2026-10-13 18:54:39,647 DEBUG (8afa725c-c737-11f1-a4d7-0a5819030fac) GET request to URL: https://sicsn.caixa/BeyondTrust/api/public/v3/secrets-safe/secrets?path=SINFS_TQS&separator=%2F&version=3.1&title=TGNFSNFDV_SENHA
2026-10-13 18:54:39,715 INFO (8afa725c-c737-11f1-a4d7-0a5819030fac) Secrets folder Path /usr/src/app/secrets_files
2026-10-13 18:54:39,715 INFO (8afa725c-c737-11f1-a4d7-0a5819030fac) Creating files with the secrets as content, number of files 0
2026-10-13 18:54:39,715 DEBUG (8afa725c-c737-11f1-a4d7-0a5819030fac) Calling sign_app_out endpoint: https://sicsn.caixa/BeyondTrust/api/public/v3/Auth/Signout
2026-10-13 18:54:39,727 INFO (8afa725c-c737-11f1-a4d7-0a5819030fac) {
    "execution_id": "8afa725c-c737-11f1-a4d7-0a5819030fac",
    "input": {
        "secret_list": [
            "SINFS_TQS/JCICSDIRECT",
            "SINFS_TQS/SSO_SENHA",
            "SINFS_TQS/TGNFSNFDV_SENHA"
        ],
        "folder_list": [],
        "managed_account_list": [],
        "secret_safe_url": "https://sicsn.caixa/BeyondTrust/api/public/v3",
        "user": {
            "UserId": 1914,
            "SID": null,
            "EmailAddress": null,
            "UserName": "SNFSTR02",
            "Name": "SNFSTR02"
        }
    },
    "output": {
        "secrets": [],
        "messages": [
            {
                "message": "Creating files with the secrets as content, number of files 0",
                "type": "INFO"
            }
        ],
        "errors": [
            {
                "message": "Error while calling get_secret_with_metadata: SINFS_TQS/JCICSDIRECT, Secret was not found",
                "type": "ERROR"
            },
            {
                "message": "Error while calling get_secret_with_metadata: SINFS_TQS/SSO_SENHA, Secret was not found",
                "type": "ERROR"
            },
            {
                "message": "Error while calling get_secret_with_metadata: SINFS_TQS/TGNFSNFDV_SENHA, Secret was not found",
                "type": "ERROR"
            }
        ]
    }
}
2026-10-13 18:54:39,727 INFO (8afa725c-c737-11f1-a4d7-0a5819030fac) Ending Execution...8afa725c-c737-11f1-a4d7-0a5819030fac


<img width="1476" height="821" alt="image" src="https://github.com/user-attachments/assets/418b5fa3-5aef-475b-9396-c52ac8c31fc0" />


contua dando pau


