# API de Autenticação com Flask e JWT

Este é um exemplo de uma API de autenticação construída com o Flask que utiliza tokens JWT (JSON Web Tokens) para autenticar usuários.


## Tecnologias Utilizadas

- **Flask**: Flask é um framework web em Python para o desenvolvimento rápido de aplicativos web.

- **JSON Web Tokens (JWT)**: JWT é um padrão de indústria que define um método compacto e autossuficiente para representar informações entre as partes como um objeto JSON.

- **Python**: A linguagem de programação usada para criar a lógica da API.

## Bibliotecas Utilizadas

- **Flask**: O Flask é a biblioteca principal usada para criar a API.

- **JWT (PyJWT)**: PyJWT é uma biblioteca Python que permite codificar e decodificar tokens JWT.



## Funcionalidades

- **Rota `/unprotected`**: Uma rota pública que retorna uma mensagem simples que pode ser acessada por qualquer pessoa.

- **Rota `/protected`**: Uma rota protegida por autenticação JWT. Para acessá-la, é necessário incluir um token JWT válido como parâmetro de consulta na URL.

- **Rota `/login`**: Permite que os usuários obtenham um token JWT fazendo login com um nome de usuário e senha.

## Configuração

### Definindo a Chave Secreta

A chave secreta usada para codificar e decodificar tokens JWT é definida na variável `app.config['SECRET_KEY']` no código. Certifique-se de definir uma chave secreta forte e única para a sua aplicação.

### Executando a API

Para executar a API, utilize o comando:

    
    python app.py


## Uso

Fazendo Login
Utilize a rota /login para fazer login fornecendo um nome de usuário e senha. O token JWT será gerado e retornado na resposta.

**Acessando Recursos Protegidos**:
Para acessar recursos protegidos pela autenticação, inclua o token JWT gerado como um parâmetro de consulta na URL. Por exemplo, /protected?token=token_aqui.

**Recursos Não Protegidos**:
A rota /unprotected pode ser acessada por qualquer pessoa sem a necessidade de um token.

**Expiração do Token**:
Os tokens JWT gerados têm um tempo de expiração configurado (45 segundos no exemplo). Após a expiração, o token não é mais válido e você precisará fazer login novamente.

### Importância
Esta API serve como um exemplo básico de autenticação com tokens JWT, amplamente usado em aplicativos web para proteger rotas e recursos sensíveis. Também demonstra como configurar e executar um aplicativo Flask simples.

Por favor, note que esta é uma implementação mínima e não deve ser usada em produção sem medidas adicionais de segurança, como criptografia adequada das senhas e gerenciamento seguro de chaves secretas.

Nota: Certifique-se de seguir as melhores práticas de segurança ao construir e implantar uma API de autenticação em um ambiente de produção.

A autenticação é uma parte fundamental da segurança de aplicativos, e esta API fornece um ponto de partida simples para implementações mais avançadas.



## Etiquetas


[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)
[![AGPL License](https://img.shields.io/badge/license-AGPL-blue.svg)](http://www.gnu.org/licenses/agpl-3.0)