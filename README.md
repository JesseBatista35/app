Assunto: SIPEN DES – Programa PENPO308 com tempo de resposta degradado e retorno vazio (RC 0) – WO0000082248436

Prezados,

Solicitamos apoio na análise do programa COBOL PENPO308 (transação PH), chamado pelo SIPEN no ambiente de Desenvolvimento (https://sipen2.desenvolvimento.extracaixa/sipen/), que está impedindo o login dos usuários.

SINTOMA
Após informar usuário e senha, a aplicação apresenta "Erro na montagem do Menu. null". O PENPO308 é responsável por retornar os dados de login/perfil usados na montagem do menu.

ANÁLISE REALIZADA (servidor JBoss EAP 6.4 – instância sipen_node3_lx0006, host 10.116.88.25)
1. A comunicação JBoss → CICS está funcional. As chamadas retornam sem erro:
   Erro CICS: 0 | Resp: 0000 | Resp2: 0000 | Erro SQL: 0

2. Porém, de forma intermitente, o PENPO308 retorna a área de saída vazia:
   Programa Cobol: PENPO308 | Total area saida: [0]
   Em condição normal, o retorno é de 82844 bytes.

3. Existe correlação direta com o tempo de resposta do programa:
   - Retornos com dados (82844 bytes): entre 18ms e 166ms
   - Retornos vazios (0 bytes): entre 6.115ms e 9.179ms, em 100% dos casos

4. Evolução das ocorrências de retorno vazio:
   - 04/11 a 06/11: nenhuma ocorrência
   - 08/11: 1 ocorrência
   - 09/11: 14 ocorrências
   - 10/11: degradação praticamente contínua desde 06:18

5. Os mesmos usuários (ex.: F529058, C891065, C892813) alternam entre sucesso e falha, o que descarta problema de cadastro/perfil de usuário.

6. O reinício da instância JBoss não resolve: em 10/11 o servidor foi reiniciado às 09:30 e a primeira falha ocorreu às 09:32.

Exemplo de log (10/11/2026 09:32:56):
   execute() retorno: PH F529058 PENPO308 [9179ms][Erro CICS: 0][Resp: 0000][Resp2: 0000][Erro SQL: 0][Compl.: 0000]
   Programa Cobol : PENPO308 Total area saida : [0]

CONCLUSÃO
Não foi identificado problema de deploy, infraestrutura JBoss ou comunicação. A falha está na resposta do PENPO308, que, quando demora mais que ~6 segundos, devolve área vazia sem sinalizar erro.

SOLICITAÇÕES
1. Verificar se houve alteração no programa PENPO308, na região CICS de DES ou no DB2 de DES entre 07/11 e 08/11.
2. Verificar contenção, lock ou lentidão nas tabelas acessadas pelo PENPO308.
3. Informar qual timeout ou condição faz o programa retornar área vazia com RC 0.
4. Verificar a saúde da região CICS de DES utilizada pela transação PH.

Ficamos à disposição para novos testes e para fornecer mais trechos de log.

Atenciosamente,
Jessé Batista – P585600
CTIS/CESTI – Esteiras DevOps DES/TQS
