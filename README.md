<img width="1850" height="891" alt="image" src="https://github.com/user-attachments/assets/9494889d-2729-4c1f-b81b-a4c1b22c9f56" />


2026-10-14 13:02:50,672 INFO Getting secrets just once, POLLING_WAIT_BETWEEN_REQUESTS_MINUTES was not configured
2026-10-14 13:02:50,672 INFO (8f9c0bf2-c7cf-11f1-b449-0a5819021d44) APP VERSION: 2.1.0
2026-10-14 13:02:50,672 INFO (8f9c0bf2-c7cf-11f1-b449-0a5819021d44) Starting Execution...8f9c0bf2-c7cf-11f1-b449-0a5819021d44
2026-10-14 13:02:50,672 INFO (8f9c0bf2-c7cf-11f1-b449-0a5819021d44) You are using: <,> as List delimiter
2026-10-14 13:02:50,672 WARNING (8f9c0bf2-c7cf-11f1-b449-0a5819021d44) InsecureRequestWarning: Unverified HTTPS request is being made to host https://sicsn.caixa/BeyondTrust/api/public/v3'. Adding certificate verification isstrongly advised. See: https://urllib3.readthedocs.io/en/1.26.x/advanced-usage.html#ssl-warnings
2026-10-14 13:02:50,672 INFO (8f9c0bf2-c7cf-11f1-b449-0a5819021d44) Certificate was not configured
2026-10-14 13:02:50,675 DEBUG (8f9c0bf2-c7cf-11f1-b449-0a5819021d44) How long to wait for the server to connect and send data before giving up: connection timeout: 30 seconds, request timeout 30 seconds
2026-10-14 13:02:50,675 WARNING (8f9c0bf2-c7cf-11f1-b449-0a5819021d44) verify_ca=false is insecure, it instructs the caller to not verify the certificate authority when making API calls.
2026-10-14 13:02:50,735 INFO (8f9c0bf2-c7cf-11f1-b449-0a5819021d44) Calling sign_app_in endpoint: https://sicsn.caixa/BeyondTrust/api/public/v3
2026-10-14 13:02:50,776 DEBUG (8f9c0bf2-c7cf-11f1-b449-0a5819021d44) Running get_secret method in SecretsSafe class
2026-10-14 13:02:50,776 INFO (8f9c0bf2-c7cf-11f1-b449-0a5819021d44) **************** secret path: SIIFX_DES/apikey_siifx_intranet *****************
2026-10-14 13:02:50,781 DEBUG (8f9c0bf2-c7cf-11f1-b449-0a5819021d44) Calling get_secret_by_path endpoint: /secrets-safe/secrets?path=SIIFX_DES&separator=%2F&version=3.1&title=apikey_siifx_intranet
2026-10-14 13:02:50,781 DEBUG (8f9c0bf2-c7cf-11f1-b449-0a5819021d44) GET request to URL: https://sicsn.caixa/BeyondTrust/api/public/v3/secrets-safe/secrets?path=SIIFX_DES&separator=%2F&version=3.1&title=apikey_siifx_intranet
2026-10-14 13:04:52,149 ERROR (8f9c0bf2-c7cf-11f1-b449-0a5819021d44) General error with secrets_safe.SecretsSafe: HTTPSConnectionPool(host='sicsn.caixa', port=443): Max retries exceeded with url: /BeyondTrust/api/public/v3/secrets-safe/secrets?path=SIIFX_DES&separator=%2F&version=3.1&title=apikey_siifx_intranet (Caused by ReadTimeoutError("HTTPSConnectionPool(host='sicsn.caixa', port=443): Read timed out. (read timeout=30)"))
2026-10-14 13:04:52,149 INFO (8f9c0bf2-c7cf-11f1-b449-0a5819021d44) Secrets folder Path /usr/src/app/secrets_files
2026-10-14 13:04:52,149 INFO (8f9c0bf2-c7cf-11f1-b449-0a5819021d44) Creating files with the secrets as content, number of files 0
2026-10-14 13:04:52,149 DEBUG (8f9c0bf2-c7cf-11f1-b449-0a5819021d44) Calling sign_app_out endpoint: https://sicsn.caixa/BeyondTrust/api/public/v3/Auth/Signout
2026-10-14 13:04:52,187 INFO (8f9c0bf2-c7cf-11f1-b449-0a5819021d44) {
    "execution_id": "8f9c0bf2-c7cf-11f1-b449-0a5819021d44",
    "input": {
        "secret_list": [
            "SIIFX_DES/apikey_siifx_intranet",
            "SIIFX_DES/sifxds01_oracle",
            "SIIFX_DES/cli-ser-ifx_sso_intra",
            "SIIFX_DES/siifx_api",
            "SIIFX_DES/SIFXDS04_DATAGRID"
        ],
        "folder_list": [],
        "managed_account_list": [],
        "secret_safe_url": "https://sicsn.caixa/BeyondTrust/api/public/v3",
        "user": {
            "UserId": 1706,
            "SID": null,
            "EmailAddress": null,
            "UserName": "SIFXDS05",
            "Name": "SIFXDS05"
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
        "errors": []
    }
}
2026-10-14 13:04:52,187 INFO (8f9c0bf2-c7cf-11f1-b449-0a5819021d44) Ending Execution...8f9c0bf2-c7cf-11f1-b449-0a5819021d44
