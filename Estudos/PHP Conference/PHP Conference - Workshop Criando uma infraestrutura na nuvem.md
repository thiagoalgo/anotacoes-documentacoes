
[https://github.com/vcampitelli/curso-criando-infra-nuvem](https://github.com/vcampitelli/curso-criando-infra-nuvem)

Material do curso "Criando uma infraestrutura na nuvem" (aplicação, banco, testes, e deploy em ambientes de sandbox e produção).

## Preparação

[](https://github.com/vcampitelli/curso-criando-infra-nuvem/tree/main#prepara%C3%A7%C3%A3o)

### Pré-requisitos

[](https://github.com/vcampitelli/curso-criando-infra-nuvem/tree/main#pr%C3%A9-requisitos)

Certifique-se que você tenha instalados:

1. [Docker](https://docs.docker.com/get-docker) e [Docker Compose](https://docs.docker.com/compose)
2. [AWS CLI](https://aws.amazon.com/pt/cli/)

### Imagens Docker

[](https://github.com/vcampitelli/curso-criando-infra-nuvem/tree/main#imagens-docker)

Para facilitar no dia do curso, baixe as imagens Docker necessárias para nossa aplicação de demonstração:

```shell
docker pull php:8.3-cli-alpine
docker pull node:23-alpine
docker pull mariadb:11
```

## Slides

[Slides](https://github.com/vcampitelli/curso-criando-infra-nuvem/tree/main#slides)

Clone este repositório com a _flag_ `--recursive`:

```shell
git clone --recursive git@github.com:vcampitelli/curso-criando-infra-nuvem.git
```

Acesse o arquivo [`docs/index.html`](https://github.com/vcampitelli/curso-criando-infra-nuvem/blob/main/docs/index.html) em seu navegador.

## Código da demonstração

[Código demo](https://github.com/vcampitelli/curso-criando-infra-nuvem/tree/main#c%C3%B3digo-da-demonstra%C3%A7%C3%A3o)

Estão na pasta [`demo`](https://github.com/vcampitelli/curso-criando-infra-nuvem/blob/main/demo).