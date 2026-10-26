
[p585600@cadsvitrlx100 ~]$
[p585600@cadsvitrlx100 ~]$ ssh 10.116.201.173
p585600@10.116.201.173's password:
Last login: Tue Oct  6 16:12:01 2026 from 10.122.150.31
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$ java -version
openjdk version "21.0.11" 2026-04-21 LTS
OpenJDK Runtime Environment (Red_Hat-21.0.11.0.10-1) (build 21.0.11+10-LTS)
OpenJDK 64-Bit Server VM (Red_Hat-21.0.11.0.10-1) (build 21.0.11+10-LTS, mixed mode, sharing)
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$ wich java
-sh: wich: comando não encontrado
[p585600@caddeapllx2695 ~]$ which java
/usr/bin/java
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$ readlink =f $(which java)
/etc/alternatives/java
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$ alternatives --list 2>/dev/null || upadate-alternatives --list java 2>/dev/null
soelim                  auto    /usr/bin/soelim.groff
libnssckbi.so.x86_64    auto    /usr/lib64/pkcs11/p11-kit-trust.so
iptables                auto    /usr/sbin/iptables-nft
ebtables                auto    /usr/sbin/ebtables-nft
arptables               auto    /usr/sbin/arptables-nft
ld                      auto    /usr/bin/ld.bfd
cifs-idmap-plugin       auto    /usr/lib64/cifs-utils/cifs_idmap_sss.so
ksh                     auto    /usr/bin/ksh93
man                     auto    /usr/bin/man.man-db
java                    auto    /usr/lib/jvm/java-21-openjdk-21.0.11.0.10-2.el9.x86_64/bin/java
jre_openjdk             auto    /usr/lib/jvm/java-21-openjdk-21.0.11.0.10-2.el9.x86_64
jre_21                  auto    /usr/lib/jvm/java-21-openjdk-21.0.11.0.10-2.el9.x86_64
jre_21_openjdk          auto    /usr/lib/jvm/jre-21-openjdk-21.0.11.0.10-2.el9.x86_64
javac                   auto    /usr/lib/jvm/java-21-openjdk-21.0.11.0.10-2.el9.x86_64/bin/javac
java_sdk_openjdk        auto    /usr/lib/jvm/java-21-openjdk-21.0.11.0.10-2.el9.x86_64
java_sdk_21             auto    /usr/lib/jvm/java-21-openjdk-21.0.11.0.10-2.el9.x86_64
java_sdk_21_openjdk     auto    /usr/lib/jvm/java-21-openjdk-21.0.11.0.10-2.el9.x86_64
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$ ps aux | grep -i ctm
root     2246608  0.3  6.5 2920440 243176 ?      Sl   09:53   0:12 /opt/ctmage/JRE/bin/java -Xmx256m -XX:+UseG1GC -XX:+CrashOnOutOfMemoryError -agentpath:/opt/ctmage/ctm/exe/libBMCJW.so -Djava.io.tmpdir=/tmp -Djava.net.preferIPv4Stack=true -Doverride.default.services= -Dspring.profiles.active=tcp -DCTMAG.CONFIG.DBGLVL=0 -Dctm.logs.dir=/opt/ctmage/ctm/proclog -Dlogging.config=/opt/ctmage/ctm/data/logback.xml -Dctm.data.dir=/opt/ctmage/ctm/data -XX:+HeapDumpOnOutOfMemoryError -Dstdout=/opt/ctmage/ctm/proclog/agjstd_2245854-2026-10-26.0.tmp -DLIMIT_LOG_VERSIONS=8 -DLIMIT_LOG_FILE_SIZE=10 -jar /opt/ctmage/ctm/exe/ag-app.jar
root     2246762  0.0  0.1  24304  6300 ?        S    09:53   0:00 /opt/ctmage/ctm/exe/p_ctmag
root     2246826  0.0  0.1  24472  6388 ?        S    09:53   0:00 /opt/ctmage/ctm/exe/p_ctmat
root     2246870  0.0  0.2  33460  9600 ?        S    09:53   0:00 /opt/ctmage/ctm/exe/p_ctmatw -ATW_NAME ATW000
root     2246939  0.0  0.0   7244  3692 ?        S    10:19   0:00 /bin/sh /opt/ctmage/ctm/cm/AI/exe/cm_container start 0
root     2246953  0.4 11.5 3712300 432356 ?      Sl   10:19   0:10 /opt/ctmage/JRE/bin/java -DappName=AI -DcmVer=921300 -Dagent.logs=/opt/ctmage/ctm/proclog -Dcm.home=/opt/ctmage/ctm/cm/AI -Dlog4j2.configurationFile=/opt/ctmage/ctm/cm/AI/data/log4j2.xml --add-opens java.base/java.lang=ALL-UNNAMED -Dlog4j2.isThreadContextMapInheritable=true -Xms512m -Xmx1024m -XX:-ExitOnOutOfMemoryError -XX:+HeapDumpOnOutOfMemoryError -XX:+UseStringDeduplication -Djavax.net.ssl.trustStore=/opt/ctmage/ctm/cm/AI/data/security/apcerts -Djavax.net.ssl.keyStore=/opt/ctmage/ctm/cm/AI/data/security/apks -classpath /opt/ctmage/ctm/cm/AI/exe/jars/*:/opt/ctmage/ctm/cm/AI/exe/cmAI-921300.jar com.bmc.cm.ServerActions start 0
p585600  2247240  0.0  0.0   6420  2332 pts/0    S+   10:54   0:00 grep --color=auto -i ctm
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
