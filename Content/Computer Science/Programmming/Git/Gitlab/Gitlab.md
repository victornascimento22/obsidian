
[[Gitlab]]

clonar git clone --branch dev --single-branch git@gitlab.com:applications2285147/api-go.git

S.O.S 

git reset --soft HEAD~1

Esse comando:

1. **Remove o commit mais recente**, como se ele nunca tivesse acontecido.
2. **Mantém todas as alterações no stage**, prontas para um novo commit.
3. **Não altera os arquivos no disco**, então nada foi perdido.
git reset nome-do-arquivo

Isso fez com que:  
✅ O arquivo saísse do **stage**, ou seja, ele não entraria no novo commit.  
✅ O arquivo **continuasse no disco**, então você não perdeu nada.

Se em vez disso tivéssemos usado `git rm nome-do-arquivo`, o Git teria **removido o arquivo do disco também**, o que não era o que você queria.


O `--force`:  
✅ Substitui o commit antigo pelo novo no repositório remoto.  
✅ Remove qualquer rastro do commit anterior.  
✅ Pode causar problemas **se outras pessoas já tiverem feito pull do commit antigo**, então use com cuidado!