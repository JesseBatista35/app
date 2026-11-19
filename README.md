1. Conferir que o pacote novo não tem dois módulos web no /sipen (no bash do 471)
bash
unzip -p /tmp/pen-ear-2.32.0.2.ear META-INF/application.xml | grep -iE "web-uri|context-root"

Tem que aparecer um único <context-root> com /sipen. Se aparecerem dois, o problema é do pacote, e aí paramos.

2. Fazer em duas etapas: tirar a antiga e depois subir a nova (CLI do 471)

Desse jeito o pacote antigo continua guardado para rollback. Avise na sala antes, porque o SIPEN fica fora do ar por cerca de 1 minuto.

/server-group=sipen/deployment=SIPEN:remove
deploy /tmp/pen-ear-2.32.0.2.ear --name=SIPEN-2.32.0.2 --runtime-name=pen-ear-2.32.0.2.ear --server-groups=sipen

Rollback, se a nova falhar:

/server-group=sipen/deployment=SIPEN:add(enabled=true)

Deixe o tail -f aberto no 409 e me mande a saída do passo 1 antes de seguir para o 2.
