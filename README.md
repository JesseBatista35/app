
Publish Quality Gate Result

View raw log

Starting: Publish Quality Gate Result
==============================================================================
Task         : Bash
Description  : Run a Bash script on macOS, Linux, or Windows
Version      : 3.227.0
Author       : Microsoft Corporation
Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
==============================================================================
Generating script.
========================== Starting Command Output ===========================
/usr/bin/bash /opt/ads-agent/_work/_temp/dbf5134d-a6b3-4694-8910-01dece257057.sh
QG Script --> Using SonarQube instance http://sonar-esteira.apps.produtos4.caixa
QG Script --> Using SonarQube access login ads-sa
QG Script --> Using task id of AaGCbfknPmqzl3Vc6sZS
QG Script --> Status of SonarQube task is PENDING
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is SUCCESS
QG Script --> Using analysis id of AaGCbgYFFkwt0Lh6bnSA
QG Script --> Quality Gate status is ERROR
##[error]QG Script --> Ocorrência prevista na TE102 - Não atendimento aos critérios de qualidade
##[error]Bash exited with code '1'.
Finishing: Publish Quality Gate Result


QUEBROU AQUI

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
October 28, 2026 at 9:12 AM
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
Failed
1 conditions failed
The quality gate used by this project does not comply with Clean as You Code.
Fixing this quality gate will help you achieve a Clean Code state.

Learn why
1 condition(s) failed on new code
0.0%
Coverage on New Codeis less than 80.0%
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
0.0%
Coverage on 567 New Lines to cover
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
October 28, 2026 at 9:12 AM
1.0.0-snapshot
October 22, 2026 at 5:26 PM
1.0.4-SNAPSHOT
October 21, 2026 at 3:52 PM
Quality Gate: Failed
SonarQube™ technology is powered by SonarSource SA
Community Editionv9.9.5 (build 90363)NO LONGER ACTIVELGPL v3CommunityDocumentationPluginsWeb API




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
Bug
Clear

Bug
58

Vulnerability
0

Code Smell
831
Press Ctrl to add to selection
Severity

Blocker
0

Minor
24

Critical
0

Info
0

Major
34
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
1 / 58issues
5h 58min effort
List of issues
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
src/app/modules/abstract-component.ts
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
src/.../conformidade-contratacao/conformidade-contratacao.component.ts
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L641

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L651

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L661

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L671

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L681

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L690

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
src/.../detalhe-conversao-municipio/detalhe-conversao-municipio.component.html
Surround this <li> item tag by a <ul> or <ol> container one.

4 months ago
L17

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

No tags
src/.../detalhar-destinatario-mensagem/detalhar-destinatario-mensagem.component.html
Surround this <li> item tag by a <ul> or <ol> container one.

4 months ago
L15

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

No tags
Surround this <li> item tag by a <ul> or <ol> container one.

4 months ago
L195

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

No tags
src/.../detalhar-destinatario-mensagem/detalhar-destinatario-mensagem.component.ts
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L108

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
src/.../detalhar-funcionalidade-destinatario-mensagem.component.html
Surround this <li> item tag by a <ul> or <ol> container one.

4 months ago
L15

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

No tags
Surround this <li> item tag by a <ul> or <ol> container one.

4 months ago
L206

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

No tags
src/.../visualizar-dossie-participante/visualizar-dossie-participante.component.html
Add a "title" attribute to this <iframe> tag.

4 months ago
L189

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

accessibility
Add a "title" attribute to this <iframe> tag.

4 months ago
L197

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

accessibility
src/.../detalhe-empreendimento/detalhe-empreendimento.component.html
Surround this <li> item tag by a <ul> or <ol> container one.

4 months ago
L643

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

No tags
Surround this <li> item tag by a <ul> or <ol> container one.

4 months ago
L653

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

No tags
Surround this <li> item tag by a <ul> or <ol> container one.

4 months ago
L663

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

No tags
src/.../detalhar-ente-publico/detalhar-ente-publico.component.html
Surround this <li> item tag by a <ul> or <ol> container one.

4 months ago
L15

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

No tags
Surround this <li> item tag by a <ul> or <ol> container one.

4 months ago
L129

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

No tags
src/.../salvar-ente-publico/salvar-ente-publico.component.ts
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L121

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
src/.../detalhar-funcionalidade/detalhar-funcionalidade.component.html
Surround this <li> item tag by a <ul> or <ol> container one.

4 months ago
L15

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

No tags
Surround this <li> item tag by a <ul> or <ol> container one.

4 months ago
L71

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

No tags
src/.../detalhar-grupo-familiar/detalhar-grupo-familiar.component.ts
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L184

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
src/.../detalhar-indicao-pessoa-indicado.component.ts
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L147

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
src/.../detalhar-indicao-pessoa-parametro.component.ts
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L161

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
src/.../detalhar-limite-renda-empreendimento.component.ts
Unreachable code.

4 months ago
L158

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

cwe, unused
src/.../configurar-criterio-analise/configurar-criterio-analise.component.ts
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L252

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
src/.../alterar-grupo-tarifa-modal/alterar-grupo-tarifa-modal.component.ts
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L87

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
src/.../detalhar-periodicidade-execucao-rotina.component.html
Surround this <li> item tag by a <ul> or <ol> container one.

4 months ago
L15

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

No tags
Surround this <li> item tag by a <ul> or <ol> container one.

4 months ago
L75

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

No tags
src/.../detalhe-programa-habitacional/detalhe-programa-habitacional.component.html
Surround this <li> item tag by a <ul> or <ol> container one.

4 months ago
L168

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

No tags
src/.../detalhar-configuracao-comunicacao-programa.component.ts
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L169

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
src/.../programa/detalhar-programa/detalhar-programa.component.ts
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L127

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
src/.../buscar-rel-pesquisa-sob-demanda.component.ts
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L87

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
src/.../repesquisa/incluir-repesquisa/incluir-repesquisa.component.ts
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L96

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
src/.../modules/rotina/detalhar-rotina/detalhar-rotina.component.html
Surround this <li> item tag by a <ul> or <ol> container one.

4 months ago
L15

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

No tags
Surround this <li> item tag by a <ul> or <ol> container one.

4 months ago
L95

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

No tags
src/.../relatorio-tarifa/relatorio-tarifa.component.ts
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L153

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
src/.../detalhe-tomador-empreendimento/detalhe-tomador-empreendimento.component.html
Surround this <li> item tag by a <ul> or <ol> container one.

4 months ago
L15

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

No tags
Surround this <li> item tag by a <ul> or <ol> container one.

4 months ago
L82

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

No tags
src/.../components/grupo-familiar/grupo-familiar.component.ts
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L152

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L301

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
src/app/shared/components/input/input.component.ts
'this.partentForm' is assigned to itself.

4 months ago
L154

Bug

Major

Open

FABRICIO FERNANDES FREITAS
3min effort

Comment

No tags
Unreachable code.

4 months ago
L164

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

cwe, unused
src/app/shared/components/select/select.component.ts
Consider using "forEach" instead of "map" as its return value is not being used here.

4 months ago
L245

Bug

Major

Open

FABRICIO FERNANDES FREITAS
5min effort

Comment

No tags
src/app/shared/components/table/table.component.html
Surround this <li> item tag by a <ul> or <ol> container one.

4 months ago
L55

Bug

Minor

Open

FABRICIO FERNANDES FREITAS
10min effort

Comment

No tags
src/assets/sass/components/input/_inputs.scss
Unexpected duplicate "background"

4 months ago
L68

Bug

Major

Open

FABRICIO FERNANDES FREITAS
1min effort

Comment

No tags
src/assets/sass/layout/_header.scss
Unexpected duplicate "padding"

4 months ago
L16

Bug

Major

Open

FABRICIO FERNANDES FREITAS
1min effort

Comment

No tags
Unexpected duplicate "float"

4 months ago
L154

Bug

Major

Open

FABRICIO FERNANDES FREITAS
1min effort

Comment

No tags
Unexpected duplicate "float"

4 months ago
L168

Bug

Major

Open

FABRICIO FERNANDES FREITAS
1min effort

Comment

No tags
Unexpected duplicate "line-height"

4 months ago
L183

Bug

Major

Open

FABRICIO FERNANDES FREITAS
1min effort

Comment

No tags
src/assets/sass/views/_detalhe.scss
Unexpected duplicate "display"

4 months ago
L92

Bug

Major

Open

FABRICIO FERNANDES FREITAS
1min effort

Comment

No tags
Unexpected duplicate "font-size"

4 months ago
L233

Bug

Major

Open

FABRICIO FERNANDES FREITAS
1min effort

Comment

No tags
58 of 58 shown
SonarQube™ technology is powered by SonarSource SA
Community Editionv9.9.5 (build 90363)NO LONGER ACTIVELGPL v3CommunityDocumentationPluginsWeb API


