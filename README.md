Falta confirmar se é só esse usuário ou todos. Compare as chamadas do PENPO308 nos logs, incluindo os dias em que funcionava:

bash
cd /logs/jboss-eap/hc/servers/sipen_node3_lx0006/
grep -h "PENPO308 Total area saida" sipen.log* | grep -o "USUA.*" | sed 's/Programa Cobol : PENPO308 //' | sort | uniq -c
Se outros usuários tiverem área de saída maior que 0, o problema é cadastro ou perfil do F529058 (e de quem mais falhar) na base do SIPEN DES.
Se todos estiverem [0 ], o PENPO308 ou a base DB2 de DES está quebrado para todo mundo, e o caso vai para o time do Mainframe ou para o dev responsável pelo programa.

Para ver desde quando o retorno vazio acontece:

bash
grep -c "PENPO308 Total area saida : \[0 \]" sipen.log*

O framework.jar deixou de ser prioridade, já que a integração está respondendo. Se ainda quiser abrir o jar, o caminho é só o diretório, sem o prefixo jboss.home.dir=:

bash
find /opt/jboss/jboss-eap -name "framework.jar" 2>/dev/null
Como o Claude está se saindo nesta sessão?
