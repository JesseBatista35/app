Oi, Cleomar!

A regra que foi aberta e aplicada era para o SIMPF (DES → SIGCT, 10.116.83.19:8443). Testei a partir do pod do SIMPF em DES e a comunicação com o SIGCT está OK. Ela não tem relação com o SIPDM, que usa outro namespace e outro destino.

Sobre o SIMPF, no log atual não aparece erro de comunicação com o SIGCT. Os erros que aparecem são NullPointerException no NegocioExceptionMapper (linha 28) nos endpoints /ParametrosGerais/avisoGeral e /indsSistema, desde o deploy de 20/10, o que indica ajuste na aplicação.

Para eu seguir com a análise, consegue me mandar a evidência do erro que você está vendo? Preciso de:

qual sistema (SIMPF ou SIPDM) e qual funcionalidade/endpoint;
print ou mensagem do erro;
data e horário aproximado do teste.

Valeu!
