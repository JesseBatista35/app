<img width="1882" height="606" alt="image" src="https://github.com/user-attachments/assets/dd40b93e-fcbd-4998-99f4-a1c5f1451061" />


Skip to main content
Azure DevOps
projetos
/
Caixa
/
Pipelines
/
Releases
/
SIAME-Android-Nativo
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
All pipelines

SIAME

SIAME-Android-Nativo
Predefined variables
Filter by keywords
Scope


AdapterGroupId
$(PackageId)
build.tools
30.0.3
BuildGradle
gradle clean assemble$(typeApp) lint$(typeApp) -PversionApp=$(versionApp) -PversionCode=${CodeNew} -PunicoSdkKey=$(UNICO_BIOMETRIC_SDK_KEY)
BuildGradle
gradle clean assemble$(typeApp) -PversionApp=$(versionApp) -PversionCode=${CodeNew}
BuildGradle
gradle clean assemble$(typeApp) -PversionApp=$(versionApp) -PversionCode=${CodeNew}
BuildGradle
gradle clean assemble$(typeApp) -PversionApp=$(versionApp) -PversionCode=${CodeNew}
FIREBASE_ID_APP
1:978309264263:android:fb2ea54ff4fdfdc1b95922
FIREBASE_NOTE

FIREBASE_NOTES
$(versionApp)-$(typeApp).$(versionBuild)-Nativo $(FIREBASE_NOTE)
FORTIFY_BUILD
assemble$(typeApp)
GradleVersion
8.11.1
JavaVersion
17.0.7
nameApp
habitacao
nameAppNexus
$(nameApp)
OldVersionApp
4.6.2
Patch
$[counter(variables['versionApp'],1)]
system.debug
true
UNICO_BIOMETRIC_SDK_KEY
r001-08d8bc7e-cb20-4cf4-b501-9db7f4b81e1a
versionApp

versionBuild
$(RELEASE.RELEASEID)
versionCode

Showing filters 1 through 2

Showing filters 1 through 2

Showing filters 1 through 2

Skip to main content
Azure DevOps
projetos
/
Caixa
/
Pipelines
/
Releases
/
SIAME-Android-Nativo
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
All pipelines

SIAME

SIAME-Android-Nativo
Predefined variables
ANDROID_VARIABLES-Caixakeystore-RELEASE (3)
Variáveis disponíveis para assinatura Caixakeystore projetos ANDROID

Scopes: Release
Alias_KeyStore
"caixa keystore"
KeyStore
Caixakeystore
KeyStorePass
********
Usuario-Azure-DevOps (12)
Scopes: Release
AZPAT
********
AZUSER
s736639
BT_API_URL
https://sicsn.caixa/BeyondTrust/api/public/v3
BT_SECRETS_PATH
********
FORTIFY_API
https://novocodigoseguro.caixa/ssc/api/v1
FORTIFY_APITOKEN
********
FORTIFY_PASS
********
FORTIFY_USER
admin
OKD_KAFKA
api.kafka-nprd.caixa:6443
OKD_TOKEN_KAFKA
********
TOKEN_CRQ
********
URL_CRQ
https://infradevops-novoportal-backend-prd.apps.produtos4.caixa/api.php?acao=devopsCaixacriarMudancaPadrao
ANDROID_VARIABLES-RELEASE (16)
Variáveis genéricas disponíveis para todos os projetos ANDROID
Scopes: Release
ApiJsonGoogle
********
FIREBASE_TOKEN
********
GRADLE_PATH
build.gradle
GitName
devops.caixa/projetos/Caixa/_git/$(BUILD.REPOSITORY.NAME)
GitToken
$(AZPAT)
GitUrl
https://devops.caixa/projetos/98fe0311-ffd2-418a-9d0d-507043380abd/_apis/git/repositories/$(BUILD.DEFINITIONID)
GitUser
$(AZUSER)
GradleVersion
$(awk '/distributionUrl/ {print $0}' $(System.DefaultWorkingDirectory)/$(Release.PrimaryArtifactSourceAlias)/gradle/wrapper/gradle-wrapper.properties | sed 's/.*gradle-\(.*\)-.*/\1/g')
JAVA_HOME
/opt/ferramentas/jdk/jdk$(JavaVersion)
MobileFirst
$(Release.DefinitionName)-$(Release.EnvironmentName)
NexusUrl
http://binario.caixa:8081/repository/caixa-adapters-zip/
PackageId
$(awk '/applicationId/ {print $2}' $(System.DefaultWorkingDirectory)/$(Release.PrimaryArtifactSourceAlias)/app/build.gradle | sed 's/"//g')
Platform
android
SonarProjectKey
$(Release.DefinitionName)
SonarProjectName
$(Release.DefinitionName)
build.artifactStagingDirectory
$(SYSTEM.ARTIFACTSDIRECTORY)
ANDROID_VARIABLES-SIAME-APPHAB-NATIVO-TQS (9)
Variáveis disponíveis para o projeto SIAME APP ANDROID NATIVO - Etapa TQS.
Scopes: TQS,TQS - Firebase
FIREBASE_GROUPS
teste-de-qualidade
MfpPassword
********
MfpServerIp
10.116.94.107
MfpServerPort
9080
MfpUser
s7562293
N
0
dirApp
apk
extApp
$(dirApp)
typeApp
Dev
BUILD_VARIABLES (58)
Variáveis disponíveis para todas as builds.
Scopes: TQS
ANSIBLE_INVENTORY
$(HOME_ADS_AGENT)/$(DIR_ANSIBLE)/hosts
AZPAT
********
AZUSER
s736639
DIR_ANSIBLE
esteira-qa
DOTNET_TESTARGS
--configuration Release --collect "code coverage"
FORTIFY_API
https://novocodigoseguro.caixa/ssc/api/v1
FORTIFY_APITOKEN
********
FORTIFY_BUILD_FILE
.
FORTIFY_CI_TOKEN
********
FORTIFY_CLIENT_AUTH_TOKEN
********
FORTIFY_PASS
********
FORTIFY_POOL_COMPLEX_NOVO
55e6b358-710a-4c3d-ad15-4a3ec96c3dca
FORTIFY_POOL_DIAMOND_NOVO
9fa96d5a-3b13-4ecb-8639-e2ec97d1b4e9
FORTIFY_POOL_GOLD_NOVO
1a3e11fe-719a-475a-905b-e61b743e550d
FORTIFY_POOL_MONOLITO_NOVO
7c2e05fb-2f1d-4045-ac12-69c806df50be
FORTIFY_POOL_SILVER_NOVO
794601f7-da27-467b-a734-06f92c4d63aa
FORTIFY_REGEX
'(?:\*\/)?(\d{1,3}\.\d{1,3}\.\d{1,3})'
FORTIFY_REGISTRY_PASSWORD
********
FORTIFY_REGISTRY_USERNAME
ads-sa
FORTIFY_SENSOR_VERSION
24.4
FORTIFY_TOKEN
********
FORTIFY_UPTOKEN
********
FORTIFY_URL
https://sast.caixa/ssc
FORTIFY_URL_CONTROLLER
http://sast.caixa/scancentral-ctrl
FORTIFY_USER
admin
HOME_ADS_AGENT
/opt/ads-agent
KEYSTORE_PWD
********
KEYSTORE_SECUREFILEPATH
/etc/pki/ca-trust/source/anchors/keystore-ssc24.jks
NEXUS_REPOSITORY_ID
NEXUS_INTERNO
NEXUS_URL_ANGULAR_RELEASE
http://binario.caixa:8081/repository/caixa-raw-releases/angular
NEXUS_URL_ANGULAR_SNAPSHOT
http://binario.caixa:8081/repository/caixa-raw-snapshots/angular
NEXUS_URL_ASP_RELEASE
http://binario.caixa:8081/repository/caixa-raw-releases/asp
NEXUS_URL_ASP_SNAPHOT
http://binario.caixa:8081/repository/caixa-raw-snapshots/asp
NEXUS_URL_CAIXA_GROUP
http://binario.caixa:8081/repository/caixa-group-br/
NEXUS_URL_DOTNET_RELEASE
http://binario.caixa:8081/repository/caixa-raw-releases/dotnet
NEXUS_URL_DOTNET_SNAPSHOT
http://binario.caixa:8081/repository/caixa-raw-snapshots/dotnet
NEXUS_URL_MAVEN_RELEASE
http://binario.caixa:8081/repository/releases
NEXUS_URL_MAVEN_SNAPSHOT
http://binario.caixa:8081/repository/snapshots
NEXUS_URL_NODE_INTERNAL_RELEASE
http://binario.caixa:8081/repository/npm-internal
NEXUS_URL_NODE_RELEASE
http://binario.caixa:8081/repository/caixa-raw-releases/node
NEXUS_URL_NODE_SNAPSHOT
http://binario.caixa:8081/repository/caixa-raw-snapshots/node
NEXUS_URL_NPM_RELEASE
http://binario.caixa:8081/repository/caixa-npm-releases/
NEXUS_URL_NPM_SNAPSHOT
http://binario.caixa:8081/repository/caixa-npm-snapshots/
NEXUS_URL_PHP_RELEASE
http://binario.caixa:8081/repository/caixa-php-releases
NEXUS_URL_PHP_SNAPSHOT
http://binario.caixa:8081/repository/caixa-php-snapshots
NEXUS_URL_RAW_RELEASE
http://binario.caixa:8081/repository/caixa-raw-releases
NEXUS_URL_RAW_SNAPSHOT
http://binario.caixa:8081/repository/caixa-raw-snapshots
NEXUS_URL_ZCONBT_RELEASE
http://binario.caixa:8081/repository/caixa-raw-releases/zconbt
NEXUS_URL_ZCONBT_SNAPSHOT
http://binario.caixa:8081/repository/caixa-raw-snapshots/zconbt
NODE_EXTRA_CA_CERTS
/etc/pki/ca-trust/source/anchors/AC-V4.cer
SCANCENTRAL_URL
http://scancentral.apps.produtos4.caixa/scancentral-ctrl
SSC_URL
https://novocodigoseguro.caixa/ssc
ScanCentral.ClientToken
********
ScanCentral.SscCiToken
********
fortify_disable
false
nexus_interno_pass
********
nexus_interno_user
pipeline-agil
sonar_disable
false
ANDROID_VARIABLES-SIAME-APPHAB-NATIVO-HMP (5)
Variáveis disponíveis para o projeto SIAME APP ANDROID NATIVO - Etapa HMP.
Scopes: HMP,HMP - Firebase,HMP - Google Play
FIREBASE_GROUPS
teste-de-certificacao
N
0
dirApp
apk
extApp
$(dirApp)
typeApp
Hmp
ANDROID_VARIABLES-SIAME-APPHAB-NATIVO-PILOTO (5)
Variáveis disponíveis para o projeto SIAME APP ANDROID NATIVO - Etapa PILOTO.
Scopes: PILOTO,PILOTO - Google Play
FIREBASE_GROUPS
teste-de-certificacao
N
1
dirApp
apk
extApp
apk
typeApp
Piloto
SIECO-ANDROID-PRD (4)
Scopes: PRD,PRD - Google Play
N
2
dirApp
apk
extApp
apk
typeApp
Producao
|Manage variable groups
Showing filters 1 through 2

Showing filters 1 through 2

Showing filters 1 through 2



entoa pelo o historui co thiago jeferson meu amigo analista fizemos as alteraçoes, 11h ele rodou a rele===uma nova relasea as 14h 

e tameb m fez atelraçoes ali. 
