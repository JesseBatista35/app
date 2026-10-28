<img width="615" height="387" alt="image" src="https://github.com/user-attachments/assets/8452b52d-0071-4d25-bfee-631b84fab52e" />


2026-10-28T12:10:56.5539827Z ##[section]Starting: Build Application
2026-10-28T12:10:56.5543762Z ==============================================================================
2026-10-28T12:10:56.5543843Z Task         : Bash
2026-10-28T12:10:56.5543887Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-28T12:10:56.5544016Z Version      : 3.227.0
2026-10-28T12:10:56.5544061Z Author       : Microsoft Corporation
2026-10-28T12:10:56.5544114Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-28T12:10:56.5544217Z ==============================================================================
2026-10-28T12:10:56.7007908Z Generating script.
2026-10-28T12:10:56.7020597Z ========================== Starting Command Output ===========================
2026-10-28T12:10:56.7028260Z [command]/usr/bin/bash /opt/ads-agent/_work/_temp/83a50013-c2e9-4208-9826-c309e1d1ff22.sh
2026-10-28T12:10:56.7094254Z npm test -- --watch=false --code-coverage --browsers=ChromeHeadlessCI ; ng build --configuration production --aot --output-path=dist
2026-10-28T12:10:56.7094669Z <----ANGULAR---->
2026-10-28T12:10:57.2733614Z 
2026-10-28T12:10:57.2734413Z      _                      _                 ____ _     ___
2026-10-28T12:10:57.2734606Z     / \   _ __   __ _ _   _| | __ _ _ __     / ___| |   |_ _|
2026-10-28T12:10:57.2735283Z    / △ \ | '_ \ / _` | | | | |/ _` | '__|   | |   | |    | |
2026-10-28T12:10:57.2735599Z   / ___ \| | | | (_| | |_| | | (_| | |      | |___| |___ | |
2026-10-28T12:10:57.2735869Z  /_/   \_\_| |_|\__, |\__,_|_|\__,_|_|       \____|_____|___|
2026-10-28T12:10:57.2736091Z                 |___/
2026-10-28T12:10:57.2736274Z     
2026-10-28T12:10:57.2736349Z 
2026-10-28T12:10:57.2736542Z Angular CLI: 19.2.27
2026-10-28T12:10:57.2736868Z Node: 22.13.1
2026-10-28T12:10:57.2737072Z Package Manager: npm 10.9.2
2026-10-28T12:10:57.2737233Z OS: linux x64
2026-10-28T12:10:57.2737348Z 
2026-10-28T12:10:57.2737489Z Angular: 19.2.25
2026-10-28T12:10:57.2737813Z ... animations, common, compiler, compiler-cli, core, forms
2026-10-28T12:10:57.2738185Z ... language-service, localize, platform-browser
2026-10-28T12:10:57.2738746Z ... platform-browser-dynamic, router
2026-10-28T12:10:57.2738836Z 
2026-10-28T12:10:57.2739036Z Package                         Version
2026-10-28T12:10:57.2739357Z ---------------------------------------------------------
2026-10-28T12:10:57.2740135Z @angular-devkit/architect       0.1902.27
2026-10-28T12:10:57.2740445Z @angular-devkit/build-angular   19.2.27
2026-10-28T12:10:57.2740720Z @angular-devkit/core            19.2.27 (cli-only)
2026-10-28T12:10:57.2741035Z @angular-devkit/schematics      19.2.27
2026-10-28T12:10:57.2741282Z @angular/cli                    19.2.27
2026-10-28T12:10:57.2741506Z @schematics/angular             19.2.27
2026-10-28T12:10:57.2741726Z rxjs                            7.8.2
2026-10-28T12:10:57.2741940Z typescript                      5.6.3
2026-10-28T12:10:57.2742107Z zone.js                         0.15.1
2026-10-28T12:10:57.2742924Z     
2026-10-28T12:10:57.7079447Z 
2026-10-28T12:10:57.7080491Z > name_app@1.0.0-snapshot test
2026-10-28T12:10:57.7080979Z > ng test --watch=false --code-coverage --browsers=ChromeHeadlessCI
2026-10-28T12:10:57.7081143Z 
2026-10-28T12:10:58.9848681Z One or more browsers which are configured in the project's Browserslist configuration will be ignored as ES5 output is not supported by the Angular CLI.
2026-10-28T12:10:58.9849248Z Ignored browsers: kaios 2.5, op_mini all
2026-10-28T12:10:59.4994419Z - Generating browser application bundles (phase: setup)...
2026-10-28T12:11:28.8856822Z ✔ Browser application bundle generation complete.
2026-10-28T12:11:28.9473385Z [32m28 10 2026 09:11:28.945:INFO [karma-server]: [39mKarma v6.4.4 server started at http://localhost:9876/
2026-10-28T12:11:28.9476300Z [32m28 10 2026 09:11:28.947:INFO [launcher]: [39mLaunching browsers ChromeHeadlessCI with concurrency unlimited
2026-10-28T12:11:28.9518229Z [32m28 10 2026 09:11:28.951:INFO [launcher]: [39mStarting browser ChromeHeadless
2026-10-28T12:11:28.9522812Z [91m28 10 2026 09:11:28.952:ERROR [launcher]: [39mNo binary for ChromeHeadless browser on your platform.
2026-10-28T12:11:28.9523024Z   Please, set "CHROME_BIN" env variable.
2026-10-28T12:11:31.3646997Z ✔ Browser application bundle generation complete.
2026-10-28T12:11:31.3659744Z ✔ Browser application bundle generation complete.
2026-10-28T12:11:33.2692509Z One or more browsers which are configured in the project's Browserslist configuration will be ignored as ES5 output is not supported by the Angular CLI.
2026-10-28T12:11:33.2693101Z Ignored browsers: kaios 2.5, op_mini all
2026-10-28T12:11:33.4658358Z - Generating browser application bundles (phase: setup)...
2026-10-28T12:12:42.9559277Z ✔ Browser application bundle generation complete.
2026-10-28T12:12:45.6863219Z ✔ Browser application bundle generation complete.
2026-10-28T12:12:45.6874557Z - Copying assets...
2026-10-28T12:12:45.7125760Z ✔ Copying assets complete.
2026-10-28T12:12:45.7126268Z - Generating index html...
2026-10-28T12:12:45.8650479Z ✔ Index html generation complete.
2026-10-28T12:12:45.8694102Z 
2026-10-28T12:12:45.8694579Z Initial chunk files           | Names                                                                  |  Raw size | Estimated transfer size
2026-10-28T12:12:45.8694797Z main.aecf0d77cc6d721d.js      | main                                                                   |   4.81 MB |                 1.16 MB
2026-10-28T12:12:45.8695011Z styles.e92ecd7289248279.css   | styles                                                                 | 241.31 kB |                27.48 kB
2026-10-28T12:12:45.8695910Z polyfills.d00944c2151e787a.js | polyfills                                                              |  35.39 kB |                11.55 kB
2026-10-28T12:12:45.8696147Z runtime.5ddb6340780808db.js   | runtime                                                                |   4.20 kB |                 2.01 kB
2026-10-28T12:12:45.8696239Z 
2026-10-28T12:12:45.8696560Z                               | Initial total                                                          |   5.09 MB |                 1.20 MB
2026-10-28T12:12:45.8696662Z 
2026-10-28T12:12:45.8696773Z Lazy chunk files              | Names                                                                  |  Raw size | Estimated transfer size
2026-10-28T12:12:45.8697338Z 52.c3e48f23f2b2dfe5.js        | modules-conformidade-contratacao-conformidade-contratacao-module       | 222.67 kB |                25.64 kB
2026-10-28T12:12:45.8697642Z 5296.65f74e018fae752c.js      | ngx-quill-quill-CUw8Q_m0-mjs                                           | 201.18 kB |                51.69 kB
2026-10-28T12:12:45.8698141Z 7867.26cebb6e330df204.js      | modules-dossie-dossie-module                                           | 123.71 kB |                18.48 kB
2026-10-28T12:12:45.8698452Z 588.52b0a03829d1621d.js       | modules-grupo-familiar-grupo-familiar-module                           |  89.03 kB |                12.59 kB
2026-10-28T12:12:45.8698752Z 7614.329659e7ee86f6ee.js      | modules-limite-renda-limite-renda-module                               |  73.67 kB |                12.79 kB
2026-10-28T12:12:45.8699650Z 7376.e52b0656680ef1e2.js      | modules-dossie-documentos-dossie-documentos-module                     |  71.18 kB |                23.06 kB
2026-10-28T12:12:45.8699983Z 5580.26a36fe75840d647.js      | modules-dossie-documentos-dossie-documentos-module                     |  68.26 kB |                13.15 kB
2026-10-28T12:12:45.8700353Z 9454.3fd28fdb4181e19f.js      | modules-relatorio-relatorio-module                                     |  65.29 kB |                11.64 kB
2026-10-28T12:12:45.8700831Z 2349.7096991f0d5872a4.js      | modules-tomador-tomador-module                                         |  61.62 kB |                13.28 kB
2026-10-28T12:12:45.8701276Z 311.08651666c0f3ab7a.js       | modules-remessa-indicacao-remessa-indicacao-module                     |  56.59 kB |                11.40 kB
2026-10-28T12:12:45.8701629Z 6546.d431715d3be9726e.js      | modules-empreendimento-empreendimento-module                           |  54.55 kB |                10.18 kB
2026-10-28T12:12:45.8702348Z 4216.4f2ba17e43960a16.js      | modules-pesquisa-operacional-pesquisa-operacional-module               |  51.16 kB |                 9.47 kB
2026-10-28T12:12:45.8702750Z 3243.4f9c2a6548db7479.js      | modules-manter-tarifa-tarifa-module                                    |  49.27 kB |                 9.56 kB
2026-10-28T12:12:45.8703144Z 5179.9a1ed0e770bf5c31.js      | modules-bolsa-familia-bolsa-familia-module                             |  48.51 kB |                 9.54 kB
2026-10-28T12:12:45.8703567Z 6463.be53bdf4e4440d15.js      | modules-lista-publicacao-lista-publicacao-module                       |  45.44 kB |                 9.19 kB
2026-10-28T12:12:45.8703891Z 684.396195a391a0add5.js       | modules-destinatario-mensagem-destinatario-mensagem-module             |  42.33 kB |                 7.34 kB
2026-10-28T12:12:45.8704188Z 7660.f67b04b1e3180408.js      | modules-almo-almo-module                                               |  38.36 kB |                 8.23 kB
2026-10-28T12:12:45.8704914Z 3518.08c8e6f9ac91161b.js      | modules-demanda-empreendimento-demanda-empreendimento-module           |  36.11 kB |                 7.82 kB
2026-10-28T12:12:45.8705258Z 5721.2282b4e917649e35.js      | modules-parametro-lista-publicacao-parametro-lista-publicacao-module   |  34.92 kB |                 7.57 kB
2026-10-28T12:12:45.8705586Z 9427.33f403b860bec502.js      | modules-limite-renda-empreendimento-limite-renda-empreendimento-module |  33.97 kB |                 7.42 kB
2026-10-28T12:12:45.8705853Z 2505.f98133867c3dc017.js      | modules-modalidade-modalidade-module                                   |  33.10 kB |                 7.01 kB
2026-10-28T12:12:45.8706209Z 9695.030999ecff0c4337.js      | modules-programa-programa-module                                       |  32.34 kB |                 5.04 kB
2026-10-28T12:12:45.8706519Z 7589.35aa03893b989ec8.js      | modules-programa-habitacional-programa-habitacional-module             |  31.77 kB |                 6.47 kB
2026-10-28T12:12:45.8706820Z 4499.ce99e5472c4b8ccc.js      | modules-origem-recurso-origem-recurso-module                           |  30.92 kB |                 6.52 kB
2026-10-28T12:12:45.8707210Z 2760.c14220a085f0f991.js      | modules-processamento-rotina-processamento-rotina-module               |  29.91 kB |                 5.73 kB
2026-10-28T12:12:45.8707562Z 190.034f438c52c3241a.js       | modules-manter-documento-manter-documento-module                       |  28.68 kB |                 6.41 kB
2026-10-28T12:12:45.8707890Z 3607.265de70ac9845163.js      | modules-manter-criterio-analise-criterio-analise-module                |  28.25 kB |                 6.56 kB
2026-10-28T12:12:45.8708197Z 5963.2eb7d869bebbab1e.js      | modules-indicacao-pessoa-indicacao-pessoa-module                       |  28.06 kB |                 5.72 kB
2026-10-28T12:12:45.8708489Z 861.31aeac42fba32e37.js       | modules-ente-publico-ente-publico-module                               |  27.38 kB |                 6.21 kB
2026-10-28T12:12:45.8708793Z 554.e50773e5e68cba1e.js       | modules-restricao-judicial-restricao-judicial-module                   |  27.14 kB |                 6.15 kB
2026-10-28T12:12:45.8709102Z 5829.e24392927fbbd3e8.js      | modules-empreendimento-bloqueado-empreendimento-bloqueado-module       |  24.49 kB |                 5.91 kB
2026-10-28T12:12:45.8709297Z common.ff45dc63fb0f3f72.js    | common                                                                 |  24.09 kB |                 5.19 kB
2026-10-28T12:12:45.8709644Z 1014.69ef20cc6e02c410.js      | modules-emitir-relatorio-tarifa-emitir-relatorio-tarifa-module         |  23.74 kB |                 4.42 kB
2026-10-28T12:12:45.8709955Z 897.39ef05a793f655d7.js       | modules-repesquisa-repesquisa-module                                   |  22.18 kB |                 5.36 kB
2026-10-28T12:12:45.8710238Z 418.e8c6c6e7606d9efe.js       | modules-tomador-tomador-module                                         |  19.39 kB |                 4.78 kB
2026-10-28T12:12:45.8710621Z 1013.23a7b587b6affeab.js      | modules-grupo-familiar-grupo-familiar-module                           |  18.80 kB |                 3.85 kB
2026-10-28T12:12:45.8710921Z 6592.6ebe88a80c5a941f.js      | modules-contrato-beneficiario-contrato-beneficiario-module             |  18.00 kB |                 4.49 kB
2026-10-28T12:12:45.8711224Z 8104.75dfadd965323c18.js      | modules-conversao-municipio-conversao-municipio-module                 |  17.98 kB |                 4.47 kB
2026-10-28T12:12:45.8711516Z 5255.18e35c41b698e6b9.js      | modules-tomador-tomador-module                                         |  15.75 kB |                 3.91 kB
2026-10-28T12:12:45.8711803Z 151.afac83da56e4788a.js       | modules-parametros-gerais-parametros-gerais-module                     |  15.55 kB |                 4.17 kB
2026-10-28T12:12:45.8712102Z 8680.8af1a581ccb8d34c.js      | modules-deficit-habitacional-deficit-habitacional-module               |  15.36 kB |                 4.20 kB
2026-10-28T12:12:45.8712399Z 6092.46671711443b4317.js      | modules-rotina-rotina-module                                           |  13.89 kB |                 3.48 kB
2026-10-28T12:12:45.8712654Z 9654.78d6070853ab2a9d.js      | modules-emitir-tarifa-emitir-tarifa-module                             |  13.57 kB |                 2.80 kB
2026-10-28T12:12:45.8712963Z 6363.970106ec81c68359.js      | modules-parametro-beneficio-parametro-beneficio-module                 |  13.14 kB |                 3.48 kB
2026-10-28T12:12:45.8713291Z 3230.b36b7e7a561c0e7f.js      | modules-manter-criterio-analise-criterio-analise-module                |  11.79 kB |                 3.03 kB
2026-10-28T12:12:45.8713592Z 5204.b5263a543e63a7e6.js      | modules-mensagem-erro-mensagem-erro-module                             |  11.28 kB |                 2.92 kB
2026-10-28T12:12:45.8713888Z 8141.36702e5b078a5c1d.js      | modules-periodicidade-periodicidade-module                             |  11.15 kB |                 2.87 kB
2026-10-28T12:12:45.8714185Z 6070.4886ed2c9e4f2448.js      | modules-remuneracao-rais-remuneracao-rais-module                       |  10.95 kB |                 2.97 kB
2026-10-28T12:12:45.8714509Z 600.c71b5e333b5977db.js       | modules-funcionalidade-funcionalidade-module                           |  10.94 kB |                 2.86 kB
2026-10-28T12:12:45.8714800Z 2712.11dde95dcd25e5f1.js      | modules-grupo-familiar-grupo-familiar-module                           |  10.58 kB |                 2.81 kB
2026-10-28T12:12:45.8715110Z 2745.5c42079ae482e8ef.js      | modules-indicacao-rejeitada-indicacao-rejeitada-module                 |  10.38 kB |                 2.91 kB
2026-10-28T12:12:45.8715408Z 2024.b766357cbccb25e3.js      | modules-indicado-ministerio-indicado-ministerio-module                 |   9.92 kB |                 2.88 kB
2026-10-28T12:12:45.8715669Z 6544.31c7766d198407f1.js      | modules-erro-acesso-erro-acesso-sistema-module                         |   7.31 kB |                 2.13 kB
2026-10-28T12:12:45.8715980Z 5600.1c5fa85ea3c83f33.js      | modules-dashboard-dashboard-module                                     |   3.72 kB |                 1.42 kB
2026-10-28T12:12:45.8716354Z 3847.a9e4a33600834725.js      | modules-erro-acesso-page-not-found-module                              |   1.02 kB |               476 bytes
2026-10-28T12:12:45.8716721Z 8315.e33fc59d45d59465.js      | modules-erro-acesso-acesso-negado-module                               | 973 bytes |               454 bytes
2026-10-28T12:12:45.8716895Z 
2026-10-28T12:12:45.8717209Z Build at: 2026-10-28T12:12:45.866Z - Hash: 7741332f44dbefb9 - Time: 72254ms
2026-10-28T12:12:45.8717374Z 
2026-10-28T12:12:45.8717661Z ./src/styles.scss - Warning: Module Warning (from ./node_modules/sass-loader/dist/cjs.js):
2026-10-28T12:12:45.8718006Z Deprecation Warning on line 0, column 8 of file:///opt/ads-agent/_work/71/s/src/assets/sass/main.scss:0:8:
2026-10-28T12:12:45.8718381Z Sass @import rules are deprecated and will be removed in Dart Sass 3.0.0.
2026-10-28T12:12:45.8718517Z 
2026-10-28T12:12:45.8718735Z More info and automated migrator: https://sass-lang.com/d/import
2026-10-28T12:12:45.8718907Z 
2026-10-28T12:12:45.8719131Z 0 | @import 'vendor/bootstrap';
2026-10-28T12:12:45.8719205Z 
2026-10-28T12:12:45.8719248Z 
2026-10-28T12:12:45.8719431Z src/assets/sass/main.scss 1:9  @import
2026-10-28T12:12:45.8719828Z src/styles.scss 1:9            root stylesheet
2026-10-28T12:12:45.8719909Z 
2026-10-28T12:12:45.8719960Z 
2026-10-28T12:12:45.8720292Z ./src/styles.scss - Warning: Module Warning (from ./node_modules/sass-loader/dist/cjs.js):
2026-10-28T12:12:45.8720595Z Deprecation Warning on line 0, column 8 of file:///opt/ads-agent/_work/71/s/src/styles.scss:0:8:
2026-10-28T12:12:45.8720786Z Sass @import rules are deprecated and will be removed in Dart Sass 3.0.0.
2026-10-28T12:12:45.8720851Z 
2026-10-28T12:12:45.8721055Z More info and automated migrator: https://sass-lang.com/d/import
2026-10-28T12:12:45.8814348Z 
2026-10-28T12:12:45.8815176Z 0 | @import 'assets/sass/main';
2026-10-28T12:12:45.8815282Z 
2026-10-28T12:12:45.8815381Z 
2026-10-28T12:12:45.8815657Z src/styles.scss 1:9  root stylesheet
2026-10-28T12:12:45.8815714Z 
2026-10-28T12:12:45.8815951Z 
2026-10-28T12:12:45.8816347Z ./src/styles.scss - Warning: Module Warning (from ./node_modules/sass-loader/dist/cjs.js):
2026-10-28T12:12:45.8816615Z Deprecation Warning on line 1, column 8 of file:///opt/ads-agent/_work/71/s/src/assets/sass/main.scss:1:8:
2026-10-28T12:12:45.8816828Z Sass @import rules are deprecated and will be removed in Dart Sass 3.0.0.
2026-10-28T12:12:45.8816951Z 
2026-10-28T12:12:45.8817184Z More info and automated migrator: https://sass-lang.com/d/import
2026-10-28T12:12:45.8817250Z 
2026-10-28T12:12:45.8817418Z 1 | @import 'utils/variables';
2026-10-28T12:12:45.8817468Z 
2026-10-28T12:12:45.8817502Z 
2026-10-28T12:12:45.8817638Z src/assets/sass/main.scss 2:9  @import
2026-10-28T12:12:45.8817803Z src/styles.scss 1:9            root stylesheet
2026-10-28T12:12:45.8817859Z 
2026-10-28T12:12:45.8817928Z 
2026-10-28T12:12:45.8818115Z ./src/styles.scss - Warning: Module Warning (from ./node_modules/sass-loader/dist/cjs.js):
2026-10-28T12:12:45.8818440Z Deprecation Warning on line 2, column 8 of file:///opt/ads-agent/_work/71/s/src/assets/sass/main.scss:2:8:
2026-10-28T12:12:45.8818851Z Sass @import rules are deprecated and will be removed in Dart Sass 3.0.0.
2026-10-28T12:12:45.8818913Z 
2026-10-28T12:12:45.8819117Z More info and automated migrator: https://sass-lang.com/d/import
2026-10-28T12:12:45.8819234Z 
2026-10-28T12:12:45.8819362Z 2 | @import 'utils/helpers';
2026-10-28T12:12:45.8819451Z 
2026-10-28T12:12:45.8819577Z 
2026-10-28T12:12:45.8819723Z src/assets/sass/main.scss 3:9  @import
2026-10-28T12:12:45.8819895Z src/styles.scss 1:9            root stylesheet
2026-10-28T12:12:45.8819952Z 
2026-10-28T12:12:45.8819982Z 
2026-10-28T12:12:45.8820279Z ./src/styles.scss - Warning: Module Warning (from ./node_modules/sass-loader/dist/cjs.js):
2026-10-28T12:12:45.8820649Z Deprecation Warning on line 3, column 8 of file:///opt/ads-agent/_work/71/s/src/assets/sass/main.scss:3:8:
2026-10-28T12:12:45.8820844Z Sass @import rules are deprecated and will be removed in Dart Sass 3.0.0.
2026-10-28T12:12:45.8820909Z 
2026-10-28T12:12:45.8821127Z More info and automated migrator: https://sass-lang.com/d/import
2026-10-28T12:12:45.8821221Z 
2026-10-28T12:12:45.8821454Z 3 | @import 'components/components';
2026-10-28T12:12:45.8821504Z 
2026-10-28T12:12:45.8821568Z 
2026-10-28T12:12:45.8821702Z src/assets/sass/main.scss 4:9  @import
2026-10-28T12:12:45.8821826Z src/styles.scss 1:9            root stylesheet
2026-10-28T12:12:45.8821914Z 
2026-10-28T12:12:45.8821946Z 
2026-10-28T12:12:45.8822165Z ./src/styles.scss - Warning: Module Warning (from ./node_modules/sass-loader/dist/cjs.js):
2026-10-28T12:12:45.8822477Z Deprecation Warning on line 240, column 20 of file:///opt/ads-agent/_work/71/s/src/assets/sass/utils/variables/_colors.scss:240:20:
2026-10-28T12:12:45.8822845Z Global built-in functions are deprecated and will be removed in Dart Sass 3.0.0.
2026-10-28T12:12:45.8822968Z Use map.get instead.
2026-10-28T12:12:45.8823047Z 
2026-10-28T12:12:45.8823266Z More info and automated migrator: https://sass-lang.com/d/import
2026-10-28T12:12:45.8823333Z 
2026-10-28T12:12:45.8823552Z 240 |   background-color: map-get($azul_cx, 'standard');
2026-10-28T12:12:45.8823613Z 
2026-10-28T12:12:45.8823643Z 
2026-10-28T12:12:45.8823827Z src/assets/sass/utils/variables/_colors.scss 241:21  @import
2026-10-28T12:12:45.8824087Z src/assets/sass/utils/_variables.scss 54:9           @import
2026-10-28T12:12:45.8824309Z src/assets/sass/main.scss 2:9                        @import
2026-10-28T12:12:45.8824531Z src/styles.scss 1:9                                  root stylesheet
2026-10-28T12:12:45.8824624Z 
2026-10-28T12:12:45.8824672Z 
2026-10-28T12:12:45.8824916Z ./src/styles.scss - Warning: Module Warning (from ./node_modules/sass-loader/dist/cjs.js):
2026-10-28T12:12:45.8825223Z Deprecation Warning on line 244, column 14 of file:///opt/ads-agent/_work/71/s/src/assets/sass/utils/variables/_colors.scss:244:14:
2026-10-28T12:12:45.8825516Z Global built-in functions are deprecated and will be removed in Dart Sass 3.0.0.
2026-10-28T12:12:45.8825675Z Use map.get instead.
2026-10-28T12:12:45.8825721Z 
2026-10-28T12:12:45.8825919Z More info and automated migrator: https://sass-lang.com/d/import
2026-10-28T12:12:45.8825980Z 
2026-10-28T12:12:45.8826182Z 244 |   background: map-get(
2026-10-28T12:12:45.8826383Z     $azul_cx,
2026-10-28T12:12:45.8826586Z     'standard'
2026-10-28T12:12:45.8826698Z   ); /* For browsers that do not support gradients */
2026-10-28T12:12:45.8826795Z 
2026-10-28T12:12:45.8826830Z 
2026-10-28T12:12:45.8826983Z src/assets/sass/utils/variables/_colors.scss 245:15  @import
2026-10-28T12:12:45.8827179Z src/assets/sass/utils/_variables.scss 54:9           @import
2026-10-28T12:12:45.8827348Z src/assets/sass/main.scss 2:9                        @import
2026-10-28T12:12:45.8827476Z src/styles.scss 1:9                                  root stylesheet
2026-10-28T12:12:45.8827579Z 
2026-10-28T12:12:45.8827614Z 
2026-10-28T12:12:45.8827836Z ./src/styles.scss - Warning: Module Warning (from ./node_modules/sass-loader/dist/cjs.js):
2026-10-28T12:12:45.8828227Z Deprecation Warning on line 250, column 4 of file:///opt/ads-agent/_work/71/s/src/assets/sass/utils/variables/_colors.scss:250:4:
2026-10-28T12:12:45.8828529Z Global built-in functions are deprecated and will be removed in Dart Sass 3.0.0.
2026-10-28T12:12:45.8828656Z Use map.get instead.
2026-10-28T12:12:45.8828736Z 
2026-10-28T12:12:45.8828932Z More info and automated migrator: https://sass-lang.com/d/import
2026-10-28T12:12:45.8828995Z 
2026-10-28T12:12:45.8829199Z 250 |     map-get($azul_cx, 'standard') 0%,
2026-10-28T12:12:45.8829254Z 
2026-10-28T12:12:45.8829285Z 
2026-10-28T12:12:45.8829439Z src/assets/sass/utils/variables/_colors.scss 251:5  @import
2026-10-28T12:12:45.8829703Z src/assets/sass/utils/_variables.scss 54:9          @import
2026-10-28T12:12:45.8829873Z src/assets/sass/main.scss 2:9                       @import
2026-10-28T12:12:45.8830028Z src/styles.scss 1:9                                 root stylesheet
2026-10-28T12:12:45.8830085Z 
2026-10-28T12:12:45.8830122Z 
2026-10-28T12:12:45.8830346Z ./src/styles.scss - Warning: Module Warning (from ./node_modules/sass-loader/dist/cjs.js):
2026-10-28T12:12:45.8830642Z Deprecation Warning on line 251, column 4 of file:///opt/ads-agent/_work/71/s/src/assets/sass/utils/variables/_colors.scss:251:4:
2026-10-28T12:12:45.8830911Z Global built-in functions are deprecated and will be removed in Dart Sass 3.0.0.
2026-10-28T12:12:45.8831094Z Use map.get instead.
2026-10-28T12:12:45.8831161Z 
2026-10-28T12:12:45.8831425Z More info and automated migrator: https://sass-lang.com/d/import
2026-10-28T12:12:45.8831487Z 
2026-10-28T12:12:45.8831675Z 251 |     map-get($turquesa, 'standard') 65.63%
2026-10-28T12:12:45.8831731Z 
2026-10-28T12:12:45.8831858Z 
2026-10-28T12:12:45.8832037Z src/assets/sass/utils/variables/_colors.scss 252:5  @import
2026-10-28T12:12:45.8832171Z src/assets/sass/utils/_variables.scss 54:9          @import
2026-10-28T12:12:45.8832334Z src/assets/sass/main.scss 2:9                       @import
2026-10-28T12:12:45.8832495Z src/styles.scss 1:9                                 root stylesheet
2026-10-28T12:12:45.8832550Z 
2026-10-28T12:12:45.8832613Z 
2026-10-28T12:12:45.8832857Z ./src/styles.scss - Warning: Module Warning (from ./node_modules/sass-loader/dist/cjs.js):
2026-10-28T12:12:45.8833118Z Deprecation Warning on line 255, column 4 of file:///opt/ads-agent/_work/71/s/src/assets/sass/utils/variables/_colors.scss:255:4:
2026-10-28T12:12:45.8833391Z Global built-in functions are deprecated and will be removed in Dart Sass 3.0.0.
2026-10-28T12:12:45.8833549Z Use map.get instead.
2026-10-28T12:12:45.8833591Z 
2026-10-28T12:12:45.8833790Z More info and automated migrator: https://sass-lang.com/d/import
2026-10-28T12:12:45.8833889Z 
2026-10-28T12:12:45.8834034Z 255 |     map-get($azul_cx, 'standard') 0%,
2026-10-28T12:12:45.8834119Z 
2026-10-28T12:12:45.8834150Z 
2026-10-28T12:12:45.8834288Z src/assets/sass/utils/variables/_colors.scss 256:5  @import
2026-10-28T12:12:45.8834463Z src/assets/sass/utils/_variables.scss 54:9          @import
2026-10-28T12:12:45.8834645Z src/assets/sass/main.scss 2:9                       @import
2026-10-28T12:12:45.8834771Z src/styles.scss 1:9                                 root stylesheet
2026-10-28T12:12:45.8834860Z 
2026-10-28T12:12:45.8834892Z 
2026-10-28T12:12:45.8835111Z ./src/styles.scss - Warning: Module Warning (from ./node_modules/sass-loader/dist/cjs.js):
2026-10-28T12:12:45.8835281Z 268 repetitive deprecation warnings omitted.
2026-10-28T12:12:45.8835437Z Run in verbose mode to see all warnings.
2026-10-28T12:12:45.8835493Z 
2026-10-28T12:12:45.8835812Z Warning: /opt/ads-agent/_work/71/s/node_modules/angular-oauth2-oidc-jwks/fesm2022/angular-oauth2-oidc-jwks.mjs depends on 'jsrsasign'. CommonJS or AMD dependencies can cause optimization bailouts.
2026-10-28T12:12:45.8836184Z For more info see: https://angular.dev/tools/cli/build#configuring-commonjs-dependencies
2026-10-28T12:12:45.8836304Z 
2026-10-28T12:12:45.8836636Z Warning: /opt/ads-agent/_work/71/s/node_modules/quill/core.js depends on 'quill-delta'. CommonJS or AMD dependencies can cause optimization bailouts.
2026-10-28T12:12:45.8837027Z For more info see: https://angular.dev/tools/cli/build#configuring-commonjs-dependencies
2026-10-28T12:12:45.8837103Z 
2026-10-28T12:12:45.8837417Z Warning: /opt/ads-agent/_work/71/s/src/app/modules/relatorio/parametrizar-relatorio/parametrizar-relatorio.component.ts depends on 'lodash'. CommonJS or AMD dependencies can cause optimization bailouts.
2026-10-28T12:12:45.8837718Z For more info see: https://angular.dev/tools/cli/build#configuring-commonjs-dependencies
2026-10-28T12:12:45.8837788Z 
2026-10-28T12:12:45.8838069Z Warning: /opt/ads-agent/_work/71/s/src/app/shared/export-pdf/export.component.ts depends on 'html2canvas'. CommonJS or AMD dependencies can cause optimization bailouts.
2026-10-28T12:12:45.8838365Z For more info see: https://angular.dev/tools/cli/build#configuring-commonjs-dependencies
2026-10-28T12:12:45.8838436Z 
2026-10-28T12:12:45.8838727Z Warning: /opt/ads-agent/_work/71/s/src/app/shared/export-pdf/export.component.ts depends on 'pdfmake/build/pdfmake'. CommonJS or AMD dependencies can cause optimization bailouts.
2026-10-28T12:12:45.8839030Z For more info see: https://angular.dev/tools/cli/build#configuring-commonjs-dependencies
2026-10-28T12:12:45.8839100Z 
2026-10-28T12:12:45.8839441Z Warning: /opt/ads-agent/_work/71/s/src/app/shared/export-pdf/export.component.ts depends on 'pdfmake/build/vfs_fonts'. CommonJS or AMD dependencies can cause optimization bailouts.
2026-10-28T12:12:45.8839911Z For more info see: https://angular.dev/tools/cli/build#configuring-commonjs-dependencies
2026-10-28T12:12:45.8839984Z 
2026-10-28T12:12:45.8840265Z Warning: /opt/ads-agent/_work/71/s/src/app/shared/export-pdf/export.component.ts depends on 'xlsx'. CommonJS or AMD dependencies can cause optimization bailouts.
2026-10-28T12:12:45.8840613Z For more info see: https://angular.dev/tools/cli/build#configuring-commonjs-dependencies
2026-10-28T12:12:45.8840680Z 
2026-10-28T12:12:45.8840852Z Warning: bundle initial exceeded maximum budget. Budget 3.00 MB was not met by 2.09 MB with a total of 5.09 MB.
2026-10-28T12:12:45.8840975Z 
2026-10-28T12:12:45.8841028Z 
2026-10-28T12:12:46.2764174Z ##[section]Finishing: Build Application



Skip to main contentSkip to issue filters
Logo, link to homepage
Projects
Issues
Rules
Quality Profiles
Quality Gates

Search for projects...
JM
SINCH-web-angular20-intra


atualizacao-angular
Last analysis of this Branch had 2 warnings
October 28, 2026 at 9:12 AM
Version 1.0.0-snapshot

Overview
Issues
Security Hotspots
Measures
Code
Activity
Project Information
Issues
My Issues
All
Clear All Filters
Filters

Issues in new code
Type
Code Smell
Clear

Bug
0

Vulnerability
0

Code Smell
27
Press Ctrl to add to selection
Severity

Blocker
0

Minor
25

Critical
0

Info
0

Major
2
Scope
Resolution
Status
Security Category
Creation Date
Language
Rule
Tag
Directory
File
Assignee
Author
Bulk Change
↑
←↓→
1 / 27issues
1h 26min effort
List of issues
src/app/interceptors/error.interceptor.ts
'throwError' is deprecated. Support for passing an error value will be removed in v8. Instead, pass a factory function to `throwError(() => new Error('test'))`. This is because it will create the error at the moment it should be created and capture a more appropriate stack trace. If for some reason you need to create the error ahead of time, you can still do that: `const err = new Error('test'); throwError(() => err);`.

6 days ago
L88

Code Smell

Minor

Open

Not assigned
15min effort

Comment

cwe, obsolete
src/.../buscar-conformidade-contratacao.component.ts
Remove this unused import of 'OnInit'.

6 days ago
L1

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/.../dados-basicos-grupo-familiar/dados-basicos-grupo-familiar.component.ts
Remove this unused import of 'OnInit'.

6 days ago
L4

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/.../dados-basicos-indicacao-demanda-dossie.component.ts
Remove this unused import of 'OnInit'.

6 days ago
L4

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/.../components/dados-participante/dados-participante.component.ts
Remove this unused import of 'OnInit'.

6 days ago
L4

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/.../situacao-grupo-familiar-dossie/situacao-grupo-familiar-dossie.component.ts
Remove this unused import of 'OnInit'.

6 days ago
L1

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/.../detalhar-documentos-grupo-familiar-dossie.component.ts
Remove this unused import of 'OnInit'.

6 days ago
L1

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/.../hitorico-participante-dossie/hitorico-participante-dossie.component.ts
Remove this unused import of 'OnInit'.

6 days ago
L2

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/.../detalhar-participante-grupo-familiar.component.ts
Extract this nested ternary operation into an independent statement.

6 days ago
L272

Code Smell

Major

Open

Not assigned
5min effort

Comment

confusing
src/.../buscar-indicacao-rejeitada/buscar-indicacao-rejeitada.component.ts
Remove this unused import of 'OnInit'.

5 days ago
L1

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/.../dados-empreendimento/dados-empreendimento.component.ts
Remove this unused import of 'OnInit'.

6 days ago
L1

Code Smell

Minor

Open

Not assigned
2min effort

Comment

es2015, unused
src/.../buscar-documento/buscar-documento.component.ts
Remove this unused import of 'OnInit'.

6 days ago
L1

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/.../historico-grupo-tarifa/historico-grupo-tarifa.component.ts
Remove this unused import of 'OnInit'.

6 days ago
L1

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/.../buscar-mensagem-erro/buscar-mensagem-erro.component.ts
Remove this unused import of 'OnInit'.

6 days ago
L1

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/.../buscar-parametro-beneficio/buscar-parametro-beneficio.component.ts
Remove this unused import of 'OnInit'.

6 days ago
L1

Code Smell

Minor

Open

Not assigned
2min effort

Comment

es2015, unused
src/.../buscar-parametros-gerais/buscar-parametros-gerais.component.ts
Remove this unused import of 'OnInit'.

6 days ago
L2

Code Smell

Minor

Open

Not assigned
2min effort

Comment

es2015, unused
src/.../programa/buscar-programa/buscar-programa.component.ts
Remove this unused import of 'OnInit'.

6 days ago
L1

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/.../buscar-remuneracao-rais/buscar-remuneracao-rais.component.ts
Remove this unused import of 'OnInit'.

6 days ago
L1

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/.../repesquisa/buscar-repesquisa/buscar-repesquisa.component.ts
Remove this unused import of 'OnInit'.

6 days ago
L3

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/.../shared/components/button-group/button-group.component.ts
Remove this unused import of 'OnInit'.

6 days ago
L5

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/app/shared/components/button/button.component.ts
Remove this unused import of 'OnInit'.

6 days ago
L1

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/.../shared/components/filter-table/filter-table.component.ts
'toPromise' is deprecated. Replaced with {@link firstValueFrom } and {@link lastValueFrom } . Will be removed in v8. Details: https://rxjs.dev/deprecations/to-promise

6 days ago
L887

Code Smell

Minor

Open

Not assigned
15min effort

Comment

cwe, obsolete
src/app/shared/components/form/form.component.ts
Remove this unused import of 'OnInit'.

6 days ago
L1

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/.../progress-bar/progress-bar/progress-bar.component.ts
Remove this unused import of 'OnInit'.

6 days ago
L1

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/app/shared/components/table/table.component.html
Remove this commented out code.

18 hours ago
L118

Code Smell

Major

Open

Not assigned
5min effort

Comment

unused
src/app/shared/layout/footer/footer.component.ts
Remove this unused import of 'OnInit'.

6 days ago
L1

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/app/shared/layout/sidebar/sidebar.component.ts
Remove this unused import of 'OnInit'.

6 days ago
L1

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
27 of 27 shown
SonarQube™ technology is powered by SonarSource SA
Community Editionv9.9.5 (build 90363)NO LONGER ACTIVELGPL v3CommunityDocumentationPluginsWeb API
