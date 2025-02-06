# Tag
Checkpoint criado na linha dos commits para se referenciar a uma versão do projeto. Por exemplo, a partir dali foi gerada a versão 0.1.0 do projeto.

A tag nunca vai se mover, vai sempre apontar para aquele commit.

No github, cada tag aparece na opção releases.

`git tag {nome}` por exemplo `git tag v0.1.0`
Cria para o HEAD.

`git tag {nome} <id_commit>`
Cria a tag para qualquer commit do histórico.

`git tag`
Exibe todas as tags.

`git push origin {nome}`
Envia a tag _{nome}_ para o repositório remoto.

`git push origin --tags`
Envia todas as tags.

`git tag -d {nome}`
Apaga a tag localmente.

## Anotated tags
Funcionam como um commit.

`git tag {nome} -m "Lançamento da versão tal"`
Tags com informações adicionais, annotated.

`git tag -v {nome}`
Informações completas da tag.
Se tentar isso paga uma tag sem mensagem não vai funcionar.
