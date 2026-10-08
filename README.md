
Informe a URL do repositório no GitHub*:	https://github.com/caixagithub/siobs-intra-administracaopingfederate/actions/runs/37801920581/job/113396075904#step:12:34
Selecione a sua Comunidade*:	OpenFinance
Formas de contato*:	61981519449
Descrição da necessidade*:	Ao tentar executar a esteira ágil estamos recebendo erro de secret scanning. Acontece que as secrets que teoricamente estavam expostas já foram tratadas, inclusive com o status fixed.

Sendo assim, solicitamos a análise do caso para que possamos fazer a publicação correta da aplicação pela esteira do GitHub.


Skip to content
GitHub Enterprise
Users managed by Caixa Economica Federal
caixagithub
siobs-intra-administracaopingfederate
Repository navigation
Code
Issues
Pull requests
Actions
Projects
Wiki
Security and quality
Insights
Settings
CI/CD Workflow Generic
caixagithub/siobs-intra-administracaopingfederate_develop_37835810072.25 #25
All jobs
Run details
Annotations
1 error, 1 warning, and 1 notice
CI_DES / VALIDATION
failed 1 hour ago in 21s
Search logs
2s
1s
1s
1s
0s
0s
1s
3s
2s
Run caixagithub/DevSecOps-Actions/.github/util/ghas-security-check/code-scanning@main
Configurar Python
0s
Install required package
0s
Check code scanning
1s
4s
Run caixagithub/DevSecOps-Actions/.github/util/ghas-security-check/secret-scanning@main
Configurar Python
0s
Install required package
0s
Run actions/checkout@v6
1s
Check secret scanning
3s
0s
Run python devsecops-actions/src/validations/validate-topics.py
Validação de tópicos...
Um Tópico válido encontrado: "backend". A pipeline pode prosseguir, e o teste será realizado!
0s
Run python devsecops-actions/src/validations/validate-steps-logs.py
❌ Existem alertas GHAS:

Secret Scanning - 
        🚨 3 alertas de Secret Scanning encontrados!
        📌 Motivo da reprovação: a API retornou 3 alertas cujos secrets ainda constam na branch develop.


        📋 Lista dos alertas reprovados:
        - https://github.com/caixagithub/siobs-intra-administracaopingfederate/security/secret-scanning/8
- https://github.com/caixagithub/siobs-intra-administracaopingfederate/security/secret-scanning/6
- https://github.com/caixagithub/siobs-intra-administracaopingfederate/security/secret-scanning/5

         

Interrompendo pipeline.
Para mais informações, entre em contato com a GESED05 - Segurança no Processo de Desenvolvimento pelo e-mail gesed05@caixa.gov.br
Error: Process completed with exit code 1.
0s
0s
1s
0s
0s
0s
0s
0s
0s
