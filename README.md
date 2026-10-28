ls -l /sigdb/run /etc/init.d/sigdb
cat -A /sigdb/run | tail -5          # "^M$" no fim das linhas = CRLF
sudo bash -x /sigdb/run              # mostra a linha exata que falha
sudo journalctl -u sigdb --no-pager | tail -20

sudo sed -i 's/\r$//' /sigdb/run /etc/init.d/sigdb
sudo systemctl restart sigdb
systemctl status sigdb --no-pager; ps -ef | grep -i [A]gtSigdb
