Confira:

bash
df -h /tmp
sudo lsof +L1 2>/dev/null | grep /tmp
Se o df mostrar espaço livre: já resolveu. Rode a release de novo.
Se continuar em 100% e o lsof listar arquivos (deleted): veja qual processo está na coluna COMMAND e no PID. Se for o java do JBoss (PID 677441, pelo hsperfdata_jboss), reinicie o JBoss para liberar o espaço:
bash
sudo systemctl restart jboss-eap 2>/dev/null || sudo systemctl list-units | grep -iE "jboss|eap"

O segundo comando mostra o nome do serviço, caso não seja jboss-eap. Se for outro processo (dnf ou ansible travado), basta matar o PID:

bash
sudo kill <PID>

Me manda a saída dos dois comandos que eu confirmo o passo seguinte.
