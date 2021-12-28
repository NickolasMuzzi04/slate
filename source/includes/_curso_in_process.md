*
# Curso

## Curso no Processo Diploma

### Listar alunos do processo

### HTTP Requests
`GET /diplomas/processos/<processId>/curso`

### URL Parameters

| Parameter | Description                  |
| --------- | ---------------------------- |
| processId    | O ID do processo |

> 200

```json
{
"0":,
  "autorizacao": {
    "data": "11/11/1111",
    "id": 3,
    "numero": "3213",
    "pagina_publicacao": null,
    "publicado_em": "11/11/1111",
    "secao_publicacao": null,
  },
  "tipo": {
    "id": 1,
    "nome": "Portaria",
    "campus": "são gabriel",
    "codigo_mec": "213",
    },
  "endereco": {
    "bairro": "bairro",
    "cep": "cep",
    "complemento": "",
    "id": 34,
    "logradouro": "Rua",
  },
  "municipio": {
    "codigo_ibge": "codigo",
    "estado": {
      "id": 1,
      "nome": "nome",
      "uf": "uf"
    },
    "id": 1,
    "nome": "nome",
    "numero": "numero",
    "grau_conferido": {
      "id": 1,
      "nome": "nome"
    },
    "modalidade": {
      "id": 1,
      "nome": "nome",
    },
    "nome": "nome",
    "nome_habilitacao": "nome",
    "numero_documento_autoriazacao": "",
    "numero_documento_reconhecido": "",
    "reconhecimento": {
    "id": 4,
      "tipo": {
        "id": 1,
        "nome": "nome",
      },
        "numero": "numero",
        "data": "11/11/1111",
        "publicado_em": "11/11/1111",
      },
    "pagina_publicacao": "",
    "publicado_em": "11/11/1111",
    "secao_publicacao": "",
    "tipo": {
      "id": 1,
      "nome": "nome",
    },
    "id": 1,
    "nome": "nome",
    "referencia": "referencia",
    "titulo_conferido": {
      "id": 1,
      "nome": "nome",
      },
    "id": 1,
    "nome": "nome",
}
```
## Criando Curso

### HTTP Requests
`POST /diplomas/processos/<processId>/curso`

> Payload Example

```json
{
"autorizacao": {
  "id": 3,
  "tipo": 1,
  "numero": "numero",
  "data": "11/11/1111",
  "publicado_em": "11/11/1111",
  "pagina_publicacao": "",
  "publicado_em": "11/11/1111",
  "secao_publicacao": "",
},
"campus": "campus",
"carga_horario": "00h",
"codigo_mec": "codigo",
"endereco": {
  "id": 27,
  "municipio": 1,
  "cep": "cep",
  "logradouro": "Rua",
  "numero": "numero",
  "bairro": "bairro",
  "cep": "cep",
  "complemento": "",
},
"estado": {
  "id": 1,
  "nome": "nome",
  "uf": "uf",
  },
"grau_conferido": 1,
"modalidade": 1,
"nome": "nome",
"nome_habilitacao": "nome",
"numero_documento_autoriazacao": "",
"numero_documento_reconhecido": "",
"reconhecimento": {
  "id": 4,
  "tipo": 1,
  "numero": "numero",
  "data": "11/11/1111",
  "publicado_em": "11/11/1111",
  "secao_publicacao": "",
},

"referencia": "referencia",
"titulo_conferido": 1,
}

```

| Parameter                  | Type      | Description                               |
| -------------------------- | --------- | ----------------------------------------- |
| `autorizacao`              | _string_  | [Autorizacao] (#credenciamento-e-recredenciamento-autorizacao-e-reconhecimento)|
| `reconhecimento`           | _string_  | [Reconhecimento](#endereco)               |
| `campus`                   | _string_  | Campus                                    |
| `carga_horario`            | _string_  | Carga horaria                             |
| `codigo_mec`               | _string_  | Codigo mec                                |
| `endereco`                 | _string?_ | [Endereco](#endereco)                     |
| `estado`                   | _string_  | Estado                                    |
| `grau_conferido`           | _id_      | Grau conferido                            |
| `modalidade.id`            | _id_      | Modalidade                                |
| `nome`                     | _string_  | Nome                                      |
| `nome_habilitacao`         | _string_  | Nome Habilitacao                          |
| `numero_documento_autoriazacao`| _string_  | Numero Documento Autoriazacao         |
| `numero_documento_reconhecido` | _string_  | Numero Documento Reconhecido          |
| `nome_social_filiacao`     | _string_  | Nome Social Filiação                      |
| `referencia`               | _string_  | Referencia                                |
| `titulo_conferido`         | _string_  | Titulo Conferido                          |
