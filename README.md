cat /apl/sigsj/properties/config.properties

curl -s -o /dev/null -w "intranet: %{http_code}\n" http://10.116.194.179/sigsj_intranet/default.jsp
