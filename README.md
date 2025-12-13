
# 🧪 Testes Exploratórios - API ServeRest

[![Badge ServeRest](https://img.shields.io/badge/API-ServeRest-green)](https://github.com/ServeRest/ServeRest/)
[![Postman](https://img.shields.io/badge/Postman-Collection-orange)](https://www.postman.com/)

Projeto de testes exploratórios de API utilizando a **ServeRest**, uma API REST pública para estudo e prática de testes automatizados.

## 📋 Sobre o Projeto

Esta collection do Postman contém testes exploratórios completos para operações CRUD de usuários, incluindo:

- ✅ Cadastro de usuários
- ✅ Login e autenticação
- ✅ Busca por ID
- ✅ Atualização de dados
- ✅ Listagem de usuários
- ✅ Exclusão de registros

### 🎯 Diferenciais

- **Geração dinâmica de dados** com personagens de Star Wars e Senhor dos Anéis
- **Emails temáticos** vinculados ao universo do personagem (`@starwars.com` ou `@middleearth.com`)
- **Ordem aleatória** de nomes (normal ou invertida)
- **Senhas fortes** geradas automaticamente
- **Validações completas** em todos os endpoints
- **Scripts de pré-requisição** e testes automatizados

---

## 🌐 Sobre a API ServeRest

A **ServeRest** é um servidor REST criado para estudos e prática de testes de API.

### Características:
- 🔄 Verbos HTTP: GET, POST, PUT, DELETE
- 🔐 Autenticação via header
- 📊 Persistência de dados
- 🧪 Ideal para testes de carga
- 📝 Validação de schema JSON

### Ambientes Disponíveis:

**Online (Recomendado para início):** `https://serverest.dev`

## 📋 Como usar

- **Importar collection**: importe o arquivo `apiDicasGabs.json` no Postman (File -> Import).
- **Variáveis importantes**: configure no Postman (Collection/Environment) as variáveis abaixo:
  - `baseUrl`: URL base da API (ex: `https://serverest.dev`)
  - `email`, `senha`, `emailPadrao`, `senhaPadrao`, `idUsuario`, `administrador`, `nome`, `usuarioEmail`, `userSenha`, `emailUsuario`.

- **Executar localmente (opcional)**: se usar `newman`:

```
npx newman run apiDicasGabs.json --environment postman_environment.json
```

## 📈 Melhorias Futuras

- [ ] Testes de performance/carga
- [ ] Testes de segurança
- [ ] Integração com CI/CD
- [ ] Relatórios HTML com Newman
- [ ] Testes de contrato (schema validation)
- [ ] Cenários negativos expandidos

---

## 👨‍💻 Autor

**Gabriel Roquim**
- GitHub: [@gabrielroquim](https://github.com/gabrielroquim)
- LinkedIn: [Gabs QA](https://www.linkedin.com/in/gabsqa/)

---

## 🙏 Agradecimentos

- [ServeRest](https://github.com/ServeRest/ServeRest) - API utilizada nos testes
- [Paulo Gonçalves](https://github.com/PauloGoncalvesBH) - Criador da ServeRest
- Comunidade de QA Brasil

- Repositório ServeRest: https://github.com/ServeRest/ServeRest

## ⚙️ Rodando a ServeRest localmente

Se preferir executar a API localmente (útil para desenvolvimento/testes offline), instale e rode a versão mais recente com o comando:

```
npx serverest@latest
```

Após subir, ajuste `baseUrl` para o endpoint local conforme o console do Serverest e execute a collection normalmente.

## 📚 Recursos Úteis

- [Documentação ServeRest](https://serverest.dev)
- [Postman Learning Center](https://learning.postman.com/)
- [REST API Testing Guide](https://www.postman.com/api-platform/api-testing/)

---

⭐ Se este projeto te ajudou, deixe uma estrela no repositório!

