ls -la /apl/sigsj/lib/                                  # a .so ainda esta la?
grep -n "library.path" /opt/jboss-eap/bin/standalone.conf   # a linha sumiu?
ps -ef | grep -v grep | grep -o "java.library.path=[^ ]*"   # o JVM atual usa o path?
