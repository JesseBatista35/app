mkdir -p /apl/sigsj/properties && cd /apl/sigsj/properties
scp p585600@10.116.88.96:/apl/sigsj/properties/\*.properties .
chown -R jboss:jboss /apl/sigsj
chmod 644 /apl/sigsj/properties/*.properties
ls -la /apl/sigsj/properties/




intranet: https://sigsj-intranet.des.caixa/sigsj_intranet/
internet: https://sigsj-internet.des.caixa/sigsj_internet/login.xhtml
boleto (SOAP): https://sigsj-boleto.des.caixa/boletoService/contaJudicial
