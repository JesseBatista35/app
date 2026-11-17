Próximo passo: snapshot e remoção. No mesmo CLI, um comando de cada vez:

:take-snapshot
/profile=full-ha-sifec-intranet/subsystem=keycloak/secure-deployment=ccr-api.war:remove

A remoção sozinha ainda não afeta o CCR. Só vale depois do redeploy, que faremos no passo seguinte, depois de avisar na sala.

Me mande a saída dos dois.

Para referência, o rollback exato fica assim. Não rode agora:

/profile=full-ha-sifec-intranet/subsystem=keycloak/secure-deployment=ccr-api.war:add(realm=internet,resource=cli-ser-fec_api,bearer-only=true,ssl-required=external)
/server-group=sifec-intranet/deployment=SIFEC-CCR:redeploy
