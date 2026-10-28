REPO=$(echo $(Release.PrimaryArtifactSourceAlias) | sed 's/_//')
echo ansible-playbook $(HOME_ADS_AGENT)/$(DIR_ANSIBLE)/site.yml --tags sigdb --skip-tags "vm,monitoracao,autenticacao,git_conf,tsm,controlm"


ansible-playbook $(HOME_ADS_AGENT)/$(DIR_ANSIBLE)/site.yml --tags sigdb --skip-tags "vm,monitoracao,autenticacao,git_conf,tsm,controlm" -e sistema_ambiente=$(sistema_ambiente) -e sistema_nome=$(sistema_nome) -e site=$(site) -e source_dir_sigdb=$(System.DefaultWorkingDirectory)/$(Release.PrimaryArtifactSourceAlias)-config/sigdb/$(sistema_ambiente)/ -e source_dir_sigdb_service=$(System.DefaultWorkingDirectory)/$(Release.PrimaryArtifactSourceAlias)-config/sigdb/sigdb


<img width="1874" height="905" alt="image" src="https://github.com/user-attachments/assets/c80a0ef9-45fd-4dd2-81ad-5bea3d1bd68e" />
