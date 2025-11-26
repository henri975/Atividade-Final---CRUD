# Atividade-Final---CRUD
Atividade Final - CRUD - ETEC Pedro Ferreira Alves

## Pré-requisitos
- **JDK 17+**
- **MySQL** local
- **Maven 3.9+** (ou o Maven embutido da IDE)

## Banco de dados
Crie o banco uma vez:
```sql
CREATE DATABASE escola CHARACTER SET utf8mb4;
```
Depois edite `src/main/resources/com/example/fxmysqlfxml/config.properties` com usuário/senha.

> Na primeira execução, a tabela `students` e `teacher` é criada automaticamente.

## Rodando
No terminal, dentro da pasta do projeto:
```bash
mvn -P runfx javafx:run
```
Na IDE, execute o goal **javafx:run**.

## Telas
- **MainView.fxml** — tabela de alunos e botões *Novo, Editar, Excluir, Atualizar*.
- **StudentForm.fxml** — formulário modal para criar/editar a tabela student.
- **TeacherForm.fxml** — formulário modal para criar/editar a tabela teacher.
- **AboutView.fxml** — janela "Sobre".

## Estrutura Java
- `App` — carrega a tela principal.
- `MainController` — ações da tela principal e abertura dos diálogos.
- `StudentFormController` — validação e retorno do aluno digitado.
- `TeacherFormController` — validação e retorno do professor digitado.
- `AboutController` — texto estático.
- `Db` — lê `config.properties`, abre conexão e cria tabela.
- `StudentDao` — CRUD com `PreparedStatement`.
- `TeacherDao` — CRUD com `PreparedStatement`.
- `Student` — entidade aluno.
- `Teacher` — entidade professor.
