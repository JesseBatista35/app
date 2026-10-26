Ailton, achei a causa do “invalid_client”: a troca dos caracteres especiais que você fez no Secret mudou o valor real dele. Testei a credencial original (sem nenhuma alteração) direto via curl, fora do Control-M, e o token veio certinho — então a credencial do Pedro está correta.

Pode reverter o campo Secret no Connection Profile pro valor original, exatamente como veio, sem trocar nenhum caractere:

hOXSgaD1YECHSRVWAlT/Xt1l25N2HwTWYYMb2M/otHI=

Salva, faz Publish & Deploy e roda de novo. Com isso o “Gerar token” deve passar — e aí finalmente vamos ver se o “Obter credencial” passa também com esse client novo.
