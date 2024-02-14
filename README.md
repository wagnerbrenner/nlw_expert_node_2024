# Enquetes / Polls

Este projeto foi criado durante o evento NLW - Next Level Week da [Rocketseat](https://www.rocketseat.com.br/), edição Expert. O projeto permite criar enquetes e votar nelas. Essas enquetes são armazenadas em um banco de dados PostgreSQL, e para isso, utilizamos a ferramenta de Mapeamento Objeto-Relacional, o ORM Prisma. Além disso, a API possui uma conexão Websocket onde, sempre que um usuário vota em uma enquete, a API envia uma mensagem através dessa conexão, incluindo as atualizações no voto de uma única enquete. O ranking de votos das enquetes é gerenciado com o Redis, que é um banco de dados em memória de código aberto, utilizado principalmente como armazenamento de estrutura de dados de chave-valor de alta performance.
___
This project was created during the NLW - Next Level Week event by [Rocketseat](https://www.rocketseat.com.br/), Expert edition. The project allows for the creation of polls and voting on them. These polls are stored in a PostgreSQL database, and for this, we use the Object-Relational Mapping tool, Prisma ORM. Additionally, the API has a Websocket connection where, every time a user votes in a poll, the API sends a message through this connection, including updates on the vote of a single poll. The polls' vote ranking is managed with Redis, which is an open-source, in-memory database primarily used as a high-performance key-value data store.


## Getting Started / Começando

###  Versions / Versões

   Node v20.11.0

### Installations / Instalações 

```bash
npm install
```

### Environment Variables / Variáveis de Ambiente

  Crie um novo arquivo `.env` dentro da raiz do projeto e defina a URL do seu banco de dados usando o conteúdo abaixo e substituindo o `<user` e `<password` pelo usuário e senha do banco de dados, respectivamente.
  ___
  Create a new `.env` file inside the project root, and define your database URL using the content below and replacing the `<user` and `<password` by the database user and password respectively.

  `.env`:

    DATABASE_URL="postgresql://<user>:<password>@localhost:5432/polls?schema=public"

 ### Running Docker images / Executando Imagens Docker
 
```bash
docker compose up -d
```

  Isso iniciará uma instância do PostgreSQL e uma instância do Redis no Docker.
  ___
  This will start a PostgreSQL instance and a Redis instance on Docker.

### Running migrations / Executando Migrações

   ```bash
npx prisma migrate dev
```

Isso executará todas as migrations criando as tabelas e outras configurações dentro do banco de dados.
___
This will run all migrations creating the tables and other configs inside the database.


 ### Running / Executando

```bash
npm run dev
```
    
A API estará sendo executada em `http://localhost:3333` e o websocket em `ws://localhost:3333`.
___
The API will be running on `http://localhost:3333` and websocket on `ws://localhost:3333`.

## Routes / Rotas

Você pode importar a coleção de requisições HTTP com o arquivo `request-collection.json`.

| Rota                 | Método | Protocolo | Descrição                            |
|----------------------|--------|-----------|--------------------------------------|
| /polls               | POST   | HTTP      | Criar uma nova enquete.              |
| /polls/:pollId       | GET    | HTTP      | Obter uma única enquete.             |
| /polls/:pollId/vote  | POST   | HTTP      | Votar em uma opção de enquete.      |
| /polls/:pollId/results | --    | WS        | Abrir uma conexão WS para receber resultados de votos. |

___

You can import the HTTP requests collection with the file `request-collection.json`.

| Route               | Method | Protocol | Description                           |
|---------------------|--------|----------|---------------------------------------|
| /polls              | POST   | HTTP     | Create a new poll.                    |
| /polls/:pollId      | GET    | HTTP     | Get a single poll.                    |
| /polls/:pollId/vote | POST   | HTTP     | Vote on a poll option.                |
| /polls/:pollId/results | --   | WS       | Open a WS connection to receive votes results. |

---

## 🔗  Technologies / Tecnologias

![Redis](https://img.shields.io/badge/Redis-D9281A?style=for-the-badge&logo=redis&logoColor=white)
![Netlify](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)
![html5](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)

---

## 🔗 My Links / Meus Links

  <a href="https://instagram.com/wagnerbrenner" target="_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
<a href="https://discord.gg/< Wagner Brenner ◢ ◤ />#8196" target="_blank"><img src="https://img.shields.io/badge/Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white" target="_blank"></a>
  <a href ="mailto:wagner.brenner13@gmail.com"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white " target="_blank"></a>
  <a href="https://www.linkedin.com/in/wagnercarvalhobrenner/" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>
  <a href="https://api.whatsapp.com/send?phone=5551997438310" target="_blank"><img src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" target="_blank"></a> 
