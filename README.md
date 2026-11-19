# pega o bloco do teste das 11:32, ignorando o ruído da página de erro
grep -n "2026/11/19 11:32\|11:32:" /log_jboss/sigsj_internet/sigsj_internet.log | head -20

# e o primeiro ERROR do horário com o que vem logo depois (a causa raiz)
awk '/11:32:3[0-6]/{p=1} p' /log_jboss/sigsj_internet/sigsj_internet.log | grep -vE "erro\.jsp|error_jsp|erro_jsp|ExceptionFilter.forwardErrorPage|generating error page" | grep -A25 -iE "ERROR|Exception|Caused by" | head -60
