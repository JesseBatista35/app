1. Confira se o vault foi criado no 473 (CLI do 471). No seu print não aparece o comando do passo 3 (core-service=vault:add), então vale confirmar:

/host=hc_cbrdeapllx473/core-service=vault:read-resource
Mostrou vault-options com o vaultcaixa_sirur.keystore: ok.
Veio undefined: o :add não foi rodado. Rode o comando do passo 3 e faça /host=hc_cbrdeapllx473:reload de novo.

2. Veja o estado dos servidores do 473:

/host=hc_cbrdeapllx473:read-children-resources(child-type=server-config,include-runtime=true)

Procure o "status" do sifec-intranet_node1_lx473. Se continuar STOPPED depois do boot do HC, suba ele:

/host=hc_cbrdeapllx473/server-config=sifec-intranet_node1_lx473:start(blocking=true)
/host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:read-attribute(name=server-state)

O esperado é running. Faça o mesmo para qualquer outro servidor do 473 que esteja STOPPED e antes estava rodando.

3. Teste o vault (só confira o success; não cole a saída, porque ela mostra o valor real):

/host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:resolve-expression(expression="${VAULT::FEC-SIRUR::SirurAPIKey::1}")

4. Limpeza no 472 (as cópias do /tmp ainda estão lá):

sudo rm -f /tmp/vaultcaixa_sirur.keystore /tmp/VAULT.dat

Enquanto o HC sobe, rode o grep do datasource no bash do 6.4 (-sh-4.1$):

grep -A4 'OracleSirurDS"' /opt/jboss/jboss-eap/dc/configuration/domain.xml | grep -E "jndi-name|connection-url|user-name" | sort -u

O restart derrubou o SIFEC por alguns minutos. Se alguém estiver testando, vale um aviso rápido na sala:

Pessoal, o sifec-intranet está reiniciando para configurarmos o vault do SIRUR. Volta em alguns minutos, aviso quando estiver ok.




[p585600@cbrdeapllx472 ~]$ sudo rm -f /tmp/vaultcaixa_sirur.keystore /tmp/VAULT.dat

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for p585600:
[p585600@cbrdeapllx472 ~]$
[p585600@cbrdeapllx472 ~]$
[p585600@cbrdeapllx472 ~]$




-sh-4.1$
-sh-4.1$
-sh-4.1$ grep -A4 'OracleSirurDS"' /opt/jboss/jboss-eap/dc/configuration/domain.xml | grep -E "jndi-name|connection-url|user-name" | sort -u
                        <connection-url>jdbc:oracle:thin:@oracle-nprd-1000.caixa:1521/prim_D01NGSRV</connection-url>
                    <datasource jta="true" jndi-name="java:/jdbc/OracleSirurDS" pool-name="jdbc/OracleSirurDS" enabled="true" use-ccm="true">
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$





[p585600@cbrdeapllx473 ~]$ sudo mkdir -p /opt/jboss/jboss-eap/modules/security
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$ sudo cp /tmp/vaultcaixa_sirur.keystore /tmp/VAULT.dat /opt/jboss/jboss-eap/modules/security/
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$ sudo chown -R jboss:jboss /opt/jboss/jboss-eap/modules/security
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$ sudo rm -f /tmp/vaultcaixa_sirur.keystore /tmp/VAULT.dat
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$ ^C
[p585600@cbrdeapllx473 ~]$ /host=hc_cbrdeapllx473:read-children-resources(child-type=server-config,include-runtime=true)
-sh: syntax error near unexpected token `child-type=server-config,include-runtime=true'
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$






[domain@localhost:9999 /] /host=hc_cbrdeapllx473/core-service=vault:read-resource
{
    "outcome" => "success",
    "result" => {
        "code" => undefined,
        "module" => undefined,
        "vault-options" => {
            "KEYSTORE_URL" => "/opt/jboss/jboss-eap/modules/security/vaultcaixa_sirur.keystore",
            "KEYSTORE_PASSWORD" => "MASK-lHQotGsUSmQ5YQRzdtNLD361rwn0c0oJ",
            "KEYSTORE_ALIAS" => "SecurityK",
            "SALT" => "87654321",
            "ITERATION_COUNT" => "44",
            "ENC_FILE_DIR" => "/opt/jboss/jboss-eap/modules/security/"
        }
    }
}

[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /] /host=hc_cbrdeapllx473:read-children-resources(child-type=server-config,include-runtime=true)
{
    "outcome" => "success",
    "result" => {
        "sifec-intranet2_node1_llx473" => {
            "auto-start" => true,
            "cpu-affinity" => undefined,
            "group" => "sifec-intranet2",
            "name" => "sifec-intranet2_node1_llx473",
            "priority" => undefined,
            "socket-binding-default-interface" => undefined,
            "socket-binding-group" => "caixa-full-ha-sockets",
            "socket-binding-port-offset" => 2720,
            "status" => "STARTED",
            "update-auto-start-with-server-status" => false,
            "interface" => undefined,
            "jvm" => undefined,
            "path" => undefined,
            "ssl" => undefined,
            "system-property" => undefined
        },
        "sifec-intranet_node1_lx473" => {
            "auto-start" => true,
            "cpu-affinity" => undefined,
            "group" => "sifec-intranet",
            "name" => "sifec-intranet_node1_lx473",
            "priority" => undefined,
            "socket-binding-default-interface" => undefined,
            "socket-binding-group" => "caixa-full-ha-sockets",
            "socket-binding-port-offset" => 2570,
            "status" => "STARTED",
            "update-auto-start-with-server-status" => false,
            "interface" => undefined,
            "jvm" => undefined,
            "path" => undefined,
            "ssl" => undefined,
            "system-property" => undefined
        }
    }
}

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
[domain@localhost:9999 /]
