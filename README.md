
-sh-4.1$
-sh-4.1$ cat /tmp/props_sirur.cli
/server-group=sifec-intranet/system-property=SIRUR_AMBIENTE:add(value="D")
/server-group=sifec-intranet/system-property=SIRUR_SITAE_USUARIO:add(value="SRURTAED")
/server-group=sifec-intranet/system-property=SIRUR_SITAE_PASSWORD:add(value="${VAULT::SIRUR::password::1}")
/server-group=sifec-intranet/system-property=SIRUR_API_MANAGER_API_KEY:add(value="${VAULT::FEC-SIRUR::SirurAPIKey::1}")
/server-group=sifec-intranet/system-property=SIRUR_SSO_INTRANET_SERVICE_RESOURCE_NAME:add(value="${VAULT::FEC-SIRUR::SirurSSOIntraResource::1}")
/server-group=sifec-intranet/system-property=SIRUR_SSO_INTRANET_SERVICE_SECRET :add(value="${VAULT::FEC-SIRUR::SirurSSOIntraSecret::1}")
-sh-4.1$


