Prezados,

Após análise, verificamos que a demanda não pertence ao escopo de atendimento da Esteira DevOps NPRD, pois o servidor envolvido é de ambiente de PRODUÇÃO.

Evidências:
- Servidor: PR0000SR400 (VM PR0000SR400_new) – FTP do SICOW
- vCenter: cluster CTC_PRDXF2488HV7_DESCENTRALIZADO, datacenter CETEC
- IPs: 10.123.10.111 e 10.184.17.95 (GestióIP: rede REDE_BACKUP_PRO…)
- SO: Debian GNU/Linux 6 (64-bit)

Observação para apoio à análise: conforme as notas da VM, o PR0000SR400_new é um clone criado para o novo servidor pr0000sr400 (via InfraSimples). Sugerimos verificar se, na substituição do servidor, foram mantidos:
- o agendamento da shell sicow_conres_entrada.sh na CRON;
- os pontos de montagem /var/sigdb/PUB e /var/home/ftp/sicor;
- o destino de envio dos arquivos do SIGDB (se ainda aponta para o servidor antigo).

Dessa forma, encaminhamos a demanda à equipe de INFRA responsável pelo ambiente de Produção para o devido tratamento.

Atenciosamente,
Esteira DevOps NPRD
