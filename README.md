Substitua o script por este, sem aspas:

bash
ls -l /usr/java/open-jdk-17.0.8/bin/javac
echo ##vso[task.prependpath]/usr/java/open-jdk-17.0.8/bin

Se o editor do Azure DevOps estranhar o # sem aspas, use aspas simples digitadas à mão:

bash
echo '##vso[task.prependpath]/usr/java/open-jdk-17.0.8/bin'
