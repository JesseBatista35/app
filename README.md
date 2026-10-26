Configurar Módulo: SIIFX-caixinhas-batch na release, conforme detalhamento em REQ

Módulo: SIIFX-caixinhas-batch
Na release foi configurada uma etapa nova "Correção Artefato Final SIIFX-CAIXINHAS-BATCH", porem no seu código, o nome do artefato informado para URL_CORRETA está fixo. Esse favor pode ser alterado a cada release, devendo ser informado o artefato gerado pelo último Reactor Maven do processo de Build. 

URL da Release: https://devops.caixa/projetos/Caixa/_releaseDefinition?definitionId=6461&_a=definition-tasks&environmentId=29609


<img width="1770" height="925" alt="image" src="https://github.com/user-attachments/assets/782291b3-a9a4-4400-9c01-3b437e9fb4e3" />



<img width="1103" height="711" alt="image" src="https://github.com/user-attachments/assets/ed1600a2-5b11-467c-a3db-b920ea5d0fe3" />





URL_CORRETA="http://binario.caixa:8081/repository/snapshots/br/gov/caixa/siifx/caixinhas/siifx-caixinhas-batch/0.0.7-SNAPSHOT/siifx-caixinhas-batch-0.0.7-20260922.183950-1.jar"

mkdir -p "$(System.DefaultWorkingDirectory)/binario"

curl -f "$URL_CORRETA" \
-o "$(System.DefaultWorkingDirectory)/binario/siifx-caixinhas-batch-0.0.7-20260922.183950-1.jar"

ls -l "$(System.DefaultWorkingDirectory)/binario"

echo "##vso[task.setvariable variable=URL_DEPLOY]$URL_CORRETA"
