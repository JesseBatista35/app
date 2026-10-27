POD=sispi-qrcode-api-validador-des-311-9wrn4

# Log completo até agora
oc logs $POD -n sispi-des -c sispi-qrcode-api-validador-des | tail -80

# Confirmar que o PID 1 é o java
oc exec $POD -n sispi-des -c sispi-qrcode-api-validador-des -- cat /proc/1/cmdline | tr '\0' ' ' | cut -c1-200; echo


oc exec $POD -n sispi-des -c sispi-qrcode-api-validador-des -- jcmd 1 Thread.print > /tmp/td-311.txt 2>&1
grep -A 30 '"main"' /tmp/td-311.txt
# se não existir jcmd, tente: ... -- jstack 1

oc exec $POD -n sispi-des -c sispi-qrcode-api-validador-des -- cat /proc/1/net/tcp | awk 'NR>1 && $4=="02"{print $3}'
