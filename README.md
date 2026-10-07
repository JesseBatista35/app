ping -c2 10.188.0.16
ping -c2 10.188.0.11

ip -4 -br addr
ip -4 addr show ens224
ip link show ens224
ip neigh show | grep 10.188
bash -c 'timeout 3 bash -c "</dev/tcp/10.188.0.11/2049" && echo 2049 ok || echo 2049 falhou'
