📚 Sistema de Cadastro de Alunos (CRUD)

> Aplicação de console para gerenciar o cadastro, consulta, atualização e exclusão de alunos, utilizando Java, Maven e PostgreSQL.

![Demonstração do Console](https://i.ibb.co/zhf7hDW4/console-crud-escola.png)
---

📝 Sobre o Projeto

Este projeto é uma aplicação Java que implementa as quatro operações básicas de persistência de dados (Create, Read, Update, Delete). Ele foi construído para demonstrar o uso de **JDBC** para comunicação com um banco de dados PostgreSQL, com todas as dependências gerenciadas pelo **Maven**.

A arquitetura segue o padrão **DAO (Data Access Object)** para separar as regras de negócio da lógica de acesso a dados, e a interação com o usuário é feita através de um menu interativo no console.

---

✨ Funcionalidades

O menu da aplicação permite ao usuário executar as seguintes operações:
* Inserir um novo aluno no banco de dados.
* Atualizar os dados de um aluno existente a partir de seu ID.
* Listar todos os alunos cadastrados.
* Buscar um aluno específico pelo seu ID.
* Deletar um aluno do banco de dados.

---

🚀 Tecnologias Utilizadas

* Linguagem: [Java 17](https://www.oracle.com/java/)
* Banco de Dados: [PostgreSQL](https://www.postgresql.org/)
* Comunicação com BD: [JDBC](https://www.oracle.com/java/technologies/javase/javase-tech-database.html)
* Gerenciador de Dependências: [Maven](https://maven.apache.org/)
* Versionamento: [Git](https://git-scm.com/)

---

▶️ Como Executar o Projeto

Pré-requisitos

Antes de começar, você vai precisar ter instalado em sua máquina as seguintes ferramentas:
* [Git](https://git-scm.com)
* [Java JDK 17](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)
* [Apache Maven](https://maven.apache.org/download.cgi)
* [PostgreSQL](https://www.postgresql.org/download/)

### Rodando o Projeto

```bash
# 1. Clone este repositório
$ git clone [https://github.com/marinho-marcos/Sistema-de-cadastro-de-alunos-CRUD](https://github.com/marinho-marcos/Sistema-de-cadastro-de-alunos-CRUD)

# 2. Acesse a pasta do projeto no terminal/cmd
$ cd Sistema-de-cadastro-de-alunos-CRUD

# 3. Configure o Banco de Dados
# Acesse seu terminal do PostgreSQL (psql) e crie o banco de dados
CREATE DATABASE crud_escola;

# Conecte-se ao banco criado e execute os scripts SQL abaixo para criar as tabelas:
CREATE TABLE curso (
    id_curso SERIAL PRIMARY KEY,
    nome VARCHAR(50)
);

CREATE TABLE aluno (
    id_aluno SERIAL PRIMARY KEY,
    nome VARCHAR(30),
    sobrenome VARCHAR (30),
    idade INT
);

# 4. Configure as Variáveis de Ambiente
# Este projeto utiliza variáveis de ambiente para as credenciais do banco, uma prática segura.
# Configure as seguintes variáveis no seu sistema:

# No Windows (PowerShell)
$ $env:DB_USER="seu_usuario_postgres"
$ $env:DB_PASS="sua_senha_postgres"

# No Linux/Mac
$export DB_USER="seu_usuario_postgres"$ export DB_PASS="sua_senha_postgres"

# 5. Execute a aplicação com o Maven
# O plugin exec-maven-plugin irá compilar e rodar a classe principal
$ mvn exec:java
