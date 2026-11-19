
[root@caddeapllx955 p585600]# sed -n '1525,1665p' /log_jboss/sigsj_intranet/sigsj_intranet.log | grep -iE "Caused by|Exception|bemVindo|properties|NullPointer|FileNotFound|Could not|at br.gov.caixa" | head -30
grep: (entrada padrão): arquivo binário coincide com o padrão
[ERROR] 2026/11/19 14:52:27 facelets.viewhandler[default task-19] - Error Rendering View[/bemVindo.xhtml]
        at br.gov.caixa.sigsj.intranet.filter.ExceptionFilter.doFilter(ExceptionFilter.java:30)
Caused by: java.lang.NullPointerException
        at br.gov.caixa.sigsj.intranet.transaction.sirot.GJ02Transaction.<init>(GJ02Transaction.java:18)
        at br.gov.caixa.sigsj.intranet.dao.sirot.impl.AvisoDAOSirot.detalhar(AvisoDAOSirot.java:63)
        at br.gov.caixa.sigsj.intranet.service.impl.AvisoService.detalhar(AvisoService.java:145)
        at br.gov.caixa.sigsj.intranet.mb.AvisoMB.detalhar(AvisoMB.java:164)
        at br.gov.caixa.sigsj.intranet.mb.AvisoMB.<init>(AvisoMB.java:56)
[ERROR] 2026/11/19 14:52:27 jsf.lifecycle[default task-19] - JSF1054: (Phase ID: RENDER_RESPONSE 6, View ID: /bemVindo.xhtml) Exception thrown during phase execution: javax.faces.event.PhaseEvent[source=com.sun.faces.lifecycle.LifecycleImpl@292b8c3a]
[ERROR] 2026/11/19 14:52:27 webapp.BaseXMLFilter[default task-19] - Exception in the filter chain
javax.servlet.ServletException
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#
