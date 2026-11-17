ps -ef | grep -oE 'jboss\.domain\.[a-z.]*dir=[^ ]*|--domain-config=[^ ]*' | sort -u
