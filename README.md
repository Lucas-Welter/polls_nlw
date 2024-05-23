# Polls

This project was created during the NLW - Next Level Week event by [Rocketseat](https://www.rocketseat.com.br/), Expert edition. The project allows the creation of polls that you can vote on.

## Getting Started 

###  Versions

   Node v20.13.1

### Installation

```bash
npm install
```

### Environment Variables / Variáveis de Ambiente

  Create a new `.env` file inside the project root, define your database URL using the content below, and replace the `<user` and `<password` with the database user and password respectively.

  `.env`:

    DATABASE_URL="postgresql://<user>:<password>@localhost:5432/polls?schema=public"

 ### Running Docker 
 
```bash
docker compose up -d
```

  This will start a PostgreSQL and Redis instance.

### Running migrations 

   ```bash
npx prisma migrate dev
```
This will run all migrations creating the tables and other configs inside the database.

 ### Running 

```bash
npm run dev
```
    
The API will be running on `http://localhost:3333` and websocket on `ws://localhost:3333`.

## Routes 

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
