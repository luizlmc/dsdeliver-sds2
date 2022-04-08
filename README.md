<h1 align="center">
    <strong>DsDeliver</strong>
    <br>Semana Dev Superior 2.0<br/>
    Spring | React.JS | TypeScript
</h1>

<p align="center">
  <a href="#sobre-o-projeto">Sobre</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#tecnologias-utilizadas">Tecnologias</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#como-executar">Como Executar</a>
</p>

<p align="center">
  <img alt="Design do Projeto" width="1080px" src="https://user-images.githubusercontent.com/77021623/162495520-599643f6-753b-4007-a9f9-463c4aa47e00.png" />
  <img alt="Design do Projeto" width="1080px" src="https://user-images.githubusercontent.com/77021623/162495526-e310b0f7-6946-4536-95c3-d901c5e207bc.png" />
<p>
  
 ## Sobre o Projeto

  Acesse a aplicação [DsDeliver](https://dsdeliver-sds2-luizlmc.netlify.app) no netlify.

O DsDeliver é um sistema de delivery que registra os pedidos dos clientes e organiza a entrega com o endereço em um mapa interativo e dinâmico. Desenvolvido durante a [Semana Dev Superior 2.0](https://devsuperior.com.br) utilizando a tecnologias React.Js com TypeScript no desenvolimento do frontend e SpringBoot para desenolver a API RestFull no backend.

## Tecnologias Utilizadas

- [JDK 11](https://www.oracle.com/java/technologies/downloads/#java11)
- [SpringBoot](https://spring.io/projects/spring-boot)
- [Intellij IDEA](https://www.jetbrains.com/pt-br/idea/)
- [Postgresql](https://www.postgresql.org/download/)
- [Node.js](https://nodejs.org/)
- [ReactJS](https://reactjs.org/)
- [TypeScript](https://www.typescriptlang.org/)
- [API MapBox](https://www.mapbox.com) 

## Como Executar

 ### **Backend**

  1. Faça um clone do repositório:
      Para baixar o código-fonte do projeto em sua máquina, primeiramente terá que ter instalado o Git.
      Com o Git instalado, em seu terminal execute o seguinte comando:

      ```sh
        $ git clone https://github.com/luizlmc/dsdeliver-sds2.git
      ```
  2. Com o projeto baixado navegue até a pasta backend:
      ```sh
        $ cd backend
      ```
      Estando na pasta backend abra-o em sua IDE.
      Como será executado localmente em sua máquina, abra o arquivo application.properties e altere o perfil ativo de prod para test:
      Execute o arquivo DsdeliverApplication.java.
      A aplicação Spring Boot será executada no endereço: http://localhost:8080/.

  ### **Frontend**
  1. Navegue até a pasta frontend: 
  
  ```sh
    $ cd frontend
  ```
  2. Instale as dependências:
      Estando na pasta frontend abra-o em seu editor de texto (vscode, use o atalho **code .** em seu terminal). 
  Em seguida, no terminal do vscode execute: 
  
  ```sh
    $ yarn install
  ```
  3. Atenção, antes de executar a aplicação React:

  > Para a busca de endereços no mapa, foi utilizado o [**Mapbox**](https://www.mapbox.com/), uma plataforma de mapeamento que permite que seus clientes criem soluções de mapeamento personalizadas.

  - Então, se deseja carregar os endereços no mapa, você precisará [**criar uma conta gratuita na plataforma**](https://account.mapbox.com/auth/signup/) e utilizar seu token pessoal de acesso à API.
  - Após a criação da sua conta, na página principal do MapBox, clique em “Account”. Em configurações, clique em **“API access tokens”** e depois em “Create a new token”;
  - Copie o token gerado, e dentro da pasta **`frontend`**, crie um arquivo com a extensão **`.env`**, onde serão definidas as variáveis de ambiente do projeto.
  - Adicione o seguinte conteúdo ao seu arquivo, substituindo **`token`** pelo seu token copiado:
  ```
    REACT_APP_ACCESS_TOKEN_MAP_BOX=token
    REACT_APP_API_URL=http://localhost:8080
  ```

  - Inicie a aplicação React:
  ```sh
    $ yarn start
  ```
  - Acesse a aplicação pelo endereço: _**`http://localhost:3000/`**_.
