for h in sigsj-internet.des.caixa sigsj-intranet.des.caixa sigsj-boleto.des.caixa; do
  echo "=== $h ==="; nslookup $h | grep -iA2 "name\|address"
done
echo "--- IP do caddeapllx135 ---"
getent hosts caddeapllx135.agil.nprd.caixa.gov.br || nslookup caddeapllx135

echo "--- app direto nas VMs novas (pra provar que a app está ok) ---"
curl -s -o /dev/null -w "boleto VM 2557: %{http_code}\n"  http://10.116.201.25/boletoService/
curl -s -o /dev/null -w "intranet VM 955: %{http_code}\n" http://10.116.194.179/sigsj_intranet/
