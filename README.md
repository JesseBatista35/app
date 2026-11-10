A aplicação SILCR não está falhando por datasource ou JNDI. O deploy é interrompido pelo CDI/Weld durante a validação de injeções.
 
Foram identificadas dependências não resolvidas:
 
- DadosSICLIDao em DadosSICLIBean
- AliquotasIofDao em AliquotasIofBean
- Logger em UserProfile
 
Verificar se as implementações dos DAOs estão empacotadas na EAR e sendo reconhecidas como beans CDI (beans.xml, anotações @Stateless/@ApplicationScoped/@Dependent etc.).
 
Verificar também a injeção de Logger em UserProfile. O servidor encontrou apenas um producer com qualifier @BatchProperty, incompatível com a injeção @Inject Logger sem qualifier.
 
Necessário corrigir o empacotamento/configuração CDI da versão silcr-1.19.0-b152.ear.
