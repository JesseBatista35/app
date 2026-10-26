Resumo — AI_IIFX_Job#1 (401 BeyondTrust) — o que descobrimos e o que falta fazer

O problema
O job AI_IIFX_Job#1 (Control-M, pasta SIIFX) estava falhando no passo “Obter credencial” com erro 401 “User not authenticated” ao buscar a credencial no BeyondTrust (Secrets Safe), mesmo o login anterior (SignAppin) retornando sucesso.

Como diagnosticamos

Descartamos permissão/grupo/credencial — conferimos tudo no BeyondInsight (Access Management, grupo, API Registration) e estava certo.
Testamos com um client novo e totalmente válido, criado do zero pelo Pedro (cofre) — o mesmo erro aconteceu, provando que não era problema de credencial nem de permissão específica.
O Pedro testou manualmente no Postman, passo a passo, e descobriu que a chamada só funciona se a gente reenviar um cookie de sessão (ASP.NET_SessionId) que o BeyondTrust devolve logo no primeiro passo (geração do token) — esse cookie precisa ser reenviado nas chamadas seguintes (login e leitura da credencial).
Testamos no próprio servidor (caddeapllx2695) via curl e confirmamos: o cookie chega certinho até o servidor — ou seja, não é problema de rede/proxy.
Concluímos que o bug está no cliente HTTP interno do plugin Application Integrator do Control-M — ele recebe o cookie, mas não consegue capturá-lo/reenviá-lo corretamente nos passos REST do plugin (por isso sempre aparecia vazio nos logs do Control-M).

A correção validada
Como contorno do bug do plugin, criamos um script bash (/tmp/teste_cofre.sh, já está salvo no servidor) que faz a autenticação inteira via curl, controlando o cookie manualmente (gera token → login → pega a credencial SIIFX_BT_APIKEY → logout). Testamos isolado via SSH no servidor e funcionou 100%, confirmado inclusive pelo log de auditoria do próprio BeyondInsight (Login → leitura do segredo → Logout).

O que falta fazer (pro Ailton amanhã)

No Designer do Control-M, no job de teste (perfil IIFX_TESTE): apagar os passos “Gerar token”, “Login no Beyond Trust”, “Obter credencial” e “Logout no Beyond Trust”.
No passo “Executar job” que sobrar, trocar o comando pra chamar o script novo:
   export CLIENT_ID="28b5d21f-2288-4f03-89cc-c5999fa85e26"
   export CLIENT_SECRET="hOXSgaD1YECHSRVWAlT/Xt1l25N2HwTWYYMb2M/otHI="
   /tmp/teste_cofre.sh
Save → Publish & Deploy → rodar o job de teste completo dentro do Control-M (não mais só o script isolado) e conferir se passa de ponta a ponta.
Se passar, repetir a mesma mudança no job de produção (AI_IIFX_Job#1, perfil IIFX), trocando CLIENT_ID/CLIENT_SECRET pela credencial de produção (não a de teste do Pedro).
Rodar o job de produção e confirmar sucesso.

Só depois disso tudo validado em produção é que fechamos o caso de vez.
