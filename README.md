# git-concepts
Conceitos e práticas no uso do git.\
Repositórios existem locais e remotos.

## Fluxo de trabalho
1. git status
1. git add / commit / push
1. git pull

## Identidade
ssh melhor que https

Autor dos commits:\
git config --global user.email "email@email.com"\
git config --global user.name "nome completo"

## Colaborar
**Issues**: novos recursos ou correções.\
**Fork** do projeto para minha máquina.\
**Pull Request** para integrar ao repositório.

## Comandos
### Remote
`git remote -v`\
(push) - envio de commits\
(fetch) - baixar commits

Conectar código local a um diretório remoto\
`git remote add origin git@......`\
Último parâmetro informado no repositório mesmo.

[Commit](commit)

### Push
Envia as mudanças para o repositório\
`git push origin main`\
Faz o upload dos arquivos.\
origin é o apelido do repositório localmente (`git remote`)

### Pull
Baixar os commits do repositório remoto para o repositório local.\
`git pull origin main`\
origin - qual é o repositório remoto que vou baixar (origin é o apelido)\
main - branch main para onde vai trazer os commits
