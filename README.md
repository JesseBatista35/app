O pipeline SINCH-web-angular20-intra (6710) não executava os testes unitários, por isso a cobertura do código novo chegava como 0% no Sonar da esteira e o Quality Gate reprovava (TE102). A branch Cesti-test001 passava apenas por ter poucas linhas alteradas.

Ajustes realizados no pipeline:

Inclusão de etapa para instalar o Chromium no agente de build, necessário para o Karma (o agente não possui navegador).
Alteração do NG_GOAL para executar npm test -- --watch=false --code-coverage --browsers=ChromeHeadlessCI antes do build.
Criação da variável SONAR_PROPERTIES no pipeline com sonar.javascript.lcov.reportPaths, para o Sonar ler a cobertura.

Resultado: análise na branch atualizacao-angular com Quality Gate aprovado (97,5% de cobertura em 659 linhas novas) e build concluído.

Observação para o time de desenvolvimento: dos 703 testes, 207 falham, quase todos por No provider for HttpClient / ActivatedRoute nos specs. Eles não bloqueiam o pipeline, mas convém corrigir incluindo provideHttpClient(), provideHttpClientTesting() e provideRouter([]) nos providers do TestBed.
