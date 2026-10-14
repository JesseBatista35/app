
Skip to content
titletitle Administrator | sair
pesquisar
 
2
Correct
Dependency errors:

Some plugins could not be loaded due to unsatisfied dependencies. Fix these issues and restart Jenkins to restore the functionality provided by these plugins.

Folders Plugin version 6.6
Você deve atualizar o Jenkins de v2.121.1 para v2.130 ou superior para executar este plugin.
Downstream dependency errors:

These plugins failed to load because of one or more of the errors above. Fix those and these plugins will load again.

Delivery Pipeline Plugin version 1.3.2
Pipeline: Multibranch v2.20 falhou ao carregar. Corrija o problema com este plugin primeiro.
Pipeline: Declarative version 1.3.2
Pipeline: Shared Groovy Libraries v2.12 falhou ao carregar. Corrija o problema com este plugin primeiro.
Pipeline: Shared Groovy Libraries version 2.12
Folders Plugin v6.6 falhou ao carregar. Corrija o problema com este plugin primeiro.
Branch API Plugin version 2.0.20
Folders Plugin v6.6 falhou ao carregar. Corrija o problema com este plugin primeiro.
Pipeline: Multibranch version 2.20
Branch API Plugin v2.0.20 falhou ao carregar. Corrija o problema com este plugin primeiro.
There are resources Jenkins was not able to dispose automatically. 
Manage
Manage Jenkins

Jenkins
SIMCN
#2262
 Voltar ao projeto
 Estado pessoal
 Alterações
 Saída do console
 Exibir como texto puro
 Editar informações de compilação
 Excluir este build
 Parâmetros
 Git Build Data
 No Tags
 Reimplantar artefatos
 Resultado de testes
 Ver fingerprints
 Build anterior
FalhouSaída do console
Iniciado pelo usuário s535501
Construindo no workspace /opt/integracao_continua/jenkins_home/workspace/SIMCN
[WS-CLEANUP] Deleting project workspace...
[WS-CLEANUP] Deferred wipeout is used...
[WS-CLEANUP] Done
Cloning the remote Git repository
Cloning repository https://fontes.des.caixa/SIMCN/simcn.git
 > git init /opt/integracao_continua/jenkins_home/workspace/SIMCN # timeout=10
Fetching upstream changes from https://fontes.des.caixa/SIMCN/simcn.git
 > git --version # timeout=10
using GIT_ASKPASS to set credentials cesti36-p
 > git fetch --tags --progress https://fontes.des.caixa/SIMCN/simcn.git +refs/heads/*:refs/remotes/origin/*
 > git config remote.origin.url https://fontes.des.caixa/SIMCN/simcn.git # timeout=10
 > git config --add remote.origin.fetch +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git config remote.origin.url https://fontes.des.caixa/SIMCN/simcn.git # timeout=10
Fetching upstream changes from https://fontes.des.caixa/SIMCN/simcn.git
using GIT_ASKPASS to set credentials cesti36-p
 > git fetch --tags --progress https://fontes.des.caixa/SIMCN/simcn.git +refs/heads/*:refs/remotes/origin/*
 > git rev-parse refs/remotes/origin/sprint/parcial110^{commit} # timeout=10
 > git rev-parse refs/remotes/origin/origin/sprint/parcial110^{commit} # timeout=10
Checking out Revision f41c4b0340edfc7401b60c53e098dd23dfdd8e09 (refs/remotes/origin/sprint/parcial110)
 > git config core.sparsecheckout # timeout=10
 > git checkout -f f41c4b0340edfc7401b60c53e098dd23dfdd8e09
Commit message: "Merge branch 'feature/sp002-paulo-STRY00018497-criar-possibilidade-de-exclusao-em-lote-regras-de-conciliacao' into 'sprint/parcial110'"
 > git rev-list --no-walk f41c4b0340edfc7401b60c53e098dd23dfdd8e09 # timeout=10
Adding all registry entries
copy managed file [JENKINS_NPMRC] to file:/opt/integracao_continua/jenkins_home/workspace/SIMCN@tmp/config7076553055003758262tmp
[SIMCN] $ /bin/sh -xe /tmp/jenkins2129407407249844764.sh
[SIMCN] $ /bin/sh -xe /tmp/jenkins5187551482723564648.sh
+ /opt/integracao_continua/work/jenkins_script_steps/step_avaliacao_fortify.sh
[SIMCN] $ /bin/sh -xe /tmp/jenkins8296652911440713529.sh
+ /opt/integracao_continua/work/jenkins_script_steps/step_sonar_criar_projeto.sh
Parsing POMs
Modules changed, recalculating dependency graph
Established TCP socket on 44699
[SIMCN] $ /usr/java/jdk1.8.0_91/bin/java -cp /opt/integracao_continua/jenkins_home/plugins/maven-plugin/WEB-INF/lib/maven35-agent-1.12-alpha-1.jar:/opt/integracao_continua/tool_home/apache-maven-3.5.4/boot/plexus-classworlds-2.5.2.jar:/opt/integracao_continua/tool_home/apache-maven-3.5.4/conf/logging jenkins.maven3.agent.Maven35Main /opt/integracao_continua/tool_home/apache-maven-3.5.4 /var/cache/jenkins/war/WEB-INF/lib/remoting-3.20.jar /opt/integracao_continua/jenkins_home/plugins/maven-plugin/WEB-INF/lib/maven35-interceptor-1.12-alpha-1.jar /opt/integracao_continua/jenkins_home/plugins/maven-plugin/WEB-INF/lib/maven3-interceptor-commons-1.12.jar 44699
<===[JENKINS REMOTING CAPACITY]===>channel started
Executing Maven:  -B -f /opt/integracao_continua/jenkins_home/workspace/SIMCN/pom.xml -U clean package
[INFO] Scanning for projects...
[INFO] ------------------------------------------------------------------------
[INFO] Reactor Build Order:
[INFO] 
[INFO] simcn                                                              [pom]
[INFO] simcn: EJB Module                                                  [ejb]
[INFO] simcn: RESTful Module                                              [war]
[INFO] SIMCN - Web Module                                                 [war]
[INFO] simcn: EAR Module                                                  [ear]
[INFO] 
[INFO] --------------------< br.gov.caixa.bsb.simcn:simcn >--------------------
[INFO] Building simcn 2.110.11.7                                          [1/5]
[INFO] --------------------------------[ pom ]---------------------------------
[INFO] 
[INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ simcn ---
[WARNING] Attempt to (de-)serialize anonymous class hudson.maven.reporters.MavenArtifactArchiver$2; see: https://jenkins.io/redirect/serialization-of-anonymous-classes/
[JENKINS] Archiving disabled
[WARNING] Attempt to (de-)serialize anonymous class hudson.maven.reporters.MavenFingerprinter$1; see: https://jenkins.io/redirect/serialization-of-anonymous-classes/
[INFO] 
[INFO] ------------------< br.gov.caixa.bsb.simcn:simcn-ejb >------------------
[INFO] Building simcn: EJB Module 2.110.11.7                              [2/5]
[INFO] --------------------------------[ ejb ]---------------------------------
[INFO] 
[INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ simcn-ejb ---
[INFO] 
[INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ simcn-ejb ---
[INFO] Using 'UTF-8' encoding to copy filtered resources.
[INFO] Copying 9 resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.1:compile (default-compile) @ simcn-ejb ---
[INFO] Changes detected - recompiling the module!
[INFO] Compiling 477 source files to /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-ejb/target/classes
[WARNING] /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-ejb/src/main/java/br/gov/caixa/bsb/simcn/dao/ADao.java: Some input files use unchecked or unsafe operations.
[WARNING] /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-ejb/src/main/java/br/gov/caixa/bsb/simcn/dao/ADao.java: Recompile with -Xlint:unchecked for details.
[INFO] 
[INFO] --- maven-resources-plugin:2.6:testResources (default-testResources) @ simcn-ejb ---
[INFO] Using 'UTF-8' encoding to copy filtered resources.
[INFO] Copying 3 resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.1:testCompile (default-testCompile) @ simcn-ejb ---
[INFO] Changes detected - recompiling the module!
[INFO] Compiling 5 source files to /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-ejb/target/test-classes
[INFO] 
[INFO] --- maven-surefire-plugin:2.12.4:test (default-test) @ simcn-ejb ---
[INFO] Surefire report directory: /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-ejb/target/surefire-reports

-------------------------------------------------------
 T E S T S
-------------------------------------------------------
Running br.gov.caixa.bsb.simcn.service.relatorio.VisaoBalanceteServiceTest
Tests run: 3, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.471 sec
Running br.gov.caixa.bsb.simcn.service.conciliacao.ProcessamentoServiceTest
Tests run: 2, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.052 sec

Results :

Tests run: 5, Failures: 0, Errors: 0, Skipped: 0

[JENKINS] Gravando resultados de teste# Deploying the attached artifact {0}
[WARNING] Attempt to (de-)serialize anonymous class hudson.maven.reporters.SurefireArchiver$2; see: https://jenkins.io/redirect/serialization-of-anonymous-classes/
[INFO] 
[INFO] --- maven-ejb-plugin:2.3:ejb (default-ejb) @ simcn-ejb ---
[INFO] Building EJB simcn-ejb with EJB version 3.2
[INFO] Building jar: /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-ejb/target/simcn-ejb.jar
[JENKINS] Archiving disabled
[INFO] 
[INFO] ------------------< br.gov.caixa.bsb.simcn:simcn-api >------------------
[INFO] Building simcn: RESTful Module 2.110.11.7                          [3/5]
[INFO] --------------------------------[ war ]---------------------------------
[INFO] 
[INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ simcn-api ---
[INFO] 
[INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ simcn-api ---
[INFO] Using 'UTF-8' encoding to copy filtered resources.
[INFO] skip non existing resourceDirectory /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-api/src/main/resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.1:compile (default-compile) @ simcn-api ---
[INFO] Changes detected - recompiling the module!
[INFO] Compiling 56 source files to /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-api/target/classes
[WARNING] /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-api/src/main/java/br/gov/caixa/bsb/simcn/rest/batimento/ParametroBatimentoController.java: Some input files use unchecked or unsafe operations.
[WARNING] /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-api/src/main/java/br/gov/caixa/bsb/simcn/rest/batimento/ParametroBatimentoController.java: Recompile with -Xlint:unchecked for details.
[INFO] 
[INFO] --- maven-resources-plugin:2.6:testResources (default-testResources) @ simcn-api ---
[INFO] Using 'UTF-8' encoding to copy filtered resources.
[INFO] skip non existing resourceDirectory /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-api/src/test/resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.1:testCompile (default-testCompile) @ simcn-api ---
[INFO] Changes detected - recompiling the module!
[INFO] Compiling 6 source files to /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-api/target/test-classes
[INFO] 
[INFO] --- maven-surefire-plugin:2.12.4:test (default-test) @ simcn-api ---
[INFO] Surefire report directory: /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-api/target/surefire-reports

-------------------------------------------------------
 T E S T S
-------------------------------------------------------
Running br.gov.caixa.bsb.simcn.rest.ParametrosGestorControllerTest
Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.378 sec
Running br.gov.caixa.bsb.simcn.service.dominio.ContaContabilServiceTest
Tests run: 4, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.124 sec
Running br.gov.caixa.bsb.simcn.service.dominio.ProdutoServiceTest
Tests run: 4, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.053 sec
Running br.gov.caixa.bsb.simcn.service.dominio.CriticidadeServiceTest
Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.003 sec

Results :

Tests run: 10, Failures: 0, Errors: 0, Skipped: 0

[JENKINS] Gravando resultados de teste# Deploying the attached artifact {0}
[WARNING] Attempt to (de-)serialize anonymous class hudson.maven.reporters.BuildInfoRecorder$1; see: https://jenkins.io/redirect/serialization-of-anonymous-classes/
[INFO] 
[INFO] --- maven-war-plugin:2.2:war (default-war) @ simcn-api ---
[INFO] Packaging webapp
[INFO] Assembling webapp [simcn-api] in [/opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-api/target/simcn-api]
[INFO] Processing war project
[INFO] Copying webapp resources [/opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-api/src/main/webapp]
[INFO] Webapp assembled in [75 msecs]
[INFO] Building war: /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-api/target/simcn-api.war
[INFO] WEB-INF/web.xml already added, skipping
[JENKINS] Archiving disabled
[INFO] 
[INFO] ------------------< br.gov.caixa.bsb.simcn:simcn-web >------------------
[INFO] Building SIMCN - Web Module 2.110.11.7                             [4/5]
[INFO] --------------------------------[ war ]---------------------------------
[INFO] 
[INFO] --- exec-maven-plugin:1.6.0:exec (npm install (clean)) @ simcn-web ---
npm WARN deprecated protractor@6.0.0: We have news to share - Protractor is deprecated and will reach end-of-life by Summer 2023. To learn more and find out about other options please refer to this post on the Angular blog. Thank you for using and contributing to Protractor. https://goo.gle/state-of-e2e-in-angular
npm WARN deprecated @angular/flex-layout@6.0.0-beta.16: This package has been deprecated. Please see https://blog.angular.io/modern-css-in-angular-layouts-4a259dca9127
npm WARN deprecated @angular/http@6.1.10: Package no longer supported. Use @angular/common instead, see https://angular.io/guide/deprecations#angularhttp
npm WARN deprecated core-js@2.6.12: core-js@<3.23.3 is no longer maintained and not recommended for usage due to the number of issues. Because of the V8 engine whims, feature detection in old core-js versions could cause a slowdown up to 100x even if nothing is polyfilled. Some versions have web compatibility issues. Please, upgrade your dependencies to the actual version of core-js.
npm WARN deprecated ini@1.3.5: Please update to ini >=1.3.6 to avoid a prototype pollution issue
npm WARN deprecated chokidar@1.7.0: Chokidar 2 will break on node v14+. Upgrade to chokidar 3 with 15x less dependencies.
npm WARN deprecated @schematics/update@0.8.9: This was an internal-only Angular package up through Angular v11 which is no longer used or maintained. Upgrade Angular to v12+ to remove this dependency.
npm WARN deprecated istanbul@0.4.5: This module is no longer maintained, try this instead:
npm WARN deprecated   npm i nyc
npm WARN deprecated Visit https://istanbul.js.org/integrations for other alternatives.
npm WARN deprecated glob@7.1.3: Glob versions prior to v9 are no longer supported
npm WARN deprecated html-webpack-plugin@3.2.0: 3.x is no longer supported
npm WARN deprecated request@2.88.2: request has been deprecated, see https://github.com/request/request/issues/3142
npm WARN deprecated log4js@4.5.1: 4.x is no longer supported. Please upgrade to 6.x or higher.
npm WARN deprecated fsevents@1.2.13: The v1 package contains DANGEROUS / INSECURE binaries. Upgrade to safe fsevents v2
npm WARN deprecated figgy-pudding@3.5.2: This module is no longer supported.
npm WARN deprecated npm-registry-client@8.6.0: This package is no longer supported.
npm WARN deprecated glob@7.0.6: Glob versions prior to v9 are no longer supported
npm WARN deprecated acorn-dynamic-import@3.0.0: This is probably built in to whatever tool you're using. If you still need it... idk
npm WARN deprecated chokidar@2.1.8: Chokidar 2 does not receive security updates since 2019. Upgrade to chokidar 3 with 15x fewer dependencies
npm WARN deprecated uglify-es@3.3.9: support for ECMAScript is superseded by `uglify-js` as of v3.13.0
npm WARN deprecated tar@2.2.2: This version of tar is no longer supported, and will not receive security updates. Please upgrade asap.
npm WARN deprecated har-validator@5.1.5: this library is no longer supported
npm WARN deprecated uuid@3.4.0: Please upgrade  to version 7 or higher.  Older versions may use Math.random() in certain circumstances, which is known to be problematic.  See https://v8.dev/blog/math-random for details.
npm WARN deprecated date-format@2.1.0: 2.x is no longer supported. Please upgrade to 4.x or higher.
npm WARN deprecated streamroller@1.0.6: 1.x is no longer supported. Please upgrade to 3.x or higher.
npm WARN deprecated node-fetch-npm@2.0.4: This module is not used anymore, npm uses minipass-fetch for its fetch implementation now
npm WARN deprecated source-map-resolve@0.5.3: See https://github.com/lydell/source-map-resolve#deprecated
npm WARN deprecated resolve-url@0.2.1: https://github.com/lydell/resolve-url#deprecated
npm WARN deprecated source-map-url@0.4.1: See https://github.com/lydell/source-map-url#deprecated
npm WARN deprecated urix@0.1.0: Please see https://github.com/lydell/urix#deprecated

> node-sass@4.14.1 install /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-web/angular/node_modules/node-sass
> node scripts/install.js

Cached binary found at /opt/integracao_continua/node_config/.npm/node-sass/4.14.1/linux-x64-64_binding.node

> core-js@2.6.12 postinstall /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-web/angular/node_modules/core-js
> node -e "try{require('./postinstall')}catch(e){}"


> ejs@2.7.4 postinstall /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-web/angular/node_modules/ejs
> node ./postinstall.js

Thank you for installing [35mEJS[0m: built with the [32mJake[0m JavaScript build tool ([32mhttps://jakejs.com/[0m)


> node-sass@4.14.1 postinstall /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-web/angular/node_modules/node-sass
> node scripts/build.js

Binary found at /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-web/angular/node_modules/node-sass/vendor/linux-x64-64/binding.node
Testing binary
Binary is fine
npm notice created a lockfile as package-lock.json. You should commit this file.
npm WARN notsup Unsupported engine for sax@1.6.1: wanted: {"node":">=11.0.0"} (current: {"node":"10.8.0","npm":"6.14.5"})
npm WARN notsup Not compatible with your version of node/npm: sax@1.6.1
npm WARN notsup Unsupported engine for @angular-devkit/build-optimizer@0.1202.18: wanted: {"node":"^12.14.1 || >=14.0.0","npm":"^6.11.0 || ^7.5.6 || >=8.0.0","yarn":">= 1.13.0"} (current: {"node":"10.8.0","npm":"6.14.5"})
npm WARN notsup Not compatible with your version of node/npm: @angular-devkit/build-optimizer@0.1202.18
npm WARN notsup Unsupported engine for karma-cli@1.0.1: wanted: {"node":"0.10 || 0.12 || 4 || 5 || 6"} (current: {"node":"10.8.0","npm":"6.14.5"})
npm WARN notsup Not compatible with your version of node/npm: karma-cli@1.0.1
npm WARN optional SKIPPING OPTIONAL DEPENDENCY: fsevents@^1.2.2 (node_modules/chokidar/node_modules/fsevents):
npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for fsevents@1.2.13: wanted {"os":"darwin","arch":"any"} (current: {"os":"linux","arch":"x64"})
npm WARN optional SKIPPING OPTIONAL DEPENDENCY: fsevents@~2.3.2 (node_modules/watchpack/node_modules/chokidar/node_modules/fsevents):
npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for fsevents@2.3.3: wanted {"os":"darwin","arch":"any"} (current: {"os":"linux","arch":"x64"})
npm WARN optional SKIPPING OPTIONAL DEPENDENCY: fsevents@~2.3.2 (node_modules/karma/node_modules/chokidar/node_modules/fsevents):
npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for fsevents@2.3.3: wanted {"os":"darwin","arch":"any"} (current: {"os":"linux","arch":"x64"})
npm WARN notsup Unsupported engine for selenium-webdriver@4.51.0: wanted: {"node":">= 22.0.0"} (current: {"node":"10.8.0","npm":"6.14.5"})
npm WARN notsup Not compatible with your version of node/npm: selenium-webdriver@4.51.0
npm WARN notsup Unsupported engine for tmp@0.2.7: wanted: {"node":">=14.14"} (current: {"node":"10.8.0","npm":"6.14.5"})
npm WARN notsup Not compatible with your version of node/npm: tmp@0.2.7
npm WARN ngx-mask@9.1.4 requires a peer of @angular/core@^9.1.0 but none is installed. You must install peer dependencies yourself.
npm WARN ngx-mask@9.1.4 requires a peer of @angular/forms@^9.1.0 but none is installed. You must install peer dependencies yourself.
npm WARN ngx-mask@9.1.4 requires a peer of @angular/common@^9.1.0 but none is installed. You must install peer dependencies yourself.
npm WARN ajv-keywords@3.5.2 requires a peer of ajv@^6.9.1 but none is installed. You must install peer dependencies yourself.

added 1340 packages from 1359 contributors in 90.588s

117 packages are looking for funding
  run `npm fund` for details

[INFO] 
[INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ simcn-web ---
[INFO] 
[INFO] --- exec-maven-plugin:1.6.0:exec (npm run clean (clean)) @ simcn-web ---

> frontend-angular6@0.0.1 clean /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-web/angular
> echo not implemented

not implemented
[INFO] 
[INFO] --- exec-maven-plugin:1.6.0:exec (npm config list (validate)) @ simcn-web ---
; cli configs
metrics-registry = "http://binario.caixa:8081/repository/npm-all/"
scope = ""
user-agent = "npm/6.14.5 node/v10.8.0 linux x64 ci/jenkins"

; environment configs
userconfig = "/opt/integracao_continua/jenkins_home/workspace/SIMCN@tmp/config7076553055003758262tmp"

; userconfig /opt/integracao_continua/jenkins_home/workspace/SIMCN@tmp/config7076553055003758262tmp
always-auth = false
no_proxy = "*.caixa"
registry = "http://binario.caixa:8081/repository/npm-all/"
sass_binary_site = "http://binario.caixa:8081/repository/node-sass/"
strict-ssl = false

; globalconfig /opt/integracao_continua/tool_home/node-v10.8.0-linux-x64/etc/npmrc
cache = "/opt/integracao_continua/node_config/.npm"
init-module = "/opt/integracao_continua/node_config/.npm-init.js"
registry = "http://binario.caixa:8081/repository/npm-all/"

; node bin location = /opt/integracao_continua/tool_home/node-v10.8.0-linux-x64/bin/node
; cwd = /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-web/angular
; HOME = /var/lib/jenkins
; "npm config ls -l" to show all defaults.

[INFO] 
[INFO] --- exec-maven-plugin:1.6.0:exec (npm install (initialize)) @ simcn-web ---
npm WARN ajv-keywords@3.5.2 requires a peer of ajv@^6.9.1 but none is installed. You must install peer dependencies yourself.
npm WARN ngx-mask@9.1.4 requires a peer of @angular/core@^9.1.0 but none is installed. You must install peer dependencies yourself.
npm WARN ngx-mask@9.1.4 requires a peer of @angular/forms@^9.1.0 but none is installed. You must install peer dependencies yourself.
npm WARN ngx-mask@9.1.4 requires a peer of @angular/common@^9.1.0 but none is installed. You must install peer dependencies yourself.
npm WARN optional SKIPPING OPTIONAL DEPENDENCY: fsevents@1.2.13 (node_modules/fsevents):
npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for fsevents@1.2.13: wanted {"os":"darwin","arch":"any"} (current: {"os":"linux","arch":"x64"})
npm WARN optional SKIPPING OPTIONAL DEPENDENCY: fsevents@2.3.3 (node_modules/karma/node_modules/fsevents):
npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for fsevents@2.3.3: wanted {"os":"darwin","arch":"any"} (current: {"os":"linux","arch":"x64"})
npm WARN optional SKIPPING OPTIONAL DEPENDENCY: fsevents@2.3.3 (node_modules/watchpack/node_modules/fsevents):
npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for fsevents@2.3.3: wanted {"os":"darwin","arch":"any"} (current: {"os":"linux","arch":"x64"})

up to date in 3.317s

117 packages are looking for funding
  run `npm fund` for details

[INFO] 
[INFO] --- maven-resources-plugin:3.1.0:resources (default-resources) @ simcn-web ---
[INFO] Using 'UTF-8' encoding to copy filtered resources.
[INFO] skip non existing resourceDirectory /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-web/src/main/resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.1:compile (default-compile) @ simcn-web ---
[INFO] No sources to compile
[INFO] 
[INFO] --- exec-maven-plugin:1.6.0:exec (npm run build (compile)) @ simcn-web ---

> frontend-angular6@0.0.1 build /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-web/angular
> ng build --prod --base-href "/simcn-web/"


Date: 2026-10-13T19:06:58.016Z
Hash: 54ce3b6e1b5c852b2609
Time: 40520ms
chunk {7} polyfills.5bd93f69627b492e3a35.js (polyfills) 159 kB [initial] [rendered]
chunk {scripts} scripts.64eb565330cff969e678.js (scripts) 302 kB  [rendered]
chunk {0} 0.dae5add5274fc4bf1eac.js () 15.8 kB  [rendered]
chunk {1} common.25a9aa9c19d1860d187c.js (common) 11.9 kB  [rendered]
chunk {2} 2.a65370f913387d2b8e24.js () 224 kB  [rendered]
chunk {3} runtime.cdef7ee6907fbdc604d7.js (runtime) 2.48 kB [entry] [rendered]
chunk {4} 4.086093f523d822ca2559.js () 41.5 kB  [rendered]
chunk {5} 5.e087271cd8e67bd0c185.js () 38 kB  [rendered]
chunk {6} main.5582a5209d0401e7b5a7.js (main) 4.28 MB [initial] [rendered]
chunk {8} styles.0375438bca06eb84f46d.css (styles) 634 kB [initial] [rendered]
chunk {9} 9.dc6f59e42fe20f920402.js () 1.25 MB  [rendered]
chunk {10} 10.ddad02b6707ea67a4ee4.js () 675 kB  [rendered]
chunk {11} 11.626990c8f18f3075d024.js () 517 kB  [rendered]
chunk {12} 12.113961820d9d387fc114.js () 345 kB  [rendered]
chunk {13} 13.b0f9dad7630ff467efa1.js () 868 kB  [rendered]
[INFO] 
[INFO] --- maven-resources-plugin:3.1.0:copy-resources (default-copy-resources) @ simcn-web ---
[INFO] Using 'UTF-8' encoding to copy filtered resources.
[INFO] Copying 93 resources
[INFO] 
[INFO] --- maven-resources-plugin:3.1.0:testResources (default-testResources) @ simcn-web ---
[INFO] Using 'UTF-8' encoding to copy filtered resources.
[INFO] skip non existing resourceDirectory /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-web/src/test/resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.1:testCompile (default-testCompile) @ simcn-web ---
[INFO] No sources to compile
[INFO] 
[INFO] --- maven-surefire-plugin:2.12.4:test (default-test) @ simcn-web ---
[INFO] No tests to run.
[JENKINS] Gravando resultados de teste# Deploying the attached artifact {0}
[INFO] 
[INFO] --- exec-maven-plugin:1.6.0:exec (npm run test (test)) @ simcn-web ---

> frontend-angular6@0.0.1 test /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-web/angular
> echo not implemented

not implemented
[INFO] 
[INFO] --- maven-war-plugin:2.2:war (default-war) @ simcn-web ---
[INFO] Packaging webapp
[INFO] Assembling webapp [simcn-web] in [/opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-web/target/simcn-web]
[INFO] Processing war project
[INFO] Copying webapp resources [/opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-web/src/main/webapp]
[INFO] Webapp assembled in [2 msecs]
[INFO] Building war: /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-web/target/simcn-web.war
[JENKINS] Archiving disabled
[INFO] 
[INFO] ------------------< br.gov.caixa.bsb.simcn:simcn-ear >------------------
[INFO] Building simcn: EAR Module 2.110.11.7                              [5/5]
[INFO] --------------------------------[ ear ]---------------------------------
[INFO] 
[INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ simcn-ear ---
[INFO] 
[INFO] --- maven-ear-plugin:2.10:generate-application-xml (default-generate-application-xml) @ simcn-ear ---
[INFO] Generating application.xml
[INFO] 
[INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ simcn-ear ---
[INFO] Using 'UTF-8' encoding to copy filtered resources.
[INFO] skip non existing resourceDirectory /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-ear/src/main/resources
[INFO] 
[INFO] --- maven-ear-plugin:2.10:ear (default-ear) @ simcn-ear ---
[INFO] Copying artifact [war:br.gov.caixa.bsb.simcn:simcn-api:2.110.11.7] to [simcn-api.war]
[INFO] Copying artifact [war:br.gov.caixa.bsb.simcn:simcn-web:2.110.11.7] to [simcn-web.war]
[INFO] Copying artifact [ejb:br.gov.caixa.bsb.simcn:simcn-ejb:2.110.11.7] to [simcn-ejb.jar]
[INFO] Copying artifact [jar:org.apache.commons:commons-csv:1.6] to [lib/commons-csv.jar]
[INFO] Copying artifact [jar:commons-beanutils:commons-beanutils:1.6] to [lib/commons-beanutils.jar]
[INFO] Copying artifact [jar:commons-logging:commons-logging:1.0] to [lib/commons-logging.jar]
[INFO] Copying artifact [jar:commons-collections:commons-collections:2.0] to [lib/commons-collections.jar]
[INFO] Copying artifact [jar:org.apache.commons:commons-lang3:3.0.1] to [lib/commons-lang3.jar]
[INFO] Copying artifact [jar:commons-io:commons-io:2.6] to [lib/commons-io.jar]
[INFO] Copying artifact [jar:com.fasterxml.jackson.core:jackson-annotations:2.9.10] to [lib/jackson-annotations.jar]
[INFO] Copying artifact [jar:com.fasterxml.jackson.datatype:jackson-datatype-jsr310:2.9.10] to [lib/jackson-datatype-jsr310.jar]
[INFO] Copying artifact [jar:com.fasterxml.jackson.core:jackson-core:2.9.10] to [lib/jackson-core.jar]
[INFO] Copying artifact [jar:com.fasterxml.jackson.core:jackson-databind:2.9.10] to [lib/jackson-databind.jar]
[INFO] Copying artifact [jar:com.fasterxml.jackson.module:jackson-module-parameter-names:2.9.10] to [lib/jackson-module-parameter-names.jar]
[INFO] Copying artifact [jar:com.fasterxml.jackson.datatype:jackson-datatype-jdk8:2.9.10] to [lib/jackson-datatype-jdk8.jar]
[INFO] Copying artifact [jar:com.fasterxml.jackson.datatype:jackson-datatype-hibernate5:2.8.11] to [lib/jackson-datatype-hibernate5.jar]
[INFO] Copying artifact [jar:javax.transaction:jta:1.1] to [lib/jta.jar]
[INFO] Copying artifact [jar:com.github.fge:json-patch:1.9] to [lib/json-patch.jar]
[INFO] Copying artifact [jar:com.github.fge:jackson-coreutils:1.6] to [lib/jackson-coreutils.jar]
[INFO] Copying artifact [jar:com.github.fge:msg-simple:1.1] to [lib/msg-simple.jar]
[INFO] Copying artifact [jar:com.github.fge:btf:1.2] to [lib/btf.jar]
[INFO] Copying artifact [jar:com.google.guava:guava:16.0.1] to [lib/guava.jar]
[INFO] Copying artifact [jar:com.google.code.findbugs:jsr305:2.0.1] to [lib/jsr305.jar]
[INFO] Copying artifact [jar:com.flipkart.zjsonpatch:zjsonpatch:0.4.7] to [lib/zjsonpatch.jar]
[INFO] Copying artifact [jar:org.apache.commons:commons-collections4:4.2] to [lib/commons-collections4.jar]
[INFO] Copying artifact [jar:org.mybatis:mybatis:3.5.1] to [lib/mybatis.jar]
[INFO] Copying artifact [jar:com.oracle.database.jdbc:ojdbc6:11.2.0.4] to [lib/ojdbc6.jar]
[INFO] Copying artifact [jar:com.oracle.database.jdbc:ucp:11.2.0.4] to [lib/ucp.jar]
[INFO] Copying artifact [jar:com.oracle.database.security:oraclepki:11.2.0.4] to [lib/oraclepki.jar]
[INFO] Copying artifact [jar:com.oracle.database.security:osdt_cert:11.2.0.4] to [lib/osdt_cert.jar]
[INFO] Copying artifact [jar:com.oracle.database.security:osdt_core:11.2.0.4] to [lib/osdt_core.jar]
[INFO] Copying artifact [jar:com.oracle.database.ha:simplefan:11.2.0.4] to [lib/simplefan.jar]
[INFO] Copying artifact [jar:com.oracle.database.ha:ons:11.2.0.4] to [lib/ons.jar]
[INFO] Copying artifact [jar:com.h2database:h2:1.4.199] to [lib/h2.jar]
[INFO] Copying artifact [jar:org.apache.commons:commons-dbcp2:2.6.0] to [lib/commons-dbcp2.jar]
[INFO] Copying artifact [jar:org.apache.commons:commons-pool2:2.6.1] to [lib/commons-pool2.jar]
[INFO] Copying artifact [jar:org.keycloak:keycloak-core:6.0.1] to [lib/keycloak-core.jar]
[INFO] Copying artifact [jar:org.keycloak:keycloak-common:6.0.1] to [lib/keycloak-common.jar]
[INFO] Copying artifact [jar:org.bouncycastle:bcprov-jdk15on:1.60] to [lib/bcprov-jdk15on.jar]
[INFO] Copying artifact [jar:org.bouncycastle:bcpkix-jdk15on:1.60] to [lib/bcpkix-jdk15on.jar]
[INFO] Copying artifact [jar:com.univocity:univocity-parsers:2.8.3] to [lib/univocity-parsers.jar]
[INFO] Copying artifact [jar:org.reflections:reflections:0.9.12] to [lib/reflections.jar]
[INFO] Copying artifact [jar:org.javassist:javassist:3.26.0-GA] to [lib/javassist.jar]
[INFO] Could not find manifest file: /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-ear/target/simcn/META-INF/MANIFEST.MF - Generating one
[INFO] Building jar: /opt/integracao_continua/jenkins_home/workspace/SIMCN/simcn-ear/target/simcn.ear
[JENKINS] Archiving disabled
[JENKINS] Archiving disabled
[JENKINS] Archiving disabled
[JENKINS] Archiving disabled
[JENKINS] Archiving disabled
[JENKINS] Archiving disabled
[INFO] ------------------------------------------------------------------------
[INFO] Reactor Summary:
[INFO] 
[INFO] simcn 2.110.11.7 ................................... SUCCESS [  0.301 s]
[INFO] simcn: EJB Module .................................. SUCCESS [ 15.900 s]
[INFO] simcn: RESTful Module .............................. SUCCESS [  4.910 s]
[INFO] SIMCN - Web Module ................................. SUCCESS [02:20 min]
[INFO] simcn: EAR Module 2.110.11.7 ....................... SUCCESS [  1.590 s]
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time: 02:44 min
[INFO] Finished at: 2026-10-13T16:07:01-03:00
[INFO] ------------------------------------------------------------------------
Aguardando Jenkins terminar de coletar dados
[SIMCN] $ /bin/sh -xe /tmp/jenkins1540837586901245030.sh
channel stopped
+ /opt/integracao_continua/work/jenkins_script_steps/step_deploy_git.sh
Local atual: /opt/integracao_continua/jenkins_home/workspace/SIMCN
********
********
Extensão do Projeto: ear
./simcn-ear/target/simcn.ear
file name.....xxx 
DIR ./simcn-ear/target
yyyyyy ./simcn-ear/target/maven-archiver/pom.properties
basename: falta operando
Try 'basename --help' for more information.
Verificando arquivo  ./simcn-ear/target/maven-archiver/pom.properties
versão do arquivo  2.110.11.7
Implantando sistema: ./simcn-ear/target/simcn.ear no servidor: 10.116.89.0:9999 com o nome: SIMCN e runtime-name:  simcn-2.110.11.7-b2262.ear
Warning! There were errors trying to load extensions. For more details, please, execute 'extension-commands --errors'
Undeploy failed: {"host-failure-descriptions" => {"sbrdeapllx112" => "WFLYCTL0063: Composite operation was rolled back"}}
Publicando arquivo ./simcn-ear/target/simcn.ear
/opt/jboss/jboss-eap/bin/jboss-cli.sh --user=******** --password=******** --connect --controller=10.116.89.0:9999 --command=deploy --server-groups=simcn --name=SIMCN --runtime-name=simcn-2.110.11.7-b2262.ear ./simcn-ear/target/simcn.ear
Warning! There were errors trying to load extensions. For more details, please, execute 'extension-commands --errors'
'SIMCN' already exists in the deployment repository (use --force to replace the existing content in the repository).
Build step 'Executar shell' marked build as failure
Finished: FAILURE
Página gerada: 14/10/2026 10h5min49s BRTREST APIJenkins ver. 2.121.1
