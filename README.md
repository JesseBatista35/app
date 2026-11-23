Marcio, situação do login do SIGSJ-internet em DES:

Resolvido: o login quebrava na criptografia da senha (SenhasSIIBC / UnsatisfiedLinkError) porque faltava a biblioteca nativa libSenhasSIIBC.so na VM. Coloquei a lib (do legado, 64 bits) em /apl/sigsj/lib e ajustei o java.library.path no standalone.conf (vai pro repo de config pra não regredir). A criptografia já funciona.

Falta agora: com a lib OK, o login passa a falhar no SIROT (SIROTTrans.getResponse nulo) porque a VM não alcança o farm 10.116.89.101:8111 — a regra de firewall 99053 ainda não foi aplicada pela Rede. É só isso que falta pro login funcionar.

(Em paralelo: banco SIGSJ04 corrigido pra usuário SGSJSD01, senha via Segurança na REQ000147111475 — afeta telas internas, não o login.)
