Solicita-se análise do ambiente de aplicação do SIMCN em DES, pois o pacote gerado para o JBoss está sendo implantado, porém as alterações não estão sendo refletidas na aplicação, sendo necessário remover manualmente o arquivo .ear e limpar o cache do JBoss para validação das novas versões.


Estamos tendo problema na compilação do pacote para o jboss, é gerado o pacote, é implementado no jboss , aparentemente ele não é trocado , é necessário fazer a remoção do pacote .ear e limpa o chache do jboss para fazer os teste novamente


uma amigo aqui da esteira analsita viu pra mim disse que ta assim

 
Aplicação: SIMCN
Artefato implantado: simcn-2.26.3.4.0-b2260.ear
Versão: 2.26.3.4.0
Build: b2260
 
Esse é o pacote que atualmente está no simcn 


 
Skip to content
titletitle Administrator | sair
pesquisar
 
2
Correct
Dependency errors:

Some plugins could not be loaded due to unsatisfied dependencies. Fix these issues and restart Jenkins to restore the functionality provided by these plugins.

Folders Plugin version 6.6
Você deve atualizar o Jenkins de v2.121.1 para v2.130 ou superior para executar este plugin.
Downstream dependency errors:

These plugins failed to load because of one or more of the errors above. Fix those and these plugins will load again.

Delivery Pipeline Plugin version 1.3.2
Pipeline: Multibranch v2.20 falhou ao carregar. Corrija o problema com este plugin primeiro.
Pipeline: Declarative version 1.3.2
Pipeline: Shared Groovy Libraries v2.12 falhou ao carregar. Corrija o problema com este plugin primeiro.
Pipeline: Shared Groovy Libraries version 2.12
Folders Plugin v6.6 falhou ao carregar. Corrija o problema com este plugin primeiro.
Branch API Plugin version 2.0.20
Folders Plugin v6.6 falhou ao carregar. Corrija o problema com este plugin primeiro.
Pipeline: Multibranch version 2.20
Branch API Plugin v2.0.20 falhou ao carregar. Corrija o problema com este plugin primeiro.
There are resources Jenkins was not able to dispose automatically. 
Manage
Manage Jenkins

HABILITAR ATUALIZAÇÃO AUTOMÁTICA
Jenkins
SIMCN
simcn: EAR Module
#2262
 Voltar ao projeto
 Estado pessoal
 Alterações
 Saída do console
 Editar informações de compilação
 Excluir este build
 Mojos Executados
 Ver fingerprints
 Reimplantar artefatos
 Build anterior
Iniciado 17 horas atrás
Demorou 1,9 segundos
Sucesso Build #2262 (13/10/2026 16:04:14)
Adicionar descrição
	No changes. Mudanças na dependência
simcn: RESTful Module Sucesso#2261 → Sucesso#2262 (detalhe)
simcn: EJB Module Sucesso#2261 → Sucesso#2262 (detalhe)
SIMCN - Web Module Sucesso#2261 → Sucesso#2262 (detalhe)
Página gerada: 14/10/2026 10h2min18s BRTREST APIJenkins ver. 2.121.1
