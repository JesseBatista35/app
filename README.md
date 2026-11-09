ls
for f in *.war *.jar lib/*.jar; do [ -f "$f" ] && mkdir -p "x_$(basename $f)" && unzip -o -q "$f" -d "x_$(basename $f)"; done
grep -rlE 'SIGSJ04|datasources/|persistence-unit|jdbc:oracle' . 2>/dev/null | head
