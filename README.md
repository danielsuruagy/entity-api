# TrilhaApiDesafio – TarefaController

API RESTful em **ASP.NET Core** para gerenciar tarefas de um sistema de organização. Permite criar, ler, atualizar e deletar tarefas, além de consultas filtradas por título, data ou status.

## Estrutura do Projeto

- **Controller:** `TarefaController` – gerencia operações CRUD e consultas.
- **Contexto:** `OrganizadorContext` – gerencia conexão com banco via Entity Framework Core.
- **Modelo:** `Tarefa` – entidade com `Id`, `Titulo`, `Descricao`, `Data` e `Status`.

## Endpoints

### Criar, Atualizar e Deletar

- **POST /Tarefa**  
  Cria uma nova tarefa.  
  **Validações:**  Data da tarefa não pode ser vazia  

- **PUT /Tarefa/{id}**  
  Atualiza uma tarefa existente.  
  **Validações:**  Data da tarefa não pode ser vazia | ID da URL deve coincidir com ID da tarefa  

- **DELETE /Tarefa/{id}**  
  Remove tarefa pelo `id`.  

### Obter Tarefas

- **GET /Tarefa/{id}**  
  Retorna a tarefa pelo `id`.  

- **GET /Tarefa/ObterTodos**  
  Retorna todas as tarefas.  

- **GET /Tarefa/ObterPorTitulo?titulo=xxx**  
  Retorna tarefas que contêm o título especificado.  

- **GET /Tarefa/ObterPorData?data=yyyy-MM-dd**  
  Retorna tarefas de uma data específica.  

- **GET /Tarefa/ObterPorStatus?status=EnumStatusTarefa**  
  Retorna tarefas filtradas por status.  

## Tecnologias

- .NET C#
- ASP.NET Core
- Entity Framework
- SQL Server
