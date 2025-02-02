# git-concepts
Conceitos e práticas no uso do git.\
Repositórios existem locais e remotos.\
HEAD - Branch atual `cat .git/HEAD`

## Fluxo de trabalho
1. git status
1. git add / commit / push
1. git pull
1. git status / [diff](https://git-scm.com/docs/git-diff/pt_BR)

## Identidade
ssh melhor que https

Autor dos commits:\
git config --global user.email "email@email.com"\
git config --global user.name "nome completo"

## Colaborar
1.  **Issues**: novos recursos ou correções.
1. **Fork** do projeto para minha máquina.
1. **Pull Request** para integrar ao repositório.

## Comandos
### Remote
Origin é o nome do repositório remoto, na verdade o apelido.

`git remote -v`\
(push) - envio de commits\
(fetch) - baixar commits

Conectar código local a um diretório remoto\
`git init && git remote add origin git@......`\
Último parâmetro informado no repositório mesmo.

[Commit](commit)

### Push
Envia as mudanças para o repositório\
`git push origin main`\
Faz o upload dos arquivos.\
origin é o apelido do repositório remoto (`git remote`)

### Pull
Baixar os commits do repositório remoto para o repositório local.\
`git pull origin main`\
origin - qual é o repositório remoto que vou baixar (origin é o apelido)\
main - branch main para onde vai trazer os commits

### Conflito
Havendo **conflito** resolvo ele manualmente no código ou uso o [merge editor](https://learn.microsoft.com/pt-br/visualstudio/version-control/git-resolve-conflicts?view=vs-2022) e faço um commit apenas da resolução do conflito.

["The base"](https://www.youtube.com/watch?v=HosPml1qkrg&ab_channel=VisualStudioCode) - referência de resolução de conflito comparando ambos com o baseline.

### Revert
Preciso reverter uma modificação aplicada em algum commit.\
Faço o `git log` para obter o ID do commit.\
Reverto usando `git revert <ID>`.\
Verifico o arquivo gerado que será o novo commit relacionado a este revert e em seguida fecho ele.\
`git add / push`.

### Reset
Apaga um commit.\
`git reset --hard <ID>`\
O ID é do commit que estará vigente no código atual, então desfaz tudo até o commit informado. Não informo o commit para apagar, mas informo o commit que quero que seja o estado do código atual (HEAD).\
**NÃO apagar** se já tiver feito o push para evitar confusão no histórico.
[Documentação](https://git-scm.com/docs/git-reset/pt_BR).

