/opt/jboss/jboss-eap/bin/jboss-cli.sh --connect --controller=localhost:9990 --command="deployment-info --server-group=sifec-intranet"

for g in sifec-intranet sifec-intranet2 siemp sipen; do echo "== $g =="; /opt/jboss/jboss-eap/bin/jboss-cli.sh --connect --controller=localhost:9990 --command="deployment-info --server-group=$g" | grep enabled; done

/opt/jboss/jboss-eap/bin/jboss-cli.sh --connect --controller=localhost:9990 --command="deployment-info --server-group=sifec-intranet" | grep -v enabled
