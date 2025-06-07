# MostraNome - Azure Function

Este projeto implementa uma Azure Function chamada **InsereNome** que responde a requisições HTTP, retornando uma mensagem personalizada com o nome informado.

## Como funciona

- A função pode ser acionada via métodos HTTP **GET** ou **POST**.
- O nome pode ser enviado como parâmetro de query string (`?name=SeuNome`) ou no corpo da requisição em formato JSON (`{"name": "SeuNome"}`).
- A resposta será uma mensagem de saudação personalizada.

## Exemplo de uso

### GET

```
GET https://<sua-func-url>/api/Function1?name=Maria
```

**Resposta:**
```
Boa Tarde, Maria. Este triger HTTP foi executado com sucesso.
```

### POST

```
POST https://<sua-func-url>/api/Function1
Content-Type: application/json

{
  "name": "João"
}
```

**Resposta:**
```
Boa Tarde, João. Este triger HTTP foi executado com sucesso.
```

## Estrutura do Projeto

- [`MostraNome/InsereNome.cs`](MostraNome/InsereNome.cs): Implementação da Azure Function.
- `host.json`, `local.settings.json`: Arquivos de configuração da Azure Function.
- `MostraNome.csproj`: Arquivo de projeto .NET Core.

## Requisitos

- [.NET Core 3.1 SDK](https://dotnet.microsoft.com/download/dotnet/3.1)
- Azure Functions Core Tools (opcional, para rodar localmente)

## Como executar localmente

1. Clone o repositório.
2. Instale as dependências com `dotnet restore`.
3. Execute a função localmente:
   ```
   func start
   ```
4. Acesse a URL informada no terminal para testar a função.

---