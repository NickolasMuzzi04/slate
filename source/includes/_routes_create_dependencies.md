
# Rotas de Adicionar Dependências

## Credenciamento e Recredenciamento (Autorização e Reconhecimento)
### HTTP Request

`POST /diplomas/processos/<ProcessId>/instituicao_ensino`

> 200

```json
{
  "id": 5,
  "data": "12/12/1212",
  "numero": "1221",
  "pagina_publicacao": "123441",
  "publicado_em": "12/12/2121",
  "secao_publicacao": "213124",
  "tipo": {
    "id": 1,
    "nome": "Portaria"
  },
}

```


### Parameters

| Parameter                  | Type      | Description                              |
| -------------------------- | --------- | -----------------------------------------|
| `tipo.id`                  | _id_      | [Tipo](#tipo-credenciamento)             |
| `numero`                   | _string_  | Número                                   |
| `data`                     | _data_    | Data                                     |
| `publicado_em`             | _data_    | Data da Publicação                       |
| `secao_publicacao`         | _string_  | Seção da Publicação                        |
| `pagina_publciacao`        | _string_  | Pagina da Publicação                       |

## Endereço
>Payload Example

```json
{
    "id": 26,
    "municipio": 1,
    "cep": "12365478",
    "logradouro": "Rua",
    "numero": "00",
    "complemento": "",
    "bairro": "bairro",
    "principal": true,
}
```
### Parameters

| Parameter                  | Type      | Description                              |
| -------------------------- | --------- | -----------------------------------------|
| `municipio.id`             | _id_      | [Município](#municipio-e-naturalidade)   |
| `cep`                      | _string_  | CEP                                      |
| `logradouro`               | _string_  | Logradouro                               |
| `numero`                   | _string_  | Número                                   |
| `complemento`              | _string?_ | Complemento                              |
| `bairro`                   | _string_  | Bairro                                   |

## Termo De Responsabilidade
> 200

```json
{
  "nome": "nome",
"cpf": "12345678911",
"cargo": "cargo",
}
```
### Parameters

| Parameter                  | Type      | Description                              |
| -------------------------- | --------- | -----------------------------------------|
| `nome`                     | _string_  | Nome                                     |
| `cpf`                      | _string_  | CPF                                      |
| `cargo`                    | _string_  | Cargo                                    |
