# API Documentation - Authentication Users

Esta documentação descreve os endpoints e as operações disponíveis na API de CRUD de Usuários com autenticação JWT.

## Autenticação

### Autenticação - Login

Realiza o login de um usuário.

- Endpoint: `POST /auth/login`
- Descrição: Realiza o login do usuário com as credenciais fornecidas.
- Corpo da Requisição (JSON):
  ```json
  {
    "nome": "Hallison",
    "senha": "123123123"
  }
  ```

## Usuários

### Usuários - Criar Usuário

Cria um novo usuário.

- Endpoint: `POST /users`
- Descrição: Cria um novo usuário com as informações fornecidas.
- Corpo da Requisição (JSON):
  ```json
  {
    "nome": "Hallison",
    "sobrenome": "Brancalhao",
    "email": "hallison@brancalhao.com.br",
    "senha": "123123123"
  }
  ```

### Usuários - Buscar Todos

Recupera todos os usuários.

- Endpoint: `GET /users`
- Descrição: Retorna uma lista de todos os usuários cadastrados.
- Cabeçalho da Requisição:
  - Authorization: Bearer Token

### Usuários - Buscar por ID

Recupera um usuário pelo seu ID.

- Endpoint: `GET /users/{id}`
- Descrição: Retorna as informações do usuário correspondente ao ID fornecido.
- Cabeçalho da Requisição:
  - Authorization: Bearer Token

### Usuários - Atualizar Usuário

Atualiza as informações de um usuário.

- Endpoint: `PATCH /users/{id}`
- Descrição: Atualiza as informações do usuário correspondente ao ID fornecido.
- Cabeçalho da Requisição:
  - Authorization: Bearer Token
- Corpo da Requisição (JSON):
  ```json
  {
    "nome": "Hallison",
    "sobrenome": "de Oliveira Brancalhao",
    "senha": "123123123"
  }
  ```

### Usuários - Excluir Usuário

Exclui um usuário.

- Endpoint: `DELETE /users/{id}`
- Descrição: Exclui o usuário correspondente ao ID fornecido.
- Cabeçalho da Requisição:
  - Authorization: Bearer Token
