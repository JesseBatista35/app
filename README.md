$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec sisei-mgi-des-175-wmccw -c sisei-mgi-des -- sh -c 'grep -c "BEGIN CERTIFICATE" /opt/app-root/src/sisei_nprd.crt'
20
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec sisei-mgi-des-175-wmccw -c sisei-mgi-des -- sh -c 'cd /opt/app-root/src; awk "/BEGIN/{c=\"\"} {c=c \$0} /END/{print c}" sisei_nprd.crt | sort -u > /tmp/a.lst; awk "/BEGIN/{c=\"\"} {c=c \$0} /END/{print c}" sisei_nprd_082026.crt | sort -u > /tmp/b.lst; echo "antigo que NAO esta no novo:"; comm -23 /tmp/a.lst /tmp/b.lst | wc -l'
antigo que NAO esta no novo:
11
-sh-4.2$
