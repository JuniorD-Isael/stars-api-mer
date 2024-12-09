
As seguintes entidades foram identificadas no banco de dados do projeto:

- **User (Usuário)**:
  - Representa os usuários do sistema.
  - Atributos:
    - `id`: Identificador único do usuário.
    - `email`: E-mail do usuário, único no sistema.
    - `hashed_password`: Senha criptografada do usuário.
    - `is_active`: Flag que indica se o usuário está ativo ou inativo.

- **Item (Item)**:
  - Representa os itens que podem ser atribuídos a um usuário.
  - Atributos:
    - `id`: Identificador único do item.
    - `title`: Título do item.
    - `description`: Descrição do item.
    - `owner_id`: Identificador do usuário dono do item (chave estrangeira referenciando `User.id`).

- **JobTitle (Cargo)**:
  - Representa os cargos ou posições que um voluntário pode ocupar.
  - Atributos:
    - `id`: Identificador único do cargo.
    - `title`: Título do cargo.
    - `is_active`: Flag que indica se o cargo está ativo ou inativo.

- **Volunteer (Voluntário)**:
  - Representa os voluntários no sistema.
  - Atributos:
    - `id`: Identificador único do voluntário.
    - `name`: Nome do voluntário.
    - `linkedin`: URL do perfil do voluntário no LinkedIn.
    - `email`: E-mail do voluntário.
    - `is_active`: Flag que indica se o voluntário está ativo ou inativo.
    - `jobtitle_id`: Identificador do cargo que o voluntário ocupa (chave estrangeira referenciando `JobTitle.id`).
