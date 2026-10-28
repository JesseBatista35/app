sudo rm /etc/init.d/sigdb
sudo systemctl daemon-reload


Release SICCP-intra (EC DES) – travamento no step “Deploy Config no JBOSS” – host caddeapllx2651

Problema relatado:
A release do SICCP-intra em DES ficava travada no step “Deploy Config no JBOSS” até ser cancelada por timeout, sem mensagem de erro.

Causa identificada:
O travamento não estava no JBoss, no NFS nem no agente da esteira. Nesse step, a esteira executa a verificação service --status-all, que chama todos os scripts de /etc/init.d/ com o argumento status. O script /etc/init.d/sigdb, instalado junto com o agente SIGDB, não trata argumentos (start/stop/status): qualquer chamada executa nohup ./run & e inicia uma nova instância do AgtSigdb em background, sem redirecionar a saída. O agente herda a saída da task do Ansible, e a esteira fica esperando o fim dessa saída indefinidamente.

Evidências:

Task da esteira presa no comando /sbin/service --status-all 2>&1 | grep ..., aguardando um processo AgtSigdb iniciado por ela mesma.
9 instâncias do AgtSigdb com o mesmo alias (tr7261lx651) acumuladas no servidor, uma para cada execução de release desde 19/10.
O /sigdb/run não tinha shebang e iniciava o agente com nohup ... &, o que impedia o controle via systemd (erro 203/EXEC).
Na própria release SICCP-intra-67, o step “Instalar SIGDB” recriou o /etc/init.d/sigdb às 14:05, depois da correção manual. Todo deploy reinstala o script problemático.

Ações realizadas no servidor (DES – caddeapllx2651):

Liberação manual da task travada. A release SICCP-intra-67 concluiu o deploy (Partially succeeded; o erro restante é do step “Configurando Stack de Monitoração”, sem relação com este problema).
Remoção do /etc/init.d/sigdb (backup em /root/sigdb.initd.bkp), repetida depois da release 67, que o havia recriado.
Ajuste do /sigdb/run: inclusão de #!/bin/bash e execução do agente em foreground (exec ./AgtSigdb ...), sem nohup e sem & (backup em /sigdb/run.bkp).
Criação da unit /etc/systemd/system/sigdb.service, habilitada no boot.
Remoção das instâncias duplicadas. O agente roda agora em instância única, gerenciado pelo systemd.

Ação necessária da equipe de desenvolvimento:
A correção foi feita apenas no servidor. Enquanto o repositório de configuração e o step “Instalar SIGDB” não forem ajustados, cada novo deploy vai:

recriar o /etc/init.d/sigdb, travando a release novamente e acumulando instâncias do agente;
sobrescrever o /sigdb/run com a versão sem shebang, fazendo o serviço systemd falhar (203/EXEC) e deixando o SIGDB sem agente.

Solicitamos:

Remover do repositório a instalação do /etc/init.d/sigdb.
Ajustar o run: incluir #!/bin/bash na primeira linha e executar o agente com exec ./AgtSigdb ... em foreground, sem nohup e sem &.
Instalar o agente como serviço systemd:
[Unit]
Description=SIGDB Agent
After=network-online.target
Wants=network-online.target

[Service]
Type=simple
WorkingDirectory=/sigdb
ExecStart=/sigdb/run
Restart=on-failure
StandardOutput=journal
StandardError=journal

[Install]
WantedBy=multi-user.target

seguido de systemctl daemon-reload e systemctl enable --now sigdb.

A configuração aplicada no caddeapllx2651 pode ser usada como referência.

Observação:
No início do step “Deploy Config no JBOSS”, as variáveis quantidade_vm e USE_WMQ aparecem como não resolvidas (“comando não encontrado”). Não têm relação com o travamento, mas recomendamos verificar se essas variáveis deveriam estar definidas na release do SICCP-intra.
