# Diagrama de Classes

```mermaid
classDiagram
    class User {
        +Long idUser
        +String username
        +String email
        +String password
        +List<Task> tasks
        +Profile profile
        +addTask(Task task)
        +removeTask(Task task)
    }

    class Task {
        +Long idTask
        +String taskName
        +String description
        +LocalDate date
        +LocalDate reminderDate
        +boolean status
        +byte[] taskImage
        +String taskImage64
        +User user
    }

    class Profile {
        +Long idPerfil
        +String nickname
        +byte[] avatar
        +byte[] imagePrincipal
        +String imagem64
        +User user
    }

    class Access {
        +Long id
        +LocalDate dataAcesso
        +User user
    }

    User "1" --> "many" Task : has
    User "1" --> "1" Profile : has
    User "1" --> "many" Access : has
```

### Explicação do Diagrama:

- **User**: Representa a entidade do usuário, contendo atributos como `idUser`, `username`, `email`,
- `password`, uma lista de `Task`, e um `Profile`.
- **Task**: Representa as tarefas atribuídas ao usuário, com atributos como `idTask`, `taskName`, `description`,
-  `date`, `reminderDate`, `status`, `taskImage`, e `taskImage64`.
- **Profile**: Representa o perfil do usuário, contendo atributos como `idPerfil`, `nickname`, `avatar`,
- `imagePrincipal`, e `imagem64`.
- **Access**: Representa os acessos feitos pelo usuário, com atributos como `id` e `dataAcesso`.

### Relações:

- Um `User` pode ter muitas `Task` (relação um-para-muitos).
- Um `User` tem um único `Profile` (relação um-para-um).
- Um `User` pode ter muitos `Access` (relação um-para-muitos).

### Como Usar:

1. **Ambiente de Suporte**: Para visualizar esse diagrama, você precisa de um ambiente que suporte o Mermaid,
2. como alguns editores Markdown, plataformas de documentação (ex: GitHub, GitLab) ou ferramentas de geração de
3. diagramas que suportam Mermaid.
4. **Inserir o Diagrama**: Cole o código acima em seu documento Markdown, utilizando a sintaxe apropriada para o
Mermaid, e visualize o diagrama.




