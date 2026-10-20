cd /opt/jboss-eap/standalone/deployments
sudo -u jboss mv sirotcon-ejb.jar sirotcon-ejb-2.3.0.1-farm.jar
sudo -u jboss rm -f sirotcon-ejb.jar.*
sudo -u jboss touch sigsj_intranet-ear.ear.dodeploy
sleep 40; ls -l | grep -E "deployed|failed"
