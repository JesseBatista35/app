-sh-4.2$
-sh-4.2$
-sh-4.2$ IMG=$(oc get dc siifx-api-aplicacao-des -o jsonpath='{.spec.template.spec.initContainers[?(@.name=="secrets-agent-sidecar")].image}')
-sh-4.2$ S=bt-client-secret-siifx-api-aplicacao-des
-sh-4.2$ CID=$(oc get secret $S -o jsonpath='{.data.BT_CLIENT_ID}' | base64 -d)
-sh-4.2$ CSEC=$(oc get secret $S -o jsonpath='{.data.BT_CLIENT_SECRET}' | base64 -d)
-sh-4.2$ oc run bt-test --rm -it --restart=Never --image="$IMG" --env="CID=$CID" --env="CSEC=$CSEC" --command -- sh
If you don't see a command prompt, try pressing enter.
/usr/src/app # python3 - <<'EOF' import os, time, requests, urllib3 urllib3.disable_warnings() BT = "https://sicsn.caixa/BeyondTrust/api/public/v3" s = requests.Session(); s.verify = False r = s.post(BT + "/Auth/connect/token",
timeout=30, data={"grant_type": "client_credentials", "client_id": os.environ["CID"], "client_secret": os.environ["CSEC"]}) s.headers["Authorization"] = "Bearer " + r.json()["access_token"] print("SignAppIn", s.post(BT + "/Auth/
SignAppIn", timeout=30).status_code) for nome, url in [("Pastas (geral)", "/Secrets-Safe/Folders"), ("Pasta SIIFX_DES sem titulo", "/Secrets-Safe/Secrets?path=SIIFX_DES&separator=/")]: t0 = time.time() try: r = s.get(BT + url, t
imeout=(10, 60)) print(f"{nome}: HTTP {r.status_code} em {time.time()-t0:.1f}s") except Exception as e: print(f"{nome}: ERRO {type(e).name} em {time.time()-t0:.1f}s") s.post(BT + "/Auth/Signout", timeout=10) EOF
sh: syntax error: unexpected "("
/usr/src/app #
/usr/src/app #
/usr/src/app # python3 - <<'EOF'
> import os, time, requests, urllib3
> urllib3.disable_warnings()
> BT = "https://sicsn.caixa/BeyondTrust/api/public/v3"
> s = requests.Session(); s.verify = False
> r = s.post(BT + "/Auth/connect/token", timeout=30, data={"grant_type": "client_credentials",
>     "client_id": os.environ["CID"], "client_secret": os.environ["CSEC"]})
> s.headers["Authorization"] = "Bearer " + r.json()["access_token"]
> print("SignAppIn", s.post(BT + "/Auth/SignAppIn", timeout=30).status_code)
> for nome, url in [("Pastas (geral)", "/Secrets-Safe/Folders"),
>                   ("Pasta SIIFX_DES sem titulo", "/Secrets-Safe/Secrets?path=SIIFX_DES&separator=/")]:
>     t0 = time.time()
>     try:
>         r = s.get(BT + url, timeout=(10, 60))
>         print(f"{nome}: HTTP {r.status_code} em {time.time()-t0:.1f}s")
>     except Exception as e:
>         print(f"{nome}: ERRO {type(e).__name__} em {time.time()-t0:.1f}s")
> s.post(BT + "/Auth/Signout", timeout=10)
> EOF
SignAppIn 200
Pastas (geral): ERRO ReadTimeout em 60.1s




O CLIET ID QUE TA LIBRAY É ESSE O MAIS RECENTE


7bee4ea6-f78e-4291-ac59-330aa1f9da82
