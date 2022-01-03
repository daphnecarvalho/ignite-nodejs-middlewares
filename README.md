# TODOs - Challenge: Middlewares

Instructions: [Trabalhando com Middlewares](https://www.notion.so/Desafio-02-Trabalhando-com-middlewares-4f89bf538c2e4ee291382b92bdc36790).

Application for managing TODOs.

## Base URL
http://localhost:3333

## Routes

### /users

* [<span style="color:#663399">GET</span>] /:id
* [<span style="color:#79c900">POST</span>] /
* [<span style="color:#ffc000">PATCH</span>] /:id/pro

### /todos
* [<span style="color:#663399">GET</span>] / (Header: username)
* [<span style="color:#79c900">POST</span>] / (Header: username)
* [<span style="color:#ff8c00">PUT</span>] /:id (Header: username)
* [<span style="color:#ffc000">PATCH</span>] /:id/done (Header: username)
* [<span style="color:#ff0000">DELETE</span>] /:id
(Header: username)

## :orange_book: Requirements

- Criação de um usuário com `name` e `username`
- CRUD de TODOs para cada usuário
  1. Listar todos os *todos*;
  2. Criar um novo *todo*;
  3. Alterar o `title` e `deadline` de um *todo* existente;
  4. Marcar um *todo* como feito;
  5. Excluir um *todo*;
- Plano grátis onde o usuário só pode criar até dez *todos*
- Plano Pro que irá permitir criar *todos* ilimitados

## :straight_ruler: Business rules
### :ok_woman: Users Test
- [x] Should be able to create a new user
- [x] Should not be able to create a new user when username already exists

### :page_facing_up: _todos_ Test
- [x] Should be able to list all user's todos
- [x] Should be able to create a new todo
- [x] Should be able to update a todo
- [x] Should not be able to update a non existing todo
- [x] Should be able to mark a todo as done
- [x] Should not be able to mark a non existing todo as done
- [x] Should be able to delete a todo
- [x] Should not be able to delete a non existing todo

### :page_facing_up: Middlewares Test
- [x] Should be able to find user by username in header and pass it to request.user
- [x] Should not be able to find a non existing user by username in header
- [x] Should be able to let user create a new todo when is in free plan and have less than ten todos
- [x] Should not be able to let user create a new todo when is not Pro and already have ten todos
- [x] Should be able to let user create infinite new todos when is in Pro plan
- [x] Should be able to put user and todo in request when both exists
- [x] Should not be able to put user and todo in request when user does not exists
- [x] Should not be able to put user and todo in request when todo id is not uuid
- [x] Should not be able to put user and todo in request when todo does not exists
- [x] Should be able to find user by id route param and pass it to request.user
- [x] Should not be able to pass user to request.user when it does not exists

## Tests
<p>
Test Suites: 6 total
</p>
<p>
Tests: 22 total
</p>

## :memo: Project commands
### Prepare project

```bash
  # Install dependencies
  yarn install
```
### Run project

```bash
  # Run project
  yarn dev
```
### Run tests

```bash
  # Run tests
  yarn test
```