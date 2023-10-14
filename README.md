# Aplicação de Lista de Tarefas (To-Do List) com Spring Boot e MySQL

Este é um projeto de exemplo de uma aplicação de lista de tarefas (To-Do List) desenvolvida em Java com o framework Spring Boot e usando um banco de dados H2 (MySQL) para armazenar tarefas e usuários. A aplicação permite que os usuários criem tarefas, vinculem essas tarefas aos seus usuários e realizem alterações nas informações das tarefas, se necessário. Além disso, é importante destacar que as senhas dos usuários são armazenadas de forma segura, utilizando criptografia para garantir a segurança das informações.

## Requisitos

Certifique-se de ter as seguintes ferramentas instaladas em seu ambiente de desenvolvimento:

- Java Development Kit (JDK)
- Spring Boot
- MySQL H2 database port: 8080
- Apache Maven
## Uso da Aplicação
### Criar um Novo Usuário
Para criar um novo usuário, você pode usar uma solicitação POST com o seguinte formato JSON:
```markdown
[http://localhost:8080/users/](http://localhost:8080/users/)
```
```markdown
{
    "name": "Nome do Usuário",
    "username": "Nome de Usuário Escolhido",
    "password": "Senha Segura"
}
```


### Para criar uma nova tarefa:
Para criar uma nova tarefa, você pode usar uma solicitação POST com o seguinte formato JSON:
```markdown
[http://localhost:8080/tasks/](http://localhost:8080/tasks/)
```
```markdown
{
    "description": "Descrição da Tarefa",
    "title": "Título da Tarefa",
    "priority": "Prioridade da Tarefa (Baixa, Média, Alta)",
    "startAt": "Data e Hora de Início (Formato: YYYY-MM-DDTHH:mm:ss)",
    "endAt": "Data e Hora de Término (Formato: YYYY-MM-DDTHH:mm:ss)"
}
```
### Para obter informações de um usuário:
Para exibir uma tarefa, você pode usar uma solicitação GET com o seguinte formato JSON: 
- Lembre-se de substituir {id} pelo ID do usuário que deseja obter ou atualizar.
```markdown
[GET /api/usuarios/{id}](http://localhost:8080/tasks/)
```
### Para atualizar as informações de uma Tarefa:
Para atualizar uma tarefa declare apenas  o que queres mudar, você pode usar uma solicitação UPDATE com o seguinte formato JSON:
```markdown
http://localhost:8080/tasks/
```
```markdown
{
    "description": "Descrição da Tarefa",
    "title": "Título da Tarefa",
    "priority": "Prioridade da Tarefa (Baixa, Média, Alta)",
    "startAt": "Data e Hora de Início (Formato: YYYY-MM-DDTHH:mm:ss)",
    "endAt": "Data e Hora de Término (Formato: YYYY-MM-DDTHH:mm:ss)"
}
```


