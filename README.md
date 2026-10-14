sh-4.2$
-sh-4.2$
-sh-4.2$ IMG=$(oc get dc siifx-api-aplicacao-des -o jsonpath='{.spec.template.spec.initContainers[?(@.name=="secrets-agent-sidecar")].image}')
-sh-4.2$ S=bt-client-secret-siifx-api-aplicacao-des
-sh-4.2$ CID=$(oc get secret $S -o jsonpath='{.data.BT_CLIENT_ID}' | base64 -d)
-sh-4.2$ CSEC=$(oc get secret $S -o jsonpath='{.data.BT_CLIENT_SECRET}' | base64 -d)
-sh-4.2$ oc run bt-test --rm -it --restart=Never --image="$IMG" --env="CID=$CID" --env="CSEC=$CSEC" --command -- sh
If you don't see a command prompt, try pressing enter.
/usr/src/app # python3 - <<'EOF'
> import os, time, requests, urllib3
> urllib3.disable_warnings()
> BT = "https://sicsn.caixa/BeyondTrust/api/public/v3"
> s = requests.Session(); s.verify = False
> r = s.post(BT + "/Auth/connect/token", timeout=30, data={
>     "grant_type": "client_credentials",
>     "client_id": os.environ["CID"], "client_secret": os.environ["CSEC"]})
> print("token", r.status_code)
> s.headers["Authorization"] = "Bearer " + r.json()["access_token"]
> r = s.post(BT + "/Auth/SignAppIn", timeout=30)
> print("SignAppIn", r.status_code)
> for t in ["sifxds01_oracle", "cli-ser-ifx_sso_intra", "siifx_api", "SIFXDS04_DATAGRID", "apikey_siifx_intranet"]:
>     t0 = time.time()
>     try:
>         r = s.get(BT + "/Secrets-Safe/Secrets", timeout=(10, 60),
>                   params={"path": "SIIFX_DES", "separator": "/", "version": "3.1", "title": t})
>         info = f"{len(r.json())} resultado(s)" if r.ok else r.text[:120]
>         print(f"{t}: HTTP {r.status_code} em {time.time()-t0:.1f}s -> {info}")
>     except Exception as e:
>         print(f"{t}: ERRO {type(e).__name__} em {time.time()-t0:.1f}s")
> s.post(BT + "/Auth/Signout", timeout=10)
> EOF
token 200
SignAppIn 200
sifxds01_oracle: ERRO ReadTimeout em 60.1s
E^Hexit^H
exit
^CTraceback (most recent call last):
  File "<stdin>", line 15, in <module>
  File "/usr/local/lib/python3.13/site-packages/requests/sessions.py", line 602, in get
    return self.request("GET", url, **kwargs)
           ~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.13/site-packages/requests/sessions.py", line 589, in request
    resp = self.send(prep, **send_kwargs)
  File "/usr/local/lib/python3.13/site-packages/requests/sessions.py", line 703, in send
    r = adapter.send(request, **kwargs)
  File "/usr/local/lib/python3.13/site-packages/requests/adapters.py", line 667, in send
    resp = conn.urlopen(
        method=request.method,
    ...<9 lines>...
        chunked=chunked,
    )
  File "/usr/local/lib/python3.13/site-packages/urllib3/connectionpool.py", line 787, in urlopen
    response = self._make_request(
        conn,
    ...<10 lines>...
        **response_kw,
    )
  File "/usr/local/lib/python3.13/site-packages/urllib3/connectionpool.py", line 534, in _make_request
    response = conn.getresponse()
  File "/usr/local/lib/python3.13/site-packages/urllib3/connection.py", line 565, in getresponse
    httplib_response = super().getresponse()
  File "/usr/local/lib/python3.13/http/client.py", line 1430, in getresponse
    response.begin()
    ~~~~~~~~~~~~~~^^
  File "/usr/local/lib/python3.13/http/client.py", line 331, in begin
    version, status, reason = self._read_status()
                              ~~~~~~~~~~~~~~~~~^^
  File "/usr/local/lib/python3.13/http/client.py", line 292, in _read_status
    line = str(self.fp.readline(_MAXLINE + 1), "iso-8859-1")
               ~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.13/socket.py", line 719, in readinto
    return self._sock.recv_into(b)
           ~~~~~~~~~~~~~~~~~~~~^^^
  File "/usr/local/lib/python3.13/ssl.py", line 1304, in recv_into
    return self.read(nbytes, buffer)
           ~~~~~~~~~^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.13/ssl.py", line 1138, in read
    return self._sslobj.read(len, buffer)
           ~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^
KeyboardInterrupt

/usr/src/app #
/usr/src/app #
/usr/src/app # unset CID CSEC
/usr/src/app # exit
pod "bt-test" deleted
-sh-4.2$ unset CID CSEC
-sh-4.2$



