1. Confirmar que no PORTAL o módulo existe dentro da imagem

bash
oc rsh <pod-sicow-portal-okd-des>
ls -l /opt/jboss/modules/br/gov/caixa/siusr/main/
cat /opt/jboss/modules/br/gov/caixa/siusr/main/module.xml

2. Comparar os logs de build

Compare a build da tag 1.0.38.7 do SEG com a build do PORTAL 1.0.36.1. Procure por jboss-modules, siusr, loginModule, module.xml ou nexus/binario. No PORTAL deve aparecer o download e a criação do módulo; no SEG, veja se o passo foi pulado ou se houve 404 no Nexus. Se a build roda no build-images-ads, o oc get bc vazio no namespace do SEG é normal. Lá dá para ver com:

bash
oc -n build-images-ads get builds | grep sicow-seg
oc -n build-images-ads logs build/<build-do-seg>

3. Comparar o arquivo jboss-modules dos dois repositórios

Duas falhas clássicas nesse tipo de arquivo lido por script:

Sem quebra de linha no final. Um while read em bash descarta a última linha. Com o cabeçalho e uma única linha de dado, o siusr é ignorado sem nenhum erro.
CRLF (arquivo editado no Windows). A versão fica 1.11.0:jar\r, a URL do Nexus sai errada e o download falha.

Para ver os dois casos, clone o repositório e rode:

bash
cat -A jboss-modules      # "^M$" no fim = CRLF; última linha sem "$" = sem newline

4. Ver se o artefato existe no Nexus

Caminho esperado: br/gov/caixa/siusr/siusr-loginModule/1.11.0/siusr-loginModule-1.11.0.jar. Compare com a versão usada no jboss-modules do PORTAL; se o PORTAL usa outra versão, é um indício forte.

Pelo formato do arquivo, minha aposta é o item 3 (newline ou CRLF) ou o 4 (versão inexistente no Nexus). O log da build do item 2 deve mostrar qual dos dois.
