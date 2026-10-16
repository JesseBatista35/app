oc exec sisei-mgi-des-175-wmccw -c sisei-mgi-des -- sh -c 'cd /opt/app-root/src; awk "{sub(/\r$/,\"\")} /BEGIN/{c=\"\"} {c=c \$0} /END/{print c}" sisei_nprd.crt | sort -u > /tmp/a.lst; awk "{sub(/\r$/,\"\")} /BEGIN/{c=\"\"} {c=c \$0} /END/{print c}" sisei_nprd_082026.crt | sort -u > /tmp/b.lst; echo faltando:; comm -23 /tmp/a.lst /tmp/b.lst | wc -l; which openssl'



oc extract secret/sisei-nprd -n sisei-des --to=. && cat sisei_nprd.crt


