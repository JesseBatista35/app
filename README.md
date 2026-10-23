Windows PowerShell
Copyright (C) Microsoft Corporation. All rights reserved.

PS C:\Users\p585600> curl -s -X GET "https://sicsn.caixa/BeyondTrust/api/public/v3/Secrets-Safe/Secrets?FolderPath=SIIFX_BATCH_DES" \
Invoke-WebRequest : Não é possível localizar um parâmetro posicional que aceite o argumento
'https://sicsn.caixa/BeyondTrust/api/public/v3/Secrets-Safe/Secrets?FolderPath=SIIFX_BATCH_DES'.
No linha:1 caractere:1
+ curl -s -X GET "https://sicsn.caixa/BeyondTrust/api/public/v3/Secrets ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidArgument: (:) [Invoke-WebRequest], ParameterBindingException
    + FullyQualifiedErrorId : PositionalParameterNotFound,Microsoft.PowerShell.Commands.InvokeWebRequestCommand

PS C:\Users\p585600>   -H "Authorization: Bearer eyJhbGciOiJSUzI1NiIsImtpZCI6IjkwMTk3RTZCLThEMDEtNDg0Ny1CQThELTNCRDdDRDg4QUUxQSIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJodHRwczovL3NpY3NuLmNhaXhhL3BzYXV0aCIsIm5iZiI6MTc5Mjc4MDYzOSwiaWF0IjoxNzkyNzgwNjM5LCJleHAiOjE3OTI3ODQyMzksImF1ZCI6WyJwdWJsaWNhcGkiLCJtb2JpbGVhcHAiLCJodHRwczovL3NpY3NuLmNhaXhhL3BzYXV0aC9yZXNvdXJjZXMiXSwic2NvcGUiOlsicHVibGljYXBpIl0sImNsaWVudF9pZCI6IjA5OGM0ZjQ5LWVmYTUtNDA0Mi1iMTlmLThhOGI1YWZjNzlkMiIsIl9jbGllbnRBY2Nlc3NQb2xpY3lJZCI6IjMzMiIsIl9jbGllbnRVc2VySWQiOiIxOTAyIiwianRpIjoiMzc3Mzg1Nzc3ODczRDRBRkU5MDg5QjYwNzBFNDUwN0IifQ.DiiIfddnnfwlqEAlxS367sAk5cU-Kmg73aGaRJwcN39o37zA-7A_EtPdQGBAKc51I7EPy7ey7v9dpTQddQfeUbiTq8NDzHQHyNqjNrSDPrk8BvgNbtxSQsMuBwwvwjBA-IpyADwrxB-D7KDV3IaNMjgio2o3fQnOFVUP_hhNddy7v4xKJc0sAKE-QfY4kPkp2N_Itiz55xlG-kxj5MlUyQM8T1yvNXw9GG5pRrfYhuiv-lnzR4rVykSIZf4T55yUYgzTncN6GLkhFJaIZSKmjhYnOJ09zPGOAFH1uq3quJRQk-JgcKBRWaU27FTmwBYWMXqqy1HN5zWqmfoNmeVZIQ" \
-H : O termo '-H' não é reconhecido como nome de cmdlet, função, arquivo de script ou programa operável. Verifique a
grafia do nome ou, se um caminho tiver sido incluído, veja se o caminho está correto e tente novamente.
No linha:1 caractere:3
+   -H "Authorization: Bearer eyJhbGciOiJSUzI1NiIsImtpZCI6IjkwMTk3RTZCL ...
+   ~~
    + CategoryInfo          : ObjectNotFound: (-H:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException

PS C:\Users\p585600>   -H "Content-Type: application/json" \
-H : O termo '-H' não é reconhecido como nome de cmdlet, função, arquivo de script ou programa operável. Verifique a
grafia do nome ou, se um caminho tiver sido incluído, veja se o caminho está correto e tente novamente.
No linha:1 caractere:3
+   -H "Content-Type: application/json" \
+   ~~
    + CategoryInfo          : ObjectNotFound: (-H:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException

PS C:\Users\p585600>   -H "Accept: application/json"



Microsoft Windows [versão 10.0.26200.9711]
(c) Microsoft Corporation. Todos os direitos reservados.

C:\Users\p585600>curl -s -X GET "https://sicsn.caixa/BeyondTrust/api/public/v3/Secrets-Safe/Secrets?FolderPath=SIIFX_BATCH_DES" \
"User not authenticated"
C:\Users\p585600>  -H "Authorization: Bearer eyJhbGciOiJSUzI1NiIsImtpZCI6IjkwMTk3RTZCLThEMDEtNDg0Ny1CQThELTNCRDdDRDg4QUUxQSIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJodHRwczovL3NpY3NuLmNhaXhhL3BzYXV0aCIsIm5iZiI6MTc5Mjc4MDYzOSwiaWF0IjoxNzkyNzgwNjM5LCJleHAiOjE3OTI3ODQyMzksImF1ZCI6WyJwdWJsaWNhcGkiLCJtb2JpbGVhcHAiLCJodHRwczovL3NpY3NuLmNhaXhhL3BzYXV0aC9yZXNvdXJjZXMiXSwic2NvcGUiOlsicHVibGljYXBpIl0sImNsaWVudF9pZCI6IjA5OGM0ZjQ5LWVmYTUtNDA0Mi1iMTlmLThhOGI1YWZjNzlkMiIsIl9jbGllbnRBY2Nlc3NQb2xpY3lJZCI6IjMzMiIsIl9jbGllbnRVc2VySWQiOiIxOTAyIiwianRpIjoiMzc3Mzg1Nzc3ODczRDRBRkU5MDg5QjYwNzBFNDUwN0IifQ.DiiIfddnnfwlqEAlxS367sAk5cU-Kmg73aGaRJwcN39o37zA-7A_EtPdQGBAKc51I7EPy7ey7v9dpTQddQfeUbiTq8NDzHQHyNqjNrSDPrk8BvgNbtxSQsMuBwwvwjBA-IpyADwrxB-D7KDV3IaNMjgio2o3fQnOFVUP_hhNddy7v4xKJc0sAKE-QfY4kPkp2N_Itiz55xlG-kxj5MlUyQM8T1yvNXw9GG5pRrfYhuiv-lnzR4rVykSIZf4T55yUYgzTncN6GLkhFJaIZSKmjhYnOJ09zPGOAFH1uq3quJRQk-JgcKBRWaU27FTmwBYWMXqqy1HN5zWqmfoNmeVZIQ" \
'-H' não é reconhecido como um comando interno
ou externo, um programa operável ou um arquivo em lotes.

C:\Users\p585600>  -H "Content-Type: application/json" \
'-H' não é reconhecido como um comando interno
ou externo, um programa operável ou um arquivo em lotes.

C:\Users\p585600>  -H "Accept: application/json"
'-H' não é reconhecido como um comando interno
ou externo, um programa operável ou um arquivo em lotes.

C:\Users\p585600>
C:\Users\p585600>

