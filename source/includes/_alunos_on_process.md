
# Alunos

## Alunos por Processo

### Listar alunos do processo
> 200

```json
{
  "id": 1,
  "nome": "Aluno",
  "nome_social": "Nome social aluno",
  "data_formatura": "12/12/2012",
  "data_nascimento": "01/01/2001",
  "sexo": {
      "id": 1,
      "sexo": "M"
  },
  "nacionalidade": {
      "id": 1,
      "nome": "BRASILEIRA"
  },
  "estado_civil": {
      "id": 1,
      "nome": "SOLTEIRO"
  },
  "naturalidade": {
      "id": 1,
      "estado": {
          "id": 1,
          "nome": "Minas Gerais",
          "uf": "MG"
      },
      "nome": "Belo Horizonte",
      "codigo_ibge": "123"
  },
  "cpf": "12345678910",
  "uf": {
      "id": 1,
      "nome": "Minas Gerais",
      "uf": "MG"
  },
  "rg_orgaoexpedidor": "PMMG",
  "rg_numero": "20.074.153",
  "rg_uf": {
      "id": 1,
      "nome": "Minas Gerais",
      "uf": "MG"
  },
  "rg_data_expedicao": "04/12/2012",
  "profile_img_key": "img_aluno",
  "external_url": "external_url",
  "tipos_acesso": {
    "id": 1,
    "nome": "Programas de avaliação seriada ou continuada"
  },
  "nome_filiacao": "Maria Lúcia",
  "nome_social_filiacao": "Maria",
  "sexo_filiacao": {
    "id": 2,
    "sexo": "F"
  },
  "data_ingresso": "14/12/2021",
  "data_conclusao": "14/12/2022",
  "data_enade": "14/12/2021",
  "titulo_eleitor": "1231231",
  "situacao_enade": {
      "id": 2,
      "nome": "Nao Realizou"
  },
  "situacao_aluno": {
      "id": 1,
      "nome": "Aprovado"
  }
}
```

### HTTP Request

`GET /diplomas/processos/<processId>/alunos`


### Retornar um usuário específico.

### HTTP Requests

`GET /diplomas/processos/<processId>/alunos/<alunoId>`

### URL Parameters

| Parameter | Description                  |
| --------- | ---------------------------- |
| processId    | O ID do processo |
| alunoId    | O ID do aluno a ser obtido |

## Criando um Aluno

### HTTP Requests

`POST /diplomas/processos/<processId>/alunos`

### Payload

Dados que são necessários para a geração de XML do aluno:
Nome, Sexo, Nacionalidade, Naturalidade, Estado Civil , CPF, Número do RG,UF do RG, RG Orgão Expedidor,
RG Data Expedicao, data de nascimento, data formatura, Título de Eleitor, Tipos Acesso, Nome Filiação,
Sexo Filição, Data de Ingresso, Data Conclusão, Situação Aluno, Situação Enade, Data Enade.

> Payload Example:

```json
{
 "id": 1,
  "nome": "Aluno",
  "nome_social": "Nome social aluno",
  "data_formatura": "12/12/2012",
  "data_nascimento": "01/01/2001",
  "sexo": 1,
  "nacionalidade": 1,
  "estado_civil": 1,
  "naturalidade": 1,
  "cpf": "12345678910",
  "uf": 1,
  "rg_orgaoexpedidor": "PMMG",
  "rg_numero": "20.075.153",
  "rg_uf": 1,
  "rg_data_expedicao": "04/12/2012",
  "profile_img_key": "img_aluno",
  "external_url": "external_url",
  "tipos_acesso": 1,
  "nome_filiacao": "Maria Lícia",
  "nome_social_filiacao": "Maria",
  "sexo_filiacao": 2,
  "data_ingresso": "14/12/2021",
  "data_conclusao": "14/12/2022",
  "data_enade": "14/12/2021",
  "titulo_eleitor": "1231231",
  "situacao_enade": 2,
  "situacao_aluno": 1,
}
```
| Parameter                  | Type      | Description                               |
| -------------------------- | --------- | ----------------------------------------- |
| `nome`                     | _string_  | Nome completo                             |
| `nome_social`              | _string?_ | Nome Social                               |
| `sexo.id`                  | _id_      | [Sexo](#aluno-sexo)                       |
| `nacionalidade.id`         | _id_      | [Nacionalidade](#nacionalidade)           |
| `estado_civil.id`          | _id_      | [Estado Civil](#estado-civil)             |
| `naturalidade.id`          | _id_      | [Naturalidade](#municipio-e-naturalidade) |
| `data_nascimento`          | _date_    | Data de Nascimento                        |
| `data_formatura`           | _date_    | Data de Formatura                         |
| `cpf`                      | _string_  | CPF                                       |
| `rg_numero`                | _string_  | Número do RG                              |
| `rg_orgaoexpedidor`        | _string_  | Orgão Expedidor RG                        |
| `rg_uf.id`                 | _id_      | [UF Estado](#estado)                      |
| `rg_data_expedicao`        | _string_  | RG Data de Expedição                      |
| `titulo_eleitor`           | _string?_ | Título de Eleitor                         |
| `tipos_acesso.id`          | _id_      | [Tipo Acesso](#forma-acesso)              |
| `nome_filiacao`            | _string_  | Nome Filiação                             |
| `nome_social_filiacao`     | _string_  | Nome Social Filiação                      |
| `sexo_filiacao.id`         | _string_  | [Sexo](#aluno-sexo)                       |
| `data_ingresso`            | _date_    | Data Ingresso                             |
| `situacao_aluno.id`        | _id_      | [Situação Aluno](#situacao-aluno)         |
| `situacao_enade.id`        | _id_      | [Situação Enade](#situacao-enade)         |
| `data_enade`               | _date_    | Data Enade                                |

`?`: campo opcional
