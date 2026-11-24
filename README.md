grep -Rn --exclude-dir=logs 'balancer://sigec-csc' $H | grep -v ProxyPass
grep -hE 'AH01102|timeout specified has expired' /logs/apache2/sigec-csc/sigec-csc.esteiras.tqs.caixa-error.log* 2>/dev/null | tail -10
grep -E '" 504 ' /logs/apache2/sigec-csc/sigec-csc.esteiras.tqs.caixa-access.log | tail -10
