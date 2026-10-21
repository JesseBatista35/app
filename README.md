Prezados,

Encaminhamos para análise a falha nas pipelines do repositório caixagithub/sidpn-api-intra-credito-emprestimos, no job CI_DES / ArgoCD_Deploy, na action caixagithub/DevSecOps-Actions/.github/util/install_jq_curl@main.

Erro:
O apt-get install -y curl jq falha porque o pacote ca-certificates-java já está pendente no runner (“1 not fully installed or removed”). Ao tentar configurá-lo, o postinst não consegue salvar o keystore porque o diretório /etc/ssl/certs/java/ não existe:

org.debian.security.UnableToSaveKeystoreException: There was a problem saving the new Java keystore.
Caused by: java.io.FileNotFoundException: /etc/ssl/certs/java/cacerts (No such file or directory)
dpkg: error processing package ca-certificates-java (--configure)
E: Sub-process /usr/bin/dpkg returned an error code (1)

Evidências de que a causa está no ambiente do runner, não no repositório:

Run	Resultado	Runner
39451810492 (#7)	Sucesso	arc-runner-set-default-nprod-nqlwl-runner-kg27f
39474461093 (#8)	Falha	arc-runner-set-default-nprod
39493089284 (#9)	Falha	arc-runner-set-default-nprod-nqlwl-runner-qmnl2
As três execuções usaram exatamente os mesmos SHAs: DevSecOps-Actions (a79e586), DevSecOps-Workflow-Jobs (ade4066) e runner 2.336.0.
Com o mesmo código, a #7 passou e as seguintes falharam no mesmo ponto.
O pacote já está pendente antes da execução da action, o que indica alteração na imagem ou no ambiente do runner-set ARC default-nprod, ou em algum step anterior do job.

Solicitação:

Verificar a imagem do runner-set arc-runner-set-default-nprod e se houve atualização entre as execuções acima.
Corrigir a imagem (garantir o ca-certificates-java configurado e o diretório /etc/ssl/certs/java/ existente) ou, como paliativo, ajustar a action install_jq_curl para executar antes do install:
   sudo mkdir -p /etc/ssl/certs/java && sudo dpkg --configure -a
Avaliar o impacto em outros repositórios que usam esse runner-set com instalação via apt (inclusive a instalação do AZ CLI no pipeline de APIM).

A área demandante reporta que está sem conseguir realizar deploys, por isso solicitamos priorização.

Atenciosamente,
Jessé Batista – CTIS/CESTI
