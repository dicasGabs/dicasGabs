**Project**: API - Collection `apiDicasGabs.json`

- **Descrição**: Coleção Postman com testes e exemplos para a API pública do Serverest.
- **Fonte da API**: https://serverest.dev/ (esta collection consome endpoints dessa API)

**Como usar**
- **Importar collection**: importe o arquivo `apiDicasGabs.json` no Postman (File -> Import).
- **Variáveis importantes**: configure no Postman (Collection/Environment) as variáveis abaixo:
  - `baseUrl`: URL base da API (ex: `https://serverest.dev`)
  - `email`, `senha`, `emailPadrao`, `senhaPadrao` — e outras usadas pela collection (`idUsuario`, `administrador`, `nome`, `usuarioEmail`, `userSenha`, `emailUsuario`).

- **Executar localmente (opcional)**: se usar `newman`:

```
npx newman run apiDicasGabs.json --env-var "baseUrl=https://serverest.dev"
```

**Observações**
- A API utilizada pela collection é pública e pertence ao projeto Serverest (https://serverest.dev/).
- Este repositório contém apenas a collection exportada (`apiDicasGabs.json`) e documentação.

Se quiser, posso também criar um arquivo de ambiente (`postman_environment.json`) com variáveis de exemplo e commitar aqui.
