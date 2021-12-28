
# Mantendora

## Mantendora Por Processo

### Listar Mantenedora por Processo

> 200

```json
{
  "nome": "Mantenedora",
  "razao_social": "Mantenedora",
  "cnpj": "12345678901234",
  "codigo_mec": null,
  "endereco": {
      "id": 37,
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
      "cep": "12345678",
      "logradouro": "Rua",
      "numero": "00",
      "complemento": "",
      "bairro": "Bairro",
      "principal": true
  },
}
```

### HTTP Request

`GET /diplomas/processos/<ProcessId>/mantenedora`

### URL Parameters

| Parameter | Description                  |
| --------- | ---------------------------- |
| processId | O ID do processo             |

## Criando uma Mantenedora

### HTTP Request

`POST /diplomas/processos/<ProcessId>/mantenedora`

### Payload

Campos necessários para criar uma mantenedora no Processo do Diploma:
Nome, Razão Social, CNPJ, Código do MEC e Endereço.


### Parameters

| Parameter                  | Type      | Description                              |
| -------------------------- | --------- | -----------------------------------------|
| `id`                       | _id_      | Id da mantenedora                        |
| `CNPJ`                     | _string_  | CNPJ da mantenedora                      |
| `nome`                     | _string_  | Nome da mantenedora                      |
| `razao_social`             | _string_  | Razão social da mantenedora              |
| `municipio.id`             | _id_      | [Municipio] (#municipio-e-naturalidade)|
| `cep`                      | _string_  | [CEP](#endereco)                         |
| `logradouro`               | _string_  | [logradouro](#endereco)                  |
| `numero`                   | _string_  | [numero] (#endereco)                     |
| `complemento`              | _string_  | [complemento] (#endereco)                |
| `bairro`                   | _string_  | [bairro] (#endereco)                     |


> Payload Example:

```json
{
  "id": 1,
  "cnpj": "17496696000191",
   "nome": "nome",
   "razao_social": "nome",
 "endereco": {
      "id": 37,
      "municipio": 1,
      "cep": "12354678",
      "logradouro": "Rua",
      "numero": "0",
      "complemento": "",
      "bairro": "bairro",
  },
}
```
