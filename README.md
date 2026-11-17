Passo 1: ver como está no 6.4 (DC 10.116.88.20)

No bash do 10.116.88.20:

bash
D64=$(ps -ef | grep -o 'jboss.domain.base.dir=[^ ]*' | head -1 | cut -d= -f2)/configuration/domain.xml; echo $D64
grep -n -B2 -A8 "APXMail" $D64 | head -40
Passo 2: ver o que já existe de e-mail no 7.4

No CLI do 471:

/profile=full-ha-sifec-intranet/subsystem=mail:read-resource(recursive=true)
/server-group=sifec-intranet:read-attribute(name=socket-binding-group)

Me mande as duas saídas. Com elas eu monto os comandos para criar a sessão APXMail no 7.4: o servidor SMTP e a porta (outbound-socket-binding) iguais aos do 6.4. Aí refazemos o deploy do APX.
