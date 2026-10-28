Agent: azp-ads-agent-build-588fd8b7-9tv2h
Started: Just now

Job preparation parameters
1 queue time variable used



Initialize job

View raw log
Starting: Initialize job
Agent name: 'azp-ads-agent-build-588fd8b7-9tv2h'
Agent machine name: 'ads-agent-build-588fd8b7-9tv2h'
Current agent version: '3.236.1'
Agent running as: 'root'
Prepare build directory.
Set build variables.
Download all required tasks.
Checking job knob settings.
Finished checking job knob settings.
Start tracking orphan processes.
Finishing: Initialize job

Pre-job: Download secure file

View raw log
Starting: Download secure file
==============================================================================
Task         : Download secure file
Description  : Download a secure file to the agent machine
Version      : 1.220.0
Author       : Microsoft Corporation
Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/download-secure-file
==============================================================================
Finishing: Download secure file

Skip to main content
Azure DevOps
projetos
/
Caixa
/
Pipelines
/
SINCH-web-angular20-intra
/
1.0.0-snapshot
Search


Caixa

Overview

Boards

Repos

Pipelines
Pipelines
Environments
Releases
Library
Task groups
Deployment groups
Portal Infra

Test Plans

Artifacts
Project settings

Jobs in run #1.0.0-snapshot
SINCH-web-angular20-intra
Checkout SINCH-web-angular20-intra@feature/atualizacao-angular to s

View raw log
Starting: Checkout SINCH-web-angular20-intra@feature/atualizacao-angular to s
==============================================================================
Task         : Get sources
Description  : Get sources from a repository. Supports Git, TfsVC, and SVN repositories.
Version      : 1.0.0
Author       : Microsoft
Help         : [More Information](https://go.microsoft.com/fwlink/?LinkId=798199)
==============================================================================
Syncing repository: SINCH-web-angular20-intra (Git)
git version
git version 2.52.0
git init "/opt/ads-agent/_work/71/s"
hint: Using 'master' as the name for the initial branch. This default branch name
hint: will change to "main" in Git 3.0. To configure the initial branch name
hint: to use in all of your new repositories, which will suppress this warning,
hint: call:
hint:
hint: 	git config --global init.defaultBranch <name>
Initialized empty Git repository in /opt/ads-agent/_work/71/s/.git/
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint: 	git branch -m <name>
hint:
hint: Disable this message with "git config set advice.defaultBranchName false"
git remote add origin https://devops.caixa/projetos/Caixa/_git/SINCH-web-angular20-intra
git config gc.auto 0
git config --get-all http.https://devops.caixa/projetos/Caixa/_git/SINCH-web-angular20-intra.extraheader
git config --get-all http.extraheader
git config --get-regexp .*extraheader
git config --get-all http.proxy
git config http.version HTTP/1.1
git --config-env=http.extraheader=env_var_http.extraheader -c http.sslVerify=false fetch --force --tags --prune --prune-tags --progress --no-recurse-submodules origin
remote: Azure Repos        
remote: 
remote: Found 2588 objects to send. (99 ms)        
Receiving objects:   0% (1/2588)
Receiving objects:   1% (26/2588)
Receiving objects:   2% (52/2588)
Row 2. Clickable

Showing 17 filtered items.

Get started and run this pipeline for the first time!

Expanded

Finished loading items

Showing 6 items.

Collapsed

Row 2. Clickable

Showing 18 filtered items.

Get started and run this pipeline for the first time!

Row 2. Clickable

Row 2. Clickable



Obtendo branch do Sonar

View raw log
Starting: Obtendo branch do Sonar
==============================================================================
Task         : Bash
Description  : Run a Bash script on macOS, Linux, or Windows
Version      : 3.227.0
Author       : Microsoft Corporation
Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
==============================================================================
Generating script.
========================== Starting Command Output ===========================
/usr/bin/bash /opt/ads-agent/_work/_temp/7343851e-ac14-412e-81b2-aa614bb8ac32.sh
Build originada de uma BRANCH.
Branch que será informada para o SONAR: atualizacao-angular 
Finishing: Obtendo branch do Sonar


Skip to main content
Azure DevOps
projetos
/
Caixa
/
Pipelines
/
SINCH-web-angular20-intra
/
1.0.0-snapshot
Search


Caixa

Overview

Boards

Repos

Pipelines
Pipelines
Environments
Releases
Library
Task groups
Deployment groups
Portal Infra

Test Plans

Artifacts
Project settings

Jobs in run #1.0.0-snapshot
Build Application

Starting: Build Application
==============================================================================
Task         : Bash
Description  : Run a Bash script on macOS, Linux, or Windows
Version      : 3.227.0
Author       : Microsoft Corporation
Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
==============================================================================
Generating script.
========================== Starting Command Output ===========================
/usr/bin/bash /opt/ads-agent/_work/_temp/83a50013-c2e9-4208-9826-c309e1d1ff22.sh
npm test -- --watch=false --code-coverage --browsers=ChromeHeadlessCI ; ng build --configuration production --aot --output-path=dist
<----ANGULAR---->

     _                      _                 ____ _     ___
    / \   _ __   __ _ _   _| | __ _ _ __     / ___| |   |_ _|
   / △ \ | '_ \ / _` | | | | |/ _` | '__|   | |   | |    | |
  / ___ \| | | | (_| | |_| | | (_| | |      | |___| |___ | |
 /_/   \_\_| |_|\__, |\__,_|_|\__,_|_|       \____|_____|___|
                |___/
    

Angular CLI: 19.2.27
Node: 22.13.1
Package Manager: npm 10.9.2
OS: linux x64

Angular: 19.2.25
... animations, common, compiler, compiler-cli, core, forms
... language-service, localize, platform-browser
... platform-browser-dynamic, router

Package                         Version
---------------------------------------------------------
@angular-devkit/architect       0.1902.27
@angular-devkit/build-angular   19.2.27
@angular-devkit/core            19.2.27 (cli-only)
@angular-devkit/schematics      19.2.27
@angular/cli                    19.2.27
@schematics/angular             19.2.27
Row 2. Clickable

Showing 17 filtered items.

Get started and run this pipeline for the first time!

Expanded

Finished loading items

Showing 6 items.

Collapsed

Row 2. Clickable

Showing 18 filtered items.

Get started and run this pipeline for the first time!

Row 2. Clickable

Row 2. Clickable


ESA RODANDO VAMOS AGUARDAR
