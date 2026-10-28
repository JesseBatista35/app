[CESTI] Instalar Chromium para testes (Karma/Sonar) - NÃO REMOVER


# ============================================================
# NÃO REMOVER - ajuste CESTI (esteira DES/TQS) - 28/10/2026
# O agente ads-agent-build não tem Chrome. Sem esta etapa o
# Karma não roda (No binary for ChromeHeadless), o lcov.info
# não é gerado e o Sonar reprova por cobertura 0% (TE102).
# Publica CHROME_BIN para o NG_GOAL do Angular-Build.
# ============================================================
dnf install -y --setopt=install_weak_deps=False chromium 2>&1 | tail -5

CHROME=$(command -v chromium-browser || command -v chromium || true)
if [ -n "$CHROME" ]; then
  echo "Chrome encontrado: $CHROME"
  $CHROME --version
  echo "##vso[task.setvariable variable=CHROME_BIN]$CHROME"
else
  echo "##[warning]Chromium não instalado - testes não vão rodar e o Sonar vai reprovar por cobertura"
fi
exit 0


Bom dia, Eduardo!

Você tinha razão. A branch Cesti-test001 passou só porque tinha pouquíssimas linhas alteradas, e nesse caso o Sonar não aplica a regra de cobertura. Ela não servia para mostrar que o pipeline estava funcionando.

O problema real estava na esteira. O pipeline do SINCH-web-angular20-intra (6710) não executava os testes unitários, então a cobertura chegava ao Sonar como 0% e o Quality Gate reprovava (TE102). Por isso nenhum ajuste que você fez no Karma ou nos testes mudava o resultado.

O que corrigi no pipeline:
1. Incluí uma etapa para instalar o Chromium no agente de build, porque o agente não tinha navegador e o Karma não conseguia rodar.
2. Alterei o NG_GOAL para executar os testes com cobertura antes do build: npm test -- --watch=false --code-coverage --browsers=ChromeHeadlessCI
3. Criei a variável SONAR_PROPERTIES no pipeline apontando para o lcov.info, para o Sonar ler a cobertura.

Resultado na branch atualizacao-angular: Quality Gate aprovado, com 97,5% de cobertura no código novo, e o build subiu normalmente.

Um ponto de atenção do lado de vocês: dos 703 testes, 207 ainda falham, quase todos por "No provider for HttpClient" ou "ActivatedRoute" nos specs. Isso não trava o pipeline, mas vale corrigir incluindo provideHttpClient(), provideHttpClientTesting() e provideRouter([]) nos providers do TestBed.

Para eu registrar a correção formalmente, você pode abrir um chamado para a esteira e colocar aos meus cuidados (Jessé Batista – P585600)? Na descrição pode colocar: "Pipeline SINCH-web-angular20-intra (6710) reprovando no Quality Gate do Sonar (TE102) por cobertura de testes em 0% na branch feature/atualizacao-angular". Assim que me passar o número, eu relato a correção e encerro.

Qualquer dúvida, me chama!
