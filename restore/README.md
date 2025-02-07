# Restore
Restaura para o HEAD.

`git restore .`
Restaura tudo, desfazendo as alterações implementadas até o momento do HEAD.

`git checkout -- .` ou `git checkout .`
Antigo, mesmo efeito do `git restore .`

`git restore --staged <arquivo>`
Desfaz o git add.

## Viajar no tempo

`git restore --source=<id_do_commit> arquivo`
Traz o _arquivo_ para o _id_do_commit_

`git restore arquivo`
Já vi como estava o arquivo no momento do _id_do_commit_, agora volto o arquivo para o commit HEAD atual. Ou seja, equivalente ao `git restore --source=HEAD arquivo`.

