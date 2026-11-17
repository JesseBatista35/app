Veja o que está ocupando:

bash
sudo ls -lahS /tmp | head -20
sudo du -ah /tmp 2>/dev/null | sort -rh | head -20

Me cola a saída. Pelos nomes eu te digo o que pode apagar. Em geral é seguro remover:

ansible_*, .ansible*, tmp*: restos de execuções do Ansible que falharam;
*.zip, *.tar.gz, *.war, *.ear copiados pela esteira: ela copia de novo na próxima execução.

Antes de apagar um .war/.ear, confira se o JBoss não está usando esse arquivo de lá:

bash
sudo lsof +D /tmp 2>/dev/null | head

Se aparecer um processo java segurando o arquivo, não apague.

Para limpar um arquivo específico:

bash
sudo rm -f /tmp/<arquivo>
df -h /tmp

Para não acontecer de novo: 960 MB é pouco para uma VM em que a esteira descarrega o pacote do JBoss e os artefatos em /tmp. Vale pedir aumento do LV_TMP para 2 a 4 GB. Pela saída do df, o VG parece ter espaço: confira com sudo vgs, e se tiver espaço livre, o lvextend -r -L +2G /dev/VG_PRINCIPAL/LV_TMP resolve. Se a VM for recriada, também vale levar isso para o template da esteira.
