sudo dnf install -y tcpdump
sudo tcpdump -i ens224 -n -c 30 arp



sudo python3 -c "
import socket
s=socket.socket(socket.AF_PACKET,socket.SOCK_RAW,socket.ntohs(0x0806));s.bind(('ens224',0))
for _ in range(30):
    p=s.recv(65535);print(socket.inet_ntoa(p[28:32]),'pergunta por',socket.inet_ntoa(p[38:42]))
"
