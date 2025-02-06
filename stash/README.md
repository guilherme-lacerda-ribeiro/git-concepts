# Stash
Engaveta (guarda) uma alteração para continuar trabalhando depois. Ainda não está no estado compilável, está no meio do caminho e não vai dar um commit porque não está funcional, executável.\
Se tentar recuperar (pop) mais de uma vez envolvendo o mesmo arquivo ele não deixa, propondo que primeiramente seja feito o commit do que já está local e aí sim recuperar novamente (pop).

`git stash`
Pega tudo o que está no momento atual e guarda, desfazendo.

`git stash pop`
Retorna o trabalho que foi guardado.\
Conceito de pilha, sempre aplica a última que foi guardada.

`git stash list`
O que está armazenado.

`git stash clear`
Apaga tudo que estava armazenado.

`git stash push -m "Nome descritivo"`
Mensagem descritiva.

`git stash apply {indice}` ou seja, `git stash apply 1`
Recupera um armazenamento específico.

## Apply
O comando git stash apply espera um índice de um item na stash e o aplica ao repositório, porém, esse comando não remove o item da stash, ou seja, se após executar o comando git stash apply 1 você executar git stash list, o item referente ao índice 1 continuará na stash.

## Pop
O git stash pop faz exatamente a mesma coisa que o git stash apply, porém, além de aplicar o item da stash, ele também o remove de lá. Esse comando, sem nenhum parâmetro extra, vai aplicar o último item adicionado à stash, mas nós também podemos informar um índice para ele, como git stash pop 1.

## Drop
O git stash drop funciona exatamente como o pop, mas com uma simples diferença: ele apenas remove o item da stash, sem aplicá-lo em nosso repositório. Dessa forma, git stash drop remove o último item adicionado à stash, enquanto o git stash drop 1 remove da stash o item com índice 1.