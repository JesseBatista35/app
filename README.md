primeiro backup, o de 2023, porque ele não serve:

bash
rm /tmp/domain.xml.bkp_ccr_20261117_1516

Próximo passo: entrar no CLI, tirar o snapshot e guardar a configuração atual.

bash
/opt/jboss/jboss-eap/bin/jboss-cli.sh --connect --controller=10.116.97.59:9990

Já dentro do CLI, rode apenas estes dois:

:take-snapshot
/profile=full-ha-sifec-intranet/subsystem=keycloak/secure-deployment=ccr-api.war:read-resource(recursive=true)

Me mande a saída. Ainda não remova nada.
