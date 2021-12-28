
# Autenticação

O Diploma utiliza JSON Web Token (JWT) como meio de autenticação. Desse modo, cada requisição deve possuir o seguinte cabeçalho:

`Authorization: JWT token`

<aside class="notice">
Você deve substituir <code>token</code> com o token obtido via login.
</aside>
