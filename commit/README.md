# Commit
Cada commit é semelhante a um [snapshot](https://git-scm.com/book/pt-br/v2/Come%C3%A7ando-O-B%C3%A1sico-do-Git) e registra um marco no cronograma do projeto.

## Propósito
Fazer sempre que finalizar uma tarefa ou resolver um bug.

A ideia é manter histórico claro e rastreável.

Registra as mudanças, como se fosse a versão 1, 2, 3...

## Melhores práticas
Commit sempre de código funcional.

Use mensagens simples mas objetivas.

Verbo + ação: Adicionar... Corrigir... Atualizar...

Referência [melhores práticas](https://www.conventionalcommits.org/pt-br/v1.0.0-beta.4/).

## Comandos
`git commit -a -m "mensagem"`\
Adiciona tudo e faz commit.

`git log`\
Histórico dos commits.

`git commit --amend -m "Nova mensagem"`\
Alterar o commit realizado

## Coautoria
[Documentação](https://docs.github.com/pt/pull-requests/committing-changes-to-your-project/creating-and-editing-commits/creating-a-commit-with-multiple-authors).

```shell
git commit -m "Refactor usability tests.
>
>
Co-authored-by: NAME <NAME@EXAMPLE.COM>
Co-authored-by: ANOTHER-NAME <ANOTHER-NAME@EXAMPLE.COM>"
```

## cherry-pick
Aplica o commit de um branch em outro branch, por exemplo por causa de funcionalidades que ambas tenham dependência de um mesmo trecho de código mas uma pessoa já implementou (criação de uma tabela por exemplo).

1. `git switch {branch1}`
Vou para o branch que desejo **aplicar** as mudanças.
1. `git log {branch2}`
Visualizo os logs dos commits do branch que vou **buscar** as mudanças.
1. `git cherry-pick <id_do_commit>`
Aplico as mudanças realizadas no commit do _branch2_ dentro do meu repositório _branch1_.
1. Demais procedimentos `git log`, `git push origin`, `git switch main`, `git merge branch1`, `git merge branch2`, `git push origin main`.


## blame: Quem fez o que
Mostra quais linhas foram modificadas por quem.\
O comando git blame exibe todas as linhas de determinado arquivo com uma informação extra: o autor (e hash) do último commit que tocou cada uma dessas linhas. Dessa forma ele pode ver quais pessoas já podem ter trabalhado na função citada no exercício e fazer as perguntas para essas pessoas.

`git blame index.html`
Indica quem fez quais alterações no arquivo _index.html_. Na sequência posso dar um `git show <id_do_commit>` para ver os detalhes do commit.

O acento circunflexo ^ indica que é o commit inicial, quem criou o arquivo.
