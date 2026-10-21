Bom dia Jesse, tudo bem tbm!!
 
acho que entendi agora, mas o que vi é que no 99-custom-ini ele faz referência a uma variável da library chamada CERTIFICADO:
 
curl.cainfo="/opt/app-root/src/__CERTIFICADO__"
openssl.cafile="/opt/app-root/src/__CERTIFICADO__"
 
 
E em DES foi mantido o nome sisei_nprd.crt, pelo que entendi pra resolver basta eu alterar o valor dessa variável para sisei_nprd_082026.crt, pois o 99-custom-ini vai pegar o valor dessa variável, seria isso?



 <img width="687" height="66" alt="image" src="https://github.com/user-attachments/assets/fa0b43ab-00ed-4850-9570-08060ada61ba" />
