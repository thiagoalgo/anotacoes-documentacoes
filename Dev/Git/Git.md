# Git

## Rebase na branch local atual pegando o que está na main remota

```bash
git fetch origin 
git rebase origin/main 
git push --force-with-lease
```

Entendendo os comandos acima:

- `git fetch origin`: Atualiza seu repositório local com as mudanças do repositório remoto, sem aplicar essas mudanças.
- `git rebase origin/main`: Reaplica suas mudanças no topo das mudanças mais recentes do branch `main` remoto, criando uma história de commits mais linear.
- `git push --force-with-lease`: Força o envio dos commits para o repositório remoto, mas verifica se houve alterações no branch remoto desde seu último fetch para evitar sobrescrever o trabalho de outros.
## Reverter alterações de arquivo

```bash
# Arquivo único
git checkout -- <nome_do_arquivo>

# Todos os arquivos
git checkout -- .
```

## Visualizar o que foi alterado no arquivo local:

```bash
git diff <nome_do_arquivo>
```

## Para guardar as alterações de uma branch usando o stash e recuperá-las depois, siga estes passos:

Guarde as alterações:

```bash
git stash
```

Isso vai salvar suas alterações e limpar a área de trabalho.

Veja as stashes:

```bash
git stash list
```

Isso mostrará todas as stashes que você guardou, com um identificador único para cada uma.

Recupere uma stash:

```bash
git stash apply <stash_id>
```

Substitua <stash_id> pelo identificador da stash que você quer recuperar. Se você não especificar um identificador, a última stash será aplicada.

Opcional: Remova a stash após aplicar:

```bash
git stash drop 
```

## Fazer checkout de uma branch remota localmente

Atualize as referências de branches remotas:

```bash
git fetch
```

Faça checkout da branch remota:

```bash
git checkout <nome_da_branch_remota>
```

Isso criará uma nova branch local com o mesmo nome e mudará para ela.

Caso haja alterações na branch remota e você queira atualizá-la localmente, basta usar o comando abaixo:

```shell
git pull origin nome-da-branch
```

