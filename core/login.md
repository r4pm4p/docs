# Login

### Rota

    - /login

### Nível de Acesso

    - Livre


### Campos

    - email: relativo ao email do usuário, string(100), ex: "kwest@gmail.com"
    - password: relativo a senha do usuário, string(100), ex: "senha123"

### Retorno

    - token: relatuvo ao token jwt para que seja enviado nas chamdas que precisam de login
