# conferir o que o script espera montar
cat /opt/jboss-eap/standalone/configuration/custom.sh

# criar o ponto de montagem
sudo mkdir -p /arquivos-recebidos
sudo chown jboss:jboss /arquivos-recebidos
sudo chmod 770 /arquivos-recebidos

# testar a montagem que o custom.sh faz (copiar a linha mount do script)
sudo bash /opt/jboss-eap/standalone/configuration/custom.sh; echo "rc=$?"
