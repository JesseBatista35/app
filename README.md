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













[p585600@cbrdeapllx472 ~]$ sudo ls -l /opt/jboss/jboss-eap/modules/security/

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for p585600:
total 32
-rwxr-xr-x 1 jboss jboss  502 Oct 19 15:17 caixa_vault.keystore
-rw-r--r-- 1 jboss jboss 3453 Oct 19 15:17 saidavault15092026.txt
-rwxr-xr-x 1 jboss jboss 1273 Oct 19 15:17 script.sh
-rwxr-xr-x 1 jboss jboss 2771 Oct 19 15:17 vaultcaixa.keystore
-rwxr-xr-x 1 jboss jboss 2285 Oct 19 15:17 vaultcaixa.keystore.old
-rwxr-xr-x 1 jboss jboss  504 Oct 19 15:17 vaultcaixa_sirur.keystore
-rwxr-xr-x 1 jboss jboss 1751 Oct 19 15:17 VAULT.dat
-rwxr-xr-x 1 jboss jboss  504 Oct 19 15:17 vault.keystore
[p585600@cbrdeapllx472 ~]$
[p585600@cbrdeapllx472 ~]$
[p585600@cbrdeapllx472 ~]$
[p585600@cbrdeapllx472 ~]$





[domain@localhost:9999 /] /host=hc_cbrdeapllx473:reload
{
    "outcome" => "success",
    "result" => undefined
}

[domain@localhost:9999 /] /host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:read-attribute(name=server-state)
{
    "outcome" => "success",
    "result" => "STOPPED"
}

[domain@localhost:9999 /] /host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:read-attribute(name=server-state)
Failed to get the list of the operation properties: "WFLYCTL0379: O boot do sistema está em andamento; a execução das operações de gerenciamento remoto não está disponível no momento"

[domain@localhost:9999 /] /host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:read-attribute(name=server-state)
Failed to get the list of the operation properties: "WFLYCTL0379: O boot do sistema está em andamento; a execução das operações de gerenciamento remoto não está disponível no momento"

[domain@localhost:9999 /] /host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:read-attribute(name=server-state)
Failed to get the list of the operation properties: "WFLYCTL0379: O boot do sistema está em andamento; a execução das operações de gerenciamento remoto não está disponível no momento"

[domain@localhost:9999 /] /host=hc_cbrdeapllx473:reload
{
    "outcome" => "success",
    "result" => undefined
}

[domain@localhost:9999 /] /host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:read-attribute(name=server-state)
{
    "outcome" => "success",
    "result" => "STOPPED"
}

[domain@localhost:9999 /] /host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:read-attribute(name=server-state)
{
    "outcome" => "success",
    "result" => "STOPPED"
}

[domain@localhost:9999 /] /host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:read-attribute(name=server-state)
Failed to get the list of the operation properties: "WFLYCTL0379: O boot do sistema está em andamento; a execução das operações de gerenciamento remoto não está disponível no momento"

[domain@localhost:9999 /]



[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$
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
[p585600@cbrdeapllx473 ~]$




[p585600@cbrdeapllx472 ~]$ sudo ls -l /opt/jboss/jboss-eap/modules/security/

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for p585600:
total 32
-rwxr-xr-x 1 jboss jboss  502 Oct 19 15:17 caixa_vault.keystore
-rw-r--r-- 1 jboss jboss 3453 Oct 19 15:17 saidavault15092026.txt
-rwxr-xr-x 1 jboss jboss 1273 Oct 19 15:17 script.sh
-rwxr-xr-x 1 jboss jboss 2771 Oct 19 15:17 vaultcaixa.keystore
-rwxr-xr-x 1 jboss jboss 2285 Oct 19 15:17 vaultcaixa.keystore.old
-rwxr-xr-x 1 jboss jboss  504 Oct 19 15:17 vaultcaixa_sirur.keystore
-rwxr-xr-x 1 jboss jboss 1751 Oct 19 15:17 VAULT.dat
-rwxr-xr-x 1 jboss jboss  504 Oct 19 15:17 vault.keystore
[p585600@cbrdeapllx472 ~]$
[p585600@cbrdeapllx472 ~]$
[p585600@cbrdeapllx472 ~]$
[p585600@cbrdeapllx472 ~]$ sudo cp /opt/jboss/jboss-eap/modules/security/vaultcaixa_sirur.keystore /opt/jboss/jboss-eap/modules/security/VAULT.dat /tmp/ && sudo chmod 644 /tmp/vaultcaixa_sirur.keystore /tmp/VAULT.dat
[p585600@cbrdeapllx472 ~]$
[p585600@cbrdeapllx472 ~]$
[p585600@cbrdeapllx472 ~]$
[p585600@cbrdeapllx472 ~]$
[p585600@cbrdeapllx472 ~]$ scp /tmp/vaultcaixa_sirur.keystore /tmp/VAULT.dat p585600@10.116.97.79:/tmp/
The authenticity of host '10.116.97.79 (10.116.97.79)' can't be established.
ED25519 key fingerprint is SHA256:4KTbGun90zU6LwmTUGfb5C01N+fU8TW+klOMtKiAZBk.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '10.116.97.79' (ED25519) to the list of known hosts.
***********************************************************************
(1) - Este e um computador privado de propriedade da Caixa Economica
Federal. Usuarios autorizados e nao autorizados nao possuem direitos de
divulgar as informacoes contidas aqui.
(2) - Ao fazer uso do sistema, o usuario esta ciente que pode estar
sendo monitorado, interceptado e auditado pelo departamento competente
da Caixa Economica Federal.
(3) - O uso nao autorizado ou improprio deste sistema pode resultar em
um processo disciplinar administrativo e/ou punicao atraves de acoes
civis ou criminais. Ao continuar o uso deste sistema, indica que voce
esta ciente e concordando com os termos e condicoes acima descritos.

Pressione <Control+D> IMEDIATAMENTE se voce nao concorda com as
condicoes deste aviso
***********************************************************************
p585600@10.116.97.79's password:
vaultcaixa_sirur.keystore                                                                                                                                            100%  504     1.3MB/s   00:00
VAULT.dat                                                                                                                                                            100% 1751     6.1MB/s   00:00
[p585600@cbrdeapllx472 ~]$
[p585600@cbrdeapllx472 ~]$
[p585600@cbrdeapllx472 ~]$
[p585600@cbrdeapllx472 ~]$
[p585600@cbrdeapllx472 ~]$
[p585600@cbrdeapllx472 ~]$

