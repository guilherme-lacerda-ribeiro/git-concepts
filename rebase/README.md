# Rebase
Ele cria uma linha de base contínua, considerando que o branch foi atualizado e o main também. Então ele "alinha" os commits tentando inserir todas as atualizações realizadas no main antes do primeiro commit no branch.
![alt text](010-branch-e-main.png)
![alt text](020-rebase-done.png)

1. `git checkout -b main`
1. `git branch -d master`
1. `git commit`
1. `git branch funcionalidade`
1. `git commit`
1. `git commit`
1. `git commit`
1. `git checkout funcionalidade`
1. `git commit`
1. `git commit`
1. `git rebase main`