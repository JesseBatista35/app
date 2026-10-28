2026-10-28T12:30:20.6737484Z ##[section]Starting: Run Code Analisis
2026-10-28T12:30:20.6742447Z ==============================================================================
2026-10-28T12:30:20.6742586Z Task         : Bash
2026-10-28T12:30:20.6742648Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-28T12:30:20.6742741Z Version      : 3.227.0
2026-10-28T12:30:20.6742814Z Author       : Microsoft Corporation
2026-10-28T12:30:20.6742894Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-28T12:30:20.6743011Z ==============================================================================
2026-10-28T12:30:20.8232667Z Generating script.
2026-10-28T12:30:20.8246365Z ========================== Starting Command Output ===========================
2026-10-28T12:30:20.8254076Z [command]/usr/bin/bash /opt/ads-agent/_work/_temp/06fade19-736b-406f-b859-b7f3980903ea.sh
2026-10-28T12:30:20.9350529Z sonar-scanner -Dsonar.host.url=http://sonar-esteira.apps.produtos4.caixa -Dsonar.login=ads-sa -Dsonar.password=*** -Dsonar.projectKey=SINCH-web-angular20-intra -Dsonar.projectName=SINCH-web-angular20-intra -Dsonar.projectVersion=1.0.0-snapshot -Dsonar.sources=. -Dproject.settings=NONE -Dsonar.branch.name=atualizacao-angular -Dsonar.sources=src -Dsonar.tests=src -Dsonar.test.inclusions=**/*.spec.ts -Dsonar.exclusions=**/node_modules/**,**/*.spec.ts -Dsonar.javascript.lcov.reportPaths=./coverage/sinch/lcov.info,
2026-10-28T12:30:21.1387844Z INFO: Scanner configuration file: /opt/sonar-scanner/sonar-scanner-4.2.0.1873-linux/conf/sonar-scanner.properties
2026-10-28T12:30:21.1497288Z INFO: Project root configuration file: NONE
2026-10-28T12:30:21.1635612Z INFO: SonarQube Scanner 4.2.0.1873
2026-10-28T12:30:21.1636061Z INFO: Java 11.0.3 AdoptOpenJDK (64-bit)
2026-10-28T12:30:21.1636261Z INFO: Linux 5.18.5-100.fc35.x86_64 amd64
2026-10-28T12:30:21.3452949Z INFO: User cache: /opt/ads-agent/cache-tools/.sonar/cache
2026-10-28T12:30:21.4283033Z INFO: SonarQube server 9.9.5.90363
2026-10-28T12:30:21.4285857Z INFO: Default locale: "pt_BR", source code encoding: "UTF-8"
2026-10-28T12:30:21.8757968Z INFO: Load global settings
2026-10-28T12:30:22.0977706Z INFO: Load global settings (done) | time=223ms
2026-10-28T12:30:22.1109229Z INFO: Server id: C6CBE574-AZHFQ0zM20SUQoMxtCv9
2026-10-28T12:30:22.1175742Z INFO: User cache: /opt/ads-agent/cache-tools/.sonar/cache
2026-10-28T12:30:22.1199837Z INFO: Load/download plugins
2026-10-28T12:30:22.1200010Z INFO: Load plugins index
2026-10-28T12:30:22.2520962Z INFO: Load plugins index (done) | time=131ms
2026-10-28T12:30:22.3019998Z INFO: Load/download plugins (done) | time=182ms
2026-10-28T12:30:22.7650790Z INFO: Process project properties
2026-10-28T12:30:22.7763192Z INFO: Process project properties (done) | time=11ms
2026-10-28T12:30:22.7783066Z INFO: Execute project builders
2026-10-28T12:30:22.7792966Z INFO: Execute project builders (done) | time=1ms
2026-10-28T12:30:22.7830979Z INFO: Project key: SINCH-web-angular20-intra
2026-10-28T12:30:22.7831233Z INFO: Base dir: /opt/ads-agent/_work/71/s
2026-10-28T12:30:22.7831490Z INFO: Working dir: /opt/ads-agent/_work/71/s/.scannerwork
2026-10-28T12:30:22.7903019Z INFO: Load project settings for component key: 'SINCH-web-angular20-intra'
2026-10-28T12:30:22.9145758Z INFO: Load project settings for component key: 'SINCH-web-angular20-intra' (done) | time=118ms
2026-10-28T12:30:23.0307836Z INFO: Load project branches
2026-10-28T12:30:23.1468191Z INFO: Load project branches (done) | time=117ms
2026-10-28T12:30:23.1469935Z INFO: Load branch configuration
2026-10-28T12:30:23.1491947Z INFO: Load branch configuration (done) | time=2ms
2026-10-28T12:30:23.1989257Z INFO: Auto-configuring with CI 'Azure DevOps'
2026-10-28T12:30:23.2050819Z INFO: Load quality profiles
2026-10-28T12:30:23.3384791Z INFO: Load quality profiles (done) | time=138ms
2026-10-28T12:30:23.3480825Z INFO: Load active rules
2026-10-28T12:30:26.4390458Z INFO: Load active rules (done) | time=3092ms
2026-10-28T12:30:26.4400672Z INFO: Load analysis cache
2026-10-28T12:30:26.6163526Z INFO: Load analysis cache | time=169ms
2026-10-28T12:30:26.6310827Z INFO: Branch name: atualizacao-angular
2026-10-28T12:30:26.6393103Z WARN: Property 'sonar.password' is deprecated. It will not be supported in the future. Please instead use the 'sonar.login' parameter with a token.
2026-10-28T12:30:26.6501638Z INFO: Load project repositories
2026-10-28T12:30:26.7825700Z INFO: Load project repositories (done) | time=133ms
2026-10-28T12:30:26.8152299Z INFO: Indexing files...
2026-10-28T12:30:26.8218018Z INFO: Project configuration:
2026-10-28T12:30:26.8218297Z INFO:   Excluded sources: **/node_modules/**, **/dist/**, **/coverage/**, **/junit/**, **/reports/**, **/build/**, **/target/**, **/Dockerfile, **/node_modules/**, **/*.spec.ts, **/*.spec.ts
2026-10-28T12:30:26.8218481Z INFO:   Included tests: **/*.spec.ts
2026-10-28T12:30:26.8219180Z INFO:   Excluded sources for coverage: **/*.xml, **/repository/**, **/dto/**, **/entity/**, **/model/**, **/dao/**, **/*DAO.java, **/test/**, **/*Test.java, **/*.spec.ts, **/*setup-jest.ts, **/*Dto.java, **/*DTO.java, **/*Dao.java, **/*Repository.java
2026-10-28T12:30:26.8219723Z INFO:   Excluded sources for duplication: **/**/environment*.ts, **/**/environment*.prod.ts
2026-10-28T12:30:28.0449750Z INFO: 1492 files indexed
2026-10-28T12:30:28.0469796Z INFO: 1497 files ignored because of inclusion/exclusion patterns
2026-10-28T12:30:28.0470011Z INFO: 0 files ignored because of scm ignore settings
2026-10-28T12:30:28.0482712Z INFO: Quality profile for css: Sonar way
2026-10-28T12:30:28.0484912Z INFO: Quality profile for ts: Sonar way
2026-10-28T12:30:28.0486700Z INFO: Quality profile for web: HTML ACESSIBILIDADE
2026-10-28T12:30:28.0487670Z INFO: ------------- Run sensors on module SINCH-web-angular20-intra
2026-10-28T12:30:28.1267782Z INFO: Load metrics repository
2026-10-28T12:30:28.2400235Z INFO: Load metrics repository (done) | time=113ms
2026-10-28T12:30:29.2807714Z INFO: Sensor JaCoCo XML Report Importer [jacoco]
2026-10-28T12:30:29.2812718Z INFO: 'sonar.coverage.jacoco.xmlReportPaths' is not defined. Using default locations: target/site/jacoco/jacoco.xml,target/site/jacoco-it/jacoco.xml,build/reports/jacoco/test/jacocoTestReport.xml
2026-10-28T12:30:29.2816077Z INFO: No report imported, no coverage information will be imported by JaCoCo XML Report Importer
2026-10-28T12:30:29.2816720Z INFO: Sensor JaCoCo XML Report Importer [jacoco] (done) | time=2ms
2026-10-28T12:30:29.2816921Z INFO: Sensor TypeScript analysis [javascript]
2026-10-28T12:30:32.8172828Z WARN: Node.js version 22 is not recommended, you might experience issues. Please use a recommended version of Node.js [16, 18]
2026-10-28T12:30:32.8888257Z INFO: Found 2 tsconfig.json file(s): [/opt/ads-agent/_work/71/s/tsconfig.json, /opt/ads-agent/_work/71/s/e2e/tsconfig.json]
2026-10-28T12:30:32.8888672Z INFO: Creating TypeScript program
2026-10-28T12:30:32.8893997Z INFO: TypeScript configuration file /opt/ads-agent/_work/71/s/tsconfig.json
2026-10-28T12:30:32.8927119Z INFO: 1028 source files to be analyzed
2026-10-28T12:30:34.2360623Z INFO: Creating TypeScript program (done) | time=1347ms
2026-10-28T12:30:34.2360836Z INFO: Starting analysis with current program
2026-10-28T12:30:42.8985659Z INFO: 190/1028 files analyzed, current file: /opt/ads-agent/_work/71/s/src/app/modules/empreendimento/buscar-empreendimento/buscar-empreendimento.component.ts
2026-10-28T12:30:52.8987719Z INFO: 542/1028 files analyzed, current file: /opt/ads-agent/_work/71/s/src/app/modules/lista-publicacao/buscar-lista/buscar-lista.component.ts
2026-10-28T12:30:57.0853279Z INFO: Analyzed 1028 file(s) with current program
2026-10-28T12:30:57.0864053Z INFO: Creating TypeScript program
2026-10-28T12:30:57.0865646Z INFO: TypeScript configuration file /opt/ads-agent/_work/71/s/e2e/tsconfig.json
2026-10-28T12:30:57.3121675Z INFO: Creating TypeScript program (done) | time=225ms
2026-10-28T12:30:57.3124228Z INFO: Starting analysis with current program
2026-10-28T12:30:57.3124485Z INFO: Analyzed 0 file(s) with current program
2026-10-28T12:30:57.3147673Z INFO: 1028/1028 source files have been analyzed
2026-10-28T12:30:57.3150004Z INFO: Hit the cache for 0 out of 1028
2026-10-28T12:30:57.3163065Z INFO: Miss the cache for 1028 out of 1028: ANALYSIS_MODE_INELIGIBLE [1028/1028]
2026-10-28T12:30:57.3163604Z INFO: Sensor TypeScript analysis [javascript] (done) | time=28035ms
2026-10-28T12:30:57.3163802Z INFO: Sensor CSS Rules [javascript]
2026-10-28T12:30:57.3204570Z INFO: 430 source files to be analyzed
2026-10-28T12:30:59.3273762Z INFO: 430/430 source files have been analyzed
2026-10-28T12:30:59.3274024Z INFO: Hit the cache for 0 out of 0
2026-10-28T12:30:59.3276798Z INFO: Miss the cache for 0 out of 0
2026-10-28T12:30:59.3309690Z INFO: Sensor CSS Rules [javascript] (done) | time=2010ms
2026-10-28T12:30:59.3309894Z INFO: Sensor JavaScript/TypeScript Coverage [javascript]
2026-10-28T12:30:59.3310304Z INFO: Analysing [/opt/ads-agent/_work/71/s/./coverage/sinch/lcov.info]
2026-10-28T12:30:59.3909795Z INFO: Sensor JavaScript/TypeScript Coverage [javascript] (done) | time=64ms
2026-10-28T12:30:59.3910086Z INFO: Sensor CSS Metrics [javascript]
2026-10-28T12:30:59.4957125Z INFO: Sensor CSS Metrics [javascript] (done) | time=105ms
2026-10-28T12:30:59.4957346Z INFO: Sensor C# Project Type Information [csharp]
2026-10-28T12:30:59.4966553Z INFO: Sensor C# Project Type Information [csharp] (done) | time=1ms
2026-10-28T12:30:59.4966836Z INFO: Sensor C# Analysis Log [csharp]
2026-10-28T12:30:59.5063099Z INFO: Sensor C# Analysis Log [csharp] (done) | time=9ms
2026-10-28T12:30:59.5063354Z INFO: Sensor C# Properties [csharp]
2026-10-28T12:30:59.5063597Z INFO: Sensor C# Properties [csharp] (done) | time=0ms
2026-10-28T12:30:59.5063781Z INFO: Sensor HTML [web]
2026-10-28T12:31:00.3472986Z INFO: Sensor HTML [web] (done) | time=840ms
2026-10-28T12:31:00.3473190Z INFO: Sensor TextAndSecretsSensor [text]
2026-10-28T12:31:00.3543149Z INFO: 1458 source files to be analyzed
2026-10-28T12:31:01.0436913Z INFO: 1458/1458 source files have been analyzed
2026-10-28T12:31:01.0437192Z INFO: Sensor TextAndSecretsSensor [text] (done) | time=697ms
2026-10-28T12:31:01.0437560Z INFO: Sensor VB.NET Project Type Information [vbnet]
2026-10-28T12:31:01.0447053Z INFO: Sensor VB.NET Project Type Information [vbnet] (done) | time=1ms
2026-10-28T12:31:01.0447213Z INFO: Sensor VB.NET Analysis Log [vbnet]
2026-10-28T12:31:01.0542323Z INFO: Sensor VB.NET Analysis Log [vbnet] (done) | time=9ms
2026-10-28T12:31:01.0542592Z INFO: Sensor VB.NET Properties [vbnet]
2026-10-28T12:31:01.0542741Z INFO: Sensor VB.NET Properties [vbnet] (done) | time=0ms
2026-10-28T12:31:01.0543247Z INFO: Sensor com.github.mc1arke.sonarqube.plugin.scanner.ScannerPullRequestPropertySensor
2026-10-28T12:31:01.0548400Z INFO: Sensor com.github.mc1arke.sonarqube.plugin.scanner.ScannerPullRequestPropertySensor (done) | time=0ms
2026-10-28T12:31:01.0548928Z INFO: Sensor IaC Docker Sensor [iac]
2026-10-28T12:31:01.0609030Z INFO: 0 source files to be analyzed
2026-10-28T12:31:01.1002763Z INFO: 0/0 source files have been analyzed
2026-10-28T12:31:01.1002978Z INFO: Sensor IaC Docker Sensor [iac] (done) | time=45ms
2026-10-28T12:31:01.1043743Z INFO: ------------- Run sensors on project
2026-10-28T12:31:01.1384506Z INFO: Sensor Analysis Warnings import [csharp]
2026-10-28T12:31:01.1385883Z INFO: Sensor Analysis Warnings import [csharp] (done) | time=1ms
2026-10-28T12:31:01.1386074Z INFO: Sensor Zero Coverage Sensor
2026-10-28T12:31:01.1518792Z INFO: Sensor Zero Coverage Sensor (done) | time=13ms
2026-10-28T12:31:01.2655529Z INFO: CPD Executor 158 files had no CPD blocks
2026-10-28T12:31:01.2655783Z INFO: CPD Executor Calculating CPD for 678 files
2026-10-28T12:31:01.5219952Z INFO: CPD Executor CPD calculation finished (done) | time=256ms
2026-10-28T12:31:01.6900677Z INFO: Load New Code definition
2026-10-28T12:31:01.8221846Z INFO: Load New Code definition (done) | time=132ms
2026-10-28T12:31:01.8834764Z INFO: Analysis report generated in 301ms, dir size=7.5 MB
2026-10-28T12:31:03.0481566Z INFO: Analysis report compressed in 1164ms, zip size=4.6 MB
2026-10-28T12:31:03.4126752Z INFO: Analysis report uploaded in 364ms
2026-10-28T12:31:03.4138552Z INFO: ANALYSIS SUCCESSFUL, you can find the results at: https://sonar-esteira.apps.produtos4.caixa/dashboard?id=SINCH-web-angular20-intra&branch=atualizacao-angular
2026-10-28T12:31:03.4138920Z INFO: Note that you will be able to access the updated dashboard once the server has processed the submitted analysis report
2026-10-28T12:31:03.4139206Z INFO: More about the report processing at https://sonar-esteira.apps.produtos4.caixa/api/ce/task?id=AaGCfhRuPmqzl3Vc6sZr
2026-10-28T12:31:04.3125673Z INFO: Analysis total time: 41.910 s
2026-10-28T12:31:04.3147455Z INFO: ------------------------------------------------------------------------
2026-10-28T12:31:04.3147641Z INFO: EXECUTION SUCCESS
2026-10-28T12:31:04.3147840Z INFO: ------------------------------------------------------------------------
2026-10-28T12:31:04.3147979Z INFO: Total time: 43.178s
2026-10-28T12:31:04.3905590Z INFO: Final Memory: 19M/136M
2026-10-28T12:31:04.3906069Z INFO: ------------------------------------------------------------------------
2026-10-28T12:31:04.7473826Z ##[section]Finishing: Run Code Analisis



Skip to main content
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
October 28, 2026 at 9:30 AM
Version 1.0.0-snapshot

Overview
Issues
Security Hotspots
Measures
Code
Activity
Project Information
To benefit from more of SonarQube's features, ask a project administrator to set up DevOps platform integration.

Quality Gate Status
Passed
All conditions passed.
The quality gate used by this project does not comply with Clean as You Code.
Fixing this quality gate will help you achieve a Clean Code state.

Learn why
Measures

New Code
From last 409 days

Overall Code
0
New Bugs
Reliability
A
0
New Vulnerabilities
Security
A
0
New Security Hotspots
Reviewed
Security Review
A
1h 26min
Added Debt
27
New Code Smells
Maintainability
A
97.5%
Coverage on 659 New Lines to cover
0.0%
Duplications on 6k New Lines
Activity
Choose graph type
Issues
Bugs
Code Smells
Vulnerabilities
new code
0
200
400
600
800
1k
Thu 22
Fri 23
Sat 24
Oct 25
Mon 26
Tue 27
Activity
October 28, 2026 at 9:30 AM
1.0.0-snapshot
Quality Gate: Passed
October 22, 2026 at 5:26 PM
1.0.4-SNAPSHOT
October 21, 2026 at 3:52 PM
Quality Gate: Failed
SonarQube™ technology is powered by SonarSource SA
Community Editionv9.9.5 (build 90363)NO LONGER ACTIVELGPL v3CommunityDocumentationPluginsWeb API


passou



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
October 28, 2026 at 9:30 AM
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
Filters

Issues in new code
Type

Bug
58

Vulnerability
0

Code Smell
831
Severity

Blocker
0

Minor
291

Critical
0

Info
7

Major
591
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
1 / 889issues
9d 5h effort
List of issues
src/app/app-routing.module.ts
Remove this unused import of 'ConformidadeContratacaoModule'.

4 months ago
L5

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/app/app.component.scss
Unexpected empty source

6 days ago
L1

Code Smell

Major

Open

Not assigned
1min effort

Comment

No tags
src/app/app.module.ts
'@angular/common' import is duplicated.

4 months ago
L35

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
1min effort

Comment

es2015
Remove this commented out code.

4 months ago
L38

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
src/app/interceptors/blob-error-http.interceptor.ts
'throwError' is deprecated. Support for passing an error value will be removed in v8. Instead, pass a factory function to `throwError(() => new Error('test'))`. This is because it will create the error at the moment it should be created and capture a more appropriate stack trace. If for some reason you need to create the error ahead of time, you can still do that: `const err = new Error('test'); throwError(() => err);`.

4 months ago
L49

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
15min effort

Comment

cwe, obsolete
src/app/interceptors/error.interceptor.ts
Remove this unused import of 'HttpErrorResponse'.

4 months ago
L1

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
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
src/app/interceptors/timeout.interceptor.ts
Remove this useless assignment to variable "reqUrl".

4 months ago
L26

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
15min effort

Comment

cwe, unused
Remove this useless assignment to variable "totalTimer".

4 months ago
L36

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
15min effort

Comment

cwe, unused
This always evaluates to truthy. Consider refactoring this code.

4 months ago
L37

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

cwe, redundant, suspicious
Remove this useless assignment to variable "rspStatus".

4 months ago
L37

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
15min effort

Comment

cwe, unused
Remove this commented out code.

4 months ago
L38

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
Remove this commented out code.

4 months ago
L45

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
'throwError' is deprecated. Support for passing an error value will be removed in v8. Instead, pass a factory function to `throwError(() => new Error('test'))`. This is because it will create the error at the moment it should be created and capture a more appropriate stack trace. If for some reason you need to create the error ahead of time, you can still do that: `const err = new Error('test'); throwError(() => err);`.

4 months ago
L46

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
15min effort

Comment

cwe, obsolete
'throwError' is deprecated. Support for passing an error value will be removed in v8. Instead, pass a factory function to `throwError(() => new Error('test'))`. This is because it will create the error at the moment it should be created and capture a more appropriate stack trace. If for some reason you need to create the error ahead of time, you can still do that: `const err = new Error('test'); throwError(() => err);`.

4 months ago
L51

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
15min effort

Comment

cwe, obsolete
Remove this commented out code.

4 months ago
L54

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
src/.../lib/nch-categoria-documento/nch-categoria-documento.component.html
Remove this commented out code.

4 months ago
L14

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
src/.../lib/nch-categoria-documento/nch-categoria-documento.component.scss
Unexpected empty source

6 days ago
L1

Code Smell

Major

Open

Not assigned
1min effort

Comment

No tags
src/app/lib/nch-checkbox/nch-checkbox.component.scss
Unexpected empty source

6 days ago
L1

Code Smell

Major

Open

Not assigned
1min effort

Comment

No tags
src/.../nch-criterio-lista-indicacao/nch-criterio-lista-indicacao.component.scss
Unexpected empty source

6 days ago
L1

Code Smell

Major

Open

Not assigned
1min effort

Comment

No tags
src/.../nch-criterio-lista-indicacao/nch-criterio-lista-indicacao.component.ts
Remove this commented out code.

4 months ago
L84

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
src/.../nch-documento-lista-indicacao/nch-documento-lista-indicacao.component.scss
Unexpected empty source

6 days ago
L1

Code Smell

Major

Open

Not assigned
1min effort

Comment

No tags
src/.../lib/nch-header-lista-indicacao/nch-header-lista-indicacao.component.scss
Unexpected empty source

6 days ago
L1

Code Smell

Major

Open

Not assigned
1min effort

Comment

No tags
src/app/lib/nch-span/nch-span.component.scss
Unexpected empty source

6 days ago
L1

Code Smell

Major

Open

Not assigned
1min effort

Comment

No tags
src/.../models/contrato-beneficiario/contrato-beneficiario.ts
Remove this unused import of 'OrigemRecurso'.

4 months ago
L1

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/.../models/demanda-empreendimento/demanda-empreendimento.ts
Remove this unused import of 'HttpClient'.

4 months ago
L2

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/app/models/empreendimento/empreendimento.ts
Remove this unused import of 'Municipio'.

4 months ago
L8

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/app/models/listaPublicacao/lista-publicacao.ts
Replace this "String" wrapper object with primitive type "string".

6 days ago
L10

Code Smell

Minor

Open

Not assigned
1min effort

Comment

pitfall
src/.../models/pesquisa-bolsa-familia/solicitacao-pesquisa-bolsa-familia.ts
Replace this "String" wrapper object with primitive type "string".

4 months ago
L19

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
1min effort

Comment

pitfall
src/app/models/relatorio/relatorio-table-data.ts
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L24

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
Remove this commented out code.

4 months ago
L32

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
src/app/models/remessa-indicacao/remessa-indicacao.ts
Remove this unused import of 'Municipio'.

4 months ago
L1

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
Remove this unused import of 'RelatorioDemanda'.

4 months ago
L3

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
Remove this unused import of 'EntePublico'.

4 months ago
L4

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
Remove this unused import of 'Unidade'.

4 months ago
L8

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
Remove this unused import of 'MensagemErro'.

4 months ago
L13

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
Remove this commented out code.

4 months ago
L38

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
src/app/models/tarifa/tarifa-pesquisa.ts
Remove this unused import of 'Modalidade'.

4 months ago
L1

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
Remove this commented out code.

4 months ago
L7

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
src/app/models/tipo-lista-indicacao.ts
Remove this unused import of 'ModalidadeProgramaService'.

4 months ago
L1

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
src/app/modules/abstract-component.ts
Remove this commented out code.

4 months ago
L39

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L56

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
Expected a `for-of` loop instead of a `for` loop with this simple iteration.

4 months ago
L144

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

clumsy
This branch's code block is the same as the block for the branch on line 139.

4 months ago
L143

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

design, suspicious
'data' is assigned to itself.

4 months ago
L204

Bug

Major

Open

FABRICIO FERNANDES FREITAS
3min effort

Comment

No tags
This case's code block is the same as the block for the case on line 240.

4 months ago
L255

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

design, suspicious
Remove this commented out code.

4 months ago
L316

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
Remove this useless assignment to variable "arqType".

4 months ago
L322

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
15min effort

Comment

cwe, unused
Introduce a new variable or use its initial value before reassigning "arqType".

4 months ago
L322

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
Remove this useless assignment to variable "extension".

4 months ago
L323

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
15min effort

Comment

cwe, unused
Introduce a new variable or use its initial value before reassigning "extension".

4 months ago
L323

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
src/app/modules/almo/buscar-almo/buscar-almo.component.scss
Unexpected empty source

6 days ago
L1

Code Smell

Major

Open

Not assigned
1min effort

Comment

No tags
src/app/modules/almo/buscar-almo/buscar-almo.component.ts
Remove this commented out code.

4 months ago
L110

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
src/app/modules/almo/detalhe-almo/detalhe-almo.component.scss
Unexpected empty source

6 days ago
L1

Code Smell

Major

Open

Not assigned
1min effort

Comment

No tags
src/app/modules/almo/salvar-almo/salvar-almo.component.scss
Unexpected empty source

6 days ago
L1

Code Smell

Major

Open

Not assigned
1min effort

Comment

No tags
src/app/modules/almo/salvar-almo/salvar-almo.component.ts
Remove this useless assignment to variable "origem".

6 days ago
L167

Code Smell

Major

Open

Not assigned
15min effort

Comment

cwe, unused
Remove this useless assignment to variable "programa".

6 days ago
L168

Code Smell

Major

Open

Not assigned
15min effort

Comment

cwe, unused
Remove this commented out code.

6 days ago
L226

Code Smell

Major

Open

Not assigned
5min effort

Comment

unused
Remove this commented out code.

4 months ago
L372

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
src/.../buscar-bolsa-familia/buscar-bolsa-familia.component.html
Remove this commented out code.

4 months ago
L53

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
Remove this commented out code.

4 months ago
L55

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
Remove this commented out code.

4 months ago
L88

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
src/.../buscar-bolsa-familia/buscar-bolsa-familia.component.ts
Remove this commented out code.

4 months ago
L208

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
Remove this commented out code.

4 months ago
L215

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
Remove this useless assignment to variable "tableSize".

4 months ago
L258

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
15min effort

Comment

cwe, unused
src/.../detalhar-busca-bolsa-familia/detalhar-busca-bolsa-familia.component.scss
Unexpected empty source

6 days ago
L1

Code Smell

Major

Open

Not assigned
1min effort

Comment

No tags
src/.../detalhar-busca-bolsa-familia/detalhar-busca-bolsa-familia.component.ts
Remove this commented out code.

4 months ago
L60

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
src/.../importar-lote-bolsa-familia/importar-lote-bolsa-familia.component.html
Remove this commented out code.

4 months ago
L140

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
Remove this commented out code.

4 months ago
L175

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
Remove this commented out code.

4 months ago
L203

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
src/.../importar-lote-bolsa-familia/importar-lote-bolsa-familia.component.scss
Unexpected empty source

6 days ago
L1

Code Smell

Major

Open

Not assigned
1min effort

Comment

No tags
src/.../importar-lote-bolsa-familia/importar-lote-bolsa-familia.component.ts
Remove this unused import of 'FormArray'.

4 months ago
L10

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
Remove this redundant jump.

4 months ago
L225

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
1min effort

Comment

clumsy, redundant
Expected a `for-of` loop instead of a `for` loop with this simple iteration.

4 months ago
L239

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

clumsy
src/.../incluir-busca-bolsa-familia/incluir-busca-bolsa-familia.component.scss
Unexpected empty source

6 days ago
L1

Code Smell

Major

Open

Not assigned
1min effort

Comment

No tags
src/.../incluir-busca-bolsa-familia/incluir-busca-bolsa-familia.component.ts
Remove this commented out code.

4 months ago
L83

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
src/.../buscar-conformidade-contratacao.component.html
Remove this commented out code.

4 months ago
L60

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
src/.../buscar-conformidade-contratacao.component.scss
Unexpected empty source

6 days ago
L1

Code Smell

Major

Open

Not assigned
1min effort

Comment

No tags
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
Remove this unused import of 'catchError'.

4 months ago
L11

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
Remove this unused import of 'of'.

4 months ago
L12

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
2min effort

Comment

es2015, unused
Remove this commented out code.

4 months ago
L121

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
src/.../buscar-pessoa-conformidade/buscar-pessoa-conformidade.component.scss
Unexpected empty source

6 days ago
L1

Code Smell

Major

Open

Not assigned
1min effort

Comment

No tags
src/.../buscar-pessoa-conformidade/buscar-pessoa-conformidade.component.ts
Remove this commented out code.

4 months ago
L75

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
src/.../conformidade-contratacao/conformidade-contratacao.component.html
Remove this deprecated "summary" attribute.

4 months ago
L293

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

html5, obsolete
Remove this commented out code.

4 months ago
L1245

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
Remove this commented out code.

4 months ago
L1335

Code Smell

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

unused
src/.../conformidade-contratacao/conformidade-contratacao.component.ts
Rename interface "pcdPlayloadType" to match the regular expression ^[A-Z][a-zA-Z0-9]*$.

4 months ago
L24

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

convention
Rename interface "tipoMelhoriaNecessidadeEspecialType" to match the regular expression ^[A-Z][a-zA-Z0-9]*$.

4 months ago
L29

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

convention
Rename interface "telefonesType" to match the regular expression ^[A-Z][a-zA-Z0-9]*$.

4 months ago
L33

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

convention
Rename interface "enderecoType" to match the regular expression ^[A-Z][a-zA-Z0-9]*$.

4 months ago
L38

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

convention
Rename interface "escolaridadeType" to match the regular expression ^[A-Z][a-zA-Z0-9]*$.

4 months ago
L53

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

convention
Rename interface "participanteType" to match the regular expression ^[A-Z][a-zA-Z0-9]*$.

4 months ago
L58

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

convention
Rename interface "procuracaoType" to match the regular expression ^[A-Z][a-zA-Z0-9]*$.

4 months ago
L88

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

convention
Rename interface "papelParticipanteConformidadeType" to match the regular expression ^[A-Z][a-zA-Z0-9]*$.

4 months ago
L98

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

convention
Rename interface "nivelInstrucaoType" to match the regular expression ^[A-Z][a-zA-Z0-9]*$.

4 months ago
L103

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

convention
Rename interface "modalidadeContratoType" to match the regular expression ^[A-Z][a-zA-Z0-9]*$.

4 months ago
L108

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

convention
Rename interface "pcdType" to match the regular expression ^[A-Z][a-zA-Z0-9]*$.

4 months ago
L113

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

convention
Rename interface "tipoDocumentoType" to match the regular expression ^[A-Z][a-zA-Z0-9]*$.

4 months ago
L118

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

convention
Rename interface "estadoCivilType" to match the regular expression ^[A-Z][a-zA-Z0-9]*$.

4 months ago
L123

Code Smell

Minor

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

convention
100 of 889 shownShow More
SonarQube™ technology is powered by SonarSource SA
Community Editionv9.9.5 (build 90363)NO LONGER ACTIVELGPL v3CommunityDocumentationPluginsWeb API

build subiu

qual nome que eu coloco nesse bash pra ningue mapagar
