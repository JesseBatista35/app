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
