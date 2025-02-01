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

## Comandos
`git commit -a -m "mensagem"`\
Adiciona tudo e faz commit.

`git log`\
Histórico dos commits.

## Coautoria
[Documentação](https://docs.github.com/pt/pull-requests/committing-changes-to-your-project/creating-and-editing-commits/creating-a-commit-with-multiple-authors).

```shell
git commit -m "Refactor usability tests.
>
>
Co-authored-by: NAME <NAME@EXAMPLE.COM>
Co-authored-by: ANOTHER-NAME <ANOTHER-NAME@EXAMPLE.COM>"
```
