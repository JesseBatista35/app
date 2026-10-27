root@sspdeaplux0100:/# ls -l $DOM/config/ | egrep -i 'lock|pid'
/config/: No such file or directory
root@sspdeaplux0100:/# egrep -n 'admin-listener' $DOM/config/domain.xml
egrep: can't open /config/domain.xml
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/# pstack 7248 | head -50
7248:   /opt/SUNWas8/jdk/bin/java -server -XX:NewRatio=2 -Xms512m -Xmx3g -XX:M
------------  lwp# 1 / thread# 1  ---------------
 fec387b8 lwp_cond_wait (38ff8, 38fe0, 0, 0)
 fe1d69b8 __1cHMonitorEwait6Mil_i_ (0x38f88?, 0x39c78?, 0x3a858?, 0xfe81c000?, 0x39c78?, 0x38fb8?) + 4bc
 fe705c30 __1cHThreadsKdestroy_vm6F_i_ (0x39c78?, 0x38f88?, 0xfe873c90?, 0xfe81c000?, 0x0?, 0xbc00?) + ac
 fe4da6fc jni_DestroyJavaVM (0x39c78?, 0xa8cc?, 0xfe874aec?, 0xfe874ae4?, 0x2?, 0xfe874ae8?) + 1a4
 000122a0 main     (0x1?, 0x33432?, 0xfe86c868?, 0x1d8?, 0x0?, 0x1?) + 11d8
 000110b0 _start   (0x0?, 0x0?, 0x0?, 0x0?, 0x0?, 0x0?) + 108
------------  lwp# 2 / thread# 2  ---------------
 fec387b8 lwp_cond_wait (78bf8, 78be0, 0, 0)
 fe1d6668 __1cHMonitorEwait6Mil_i_ (0x78b88?, 0x78d18?, 0xfff0bc00?, 0xfe81c000?, 0xf4000?, 0x78bb8?) + 16c
 fe1adb74 __1cNGCTaskManagerIget_task6MI_pnGGCTask__ (0x78b48?, 0x0?, 0x2400?, 0x78b88?, 0x32a80?, 0xfe81c000?) + 1e4
 fe37175c __1cMGCTaskThreadDrun6M_v_ (0x78d18?, 0xfe868d6c?, 0x36288?, 0x78d18?, 0xfe81c000?, 0xfe874bf8?) + 180
 fe6abcc4 __1cG_start6Fpv_0_ (0x78d18?, 0x1c50?, 0xfe81c000?, 0x0?, 0x7534?, 0x7400?) + 208
 fec339ac _lwp_start (0x0?, 0x0?, 0x0?, 0x0?, 0x0?, 0x0?)
------------  lwp# 3 / thread# 3  ---------------
 fec387b8 lwp_cond_wait (78bf8, 78be0, 0, 0)
 fe1d6668 __1cHMonitorEwait6Mil_i_ (0x78b88?, 0x797a0?, 0xfff0bc00?, 0xfe81c000?, 0xf4000?, 0x78bb8?) + 16c
 fe1adb74 __1cNGCTaskManagerIget_task6MI_pnGGCTask__ (0x78b48?, 0x1?, 0x2400?, 0x78b88?, 0x32a80?, 0xfe81c000?) + 1e4
 fe37175c __1cMGCTaskThreadDrun6M_v_ (0x797a0?, 0xfe868d6c?, 0x79870?, 0x797a0?, 0xfe81c000?, 0xfe874bf8?) + 180
 fe6abcc4 __1cG_start6Fpv_0_ (0x797a0?, 0x1c50?, 0xfe81c000?, 0x0?, 0x7534?, 0x7400?) + 208
 fec339ac _lwp_start (0x0?, 0x0?, 0x0?, 0x0?, 0x0?, 0x0?)
------------  lwp# 4 / thread# 4  ---------------
 fec387b8 lwp_cond_wait (78bf8, 78be0, 0, 0)
 fe1d6668 __1cHMonitorEwait6Mil_i_ (0x78b88?, 0x7a830?, 0xfff0bc00?, 0xfe81c000?, 0xf4000?, 0x78bb8?) + 16c
 fe1adb74 __1cNGCTaskManagerIget_task6MI_pnGGCTask__ (0x78b48?, 0x2?, 0x2400?, 0x78b88?, 0x32a80?, 0xfe81c000?) + 1e4
 fe37175c __1cMGCTaskThreadDrun6M_v_ (0x7a830?, 0xfe868d6c?, 0x79888?, 0x7a830?, 0xfe81c000?, 0xfe874bf8?) + 180
 fe6abcc4 __1cG_start6Fpv_0_ (0x7a830?, 0x1c50?, 0xfe81c000?, 0x0?, 0x7534?, 0x7400?) + 208
 fec339ac _lwp_start (0x0?, 0x0?, 0x0?, 0x0?, 0x0?, 0x0?)
------------  lwp# 5 / thread# 5  ---------------
 fec387b8 lwp_cond_wait (78bf8, 78be0, 0, 0)
 fe1d6668 __1cHMonitorEwait6Mil_i_ (0x78b88?, 0x7b2b8?, 0xfff0bc00?, 0xfe81c000?, 0xf4000?, 0x78bb8?) + 16c
 fe1adb74 __1cNGCTaskManagerIget_task6MI_pnGGCTask__ (0x78b48?, 0x3?, 0x2400?, 0x78b88?, 0x32a80?, 0xfe81c000?) + 1e4
 fe37175c __1cMGCTaskThreadDrun6M_v_ (0x7b2b8?, 0xfe868d6c?, 0x798a0?, 0x7b2b8?, 0xfe81c000?, 0xfe874bf8?) + 180
 fe6abcc4 __1cG_start6Fpv_0_ (0x7b2b8?, 0x1c50?, 0xfe81c000?, 0x0?, 0x7534?, 0x7400?) + 208
 fec339ac _lwp_start (0x0?, 0x0?, 0x0?, 0x0?, 0x0?, 0x0?)
------------  lwp# 6 / thread# 6  ---------------
 fec387b8 lwp_cond_wait (78bf8, 78be0, 0, 0)
 fe1d6668 __1cHMonitorEwait6Mil_i_ (0x78b88?, 0x7bd40?, 0xfff0bc00?, 0xfe81c000?, 0xf4000?, 0x78bb8?) + 16c
 fe1adb74 __1cNGCTaskManagerIget_task6MI_pnGGCTask__ (0x78b48?, 0x4?, 0x2400?, 0x78b88?, 0x32a80?, 0xfe81c000?) + 1e4
 fe37175c __1cMGCTaskThreadDrun6M_v_ (0x7bd40?, 0xfe868d6c?, 0x798b8?, 0x7bd40?, 0xfe81c000?, 0xfe874bf8?) + 180
 fe6abcc4 __1cG_start6Fpv_0_ (0x7bd40?, 0x1c50?, 0xfe81c000?, 0x0?, 0x7534?, 0x7400?) + 208
 fec339ac _lwp_start (0x0?, 0x0?, 0x0?, 0x0?, 0x0?, 0x0?)
------------  lwp# 7 / thread# 7  ---------------
 fec387b8 lwp_cond_wait (78bf8, 78be0, 0, 0)
 fe1d6668 __1cHMonitorEwait6Mil_i_ (0x78b88?, 0x7c7c8?, 0xfff0bc00?, 0xfe81c000?, 0xf4000?, 0x78bb8?) + 16c
 fe1adb74 __1cNGCTaskManagerIget_task6MI_pnGGCTask__ (0x78b48?, 0x5?, 0x2400?, 0x78b88?, 0x32a80?, 0xfe81c000?) + 1e4
 fe37175c __1cMGCTaskThreadDrun6M_v_ (0x7c7c8?, 0xfe868d6c?, 0x798d0?, 0x7c7c8?, 0xfe81c000?, 0xfe874bf8?) + 180
 fe6abcc4 __1cG_start6Fpv_0_ (0x7c7c8?, 0x1c50?, 0xfe81c000?, 0x0?, 0x7534?, 0x7400?) + 208
 fec339ac _lwp_start (0x0?, 0x0?, 0x0?, 0x0?, 0x0?, 0x0?)
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/# pfiles 7248 | head -20
7248:   /opt/SUNWas8/jdk/bin/java -server -XX:NewRatio=2 -Xms512m -Xmx3g -XX:M
  Current rlimit: 65535 file descriptors
   0: S_IFIFO mode:0000 dev:16383,0 ino:167046066 uid:0 gid:0 size:0
      O_RDWR
   1: S_IFIFO mode:0000 dev:16383,0 ino:167046067 uid:0 gid:0 size:0
      O_RDWR
   2: S_IFIFO mode:0000 dev:16383,0 ino:167046068 uid:0 gid:0 size:0
      O_RDWR
   3: S_IFCHR mode:0666 dev:16379,0 ino:73924636 uid:0 gid:3 rdev:141,12
      O_RDWR FD_CLOEXEC
      /devices/pseudo/mm@0:zero
      offset:0
   4: S_IFDOOR mode:0777 dev:16381,0 ino:0 uid:0 gid:0 size:0
      O_RDONLY|O_LARGEFILE FD_CLOEXEC  door to nscd[683]
      /system/volatile/name_service_door
        peer: nscd[683] zone: global[0]
   5: S_IFREG mode:0644 dev:297,65564 ino:9751 uid:1020 gid:150 size:40371622 (38,5M)
      O_RDONLY|O_LARGEFILE FD_CLOEXEC
      /opt/SUNWas8/jdk1.5.0_36/jre/lib/rt.jar
      offset:27226417 (26M)
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/# tail -100 $DOM/logs/server.log
tail: cannot open input
root@sspdeaplux0100:/# DOM=/opt/SUNWas8/domains/das01
root@sspdeaplux0100:/#
root@sspdeaplux0100:/# tail -100 $DOM/logs/server.log
[#|2026-10-27T16:18:03.656-0300|INFO|sun-appserver-ee8.2|javax.enterprise.system.tools.admin|_ThreadID=10;|ADM0046:The Platform MBeanServer is available. It will be used to register Application Server MBeans. Platform MBeans will also be available for browsing while using standard JMX Console.|#]

[#|2026-10-27T16:18:03.662-0300|INFO|sun-appserver-ee8.2|javax.enterprise.system.tools.admin|_ThreadID=10;|ADM0001:MBeanServer initialized successfully|#]

[#|2026-10-27T16:18:04.042-0300|SEVERE|sun-appserver-ee8.2|javax.enterprise.system.core.security|_ThreadID=10;|SEC8001: Exception in initializing SunPKCS11.
java.lang.IllegalStateException
        at com.sun.enterprise.security.SecuritySupportImpl.loadStores(SecuritySupportImpl.java:80)
        at com.sun.enterprise.ee.security.EESecuritySupportImpl.loadSunPKCS11Stores(EESecuritySupportImpl.java:245)
        at com.sun.enterprise.ee.security.EESecuritySupportImpl.<clinit>(EESecuritySupportImpl.java:122)
        at java.lang.Class.forName0(Native Method)
        at java.lang.Class.forName(Class.java:164)
        at com.sun.enterprise.pluggable.PluggableFeatureFactoryBaseImpl.invoke(PluggableFeatureFactoryBaseImpl.java:53)
        at $Proxy0.getSecuritySupport(Unknown Source)
        at com.sun.enterprise.security.SecurityUtil.getSecuritySupport(SecurityUtil.java:338)
        at com.sun.enterprise.security.SSLUtils.<clinit>(SSLUtils.java:72)
        at com.sun.enterprise.security.SecurityLifecycle.onInitialization(SecurityLifecycle.java:59)
        at com.sun.enterprise.server.ApplicationServer.onInitialization(ApplicationServer.java:215)
        at com.sun.enterprise.server.PEMain.run(PEMain.java:298)
        at com.sun.enterprise.server.PEMain.main(PEMain.java:221)
|#]

[#|2026-10-27T16:18:04.047-0300|WARNING|sun-appserver-ee8.2|javax.enterprise.system.stream.err|_ThreadID=10;|Exception in thread "main" |#]

[#|2026-10-27T16:18:04.054-0300|WARNING|sun-appserver-ee8.2|javax.enterprise.system.stream.err|_ThreadID=10;|java.lang.ExceptionInInitializerError
        at java.lang.Class.forName0(Native Method)
        at java.lang.Class.forName(Class.java:164)
        at com.sun.enterprise.pluggable.PluggableFeatureFactoryBaseImpl.invoke(PluggableFeatureFactoryBaseImpl.java:53)
        at $Proxy0.getSecuritySupport(Unknown Source)
        at com.sun.enterprise.security.SecurityUtil.getSecuritySupport(SecurityUtil.java:338)
        at com.sun.enterprise.security.SSLUtils.<clinit>(SSLUtils.java:72)
        at com.sun.enterprise.security.SecurityLifecycle.onInitialization(SecurityLifecycle.java:59)
        at com.sun.enterprise.server.ApplicationServer.onInitialization(ApplicationServer.java:215)
        at com.sun.enterprise.server.PEMain.run(PEMain.java:298)
        at com.sun.enterprise.server.PEMain.main(PEMain.java:221)
Caused by: java.lang.IllegalStateException
        at com.sun.enterprise.ee.security.EESecuritySupportImpl.<clinit>(EESecuritySupportImpl.java:130)
        ... 10 more
|#]

root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/# ls -l $DOM/config/ | egrep -i 'lock|pid'
-rw-r--r--   1 sjsas8   sunjava    33251 abr 20  2026 hs_err_pid1703.log
-rw-r--r--   1 sjsas8   sunjava    25991 mar  3  2026 hs_err_pid28142.log
-rw-r--r--   1 sjsas8   sunjava    25461 abr 17  2026 hs_err_pid6525.log
root@sspdeaplux0100:/# egrep -n 'admin-listener' $DOM/config/domain.xml
388:        <http-listener acceptor-threads="1" address="0.0.0.0" blocking-enabled="false" default-virtual-server="__asadmin" enabled="true" family="inet" id="admin-listener" port="14848" security-enabled="true" server-name="" xpowered-by="true"/>
394:        <virtual-server default-web-module="admingui" hosts="${com.sun.aas.hostName}" http-listeners="admin-listener" id="__asadmin" log-file="${com.sun.aas.instanceRoot}/logs/server.log" state="on">
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/# sudo -u sjsas8 kill 7248
Sinto muito, usu▒rio root n▒o tem permiss▒o para executar "/bin/kill 7248" como sjsas8 em sspdeaplux0100.
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/# sudo -u sjsas8 kill -9 7248
Sinto muito, usu▒rio root n▒o tem permiss▒o para executar "/bin/kill -9 7248" como sjsas8 em sspdeaplux0100.
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/# sudo -sjsas8
sudo: illegal option -- j
usage: sudo -h | -K | -k | -V
usage: sudo -v [-ABknS] [-g group] [-h host] [-p prompt] [-u user]
usage: sudo -l [-ABknS] [-g group] [-h host] [-p prompt] [-U user] [-u user] [command]
usage: sudo [-ABbEHknPS] [-C num] [-D directory] [-g group] [-h host] [-p prompt] [-R directory] [-T timeout] [-u user] [VAR=value] [-i|-s] [<command>]
usage: sudo -e [-ABknS] [-C num] [-D directory] [-g group] [-h host] [-p prompt] [-R directory] [-T timeout] [-u user] file ...
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/# sudo -u sjsas8 kill 7248
Sinto muito, usu▒rio root n▒o tem permiss▒o para executar "/bin/kill 7248" como sjsas8 em sspdeaplux0100.
root@sspdeaplux0100:/# sudo -u sjsas8 kill -9 7248
Sinto muito, usu▒rio root n▒o tem permiss▒o para executar "/bin/kill -9 7248" como sjsas8 em sspdeaplux0100.
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
