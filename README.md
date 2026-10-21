# Contexto real publicado (para conferir o http_context_default = boletoService)
grep -n "WFLYUT0021" /logs/jboss/jboss-eap/standalone/sigsj-boleto/server.log | tail -3

# Erros da aplicação após o deploy (no intranet apareceu o log4j externo faltando)
grep -nE "ERROR|FileNotFound|log_jboss" /logs/jboss/jboss-eap/standalone/sigsj-boleto/server.log | tail -20
