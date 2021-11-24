# TODOs

Aplicação para gerenciar tarefas.
## :computer: Projeto

### :orange_book: Requisitos

- Criação de um usuário com `name` e `username`
- CRUD de TODOs para cada usuário
  1. Listar todos os *todos*;
  2. Criar um novo *todo*;
  3. Alterar o `title` e `deadline` de um *todo* existente;
  4. Marcar um *todo* como feito;
  5. Excluir um *todo*;
- Plano grátis onde o usuário só pode criar até dez *todos*
- Plano Pro que irá permitir criar *todos* ilimitados


### :straight_ruler: Regras de negócio

#### :ok_woman: Teste de Usuários
- [x] Should be able to create a new user
- [x] Should not be able to create a new user when username already exists

#### :page_facing_up: Teste de _todos_
- [x] Should be able to list all user's todos
- [x] Should be able to create a new todo
- [x] Should be able to update a todo
- [x] Should not be able to update a non existing todo
- [x] Should be able to mark a todo as done
- [x] Should not be able to mark a non existing todo as done
- [x] Should be able to delete a todo
- [x] Should not be able to delete a non existing todo

#### :page_facing_up: Teste de Middlewares
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


### :memo: Executando o Projeto

```bash
# Instale as dependências
$ yarn

# Execute o projeto
$ yarn dev

# Execute os testes
$ yarn test