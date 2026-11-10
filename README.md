foreach ($ext in "pom","jar") { curl.exe -s -k -o NUL -w "$ext %{http_code} %{size_download}B`n" "https://binario.caixa/repository/caixa-group-br/br/gov/caixa/arqref/arqref-services/3.31.0/arqref-services-3.31.0.$ext" }


<arqref-services.version>3.31.0</arqref-services.version>
