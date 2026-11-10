1. Na 471: qual versão do LCR está no 7.4
sudo /opt/jboss/jboss-eap/bin/jboss-cli.sh --connect --controller=localhost:9999

Dentro do CLI, liste tudo do server-group e a versão de cada deployment:

/server-group=sifec-intranet:read-children-resources(child-type=deployment)

Procure na saída o que tiver lcr ou silcr. O runtime-name é o arquivo/versão que está implantado.

Para ver também os pacotes enviados ao domain que ainda não foram atribuídos ao grupo:

:read-children-names(child-type=deployment)
2. Na 473: confirmar no log a versão que subiu e os erros do Weld
sudo grep -nE "WFLYSRV0027.*(lcr|LCR)|WFLYSRV0010.*(lcr|LCR)|WFLYSRV0021|WELD-001408|WELD-001409" /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | tail -20
WFLYSRV0027 mostra qual arquivo começou a implantar.
WELD-001408 (dependência não encontrada) e WELD-001409 (mais de uma candidata) são os erros do CDI que o Jeferson descreveu.
3. Na sbrdeapllx0001 (6.4): qual versão roda hoje
sudo grep -niE 'lcr' /opt/jboss/jboss-eap/dc/configuration/domain.xml | grep -iE 'deployment|runtime-name'
Atenção à versão

O Jeferson citou a silcr-1.19.0-b152.ear, mas a planilha de PRD do Paulo indica sifec_lcr_1.117.1. Os nomes e as numerações são diferentes. Pode ser que tenhamos subido um pacote que não corresponde ao que está em produção. Antes de levar os erros de CDI para o dev, confirme com os comandos acima qual versão está no 7.4 e qual roda no 6.4.

Se a versão do 7.4 não for a da planilha: o próximo passo é localizar e subir a sifec_lcr_1.117.1 e ver se o erro continua.
Se for a mesma: os erros de injeção (DadosSICLIDao, AliquotasIofDao e o Logger em UserProfile) são de código e empacotamento. Vão para o dev, como a análise do Jeferson aponta.

Me manda as saídas que eu fecho a análise e monto a mensagem para a sala.
