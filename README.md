sed -n '120,140p' $B/conf/login-config.xml | sed -E 's#(name="password">)[^<]*#\1***#I'
