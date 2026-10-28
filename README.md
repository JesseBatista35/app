Release SICCP-intra (EC DES) – travamento no step “Deploy Config no JBOSS” – host caddeapllx2651

Problema relatado:
A release do SICCP-intra em DES ficava travada no step “Deploy Config no JBOSS” até ser cancelada por timeout, sem mensagem de erro.

Causa identificada:
O travamento não estava no JBoss, no NFS nem no agente da esteira. Nesse step, a esteira coleta os serviços do servidor (task “Gerando fatos de servicos”, módulo service_facts do Ansible), o que executa internamente o service --status-all e chama todos os scripts de /etc/init.d/ com o argumento status.

O script /etc/init.d/sigdb, instalado pelo step “Instalar SIGDB” a partir do repositório SICCP-intra-config, não tratava argumentos: qualquer chamada executava nohup ./run &, iniciando uma nova instância do AgtSigdb em background sem redirecionar a saída. O agente herdava a saída da task do Ansible, e a esteira ficava aguardando indefinidamente. Além disso, o run não tinha shebang, o que impedia o controle do agente via systemd.

Evidências:

Task da esteira presa no service --status-all, aguardando um processo AgtSigdb iniciado por ela mesma.
9 instâncias do AgtSigdb com o mesmo alias (tr7261lx651) acumuladas no servidor, uma para cada execução de release desde 19/10.

Ações realizadas:

No servidor (caddeapllx2651):

Liberação da execução travada e remoção das instâncias duplicadas do agente.
Criação da unit systemd /etc/systemd/system/sigdb.service, habilitada no boot.

No repositório SICCP-intra-config (master):

sigdb/des/run: inclusão do shebang, proteção contra instâncias duplicadas e execução do agente em foreground (exec), com saída redirecionada para /sigdb/AgtSigdb.out.
sigdb/sigdb (origem do /etc/init.d/sigdb): reescrito com tratamento de start/stop/status/restart. O status passa a apenas consultar se o agente está em execução.

Validação:

Nova release executada: “Deploy Config no JBOSS” concluído em 56 s (antes ficava travado até o timeout).
service --status-all retorna em menos de 1 s, informando “sigdb em execucao”, sem iniciar nova instância.
Após o step “Instalar SIGDB”, o agente SIGDB permanece em execução com instância única, gerenciado pelo systemd.
