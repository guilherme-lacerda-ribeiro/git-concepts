# git-concepts
Conceitos e práticas no uso do git.\
Repositórios existem locais e remotos.

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

[Commit](commit/README.md)

### Push
Envia as mudanças para o repositório\
`git push origin main`\
Faz o upload dos arquivos.\
origin é o apelido do repositório localmente (`git remote`)

