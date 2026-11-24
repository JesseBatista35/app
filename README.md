Mensagem pro Rafael (Augusto/Guimarães):

Rafael, boa tarde! Seguindo tua orientação do SIGCX-config, montei a entrega de config externa do SIGSJ pela esteira. Usando o SIGSJ-intranet-config como exemplo, ficou assim:

configuration/
├── custom.sh
└── properties/
    ├── sigsj_intranet.xml   (log4j)
    ├── config.properties
    ├── b2b.properties
    └── release.properties

O custom.sh move esses arquivos de /opt/jboss-eap/standalone/configuration/properties/ pro destino final na VM (/log_jboss/config-log4j/ e /apl/sigsj/properties/). Em DES funcionou 100%.

Minha dúvida é sobre os múltiplos ambientes (DES, TQS, PRD): os valores desses properties mudam por ambiente (ex.: sigsj.ambiente, URLs de convivência/SIMTR/B2B). Qual o modelo que vocês recomendam seguir?

Replace Tokens + Library — deixar os arquivos com placeholders (ex.: __CONVIVENCIA_URL__) e os valores na Library por stage (EC DES/TQS/PRD), igual ao standalone-full-ha.xml. Nesse caso, o passo de Replace Tokens da esteira processa os arquivos dentro de configuration/properties/? Ou ele só pega os arquivos padrão (standalone, etc.)?
Pasta por ambiente — ter configuration/properties/des, .../tqs, .../prd e o custom.sh escolher a pasta pelo __SistemaAmbiente__, no mesmo espírito do so/etc/host-{{ambiente}} do template.

Qual dos dois é o padrão suportado? Quero deixar já preparado pra TQS e PRD sem precisar de ajuste manual. Valeu!
