Aqui estão as 6 linhas prontas, já com a última corrigida. Cole no CLI do 471:

/server-group=sifec-intranet/system-property=SIRUR_AMBIENTE:add(value="D")
/server-group=sifec-intranet/system-property=SIRUR_SITAE_USUARIO:add(value="SRURTAED")
/server-group=sifec-intranet/system-property=SIRUR_SITAE_PASSWORD:add(value="${VAULT::SIRUR::password::1}")
/server-group=sifec-intranet/system-property=SIRUR_API_MANAGER_API_KEY:add(value="${VAULT::FEC-SIRUR::SirurAPIKey::1}")
/server-group=sifec-intranet/system-property=SIRUR_SSO_INTRANET_SERVICE_RESOURCE_NAME:add(value="${VAULT::FEC-SIRUR::SirurSSOIntraResource::1}")
/server-group=sifec-intranet/system-property=SIRUR_SSO_INTRANET_SERVICE_SECRET:add(value="${VAULT::FEC-SIRUR::SirurSSOIntraSecret::1}")

Essas linhas já servem como teste do vault. Ao criar a property, o servidor em execução tenta resolver o ${VAULT::...} na hora:

Todas success, inclusive na parte "server-groups" => ... "response": o vault do 473 está resolvendo.
Erro com vault, PBOX ou cannot resolve em alguma: aquele bloco/atributo não existe no VAULT.dat copiado do 472. Me mande a mensagem.

Repare que a SIRUR_SITAE_PASSWORD usa outro bloco do vault (SIRUR, e não FEC-SIRUR). Se só ela falhar, é por isso.

Depois:

No 6.4: rm -f /tmp/props_sirur.cli
Siga o passo 1 (usuário/senha do datasource no 6.4) e o passo 4 (corrigir a connection-url do OracleSirurDS no 7.4) da mensagem anterior.
