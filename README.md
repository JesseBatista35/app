Boa tarde, pessoal. Obrigado pela captura. Concordo que ela valida a regra da CRQ000001499711: o teste que fizemos a partir do nó de egress (ceadecldlx084), com origem 10.116.221.46, às 14:20:00 (-03), aparece completo no firewall.

O ponto é que esse teste saiu direto do nó. Quando testamos a partir de pods do sihdg-tqs, o timeout continua, e esses testes não aparecem em JV nem em JV1:

Pod no nó ceadecldlx081: 14:23:47, 14:23:52 e 14:23:57 (-03)
Pod no nó ceadecldlx077: 14:34:51, 14:34:56 e 14:35:01 (-03)

Ou seja, o pacote do pod não chega ao firewall com origem 10.116.221.46. No OKD, conferimos que o egress IP está configurado corretamente (namespace, nó, interface e SNAT). Para fecharmos de que lado está o desvio, vocês podem rodar show conn | i 10.116.29.23.*1433 e informar a origem das conexões vindas do sihdg-tqs? Queremos saber se aparece 10.116.221.46 ou o IP do nó.

Com essa informação, levamos o caso à plataforma OKD, se necessário. Obrigado!
