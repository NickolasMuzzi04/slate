# Login

## Realizando o login

Recebe o retorna de um novo JWT para o usuário.

### HTTP Request

`POST /auth/login/`

### Payload

> Payload Exemple

```json
{
  "username": "usuario",
  "password": "senha",
}
```

> 200 OK

```json
{
  "token": "token",
  "user": {
    "id": 1,
    "username": "usuario",
    "email": "usuario@host.com.br",
  },
}
```

Parameter | Type | Description
--------- | ---- | -----------
`username` | *string* | Username
`password` | *string* | Senha

### Errors

Status | Message
------ | -----------
400 | {"non_field_errors": ["Impossível logar com as credenciais fornecidas."]}
