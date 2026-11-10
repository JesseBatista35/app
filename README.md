4.1$
-sh-4.1$
-sh-4.1$ cd /logs/jboss-eap/hc/servers/sipen_node3_lx0006/
-sh-4.1$ grep -h "PENPO308 Total area saida" sipen.log* | grep -o "USUA.*" | sed 's/Programa Cobol : PENPO308 //' | sort | uniq -c
      1 USUA�RIO : C032291 Total area saida : [82844 ]
      2 USUA�RIO : C159551 Total area saida : [82844 ]
      6 USUA�RIO : C891065 Total area saida : [0 ]
     32 USUA�RIO : C891065 Total area saida : [82844 ]
     20 USUA�RIO : C891069 Total area saida : [0 ]
      4 USUA�RIO : C891070 Total area saida : [0 ]
     20 USUA�RIO : C891070 Total area saida : [82844 ]
      2 USUA�RIO : C891074 Total area saida : [0 ]
      2 USUA�RIO : C892813 Total area saida : [0 ]
     18 USUA�RIO : C892813 Total area saida : [82844 ]
      3 USUA�RIO : F529058 Total area saida : [0 ]
     39 USUA�RIO : F529058 Total area saida : [82844 ]
      2 USUA�RIO : F538467 Total area saida : [82844 ]
     17 USUA�RIO : F577376 Total area saida : [82844 ]
      3 USUA�RIO : F593119 Total area saida : [0 ]
      5 USUA�RIO : F593119 Total area saida : [82844 ]
      1 USUA�RIO : F967975 Total area saida : [0 ]
      5 USUA�RIO : F967975 Total area saida : [82844 ]
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$ grep -c "PENPO308 Total area saida : \[0 \]" sipen.log*
sipen.log:41
sipen.log.2026-11-04:0
sipen.log.2026-11-05:0
sipen.log.2026-11-06:0
sipen.log.2026-11-08:1
sipen.log.2026-11-09:14
-sh-4.1$
-sh-4.1$
-sh-4.1$ find /opt/jboss/jboss-eap -name "framework.jar" 2>/dev/null
-sh-4.1$
-sh-4.1$
