Oi Andrei, tudo bem?

Queria te avisar de uma coisa que encontrei hoje no SICCP-intra (DES, caddeapllx2651), porque pode estar afetando outros sistemas da esteira-jboss-vm-v2.

A release travava no "Deploy Config no JBOSS" até cair por timeout. A causa foi o SIGDB: o `/etc/init.d/sigdb`, que o "Instalar SIGDB" copia de `sigdb/sigdb` no repositório de config, não tinha `case`, só `cd /sigdb; nohup ./run &`. Quando a task "Gerando fatos de servicos" (service_facts → `service --status-all`) chamava o `sigdb status`, ele subia outra instância do AgtSigdb em background, presa à saída da task, e o Ansible ficava esperando pra sempre. No servidor já havia 9 instâncias acumuladas, uma por release.

No SICCP já corrigi: o init.d agora trata start/stop/status, e o `run` tem shebang, proteção contra duplicata e `exec` com a saída redirecionada. O deploy voltou a rodar em menos de 1 minuto.

Como esse modelo de init.d parece vir do exemplo usado na inclusão do SIGDB, qualquer outro repositório de config que tenha recebido o agente desse jeito deve travar no mesmo ponto. Talvez valha revisar os sistemas que já têm o SIGDB, ou deixar o task group/role mais protegido contra isso.

Se quiser, te passo os dois arquivos que ficaram funcionando pra servirem de modelo.
