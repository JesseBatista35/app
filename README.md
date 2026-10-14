
-sh-4.2$ python3 - <<'EOF'
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
Traceback (most recent call last):
  File "<stdin>", line 6, in <module>
  File "/usr/lib64/python3.6/os.py", line 669, in __getitem__
    raise KeyError(key) from None
KeyError: 'CID'
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
