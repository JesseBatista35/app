
-sh-4.2$
-sh-4.2$ IMG=$(oc get dc siifx-api-aplicacao-des -o jsonpath='{.spec.template.spec.initContainers[?(@.name=="secrets-agent-sidecar")].image}')
-sh-4.2$ oc run bt-test --rm -it --restart=Never --image="$IMG" --command -- sh
If you don't see a command prompt, try pressing enter.
/usr/src/app # python3 - <<'EOF'
> import time, requests, urllib3
> urllib3.disable_warnings()
> for url in ["https://sicsn.caixa/BeyondTrust/api/public/v3/Auth/SignAppIn",
>             "https://sicsn.caixa/BeyondTrust/",
>             "https://sicsn.caixa/"]:
>     t0 = time.time()
>     try:
>         r = requests.get(url, verify=False, timeout=(10, 60), allow_redirects=True)
>         print(f"{url}: HTTP {r.status_code}, {len(r.content)} bytes em {time.time()-t0:.1f}s")
>     except Exception as e:
>         print(f"{url}: ERRO {type(e).__name__} em {time.time()-t0:.1f}s")
> EOF
https://sicsn.caixa/BeyondTrust/api/public/v3/Auth/SignAppIn: HTTP 405, 72 bytes em 0.1s
https://sicsn.caixa/BeyondTrust/: HTTP 200, 6970 bytes em 0.1s
https://sicsn.caixa/: HTTP 200, 2486 bytes em 4.7s
/usr/src/app #
/usr/src/app #
/usr/src/app # python3 - <<'EOF'
> import time, requests, urllib3
> urllib3.disable_warnings()
> for url in ["https://sicsn.caixa/BeyondTrust/api/public/v3/Auth/SignAppIn",
>             "https://sicsn.caixa/BeyondTrust/",
>             "https://sicsn.caixa/"]:
>     t0 = time.time()
>     try:
>         r = requests.get(url, verify=False, timeout=(10, 60), allow_redirects=True)
>         print("%s: HTTP %s, %d bytes em %.1fs" % (url, r.status_code, len(r.content), time.time()-t0))
>     except Exception as e:
>         print("%s: ERRO %s em %.1fs" % (url, type(e).__name__, time.time()-t0))
> EOF
https://sicsn.caixa/BeyondTrust/api/public/v3/Auth/SignAppIn: HTTP 405, 72 bytes em 0.0s
https://sicsn.caixa/BeyondTrust/: HTTP 200, 6970 bytes em 0.0s
https://sicsn.caixa/: HTTP 200, 2486 bytes em 0.0s
/usr/src/app #
/usr/src/app #
/usr/src/app #
/usr/src/app #
/usr/src/app #
/usr/src/app # exit
pod "bt-test" deleted
-sh-4.2$ IMG=$(oc get dc siifx-api-aplicacao-des -o jsonpath='{.spec.template.spec.initContainers[?(@.name=="secrets-agent-sidecar")].image}')
-sh-4.2$ oc run bt-test --rm -it --restart=Never --image="$IMG" --command -- sh
If you don't see a command prompt, try pressing enter.
/usr/src/app #
/usr/src/app #
/usr/src/app #
/usr/src/app #
/usr/src/app # for u in https://sicsn.caixa/BeyondTrust/api/public/v3/Auth/SignAppIn https://sicsn.caixa/BeyondTrust/ https://sicsn.caixa/; do
>   curl -skL -m 60 -o /dev/null -w "$u: HTTP %{http_code}, %{size_download} bytes em %{time_total}s\n" "$u"
> done
sh: curl: not found
sh: curl: not found
sh: curl: not found
/usr/src/app #
/usr/src/app #
/usr/src/app #
/usr/src/app # exit
pod "bt-test" deleted
pod siifx-des/bt-test terminated (Error)
-sh-4.2$
-sh-4.2$
-sh-4.2$ for u in https://sicsn.caixa/BeyondTrust/api/public/v3/Auth/SignAppIn https://sicsn.caixa/BeyondTrust/ https://sicsn.caixa/; do
>   curl -skL -m 60 -o /dev/null -w "$u: HTTP %{http_code}, %{size_download} bytes em %{time_total}s\n" "$u"
> done
https://sicsn.caixa/BeyondTrust/api/public/v3/Auth/SignAppIn: HTTP 405, 72 bytes em 0,181s
https://sicsn.caixa/BeyondTrust/: HTTP 200, 6970 bytes em 0,129s
https://sicsn.caixa/: HTTP 200, 2486 bytes em 0,114s
-sh-4.2$
-sh-4.2$
