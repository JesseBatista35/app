csc-ejb/src/main/java/br/gov/caixa/sigec/csc/persistencia/RelatoriosRepository.java
 
Veja o HQL executado quando etapaId == 0 (Todas):
 
sql
Select count(ecce)from EventoCessaoCreditoElegivel ecceinner join ecce.eventoCessao ecwhere ec.etapaBaseElegivel.baseElegivelCessao.id = :base
Use o código com cuidado.
 
Essa consulta gera 3 problemas graves de performance no banco:
 
Navegação implícita em 3 tabelas (ec.etapaBaseElegivel.baseElegivelCessao.id): O Hibernate gera um INNER JOIN implícito passando por EventoCessaoCreditoElegivel -> EventoCessao -> EtapaBaseElegivel -> BaseElegivelCessao, fazendo Full Table Scan em uma tabela enorme de créditos elegíveis por evento (EventoCessaoCreditoElegivel).
Contagem desnecessária da base inteira (count(ecce)): Olhando o uso desse método no RelatoriosRest (validarCreditosExcluidos), ele serve apenas para habilitar ou desabilitar o botão "Exportar Excluídos" na tela (verificando se existe pelo menos 1 crédito excluído, ou exibindo a contagem). Quando etapa == 0 (Todas) e a base 108 tem centenas de milhares ou milhões de créditos excluídos ao longo de todas as etapas, o banco varre todos os registros até o fim.
Sem índice ou filtro direto pela FK: Ao navegar até baseElegivelCessao.id em vez de filtrar pelo ID da EtapaBaseElegivel (que é uma tabela minúscula com poucas etapas por base), o otimizador do banco escolhe um plano de execução ruim.



 estmaos em sala e o jeferson ffezx essa analise, isso ta certo pode ser esse problemo ou realmente o  que vimos, me ajsua a explciar em sala anossa teoria
