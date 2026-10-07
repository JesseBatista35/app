Pessoal, para quem pegar demanda com falha no passo "Configurando Stack de Monitoração" (esteira-jboss-vm) e este erro:

password authentication failed for user "monitdbadm"

O problema é geral: afeta todas as releases de VM, em DES e TQS, desde 05/10. Não é do sistema nem da release. A senha da conta de serviço monitdbadm no banco de monitoração (PostgreSQL Azure 10.244.74.86) foi alterada ou expirou.

A análise completa já foi encaminhada à CEPRO20 na WO0000081840070.

Para novas demandas com esse erro, basta referenciar a WO0000081840070 e informar ao solicitante que a regularização depende da atualização dessa credencial. Não precisa refazer a análise nem abrir nova demanda para o DBA.

Já confirmados: SIRTA, SIPQV e SIGPD-backend.
