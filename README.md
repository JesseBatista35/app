Certo. Se é DES e vai só para a fábrica, pode mandar o domain.xml do jeito que está, sem mascarar. A decisão é sua e do Gustavo. Só não poste o arquivo na sala aberta do ADDR: mande direto para ele.

1. Copiar o domain.xml no 471 (como root)
bash
cp -p /opt/jboss/jboss-eap/dc/configuration/domain.xml /tmp/domain_sifec_74_20261117.xml
chown p585600 /tmp/domain_sifec_74_20261117.xml
chmod 644 /tmp/domain_sifec_74_20261117.xml
ls -l /tmp/domain_sifec_74_20261117.xml
2. Baixar para a sua máquina

Pelo MobaXterm: na sessão SSH do 10.116.97.59, use o painel SFTP à esquerda, vá até /tmp, clique com o botão direito em domain_sifec_74_20261117.xml e escolha Download.

Ou pelo PowerShell do Windows:

powershell
scp p585600@10.116.97.59:/tmp/domain_sifec_74_20261117.xml $env:USERPROFILE\Downloads\
3. Entregar para o Gustavo

Pelo print, o Gustavo acessa o compartilhamento \\CD0000NT050.corecaixa\ATUALIZACAO\SONDA\Murilo. O que ele não consegue é tirar arquivo dos servidores. Então o mais simples é você copiar o domain.xml para essa mesma pasta, ao lado do zip do JBoss, e avisar. Se preferir, mande o arquivo direto no chat privado dele.

Mensagem:

Gustavo, coloquei o domain.xml atual do SIFEC 7.4 (DES, do 471, com os ajustes de hoje) na pasta \\CD0000NT050.corecaixa\ATUALIZACAO\SONDA\Murilo, com o nome domain_sifec_74_20261117.xml, ao lado do jboss-eap-7.4.23.zip.

Para a fábrica:

O zip já é o EAP 7.4 com o patch 23 aplicado. É só descompactar.
O domain.xml é de domain, então para rodar em standalone eles precisam pegar do profile full-ha-sifec-intranet os subsystems e datasources que a aplicação deles usa, e as system-properties do server-group sifec-intranet.
Lembra de tirar o “ADMIN - login e senha.txt” do zip antes de repassar.

Quando terminar o passo 1, me mande a saída do ls -l.
