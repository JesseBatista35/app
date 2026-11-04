ssh p585600@10.116.97.59
/opt/jboss/jboss-eap/bin/jboss-cli.sh --connect --controller=localhost:9990

/profile=full-ha-sifec-intranet/subsystem=modcluster/proxy=default:read-attribute(name=balancer)
/profile=full-ha-siemp/subsystem=modcluster/proxy=default:read-attribute(name=balancer)
