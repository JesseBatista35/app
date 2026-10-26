<img width="1414" height="332" alt="image" src="https://github.com/user-attachments/assets/dcc9da31-cf43-4fbc-a3a7-50e5d0f37973" />


a qustao é que eles ntao tem beyundtrust e eles usam como se tivemsem 

e aidna fora do padrao pois o padrao é esse

SISTEMA-MODULO-BT-VAULT-(AMBIENTE), contendo a variável:
 
BT_SECRETS_LIST
 
 
SISTEMA-BT-VAULT-SECRET-(AMBIENTE), contendo as variáveis:
 
BT_CLIENT_ID

BT_CLIENT_SECRET



 A TAKS  VAULT_OKD É task group vairo projetuos usam e ela e o script dela tem isso


app="$(REPOSITORIO)-$(AMBIENTE)"

oc get configmaps vault-$(REPOSITORIO) -n $(PROJETO)-$(AMBIENTE)
if [ "$?" -ne "1" ]; then
oc delete configmap vault-$(REPOSITORIO) -n $(PROJETO)-$(AMBIENTE)
fi

oc create configmap vault-$(REPOSITORIO) --from-file=$(System.DefaultWorkingDirectory)/$(Release.PrimaryArtifactSourceAlias)-config/configuration/vault-$(AMBIENTE)/VAULT.dat -n $(PROJETO)-$(AMBIENTE)

oc set volume $(KIND_DEPLOY) $app --add --name=vault-$(REPOSITORIO) --configmap-name=vault-$(REPOSITORIO)  --mount-path=/opt/jboss/standalone/configuration/VAULT.dat --sub-path=VAULT.dat --overwrite -n $(PROJETO)-$(AMBIENTE)
