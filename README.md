sed -n '1525,1665p' /log_jboss/sigsj_intranet/sigsj_intranet.log | grep -iE "Caused by|Exception|bemVindo|properties|NullPointer|FileNotFound|Could not|at br.gov.caixa" | head -30
