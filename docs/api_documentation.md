**Resumo**

- **API**: Serverest (https://serverest.dev/)
- **Collection**: `apiDicasGabs.json` (contém requests para usuários e login, com testes Postman)

**Variáveis usadas na collection**

- `baseUrl` — URL base da API (ex: `https://serverest.dev`)
- `email`, `senha`, `emailPadrao`, `senhaPadrao`, `idUsuario`, `administrador`, `nome`, `usuarioEmail`, `userSenha`, `emailUsuario`

**Endpoints principais**

- **POST /login**
  - Descrição: Autentica um usuário e retorna token/authorization.
  - Corpo (JSON):
    ```json
    { "email": "{{email}}", "password": "{{senha}}" }
    ```
  - Sucesso: `200 OK` — corpo contém `message` e `authorization` (token).
  - Exemplos de falha: `400 Bad Request` com mensagens de campos obrigatórios.

- **POST /usuarios**
  - Descrição: Cadastra um novo usuário.
  - Corpo (JSON):
    ```json
    {
      "nome": "{{nome}}",
      "email": "{{email}}",
      "password": "{{senha}}",
      "administrador": "{{administrador}}"
    }
    ```
  - Sucesso: `201 Created` — `{ "message": "Cadastro realizado com sucesso", "_id": "..." }`
  - Erros: `400 Bad Request` — ex: `Este email já está sendo usado` ou validações de formato.

- **GET /usuarios**
  - Descrição: Lista usuários cadastrados.
  - Parâmetros de query (opcional): `administrador`, `email` (alguns exemplos na collection).
  - Sucesso: `200 OK` — formato:
    ```json
    { "quantidade": 1, "usuarios": [ { "nome": "Fulano", "email": "fulano@qa.com", "password": "...", "administrador": "true", "_id": "..." } ] }
    ```

- **GET /usuarios/{id}**
  - Descrição: Retorna dados do usuário pelo ID.
  - Parâmetros de rota: `id` (path)
  - Sucesso: `200 OK` — objeto do usuário.
  - Erro: `404 Not Found` quando não existe.

- **PUT /usuarios/{id}**
  - Descrição: Atualiza dados do usuário.
  - Corpo (JSON): campos atualizáveis (nome, email, password, administrador).
  - Sucesso: `200 OK` — `{ "message": "Registro alterado com sucesso" }`
  - Erros: `400 Bad Request` — validações, email já usado, etc.

- **DELETE /usuarios/{id}**
  - Descrição: Exclui um usuário por ID.
  - Sucesso: `200 OK` — `{ "message": "Registro excluído com sucesso" }` ou `{ "message": "Nenhum registro excluído" }` caso não encontre.

**Como importar e configurar no Postman**

- Importe `apiDicasGabs.json` no Postman.
- Crie ou edite um Environment com `baseUrl=https://serverest.dev` e as variáveis de credenciais.
- Rode as requests na ordem desejada. A collection contém `pre-request scripts` e testes que salvam `idUsuario` e outros valores em variáveis para uso nas requisições subsequentes.

**Observações e dicas**

- A collection utiliza scripts para gerar nomes, emails e senhas aleatórias ao cadastrar usuários (veja `Cadastrar usuarios` pre-request script).
- Certifique-se de ajustar `baseUrl` para `https://serverest.dev` antes de rodar.
- Se preferir rodar via CLI, use `newman` (ver `README.md`).

---

**Resumo rápido (link para README)**

Veja o README principal para uma visão mais completa, badges, autor e melhorias planejadas: `README.md`.

