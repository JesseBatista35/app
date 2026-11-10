WO0000082248436 
 
Identificado erro no SIPEN durante a montagem do menu da aplicação:
 
javax.servlet.jsp.JspException: Erro na montagem do Menu
 
 
A análise dos logs mostrou a mensagem:
 
Houve um erro na conexão para obtenção dos dados de login.

SISTEMA NÃO DISPONÍVEL
 
 
Foi realizada a reciclagem da instância (sipen_node3_lx0006). Após a subida, a aplicação iniciou normalmente, recompilou as JSPs e deixaram de ocorrer os erros de montagem do menu. Indício de indisponibilidade temporária do componente responsável pela obtenção dos dados de login/perfil do usuário.
 
Errata
 
Voltou a acontecer 
 
Identificada a origem da falha do SIPEN. O erro apresentado ("Erro na montagem do Menu") é apenas reflexo de uma falha anterior na obtenção dos dados de login/perfil do usuário.
 
A análise do código mostrou que a montagem do menu depende da chamada:
 
br.com.politec.mainframe.dao.LoginMainframeImpl.consultaDadosLogin()
 
que realiza integração com Mainframe/CICS através de Connection.execute().
 
Quando ocorre falha nesta consulta, uma LoginException é gerada e posteriormente mascarada pela aplicação, resultando apenas em:
 
Erro na montagem do Menu.

null
 
Indícios apontam para instabilidade ou indisponibilidade na integração de autenticação/perfil com o Mainframe, não sendo identificado problema de deploy ou infraestrutura JBoss durante a análise.


 Solicitamos verificar motivo da indisponibilidade do ambiente de desenvolvimento SIPEN.

https://sipen2.desenvolvimento.extracaixa/sipen/

Erro na montagem do Menu.
null






<img width="1871" height="998" alt="image" src="https://github.com/user-attachments/assets/add88f4b-0af5-4578-9420-07bb677c6d1d" />


