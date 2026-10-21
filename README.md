Windows PowerShell
Copyright (C) Microsoft Corporation. All rights reserved.

PS C:\Users\p585600> timeout 5 bash -c 'cat < /dev/null > /dev/tcp/10.116.100.127/1433' && echo OK || echo FALHA
No linha:1 caractere:68
+ ... 5 bash -c 'cat < /dev/null > /dev/tcp/10.116.100.127/1433' && echo OK ...
+                                                                ~~
O token '&&' não é um separador de instruções válido nesta versão.
No linha:1 caractere:79
+ ... cat < /dev/null > /dev/tcp/10.116.100.127/1433' && echo OK || echo FA ...
+                                                                ~~
O token '||' não é um separador de instruções válido nesta versão.
    + CategoryInfo          : ParserError: (:) [], ParentContainsErrorRecordException
    + FullyQualifiedErrorId : InvalidEndOfLine

PS C:\Users\p585600>
