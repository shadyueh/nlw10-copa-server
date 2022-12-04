# NLW na Copa
Servidor para a app do Bolão da Copa

# Tecnologias utilizadas

  Fastify - microframework para roteamendo dentro da aplicação. Mais leve que o express.

  Prisma - comunicação com o banco de dados

  SQlite - database

# Iniciando o backend

## Configurações da aplicação

```bash
mkdir -p nlw10-copa/server
cd nlw10-copa/server
npm init
```
Instalando typescript

```bash
npm i typescript -D
```

Inicializando o typescript

```bash
npx tsc --init
```

Instalando o fastify

```bash
npm i fastify
```

Instalando conversor de typescript

```bash
npm i tsx -D
```

## Configurações do banco de dados

Instalando o Prisma
```bash
npm i prisma -D
npm i @prisma/client
```

Inicializando o banco SQlite com o Prisma
```bash
npx prisma init --datasource-provider sqlite
```

Criando migrations
```bash
npx prisma migrate dev
```
e então informe um nome para a migration

Acessando o banco
```bash
npx prisma studio
```
e então acesse a url da IDE pelo navegador

Gerando diagrama ER dinamicamente
```bash
npm i prisma-erd-generator @mermaid-js/mermaid-cli -D
```

crie um generator no arquivo schema.prisma
```bash
generator erd {
  provider = "prisma-erd-generator"
}
```
e então execute

```bash
npx prisma generate
```

Configurando CORS
```bash
npm i @fastify/cors
```
e então adicione a configuração no arquivo server.ts

```javascript
await fastify.register(cors, {
  origin: true,
});
```