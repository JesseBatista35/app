Robson, boa tarde. Obrigado por trazer os objetos, ajudou bastante a entender como a ferramenta funciona.

O que dá para fazer agora (solução temporária)
Pedir a regra com origem nos objetos OKD e destino só o banco (10.116.29.201, porta TCP 31153). Isso resolve o problema rápido, porque o tráfego do pod passa a ser aceito mesmo saindo com o IP do node. Mas é um contorno: libera o banco para todos os projetos que usam esses objetos, e não só para o SIHDG.

O que seria o correto (solução definitiva)
Corrigir o IP de saída (egress) do projeto. O desenho do OKD é cada projeto sair com o seu IP (10.116.221.46 no caso do sihdg-tqs), e a regra de firewall liberar só esse IP. Isso já está feito e foi validado pela Redes por captura. O que falha é o pod não estar saindo com esse IP, e isso só a Plataforma OKD consegue ajustar.

Proposta

Abrir a demanda para a Plataforma OKD corrigir o egress do namespace sihdg-tqs (definitivo).
Se o prazo apertar, avaliar com a Redes e o dono do banco a liberação pelos objetos OKD, com prazo para ser removida depois que o egress for corrigido (temporário).

Uma dúvida: na lista, o objeto genérico de OKD que vi foi o VIPS_OKD_OCP_CENTRALIZADOS_NPRD, que parece ser de entrada do cluster. Existe algum objeto que represente os nodes do OKD NPRD (faixa 10.116.208.x)? Se não existir, o contorno exigiria criar um.
