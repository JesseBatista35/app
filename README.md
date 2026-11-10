1. No 472 (10.116.97.78), veja os arquivos do vault:

sudo ls -l /opt/jboss/jboss-eap/modules/security/

O esperado é vaultcaixa_sirur.keystore e VAULT.dat (o arquivo com as senhas criptografadas).

2. Copie os dois para o 473, mesmo caminho, dono jboss. Pelo bastion, se o scp direto entre os dois não passar:

# no 472
sudo cp /opt/jboss/jboss-eap/modules/security/vaultcaixa_sirur.keystore /opt/jboss/jboss-eap/modules/security/VAULT.dat /tmp/ && sudo chmod 644 /tmp/vaultcaixa_sirur.keystore /tmp/VAULT.dat
scp /tmp/vaultcaixa_sirur.keystore /tmp/VAULT.dat p585600@10.116.97.79:/tmp/
# no 473
sudo mkdir -p /opt/jboss/jboss-eap/modules/security
sudo cp /tmp/vaultcaixa_sirur.keystore /tmp/VAULT.dat /opt/jboss/jboss-eap/modules/security/
sudo chown -R jboss:jboss /opt/jboss/jboss-eap/modules/security
# depois, apague as cópias do /tmp nos dois servidores
sudo rm -f /tmp/vaultcaixa_sirur.keystore /tmp/VAULT.dat

3. Configure o vault no host 473 (CLI do 471; os valores são os do 472, a senha já vem mascarada):

/host=hc_cbrdeapllx473/core-service=vault:add(vault-options=[("KEYSTORE_URL"=>"/opt/jboss/jboss-eap/modules/security/vaultcaixa_sirur.keystore"),("KEYSTORE_PASSWORD"=>"MASK-lHQotGsUSmQ5YQRzdtNLD361rwn0c0oJ"),("KEYSTORE_ALIAS"=>"SecurityK"),("SALT"=>"87654321"),("ITERATION_COUNT"=>"44"),("ENC_FILE_DIR"=>"/opt/jboss/jboss-eap/modules/security/")])

O vault é do host, então só vale depois de recarregar o host 473. Esse reload reinicia os servidores do 473 (o sifec-intranet inteiro). Avise a sala antes:

/host=hc_cbrdeapllx473:reload

Espere uns minutos e confira:

/host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:read-attribute(name=server-state)

4. Teste se o vault resolve (o resultado vai mostrar o valor real, então não cole a saída em lugar nenhum; só confira se deu success):

/host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:resolve-expression(expression="${VAULT::FEC-SIRUR::SirurAPIKey::1}")

5. Só depois disso, aplicamos as 6 properties do /tmp/props_sirur.cli do 6.4 do jeito que estão. Um detalhe: no 6.4 a property SIRUR_SSO_INTRANET_SERVICE_SECRET  tem um espaço no final do nome (veja o SECRET :add). Na hora de aplicar, eu te passo essa linha corrigida, sem o espaço.

Datasource: o grep foi digitado dentro do jboss-cli, por isso o erro The closing '"' is missing. Ele roda no bash do 6.4 (sbrdeapllx0001, prompt -sh-4.1$):

grep -A4 'OracleSirurDS"' /opt/jboss/jboss-eap/dc/configuration/domain.xml | grep -E "jndi-name|connection-url|user-name" | sort -u

E ainda falta o resultado do test-connection-in-pool do jdbc/OracleSirurDS no CLI do 471.
