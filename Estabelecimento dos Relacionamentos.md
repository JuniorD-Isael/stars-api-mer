
Relacionamentos entre as entidades do banco de dados:

- **User (Usuário)** e **Item (Item)**:
  - Relacionamento de **um para muitos** (1:N).
  - Um usuário pode ter vários itens, mas um item pertence a apenas um usuário.
  - O relacionamento é feito através da chave estrangeira `owner_id` na tabela `Item`, que referencia o `id` da tabela `User`.

- **JobTitle (Cargo)** e **Volunteer (Voluntário)**:
  - Relacionamento de **um para muitos** (1:N).
  - Um cargo pode ser atribuído a vários voluntários, mas um voluntário ocupa apenas um cargo.
  - O relacionamento é feito através da chave estrangeira `jobtitle_id` na tabela `Volunteer`, que referencia o `id` da tabela `JobTitle`.

- **User (Usuário)** e **Volunteer (Voluntário)**:
  - Não existe um relacionamento direto entre estas duas entidades no banco de dados. Porém, o usuário pode estar associado a um ou mais voluntários de forma indireta, com base nas ações e permissões atribuídas, caso seja implementado um relacionamento futuro entre ambas.
