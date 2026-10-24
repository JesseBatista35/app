Mensagem para o grupo (Teams)

Pessoal, boa tarde!

Recebemos as W.O.s dos módulos MTE (WO0000082082381), NIA (WO0000082082478), LG (WO0000082083307) e IMP (WO0000082083318), todas referentes ao 404 após o deploy.

Pela análise do Penhor e do CONRES, o 404 tem causas diferentes em cada módulo (configuração do standalone-okd.xml, vault, módulo siusr na imagem, Library e, no CONRES, um ajuste de código). Cada módulo exige análise e testes próprios.

Além disso, as correções do Penhor e do CONRES estão na branch Cesti-teste e ainda não foram aplicadas na branch oficial. No Penhor, as tags novas foram geradas sem esses ajustes e o 404 voltou.

Para não gerar retrabalho, proponho o seguinte fluxo:

Primeiro, vocês aplicam (merge/PR) as correções da Cesti-teste no Penhor e no CONRES, geram nova tag e confirmam o funcionamento no grupo.
Depois, vocês abrem uma W.O. por módulo, na ordem de urgência de vocês, e direcionam para mim (Jessé Batista).
Atendo um módulo por vez. Quando o módulo estiver corrigido e validado por vocês, encerro a W.O. e vocês abrem a W.O. do próximo.

Assim cada W.O. é atendida dentro do prazo, os ajustes de um módulo podem ser aproveitados no seguinte e evitamos o retorno do erro por correções não aplicadas.

Para adiantar, segue o que foi necessário nos módulos já tratados. Vale vocês já conferirem nos demais:

jboss-modules: a linha do siusr-loginModule deve aparecer duas vezes (o script de build descarta uma linha).
cli-offline.sh: deve ter o module add do br.gov.caixa.siusr.
standalone-okd.xml: deve seguir o padrão do Penhor (datasource sicow-ds, vault, security domain com __SIUSR_END_POINT__, system-properties preenchidas e handler CONSOLE no root-logger).
standalone.conf: conferir a linha do JBOSS_MODULES_SYSTEM_PKGS.
Library: SICOWPORTALURL com /sicow-portal-okd/pages/home.cef, URLs SICOW*_WAR preenchidas, JKS_FILE só com o nome do arquivo e o grupo SICOW-BT-VAULT-SECRET-DES vinculado.
Release: download do vault-sicow-des.keystore, task VAULT_OKD e VAULT.dat no repositório de config.
Código: em classes @WebService, nenhum método público que não seja operação do serviço (usar @WebMethod(exclude = true)).

Lembrando que a senha do usuário scowdb01 no banco cowdb001 continua pendente com o time do SICOW/DBA e afeta todos os módulos.

Ac Jessé Batista

Texto para as 4 W.O.s

Use o mesmo texto nas quatro, trocando o módulo:

WO0000082082381 → MTE
WO0000082082478 → NIA
WO0000082083307 → LG
WO0000082083318 → IMP

Demanda devolvida para alinhamento. As correções aplicadas nos módulos SICOW-penhor-okd e SICOW-conres-okd (branch Cesti-teste) ainda não foram incorporadas pelo time de desenvolvimento.

Conforme alinhado no grupo do SICOW, o atendimento seguirá um módulo por vez. Após o merge e a validação do Penhor e do CONRES, solicitamos a abertura de uma nova W.O. para o módulo [MTE/NIA/LG/IMP], conforme a prioridade do time, direcionada a Jessé Batista. Cada W.O. será atendida após a validação do módulo anterior. O checklist dos ajustes necessários foi encaminhado no grupo.

Ac Jessé Batista
