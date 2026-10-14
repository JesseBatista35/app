IMG=$(oc get dc siifx-api-aplicacao-des -o jsonpath='{.spec.template.spec.initContainers[?(@.name=="secrets-agent-sidecar")].image}')
S=bt-client-secret-siifx-api-aplicacao-des
CID=$(oc get secret $S -o jsonpath='{.data.BT_CLIENT_ID}' | base64 -d)
CSEC=$(oc get secret $S -o jsonpath='{.data.BT_CLIENT_SECRET}' | base64 -d)
oc run bt-test --rm -it --restart=Never --image="$IMG" --env="CID=$CID" --env="CSEC=$CSEC" --command -- sh


python3 - <<'EOF'
import os, time, requests, urllib3
urllib3.disable_warnings()
BT = "https://sicsn.caixa/BeyondTrust/api/public/v3"
s = requests.Session(); s.verify = False
r = s.post(BT + "/Auth/connect/token", timeout=30, data={
    "grant_type": "client_credentials",
    "client_id": os.environ["CID"], "client_secret": os.environ["CSEC"]})
print("token", r.status_code)
s.headers["Authorization"] = "Bearer " + r.json()["access_token"]
r = s.post(BT + "/Auth/SignAppIn", timeout=30)
print("SignAppIn", r.status_code)
for t in ["sifxds01_oracle", "cli-ser-ifx_sso_intra", "siifx_api", "SIFXDS04_DATAGRID", "apikey_siifx_intranet"]:
    t0 = time.time()
    try:
        r = s.get(BT + "/Secrets-Safe/Secrets", timeout=(10, 60),
                  params={"path": "SIIFX_DES", "separator": "/", "version": "3.1", "title": t})
        info = f"{len(r.json())} resultado(s)" if r.ok else r.text[:120]
        print(f"{t}: HTTP {r.status_code} em {time.time()-t0:.1f}s -> {info}")
    except Exception as e:
        print(f"{t}: ERRO {type(e).__name__} em {time.time()-t0:.1f}s")
s.post(BT + "/Auth/Signout", timeout=10)
EOF
exit



unset CID CSEC
