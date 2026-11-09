Oi Paulo, segue o passo a passo para solicitar a URL customizada do SIEMP-java-web (mesmo fluxo usado no SIGSJ). A aplicação roda em VM da esteira (Terraform), então o balanceamento é para o servidor na porta 80.

Antes de começar, definir:
• A URL desejada por ambiente (ex.: siemp-java-web.des.caixa / siemp-java-web.tqs.caixa)
• Hostname e IP da VM de cada ambiente

1. Certificado digital (Segurança)
Abrir REQ de certificado TE079 para a URL (uma REQ por URL).
Exemplo SIGSJ: REQ000146906949 (sigsj-intranet.des.caixa).

2. VIP + instalação do certificado (Rede)
Com o certificado gerado, abrir REQ solicitando a criação de um VIP exclusivo para a URL e a instalação do certificado no VIP (porta 443).
Modelo de referência: REQ000141059391.

3. Balanceamento
Na mesma solicitação (ou em seguida), pedir que o VIP balanceie para o servidor da aplicação: hostname/IP da VM na porta 80.

4. Regra de acesso
A fábrica solicita a regra de acesso ao VIP na porta 443 para quem vai consumir/acessar a aplicação.

5. DNS
Abrir REQ de DNS para a URL (FQDN) resolver para o IP do VIP.

6. Esteira (nosso time)
Com VIP e DNS prontos, ajustamos as variáveis de URL na Library da release (URL_CUSTOMIZADA, URL_ALIAS, URL_REDIRECT e URL_REWRITE) e rodamos a release para o Apache da VM responder pelo novo nome.

7. Validação
• nslookup <url> → deve retornar o IP do VIP
• Acessar https://<url>/<contexto>/ no navegador

A ordem importa: certificado → VIP com certificado → balanceamento → DNS → esteira. Qualquer dúvida, é só chamar!
