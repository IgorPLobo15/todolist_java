# Aplicação de Lista de Tarefas (To-Do List) com Spring Boot e MySQL

Este é um projeto de exemplo de uma aplicação de lista de tarefas (To-Do List) desenvolvida em Java com o framework Spring Boot e usando um banco de dados MySQL do H2 database para armazenar tarefas e usuários. A aplicação permite que os usuários criem tarefas, vinculem essas tarefas aos seus usuários e realizem alterações nas informações das tarefas, se necessário.

## Requisitos

Certifique-se de ter as seguintes ferramentas instaladas em seu ambiente de desenvolvimento:

- Java Development Kit (JDK)
- Spring Boot
- MySQL H2 database
- Apache Maven

## Configuração do Banco de Dados

Antes de executar a aplicação, você precisa configurar o banco de dados MySQL. Abra o arquivo `src/main/resources/application.properties` e atualize as configurações do banco de dados, como URL, nome de usuário e senha:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/seubancodedados
spring.datasource.username=seuusuario
spring.datasource.password=suasenha

## Executando a Aplicação

Após configurar o banco de dados, você pode executar a aplicação usando o Maven. Na raiz do projeto, execute o seguinte comando:

```bash
mvn spring-boot:run

