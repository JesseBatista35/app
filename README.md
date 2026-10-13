# ver o volume antigo que ocupa o caminho
oc set volume dc/sinfs-tqs -n sinfs-tqs

# remover o volume antigo (pelo nome que aparecer acima)
oc set volume dc/sinfs-tqs -n sinfs-tqs --remove --name=<volume-antigo>

# se sobrou o volume órfão criado agora pela task, remova também
oc set volume dc/sinfs-tqs -n sinfs-tqs --remove --name=cacerts-sinfs-intra-tqs2
