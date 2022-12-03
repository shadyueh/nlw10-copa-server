# NLW na Copa
Servidor para a app do Bolão da Copa

# Tecnologias utilizadas

  Fastify - microframework para roteamendo dentro da aplicação. Mais leve que o express.

  Prisma - comunicação com o banco de dados

  SQlite - database

# Configurações da aplicação

Instalando typescript

```npm i typescript -D```

Inicializando o typescript

```npx tsc --init```

Instalando o fastify

```npm i fastify```

Instalando conversor de typescript

```npm i tsx -D```

# Configurações do banco de dados

Instalando o Prisma
```npm i prisma -D```
```npm i @prisma/client```

Inicializando o banco SQlite com o Prisma
```npx prisma init --datasource-provider sqlite```

Criando migrations
```npx prisma migrate dev```
e então informe um nome para a migration

Acessando o banco
```npx prisma studio```
e então acesse a url da IDE pelo navegador

Gerando diagrama ER dinamicamente
```npm i prisma-erd-generator @mermaid-js/mermaid-cli -D```

crie um generator no arquivo schema.prisma
```
generator erd {
  provider = "prisma-erd-generator"
}
```
e então execute

```npx prisma generate```