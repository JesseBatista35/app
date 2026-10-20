LOG=/logs/jboss/jboss-eap/standalone/sigsj-intranet/server.log
ls -la $LOG /opt/jboss-eap/standalone/log/server.log

grep -nE "WFLYCTL0013|WFLYCTL0412|WFLYCTL0180|ERROR|Caused by" $LOG | tail -40
