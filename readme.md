
# API de Usuários em Memória - NestJS 

**Luan Marques** – luan.marques@aluno.faculdadeimpacta.com.br

---

## Descrição

Matéria: API Development

Esta API foi desenvolvida utilizando **Node.js** com o framework **NestJS** para gerenciar usuários em memória.  
Não há banco de dados, todos os dados são armazenados em memória enquanto a aplicação está rodando.

A API permite:

- Criar usuários (com nome e e-mail)
- Listar todos os usuários
- Consultar um usuário específico pelo ID
- Excluir um usuário pelo ID

---

## Como rodar

1. Clone o projeto
2. Instale as dependências:

   ```bash
   npm install
   ```

3. Para rodar em modo desenvolvimento (auto-reload):

   ```bash
   npm run start:dev
   ```

4. Para compilar e rodar:

   ```bash
   npm run build
   npm run start
   ```

A API estará disponível em `http://localhost:3000`. 

Para facilitar o teste da API, disponibilizamos uma **Postman Collection** pronta para importar.

---

## Endpoints

### Criar usuário

- **POST** `/users`
- Corpo JSON:

  ```json
  {
    "name": "Seu Nome",
    "email": "email@exemplo.com"
  }
  ```

- Retorna o usuário criado com ID gerado.

---

### Listar todos os usuários

- **GET** `/users`
- Retorna uma lista com todos os usuários.

---

### Obter usuário por ID

- **GET** `/users/:id`
- Retorna o usuário com o ID informado.

---

### Deletar usuário por ID

- **DELETE** `/users/:id`
- Remove o usuário com o ID informado.
- Retorna mensagem de sucesso.

---

## Exemplos usando `curl`

Criar usuário:

```bash
curl -X POST http://localhost:3000/users -H "Content-Type: application/json" -d "{"name":"Luan", "email":"luan@faculdadeimpacta.com.br"}"
```

Listar todos:

```bash
curl http://localhost:3000/users
```

Buscar por id 1:

```bash
curl http://localhost:3000/users/1
```

Deletar usuário id 1:

```bash
curl -X DELETE http://localhost:3000/users/1
```
