
Atributos das entidades identificadas no banco de dados:

- **User (Usuário)**:
  - `id`: Inteiro, chave primária, identificador único do usuário.
  - `email`: String de até 320 caracteres, e-mail único do usuário, usado para autenticação e identificador no sistema.
  - `hashed_password`: String de até 255 caracteres, senha do usuário, armazenada de forma criptografada.
  - `is_active`: Booleano, indica se o usuário está ativo no sistema.

- **Item (Item)**:
  - `id`: Inteiro, chave primária, identificador único do item.
  - `title`: String de até 255 caracteres, título do item.
  - `description`: String de até 300 caracteres, descrição opcional do item.
  - `owner_id`: Inteiro, chave estrangeira referenciando o `id` de um usuário da tabela `User`, indicando quem é o dono do item.

- **JobTitle (Cargo)**:
  - `id`: Inteiro, chave primária, identificador único do cargo.
  - `title`: String de até 255 caracteres, título do cargo.
  - `is_active`: Booleano, indica se o cargo está ativo ou inativo.

- **Volunteer (Voluntário)**:
  - `id`: Inteiro, chave primária, identificador único do voluntário.
  - `name`: String de até 45 caracteres, nome do voluntário.
  - `linkedin`: String de até 3000 caracteres, URL do perfil do voluntário no LinkedIn.
  - `email`: String de até 255 caracteres, e-mail do voluntário.
  - `is_active`: Booleano, indica se o voluntário está ativo no sistema.
  - `jobtitle_id`: Inteiro, chave estrangeira referenciando o `id` de um cargo na tabela `JobTitle`, indicando o cargo do voluntário.
