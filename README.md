Boa tarde, Vitor e Evandro!

http_context_default: pelo log do JBoss, a aplicação foi publicada no contexto /sigsj_intranet (WFLYUT0021: Contexto web registrado: '/sigsj_intranet'). Então a variável precisa ser sigsj_intranet, e não sigsj como está hoje.

URLs: como não vamos usar URL customizada, a proposta é trocar na Library do SIGSJ-intranet (DES) para a URL padrão da esteira:

Variável	Valor
http_context_default	sigsj_intranet
URL_CUSTOMIZADA	sigsj-intranet.esteiras.des.caixa
URL_ALIAS	sigsj-intranet.esteiras.des.caixa
URL_REDIRECT	sigsj-intranet.esteiras.des.caixa
URL_REWRITE	sigsj-intranet\.esteiras\.des\.caixa

Nas variáveis de URL vai só o nome do host, sem https:// e sem o contexto. O acesso fica em http://sigsj-intranet.esteiras.des.caixa/sigsj_intranet.

Podemos fazer essa alteração nas Libraries? Com o ok de vocês, ajustamos e rodamos uma nova release do intranet.
