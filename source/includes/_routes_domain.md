
# Rotas de Domínio

## Aluno Sexo

### HTTP Request

`GET /academico/aluno-sexo`

>  200

```json
[
  {
      "id": 1,
      "sexo": "M"
  },
  {
      "id": 2,
      "sexo": "F"
  }
]
```

## Nacionalidade

### HTTP Request

`GET /enderecos/nacionalidades`

> 200

```json
{
  "id": 1,
  "nome": "Brasileira"
}
```

## Estado Civil

### HTTP Request

`GET /academico/aluno-estado-civil`

> 200

```json
[{
  "id": 1,
  "nome": "SOLTEIRO"
},
{
  "id": 2,
  "nome": "CASADO"
}]
```

## Município e Naturalidade

### HTTP Request

`GET /enderecos/municipios`

> 200

```json
[
  {
    "id": 1,
    "estado": {
        "id": 1,
        "nome": "Minas Gerais",
        "uf": "MG"
    },
    "nome": "Belo Horizonte",
    "codigo_ibge": "3106200"
  },
  {
    "id": 2,
    "estado": {
        "id": 2,
        "nome": "São Paulo",
        "uf": "SP"
    },
    "nome": "Guarulhos",
    "codigo_ibge": "3518800"
  }
]
```

## Estado

### HTTP Request

`GET /enderecos/estados`

> 200

```json
[
  {
    "id": 1,
    "nome": "Minas Gerais",
    "uf": "MG"
  },
  {
    "id": 2,
    "nome": "SAO PAULO",
    "uf": "SP"
  },
  {
    "id": 1002,
    "nome": "Rio de Janeiro",
    "uf": "RJ"
  },
  {
    "id": 1003,
    "nome": "Espirito Santo",
    "uf": "ES"
  }
]
```

## Forma Acesso

### HTTP Request

`GET /academico/tipo_acesso`

> 200

```json
[
  {
    "id": 1,
    "nome": "Vestibular"
  },
  {
    "id": 2,
    "nome": "Transferência"
  }
]
```

## Situação Enade

### HTTP Request

`GET /academico/situacao_enade`

> 200

```json
[
  {
    "id": 1,
    "nome": "Realizou"
  },
  {
    "id": 2,
    "nome": "Nao Realizou"
  }
]
```

## Situação Aluno

### HTTP Request

`GET /academico/situacao_aluno`

> 200

```json
[
  {
    "id": 1,
    "nome": "Aprovado"
  },
  {
    "id": 2,
    "nome": "Reprovado"
  }
]
```
