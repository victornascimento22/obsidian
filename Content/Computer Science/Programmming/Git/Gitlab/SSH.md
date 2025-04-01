[[Gitlab]]

ls ~/.ssh

ssh-keygen -t rsa -b 4096 -C "equipesi@capitaltrade.srv.br"

- Iniciar o agente SSH
eval $(ssh-agent -s)

- adicionar chave ao agente
ssh-add ~/.ssh/id_rsa

- exibir a chave ssh
cat ~/.ssh/id_rsa.pub

teste pra ver se funciona

ssh -T git@gitlab.com



