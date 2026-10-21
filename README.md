Bom dia! Tudo bem sim, e com você? Desculpa a demora, ontem fiquei preso em outra demanda. Vou te explicar por aqui mesmo e, se ficar alguma dúvida, a gente se fala por ligação.

Hoje o SISEI-mgi e o SISEI-mgi-sip estão assim:

• A esteira baixa o secure file sisei_nprd_082026.crt, cria a secret sisei-nprd-082026 e monta o arquivo no pod em /opt/app-root/src/sisei_nprd_082026.crt
• O PHP não lê esse arquivo. No 99-custom.ini, o curl.cainfo e o openssl.cafile apontam para /opt/app-root/src/sisei_nprd.crt, que vem da secret sisei-nprd. Essa secret foi criada manualmente em agosto e a release não atualiza ela.

Por isso, na sexta, além de atualizar o secure file, precisei atualizar a secret sisei-nprd na mão. Só com a release, o PHP continuaria sem os certificados novos.

A recomendação é ajustar as duas linhas do 99-custom.ini na origem (o config que gera os ConfigMaps config-custom-sisei-mgi e config-custom-sisei-mgi-sip):

curl.cainfo="/opt/app-root/src/sisei_nprd_082026.crt"
openssl.cafile="/opt/app-root/src/sisei_nprd_082026.crt"

Esses ConfigMaps são recriados a cada release, então editar direto no OKD não adianta, a próxima release desfaz.

Hoje os dois arquivos têm exatamente o mesmo conteúdo (22 certificados), então a troca não muda nada no funcionamento atual. O ganho é para o futuro: numa próxima inclusão de certificado, basta atualizar o secure file e rodar a release, sem precisar mexer em secret manual.

Alguns cuidados:
• Manter sempre o mesmo nome do secure file (sisei_nprd_082026.crt). Se cada atualização gerar um nome novo, vai ser preciso alterar o ini toda vez.
• Aplicar em DES e TQS juntos, porque o secure file é compartilhado no NPRD.
• Depois de validado, dá para remover a secret sisei-nprd e o mount dela nos deployments. Mas ela ainda está montada também no sisei-mencache-des e no sisei-mgi-mencache-des, então isso deve ser feito com calma, como uma limpeza.
• Se o sisei-des e o sisei-sip-des (ConfigMaps config-custom-sisei e config-custom-sisei-sip) também apontarem para o sisei_nprd.crt, vale fazer o mesmo ajuste neles.

Qualquer dúvida, é só me chamar.
