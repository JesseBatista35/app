journalctl -u jboss* --since "16:25" --no-pager | tail -40
grep -nE "ERROR|WFLYCTL|WFLYSRV0056|Exception" /opt/jboss-eap/standalone/log/server.log | tail -30
