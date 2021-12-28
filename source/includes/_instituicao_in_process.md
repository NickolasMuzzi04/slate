
# Instituição de Ensino

## Instituição de Ensino Por Processo

### Listar Instituição de Ensino por Processo

> 200

```json
{
  "id": 1,
  "credenciamento": {
      "id": 1,
      "tipo": {
          "id": 1,
          "nome": "Decreto"
      },
      "numero": "432",
      "data": "10/10/1001",
      "publicado_em": "10/10/1001",
      "secao_publicacao": "1",
      "pagina_publicacao": "2"
  },
  "recredenciamento": {
      "id": 35,
      "tipo": {
          "id": 1,
          "nome": "Decreto"
      },
      "numero": "2321",
      "data": "10/10/1010",
      "publicado_em": "10/10/1010",
      "secao_publicacao": "23",
      "pagina_publicacao": "12"
  },
  "endereco": {
      "id": 40,
      "municipio": {
          "id": 1,
          "estado": {
              "id": 1,
              "nome": "Minas Gerais",
              "uf": "MG"
          },
          "nome": "Belo Horizonte",
          "codigo_ibge": "123"
      },
      "cep": "31241532",
      "logradouro": "Rua",
      "numero": "000",
      "complemento": "",
      "bairro": "bairro",
  },
  "termo_responsabilidade": {
      "nome": "Name",
      "cpf": "12313",
      "cargo": "Cargo"
  },
  "nome": "FACULDADE ",
  "codigo_mec": "1333",
  "cnpj": "12345678901234",
}
```

### HTTP Request

`GET /diplomas/processos/<ProcessId>/instituicao_ensino`

### URL Parameters

| Parameter | Description                  |
| --------- | ---------------------------- |
| processId | O ID do processo             |

## Criando uma Instituição de Ensino

### HTTP Request

`POST /diplomas/processos/<ProcessId>/instituicao_ensino`

### Payload

Campos necessários para criar uma Ies no Processo do Diploma:
Nome, Codigo do EMEC, CNPJ, Endereço, Credenciamento.

> Payload Example:

```json
{
  "id": 1,
  "credenciamento": {
      "id": 1,
      "tipo": 1,
      "numero": "432",
      "data": "10/10/1001",
      "publicado_em": "10/10/1001",
      "secao_pubicacao": "1",
      "pagina_publicacao": "2"
  },
  "recredenciamento": null,
  "endereco": {
      "id": 37,
      "municipio": 1,
      "cep": "31367786",
      "logradouro": "Rua ",
      "numero": "0",
      "complemento": "",
      "bairro": "bairro",
      "principal": true
  },
  "termo_responsabilidade": {
      "nome": "nome",
      "cpf": "12345678901",
      "cargo": "cargo"
  },
  "nome": "FACULDADE",
  "codigo_mec": "1333",
  "cnpj": "321321321",
}
```

| Parameter                  | Type      | Description                              |
| -------------------------- | --------- | -----------------------------------------|
| `nome`                     | _string_  | Nome Ies                                 |
| `credenciamento`           | _object_  | [Credenciamento](#credenciamento-e-recredenciamento)        |
| `recredenciamento`         | _object?_ | [Recredenciamento](#credenciamento-e-recredenciamento)      |
| `endereco`                 | _object_  | [Endereço](#endereco)                    |
| `codigo_mec`               | _string_  | Código do MEC                            |
| `cnpj`                     | _string_  | CNPJ                                     |
| `termo_responsabilidade`   | _object_  | [Termo De Responsabilidade](#termo-de-responsabilidade)|
