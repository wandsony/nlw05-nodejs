<h1 align="center">Chatty</h1>


<br>

## 💻 Projeto

É um chat para atendimento de clientes em tempo real com [Socket.IO](https://socket.io/) criado na [RocketSeat](https://rocketseat.com.br/) Next Level Week 5.0, usando TypeScript com Node.js.

## ✨ Tecnologias

Esse projeto foi desenvolvido com as seguintes tecnologias:

- **[Node.js](https://nodejs.org/en/)**
- **[Express](https://expressjs.com/)**
- **[TypeORM](https://www.npmjs.com/package/typeorm)**
- **[Sqlite3](https://www.npmjs.com/package/sqlite3)**
- **[Metadata Reflection API](https://www.npmjs.com/package/reflect-metadata)**
- **[uuid](https://www.npmjs.com/package/uuid)**
- **[socket.io](https://www.npmjs.com/package/socket.io)**
- **[socket.io-client](https://www.npmjs.com/package/socket.io-client)**
- **[Embedded JavaScript templates](https://www.npmjs.com/package/ejs)**

## 🚀 Comandos para começar

```bash
# Clone este repositório
- git clone https://github.com/wandsony/nlw05-nodejs

# Acesse a pasta do projeto no terminal/cmd
- cd nlw05-nodejs
```

Instalando dependências

```bash
- yarn install
```

Gerar o arquivo de database.sqlite do Sqlite3, onde ficaram armazenados as tabelas

```bash
- yarn devDB
```

Criando as migrations do Sqlite3 por meio do cli do TypeOrm

```bash
- yarn typeorm migration:run
```

Inicializando uma instância local (Script configurado no package.json)

```bash
- yarn dev
```

Por fim, a aplicação estará disponível em `http://localhost:3333`

---

## 🖥️ Endpoints

#### 💠 Para acessar o chat do admin vá para 👉 http://localhost:3333/pages/admin

#### 💠 Para acessar o chat do cliente vá para 👉 http://localhost:3333/pages/client

---

## 🗎 Documentação API

<details>
  <summary>Configurações</summary>

### 📍 Criar Configuração [/settings] [POST]

#### **Request**

- Body

```bash
{
    "chat": "true",
    "username": "admin"
}
```

#### **Response 201 (application/json)**

```bash
[
  {
    "id": "admin_id",
    "username": "admin",
    "chat": "true",
    "updated_at": "2021-04-22T19:22:37.000Z",
    "created_at": "2021-04-22T19:22:37.000Z"
}
]
```

### 📍 Atualizar Configuração [/settings/admin] [PUT]

#### **Request**

- Body

```bash
{
    "chat": "false"
}
```

#### **Response 201**

 </details>

<details>
  <summary>Usuário</summary>

### 📍Criar Usuário [/users] [POST]

#### **Request**

- Body

```bash
{
    "email": "example@email.com"
}
```

#### **Response 201 (application/json)**

```bash
[
 {
    "id": "user_id",
    "email": "example@email.com",
    "created_at": "2021-04-22T19:37:24.000Z"
}
]
```

 </details>

<details>
  <summary>Mensagem</summary>

### 📍Enviar Mensagem [/messages] [POST]

#### **Request**

- Body

```bash
{
    "user_id": "user_id",
    "text": "message"
}
```

#### **Response 201 (application/json)**

```bash
[
  {
    "id": "message_id",
    "text": "message",
    "user_id": "user_id",
    "created_at": "2021-04-23T19:40:02.000Z"
  }
]
```

### 📍Listar mensagens de um usuário [/messages/:user_id] [GET]

#### **Response 201 (application/json)**

```bash
[
  {
    "id": "message_id",
    "admin_id": "admin_id",
    "text": "message",
    "user_id": "user_id",
    "created_at": "2021-04-22T19:40:02.000Z",
    "user": {
      "id": "user_id",
      "email": "example@email.com",
      "created_at": "2021-04-22T19:37:24.000Z"
    }
  }
]
```

</details>

---

Este projeto foi desenvolvido com ❤️ por **[@Wandson Gomes](https://www.linkedin.com/in/wandsony/)**, com a instrutora **[@Daniele Leão](https://www.linkedin.com/in/daniele-le%C3%A3o-evangelista-5540ab25)**, durante a **[Next Level Week](https://rocketseat.com.br/)** na **[Rocketseat](https://www.linkedin.com/school/rocketseat/about/)** [Participe da nossa comunidade!](https://discordapp.com/invite/gCRAFhc) 💜. <br> 
