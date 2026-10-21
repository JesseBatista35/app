sso mesmo! Como o 99-custom.ini usa a variável CERTIFICADO, basta alterar o valor dela na Library de DES para sisei_nprd_082026.crt e rodar a release. O ConfigMap é recriado com o caminho novo e o PHP passa a ler o arquivo gerenciado pela esteira.

Alguns pontos:
• Só tem efeito depois da release. Alterar a variável sozinha não muda nada no pod que já está rodando.
• Hoje o conteúdo dos dois arquivos é igual (22 certificados), então não há impacto na integração que já está funcionando.
• Confira também a variável CERTIFICADO de TQS. Se estiver como sisei_nprd.crt, vale alterar para o mesmo valor, já que o secure file é compartilhado.
• Depois da release, dá para validar no pod:
grep -E “cainfo|cafile” /etc/php.d/99-custom.ini
O resultado deve mostrar /opt/app-root/src/sisei_nprd_082026.crt
• Se no futuro quiserem usar a data no nome (ex.: sisei_nprd_102026.crt), é só alterar a variável CERTIFICADO e o secure file na mesma release.

Depois que estiver validado, a secret sisei-nprd deixa de ser usada pelo PHP e pode ser removida com calma numa limpeza futura.
