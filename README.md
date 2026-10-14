O deploy está travado no init do BeyondTrust. O agente autentica no sicsn.caixa normalmente (token e SignAppIn retornam 200), mas qualquer consulta ao Secrets Safe fica sem resposta por mais de 60s. Isso inclui os segredos da pasta SIIFX_DES e até a listagem geral de pastas.

Testamos de dentro do namespace siifx-des (IP de saída 10.116.220.69), com o client antigo e com o novo (7bee4ea6-f78e-4291-ac59-330aa1f9da82). O resultado foi o mesmo nos dois.

Rede e firewall estão descartados. Pelo mesmo IP, o sicsn.caixa responde páginas de 7KB em 0,1s. Só o Secrets Safe não responde.

O siifx-caixinhas, que usa a mesma pasta, já falha desde ontem à noite.

Precisamos que o time do BeyondTrust verifique os logs do serviço/API do Secrets Safe e se houve alguma alteração ou problema no cofre ontem à noite.
