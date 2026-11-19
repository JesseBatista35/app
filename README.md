for h in sigsj-internet.des.caixa sigsj-intranet.des.caixa sigsj-boleto.des.caixa caddeapllx135.agil.nprd.caixa.gov.br caddeapllx135; do
  echo "=== $h ==="; getent hosts $h
done

echo "--- quem responde via URL (confirma o 135) ---"
for h in sigsj-intranet.des.caixa sigsj-boleto.des.caixa; do
  echo "== $h =="; curl -sk https://$h/ 2>/dev/null | grep -o "caddeapllx[0-9]*[^< ]*" | head -1
done
