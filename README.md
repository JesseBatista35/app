
-sh-4.1$
-sh-4.1$
-sh-4.1$ awk 'NR>248632' server.log | grep -n "JCicsConnect.login\|Erro na montagem" | head
3207:2026-11-10 09:32:56,517ERROR(ajp-/10.116.88.25:13309-5)JBWEB000236: Servlet.service() for servlet jsp threw exception: javax.servlet.jsp.JspException: Erro na montagem do Menu.
3244:2026-11-10 09:32:56,518ERROR(ajp-/10.116.88.25:13309-5)JBWEB000236: Servlet.service() for servlet Controller threw exception: javax.servlet.jsp.JspException: Erro na montagem do Menu.
4569:2026-11-10 09:50:22,990ERROR(ajp-/10.116.88.25:13309-7)JBWEB000236: Servlet.service() for servlet jsp threw exception: javax.servlet.jsp.JspException: Erro na montagem do Menu.
4606:2026-11-10 09:50:22,990ERROR(ajp-/10.116.88.25:13309-7)JBWEB000236: Servlet.service() for servlet Controller threw exception: javax.servlet.jsp.JspException: Erro na montagem do Menu.
4771:2026-11-10 09:52:50,576ERROR(ajp-/10.116.88.25:13309-6)JBWEB000236: Servlet.service() for servlet jsp threw exception: javax.servlet.jsp.JspException: Erro na montagem do Menu.
4808:2026-11-10 09:52:50,577ERROR(ajp-/10.116.88.25:13309-6)JBWEB000236: Servlet.service() for servlet Controller threw exception: javax.servlet.jsp.JspException: Erro na montagem do Menu.
4982:2026-11-10 09:55:12,134ERROR(ajp-/10.116.88.25:13309-6)JBWEB000236: Servlet.service() for servlet jsp threw exception: javax.servlet.jsp.JspException: Erro na montagem do Menu.
5019:2026-11-10 09:55:12,135ERROR(ajp-/10.116.88.25:13309-6)JBWEB000236: Servlet.service() for servlet Controller threw exception: javax.servlet.jsp.JspException: Erro na montagem do Menu.
5220:2026-11-10 09:56:52,797ERROR(ajp-/10.116.88.25:13309-7)JBWEB000236: Servlet.service() for servlet jsp threw exception: javax.servlet.jsp.JspException: Erro na montagem do Menu.
5257:2026-11-10 09:56:52,798ERROR(ajp-/10.116.88.25:13309-7)JBWEB000236: Servlet.service() for servlet Controller threw exception: javax.servlet.jsp.JspException: Erro na montagem do Menu.
-sh-4.1$
-sh-4.1$
-sh-4.1$ FJ=$(find / -name "framework.jar" -path "*sipen*" 2>/dev/null | head -1); echo $FJ
^C
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$ mkdir -p /tmp/jc && cd /tmp/jc && unzip -o -q $FJ 'br/gov/caixa/util/jcicsconnect/*'
unzip:  cannot find or open br/gov/caixa/util/jcicsconnect/*, br/gov/caixa/util/jcicsconnect/*.zip or br/gov/caixa/util/jcicsconnect/*.ZIP.

No zipfiles found.
-sh-4.1$
-sh-4.1$
-sh-4.1$ javap -c -l -p br/gov/caixa/util/jcicsconnect/JCicsConnect.class | sed -n '/login(/,/LineNumberTable/p'
Error: class not found: br/gov/caixa/util/jcicsconnect/JCicsConnect.class
-sh-4.1$
-sh-4.1$
-sh-4.1$
