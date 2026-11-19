for f in b2b.properties config.properties release.properties; do echo "==== $f ===="; sed -E 's#(senha|password|pwd|secret)[[:space:]]*=.*#\1=***#I' /apl/sigsj/properties/$f; done
