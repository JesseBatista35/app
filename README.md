set -euo pipefail

NEXUS="http://binario.caixa:8081/repository/snapshots"
GROUP_PATH="br/gov/caixa/siifx/caixinhas"
ARTIFACT="siifx-caixinhas-batch"
BASE="$NEXUS/$GROUP_PATH/$ARTIFACT"
DESTINO="$(System.DefaultWorkingDirectory)/binario"

# 1) Versão: usa VERSAO_BATCH se informada na release; senão, a SNAPSHOT mais recente do Nexus
VERSAO="${VERSAO_BATCH:-}"
if [ -z "$VERSAO" ]; then
  VERSAO=$(curl -sf "$BASE/maven-metadata.xml" \
    | grep -o '<version>[^<]*-SNAPSHOT</version>' \
    | sed 's/<[^>]*>//g' | sort -V | tail -1)
fi
[ -z "$VERSAO" ] && { echo "##vso[task.logissue type=error]Versão não encontrada no Nexus"; exit 1; }
echo "Versão: $VERSAO"

# 2) Último build (timestamp-buildNumber) do .jar principal dessa versão, sem classifier
VALOR=$(curl -sf "$BASE/$VERSAO/maven-metadata.xml" \
  | tr -d '\n\r\t ' \
  | sed 's/<snapshotVersion>/\n/g' \
  | grep '<extension>jar</extension>' | grep -v '<classifier>' \
  | grep -o '<value>[^<]*</value>' | sed 's/<[^>]*>//g' | tail -1)
[ -z "$VALOR" ] && { echo "##vso[task.logissue type=error]Snapshot do jar não encontrado para $VERSAO"; exit 1; }

JAR="$ARTIFACT-$VALOR.jar"
URL_CORRETA="$BASE/$VERSAO/$JAR"
echo "Artefato: $URL_CORRETA"

mkdir -p "$DESTINO"
curl -f "$URL_CORRETA" -o "$DESTINO/$JAR"
ls -l "$DESTINO"

echo "##vso[task.setvariable variable=URL_DEPLOY]$URL_CORRETA"

Como funciona:

Por padrão, pega a maior versão -SNAPSHOT publicada (hoje seria a 0.0.10) e, dentro dela, o último deploy feito pelo build, que é o jar do último reactor.
Se for preciso fixar uma versão, basta criar a variável VERSAO_BATCH (ex.: 0.0.10-SNAPSHOT) em Variables com “Settable at release time”. Assim o próprio dev a informa ao criar a release, sem pedir alteração da task, o que também atende o pedido do Geovane no Teams.
A variável URL_DEPLOY continua sendo exportada para a task “Deploy Batch” do mesmo jeito.

Antes de salvar, confira dois pontos:

Ordenação por versão. sort -V coloca 0.0.10 acima de 0.0.9, mas se existir uma branch publicando com versão maior que não deveria ir para DES, o script vai pegá-la. Nesse caso, use a VERSAO_BATCH.
Vínculo com o build. Se o artefato do build vinculado à release tiver o pom.xml, dá para ler a versão dele em vez de pegar a mais recente do Nexus. Isso amarra a release exatamente ao build que a gerou. Se quiser, me passa o alias e a estrutura do artefato (aba Pipeline → Artifacts) que eu ajusto a etapa 1 para isso.


