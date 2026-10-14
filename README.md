
-sh-4.2$ oc get pods -w | grep siifx-api-aplicacao
siifx-api-aplicacao-des-2892-deploy               0/1       Completed               0          17h
siifx-api-aplicacao-des-2893-deploy               0/1       Completed               0          14h
siifx-api-aplicacao-des-2900-deploy               1/1       Running                 0          1m
siifx-api-aplicacao-des-2900-fn7mh                0/1       Init:CrashLoopBackOff   3          1m
^C
-sh-4.2$
-sh-4.2$
-sh-4.2$ POD=$(oc get pod -l name=siifx-api-aplicacao-des --sort-by=.metadata.creationTimestamp -o name | tail -1); echo $POD
pod/siifx-api-aplicacao-des-2900-fn7mh
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc logs -f $POD -c secrets-agent-sidecar
2026-10-14 14:02:55,232 INFO Getting secrets just once, POLLING_WAIT_BETWEEN_REQUESTS_MINUTES was not configured
2026-10-14 14:02:55,232 INFO (f4184cf0-c7d7-11f1-b111-0a5819000cec) APP VERSION: 2.1.0
2026-10-14 14:02:55,232 INFO (f4184cf0-c7d7-11f1-b111-0a5819000cec) Starting Execution...f4184cf0-c7d7-11f1-b111-0a5819000cec
2026-10-14 14:02:55,232 INFO (f4184cf0-c7d7-11f1-b111-0a5819000cec) You are using: <,> as List delimiter
2026-10-14 14:02:55,232 WARNING (f4184cf0-c7d7-11f1-b111-0a5819000cec) InsecureRequestWarning: Unverified HTTPS request is being made to host https://sicsn.caixa/BeyondTrust/api/public/v3'. Adding certificate verification isstrongly advised. See: https://urllib3.readthedocs.io/en/1.26.x/advanced-usage.html#ssl-warnings
2026-10-14 14:02:55,232 INFO (f4184cf0-c7d7-11f1-b111-0a5819000cec) Certificate was not configured
2026-10-14 14:02:55,236 DEBUG (f4184cf0-c7d7-11f1-b111-0a5819000cec) How long to wait for the server to connect and send data before giving up: connection timeout: 30 seconds, request timeout 30 seconds
2026-10-14 14:02:55,236 WARNING (f4184cf0-c7d7-11f1-b111-0a5819000cec) verify_ca=false is insecure, it instructs the caller to not verify the certificate authority when making API calls.
urllib3.exceptions.ResponseError: too many 400 error responses

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/usr/local/lib/python3.13/site-packages/requests/adapters.py", line 667, in send
    resp = conn.urlopen(
        method=request.method,
    ...<9 lines>...
        chunked=chunked,
    )
  File "/usr/local/lib/python3.13/site-packages/urllib3/connectionpool.py", line 942, in urlopen
    return self.urlopen(
           ~~~~~~~~~~~~^
        method,
        ^^^^^^^
    ...<13 lines>...
        **response_kw,
        ^^^^^^^^^^^^^^
    )
    ^
  File "/usr/local/lib/python3.13/site-packages/urllib3/connectionpool.py", line 942, in urlopen
    return self.urlopen(
           ~~~~~~~~~~~~^
        method,
        ^^^^^^^
    ...<13 lines>...
        **response_kw,
        ^^^^^^^^^^^^^^
    )
    ^
  File "/usr/local/lib/python3.13/site-packages/urllib3/connectionpool.py", line 942, in urlopen
    return self.urlopen(
           ~~~~~~~~~~~~^
        method,
        ^^^^^^^
    ...<13 lines>...
        **response_kw,
        ^^^^^^^^^^^^^^
    )
    ^
  File "/usr/local/lib/python3.13/site-packages/urllib3/connectionpool.py", line 932, in urlopen
    retries = retries.increment(method, url, response=response, _pool=self)
  File "/usr/local/lib/python3.13/site-packages/urllib3/util/retry.py", line 519, in increment
    raise MaxRetryError(_pool, url, reason) from reason  # type: ignore[arg-type]
    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
urllib3.exceptions.MaxRetryError: HTTPSConnectionPool(host='sicsn.caixa', port=443): Max retries exceeded with url: /BeyondTrust/api/public/v3/Auth/connect/token (Caused by ResponseError('too many 400 error responses'))

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "/usr/src/app/get_secrets_from_secret_safe.py", line 78, in main
    get_api_access_response = authentication_obj.get_api_access()
  File "/usr/local/lib/python3.13/site-packages/secrets_safe_library/authentication.py", line 159, in get_api_access
    oauth_response = self.oauth()
  File "/usr/local/lib/python3.13/site-packages/secrets_safe_library/authentication.py", line 125, in oauth
    response = self._req.post(
        endpoint_url,
    ...<3 lines>...
        timeout=(self._timeout_connection_seconds, self._timeout_request_seconds),
    )
  File "/usr/local/lib/python3.13/site-packages/requests/sessions.py", line 637, in post
    return self.request("POST", url, data=data, json=json, **kwargs)
           ~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.13/site-packages/requests/sessions.py", line 589, in request
    resp = self.send(prep, **send_kwargs)
  File "/usr/local/lib/python3.13/site-packages/requests/sessions.py", line 703, in send
    r = adapter.send(request, **kwargs)
  File "/usr/local/lib/python3.13/site-packages/requests/adapters.py", line 691, in send
    raise RetryError(e, request=request)
requests.exceptions.RetryError: HTTPSConnectionPool(host='sicsn.caixa', port=443): Max retries exceeded with url: /BeyondTrust/api/public/v3/Auth/connect/token (Caused by ResponseError('too many 400 error responses'))
2026-10-14 14:02:56,950 ERROR (f4184cf0-c7d7-11f1-b111-0a5819000cec) There was an error in the execution: HTTPSConnectionPool(host='sicsn.caixa', port=443): Max retries exceeded with url: /BeyondTrust/api/public/v3/Auth/connect/token (Caused by ResponseError('too many 400 error responses'))
-sh-4.2$
