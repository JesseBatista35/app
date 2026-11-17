Atualização: pacotes intranet no JBoss 7.4 (DES)

✅ Implantados com sucesso, precisam de teste funcional:

1. SIFEC-GARANTIAS 1.8.0.3-b183
URL: https://migracaosifec.des.caixa/garantias-web/

Testar: navegação geral e, principalmente, integração com o SIACG, upload/download de documentos (SISGD) e consultas de contrato SIFBN/SIBAN.
Atenção: no deploy, o JBoss avisou que as classes dessas integrações não foram carregadas por falta de biblioteca no pacote (okhttp, framework SISGD, Jersey client e interfaces SIFBN/SIBAN). Se essas funcionalidades derem erro, o ajuste é no pacote: incluir as libs ou declarar a dependência.

2. SIFEC-ORIGINAÇÃO 3.11.1-b344
URL: https://migracaosifec.des.caixa/ori-web/

Testar: fluxo de originação (simulação, contrato, impressão) e as consultas de contrato SIFBN/SIBAN.
Atenção: mesmo aviso do Garantias sobre as classes SIFBN/SIBAN da biblioteca arqref. Se der erro nessa consulta, é ajuste no pacote.

3. SIFEC MINUTA GARANTIAS 1.0.0-b36
URL: https://migracaosifec.des.caixa/minutaGarantias-web/

Testar: geração e consulta de minutas.
Subiu sem avisos relevantes.

4. SIFEC-BAN 1.7.0-b117 (API SIBAN)
URL: https://migracaosifec.des.caixa/siban-api/

Testar: endpoints de contratos, clientes, imposto de renda e planilha de evolução da dívida.
Observação de segurança para a fábrica: o JBoss avisou que /siban/* não protege os métodos HTTP TRACE, HEAD, CONNECT e OPTIONS. Não impede o funcionamento, mas vale revisar o security-constraint do web.xml.

❌ Não subiu, correção no pacote:

5. SIFEC-CONSTRUCARD 1.23.1.2-b64

Deploy revertido por erro de CDI (WELD-001408). As classes REST injetam os EJBs pela interface, mas estes 5 EJBs não expõem a interface:
MaoDeObraConstrucardNegocioImpl → MaoDeObraConstrucardNegocio
CnaeConstrucardNegocioImpl → CnaeConstrucardNegocio
ConvenenteConstrucardNegocioImpl → ConvenenteConstrucardNegocio
CorrespondenteConstrucardNegocioImpl → CorrespondenteConstrucardNegocio
TotalizadorConstrucardBean → TotalizadorConstrucardService
Ajuste: em cada um, declarar implements <Interface> ou anotar com @Local(<Interface>.class), como já está em CompraConstrucardNegocioImpl e EstabelecimentoConstrucardNegocioImpl. Depois, gerar nova build.

⏳ Pendências para continuar:

MANTER DOCUMENTO 2.2.7: temos as builds b88, b91 e b94 no domain. Qual é a correta?
BNDES 1.0.4.2: precisamos do link do pacote (no domain só tem a 1.1.0).
ARC: o pacote no domain é siarc_EAP6.ear. Existe build para o 7.4?

@Gustavo Duarte Lepesteur da Costa, pode nos ajudar a direcionar os testes e as correções para os devs de cada sistema?
