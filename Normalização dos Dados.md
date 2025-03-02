
Temos as seguintes entidades identificadas no banco de dados:

- **User (Usuário)**
  - Atributos:
    - `id` (PK)
    - `email` (único)
    - `hashed_password`
    - `is_active` (boolean)
  
- **Item (Item)**
  - Atributos:
    - `id` (PK)
    - `title`
    - `description`
    - `owner_id` (FK para User)

- **JobTitle (Cargo)**
  - Atributos:
    - `id` (PK)
    - `title`
    - `is_active` (boolean)

- **Volunteer (Voluntário)**
  - Atributos:
    - `id` (PK)
    - `name`
    - `linkedin`
    - `email`
    - `is_active` (boolean)
    - `jobtitle_id` (FK para JobTitle)

Relacionamentos:

- **User ↔ Item**: Relacionamento de 1 para N, onde um usuário pode ter vários itens. `User.id` é referenciado por `Item.owner_id`.
- **JobTitle ↔ Volunteer**: Relacionamento de 1 para N, onde um cargo pode ter vários voluntários. `JobTitle.id` é referenciado por `Volunteer.jobtitle_id`.

Normalização:

- **Primeira Forma Normal (1FN)**: Todos os campos possuem valores atômicos, ou seja, não há atributos compostos ou repetidos.
- **Segunda Forma Normal (2FN)**: O banco de dados atende à 1FN e não possui dependências parciais. Todos os atributos dependem completamente da chave primária.
- **Terceira Forma Normal (3FN)**: O banco de dados está em 2FN e não possui dependências transitivas. Não há atributos que dependam de outras colunas que não sejam a chave primária.

Com isso, o banco de dados está normalizado até a **Terceira Forma Normal (3FN)**, sem redundâncias ou dependências indevidas.
