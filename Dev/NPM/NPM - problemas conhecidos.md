
## Arquivo package-lock.json sendo atualizado no serividor

Ao fazer deploy no servidor (`npm install`) o arquivo package-lock.json estava sendo alterado.

Para resolver o problema rodei o comando abaixo localmente e remotamente. 

```bash
npm ci
```

Também vou alterar o script de deploy para rodar sempre esse comando no servidor.

Segue a explicação do porque usar esse comando:

Use npm ci para Instalação Limpa: Em vez de `npm install`, use `npm ci` no servidor. Este comando é projetado para ambientes de integração contínua e garante uma instalação limpa e consistente das dependências com base no arquivo `package-lock.json`.