# AUTHENTICATION WITH JWT
A autenticação com JSON Web Tokens (JWT) é uma forma segura e eficiente de autenticação em aplicativos web. 
JWTs são tokens criptografados que são transmitidos entre o servidor e o cliente para verificar a identidade do usuário.

Nessa autenticação foi utilizado Node.js com framework express e banco de dados MongoDB.

&nbsp;

## :closed_lock_with_key: Como funciona:
Quando um usuário faz login em um aplicativo web, o servidor cria um token JWT para o usuário. 
Esse token é enviado para o cliente e armazenado no navegador do usuário. 
Em todas as solicitações subsequentes ao servidor, o token é incluído nos cabeçalhos HTTP como um Bearer Token.

O servidor verifica a validade do token e, se for válido, permite que o usuário acesse as informações solicitadas. 
Se o token for inválido ou expirado, o servidor retorna um erro de autenticação.

&nbsp;

## :card_index_dividers: Banco de Dados
Foi utilizado o ElephantSQL para a realização dessa API. Para utilizá-lo siga as instruções:

1. Primeira etapa crie uma conta no [MongoDB atlas](https://www.mongodb.com/atlas/database);
2. Próxima etapa é criar um novo projeto. Isso pode ser feito na seção **'Projects'**;
3. Depois de ter criado um projeto, crie um banco de dados free (mantenha as configurações padrões caso não tenha necessidade mudar);
4. Ao criar um cluster, será solicitado a criação de um usuário. Você pode escolha o nome que preferir 
ou manter o padrão e salvar a senha gerada.
5. Por fim, você precisará adicionar o endereço IP de sua máquina para permitir o acesso ao banco de dados. 
Depois de adicionar o endereço IP, você poderá criar e gerenciar bancos de dados no MongoDB Atlas.

&nbsp;

## ⚙️ Configuração
Para usar a API, você precisa ter o Node.js instalado em seu sistema. Depois de instalados, siga os seguintes passos:

1. Clone o repositório para sua máquina local;
2. Abra o terminal e navegue até o diretório do projeto;
3. Execute o comando `npm install jsonwebtoken express bcrypt dotenv mongoose` para instalar as dependências;
4. Execute o comando `npm install --save-dev nodemon` para sempre que utilizar **CTRL S** resetar o servidor;
5. Crie um arquivo `.env` na raiz do projeto e configure as variáveis de ambiente necessárias:
```
DB_USER = <a url disponibilizada no MongoDB atlas>
DB_PASSWORD = <a senha é gerada no MongoDB atlas>
SECRET = <sequência aleatória de números e letras>
```
6. Execute o comando `npm run start` para iniciar a API.

* OBS: Para encontrar a URL no site do MongoDB atlas é preciso ir no **overview** do banco de dados, clicar em **'connect'**, 
ir na opção **'Connect your application'** e será disponibilizado a url.

&nbsp;

## :film_strip: Vídeo - Autenticação com Node.js e MongoDB com JWT - Login e Registro com Node.js
Vídeo utilizado como suporte para a criação da API.

* https://www.youtube.com/watch?v=qEBoZ8lJR3k&t=2s&ab_channel=MatheusBattisti-HoradeCodar
 
&nbsp;

## 🛠️ Construído com
As ferramentas utilizadas:

* Express - Framework utilizada para a criação da API
* [Postman](https://www.postman.com/) -  é uma ferramenta Open Source para desenvolvimento/teste de API Clients 
* [MongoDB atlas](https://www.mongodb.com/atlas/database) - Banco de dados
