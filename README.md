
Robson, analisando o log de falha do job CX_101-abertura-movimento-aporte, são dois problemas diferentes, e os dois são do lado da aplicação — não é algo que eu, como esteiras NPRD, consiga corrigir, precisa de ação de vocês:

1. Script com erro de encoding

/producao/executa-job.sh: linha 1: ï»¿#!/usr/bin/bash: Arquivo ou diretório inexistente
/producao/env_config.sh: linha 47: export: `=': não é um identificador válido

O arquivo /producao/executa-job.sh foi salvo com um BOM (marca de encoding UTF-8) no início, provavelmente editado em Windows/Notepad — isso quebra o shebang (#!/usr/bin/bash) e o Linux não reconhece o interpretador. Precisa resalvar esse arquivo em UTF-8 sem BOM (no vi: :set nobomb antes de salvar, ou sed -i '1s/^\xEF\xBB\xBF//' /producao/executa-job.sh).

Além disso, o /producao/env_config.sh, linha 47, tem um export = sem nome de variável — erro de sintaxe que precisa ser corrigido direto no arquivo.

2. Autenticação no BeyondTrust
O passo “Gerar token” retornou 400 - invalid_client — isso indica que o ClientID/Secret configurado no Connection Profile IIFX (produção) não está sendo aceito pelo BeyondTrust no momento. Precisa confirmar com o time do cofre se essa credencial está ativa e correta.

Por causa desses dois problemas juntos, o job não consegue nem autenticar nem buscar as variáveis DB_PASS e SIIFX_DATAGRID_PASS.

Fico à disposição se precisar de algo do lado do Control-M, mas a correção do script e a validação da credencial são com vocês.
