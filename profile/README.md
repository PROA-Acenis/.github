# 🌟 ACENIS — Plataforma de Conexão: Profissionais e Responsáveis

**ACENIS** é uma aplicação web full-stack robusta, desenvolvida para ser uma ponte entre **profissionais da saúde/desenvolvimento humano** e **pais ou responsáveis**. O projeto demonstra um ciclo de desenvolvimento completo, desde a concepção da arquitetura e codificação até a publicação em uma infraestrutura de nuvem moderna e escalável.

---

## 💡 Sobre o Projeto

A plataforma foi construída para validar um sistema completo e funcional, com foco em uma arquitetura de serviços bem definida e desacoplada.

### Funcionalidades Principais

✨ **Cadastro Distinto:** Formulários e rotas específicas para o cadastro de "Profissionais" e "Responsáveis", cada um com seu respectivo tipo de perfil.

🔐 **Autenticação Unificada:** Um único endpoint de login capaz de autenticar os diferentes tipos de usuário.

⚙️ **API RESTful Completa:** Backend robusto que gerencia todas as operações de CRUD e oferece endpoints para listagens filtradas (ex: listar apenas profissionais).

🗄️ **Banco de Dados Relacional:** Estrutura de dados persistida em MySQL, com migração de um ambiente local para a nuvem.

---

## 🧩 Tecnologias e Infraestrutura

- ⚛️ **Frontend:** React.js (JavaScript)
- ☕ **Backend:** Spring Boot (Java 17) com Spring Web, Spring Data JPA e Python
- 🛢️ **Banco de Dados:** MySQL
- ☁️ **Cloud (Backend & DB):** Railway
- △ **Cloud (Frontend):** Vercel
- 📦 **Gerenciadores de Dependência:** Maven (Java) / npm (Node)
-  **Controle de Versão:** Git / GitHub

---

## 🚀 Como Inicializar o Projeto Localmente

### 🔧 Pré-requisitos

- [Node.js](https://nodejs.org/) (v18+)
- [Java 17+](https://adoptium.net/) (JDK) e [Maven](https://maven.apache.org/)
- Um servidor **MySQL** instalado e rodando localmente.

### ▶️ Executando

O frontend e o backend devem ser iniciados em terminais separados.

#### 1. Banco de Dados (MySQL)

1.  Garanta que seu servidor MySQL local esteja rodando.
2.  Crie um banco de dados (schema) para o projeto, por exemplo, `acenis_local_db`.
3.  Execute o script de criação das tabelas e insira os dados iniciais, se necessário.

#### 2. Backend (Java/Spring Boot)

1.  Abra um terminal e navegue até a pasta do backend (ex: `/backend-acenis`).
2.  Configure o arquivo `src/main/resources/application.properties` para conectar ao seu banco de dados local:
    ```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/acenis_local_db
    spring.datasource.username=seu_usuario_mysql
    spring.datasource.password=sua_senha_mysql
    spring.jpa.hibernate.ddl-auto=validate
    ```
3.  Execute o comando para iniciar a aplicação:
    ```bash
    mvn spring-boot:run
    ```
4.  O backend estará rodando em `http://localhost:8081`.

#### 3. Frontend (React)

1.  Abra um **novo terminal** e navegue até a pasta do frontend (ex: `/frontend-acenis`).
2.  Instale as dependências (só precisa fazer na primeira vez):
    ```bash
    npm install
    ```
3.  Garanta que seu código frontend está fazendo as chamadas de API para o backend local. O ideal é usar um arquivo `.env.development` com o conteúdo:
    ```
    REACT_APP_API_URL=http://localhost:8081
    ```
4.  Execute o comando para iniciar o servidor de desenvolvimento:
    ```bash
    npm start
    ```
5.  Acesse a aplicação no seu navegador em `http://localhost:3000`.
