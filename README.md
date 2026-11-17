No caddeapllx2864:

bash
df -h
df -i                       # inodes esgotados também causam esse erro
sudo du -xh / --max-depth=2 2>/dev/null | sort -rh | head -20

Os suspeitos de sempre numa VM JBoss da esteira:

bash
# logs do JBoss
sudo du -sh /opt/*/jboss*/standalone/log /opt/*/jboss*/standalone/tmp /opt/*/jboss*/standalone/data 2>/dev/null
# lixo em /tmp e cache do dnf
sudo du -sh /tmp /var/tmp /var/cache/dnf /var/log
# heap dumps
sudo find / -xdev \( -name "*.hprof" -o -name "core.*" \) -size +100M -exec ls -lh {} \; 2>/dev/null

Limpeza segura:

bash
sudo dnf clean all
sudo find /tmp /var/tmp -type f -mtime +1 -delete
sudo journalctl --vacuum-size=200M
# logs do JBoss com mais de 7 dias (confira o caminho antes)
sudo find <JBOSS_HOME>/standalone/log -name "*.log.*" -mtime +7 -delete

Depois, rode a release de novo.

Fique de olho:

Se o / tiver só 20 GB, que era o tamanho do disco da VM no print do vCenter, ele vai encher de novo. Nesse caso, peça aumento de disco ou separe o log do JBoss em outro volume.
No log também aparece tf_var_quant: comando não encontrado, e com isso o -e quantidade_vm= saiu vazio. A variável tf_var_quant não existe nessa release, então o bash tentou executar $(tf_var_quant) como comando. Hoje não quebrou, mas vale incluir a variável na release com a quantidade de VMs (por exemplo 1).

Me manda a saída do df -h e do du que eu te digo exatamente o que apagar.
