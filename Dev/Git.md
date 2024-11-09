# Git

&nbsp;
## Rebase na branch local atual pegando o que está na main remota

```bash
git fetch origin 
git rebase origin/main 
git push --force-with-lease
```

&nbsp;
## Reverter alterações de arquivo

```bash
# Arquivo único
git checkout -- <nome_do_arquivo>

# Todos os arquivos
git checkout -- .
```

&nbsp;
## Visualizar o que foi alterado no arquivo local:

```bash
git diff <nome_do_arquivo>
```

&nbsp;
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

