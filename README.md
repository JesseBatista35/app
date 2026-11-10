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






[domain@localhost:9999 /] /host=hc_cbrdeapllx473/server-config=sifec-intranet_node1_lx473:start(blocking=true)
{
    "outcome" => "success",
    "result" => "STARTED",
    "response-headers" => {"warnings" => [{
        "warning" => "WFLYCTL0449: Operation start against the resource at address /host=hc_cbrdeapllx473/server-config=sifec-intranet_node1_lx473 is deprecated, and it might be removed in future ver
sion. See the the output of the read-operation-description operation to learn more about the deprecation.",
        "level" => "WARNING",
        "operation" => {
            "address" => [
                ("host" => "hc_cbrdeapllx473"),
                ("server-config" => "sifec-intranet_node1_lx473")
            ],
            "operation" => "start"
        }
    }]}
}

[domain@localhost:9999 /] /host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:read-attribute(name=server-state)
{
    "outcome" => "success",
    "result" => "running"
}

[domain@localhost:9999 /] /host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:resolve-expression(expression="${VAULT::FEC-SIRUR::SirurAPIKey::1}")
{
    "outcome" => "success",
    "result" => "${VAULT::FEC-SIRUR::SirurAPIKey::1}",
    "response-headers" => {"warnings" => [{
        "warning" => "WFLYCTL0480: A expressão 'expression \"${VAULT::FEC-SIRUR::SirurAPIKey::1}\"' não pode ser resolvida usando a resolução de fontes não sensíveis à segurança suportada pelo operat
iob 'resolve-expression'. A resposta informará o valor não resolvido.",
        "level" => "WARNING",
        "operation" => {
            "address" => [],
            "operation" => "resolve-expression"
        }
    }]}
}

[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /] /server-group=sifec-intranet/system-property=SIRUR_AMBIENTE:add(value="D")
{
    "outcome" => "success",
    "result" => undefined,
    "server-groups" => {"sifec-intranet" => {"host" => {"hc_cbrdeapllx473" => {"sifec-intranet_node1_lx473" => {"response" => {
        "outcome" => "success",
        "result" => undefined
    }}}}}}
}

[domain@localhost:9999 /] /server-group=sifec-intranet/system-property=SIRUR_SITAE_USUARIO:add(value="SRURTAED")
{
    "outcome" => "success",
    "result" => undefined,
    "server-groups" => {"sifec-intranet" => {"host" => {"hc_cbrdeapllx473" => {"sifec-intranet_node1_lx473" => {"response" => {
        "outcome" => "success",
        "result" => undefined
    }}}}}}
}

[domain@localhost:9999 /] /server-group=sifec-intranet/system-property=SIRUR_SITAE_PASSWORD:add(value="${VAULT::SIRUR::password::1}")
{
    "outcome" => "success",
    "result" => undefined,
    "server-groups" => {"sifec-intranet" => {"host" => {"hc_cbrdeapllx473" => {"sifec-intranet_node1_lx473" => {"response" => {
        "outcome" => "success",
        "result" => undefined
    }}}}}}
}

[domain@localhost:9999 /] /server-group=sifec-intranet/system-property=SIRUR_API_MANAGER_API_KEY:add(value="${VAULT::FEC-SIRUR::SirurAPIKey::1}")
{
    "outcome" => "success",
    "result" => undefined,
    "server-groups" => {"sifec-intranet" => {"host" => {"hc_cbrdeapllx473" => {"sifec-intranet_node1_lx473" => {"response" => {
        "outcome" => "success",
        "result" => undefined
    }}}}}}
}

[domain@localhost:9999 /] /server-group=sifec-intranet/system-property=SIRUR_SSO_INTRANET_SERVICE_RESOURCE_NAME:add(value="${VAULT::FEC-SIRUR::SirurSSOIntraResource::1}")
{
    "outcome" => "success",
    "result" => undefined,
    "server-groups" => {"sifec-intranet" => {"host" => {"hc_cbrdeapllx473" => {"sifec-intranet_node1_lx473" => {"response" => {
        "outcome" => "success",
        "result" => undefined
    }}}}}}
}

[domain@localhost:9999 /] /server-group=sifec-intranet/system-property=SIRUR_SSO_INTRANET_SERVICE_SECRET:add(value="${VAULT::FEC-SIRUR::SirurSSOIntraSecret::1}")
{
    "outcome" => "success",
    "result" => undefined,
    "server-groups" => {"sifec-intranet" => {"host" => {"hc_cbrdeapllx473" => {"sifec-intranet_node1_lx473" => {"response" => {
        "outcome" => "success",
        "result" => undefined
    }}}}}}
}

[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /]



sh-4.1$
-sh-4.1$
-sh-4.1$ rm -f /tmp/props_sirur.cli
-sh-4.1$
