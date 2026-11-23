timeout 5 bash -c "cat < /dev/null > /dev/tcp/10.116.89.101/8111" && echo "SIROT OK" || echo "SIROT BLOQUEADO"
