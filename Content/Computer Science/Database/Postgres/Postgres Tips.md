[[Postgres]]
Para garantir que apenas o usuário `dba` possa acessar e utilizar o schema `starlov`, você pode seguir estas etapas no PostgreSQL. Qualquer outro usuário que precise acessar o schema terá que receber permissões explicitamente. Aqui está o passo a passo:

---
Conceder acesso a um usuário novo a um schema.
### **1. Remova as permissões padrão do schema**

Por padrão, todos os usuários podem acessar objetos no schema `public` ou em schemas que não têm restrições específicas. Para restringir o acesso ao schema `starlov`, remova todas as permissões herdadas:

sql

Copiar código

`REVOKE ALL ON SCHEMA starlov FROM PUBLIC;`

- **`PUBLIC`**: Representa todos os usuários.
- Este comando impede qualquer usuário (exceto o proprietário) de acessar o schema.

---

### **2. Conceda acesso total ao usuário `dba`**

Conceda explicitamente ao usuário `dba` as permissões necessárias no schema:

sql

Copiar código

`GRANT ALL ON SCHEMA starlov TO dba;`

Isso permite que o usuário `dba`:

- Crie tabelas e outros objetos dentro do schema.
- Acesse objetos existentes no schema.

---

### **3. Configure permissões para futuros objetos no schema**

Para garantir que o usuário `dba` seja o único com acesso a novos objetos criados no schema, ajuste as permissões padrão:

sql

Copiar código

`ALTER DEFAULT PRIVILEGES IN SCHEMA starlov  GRANT ALL ON TABLES TO dba;`

Isso garante que qualquer nova tabela criada no schema `starlov` tenha permissões concedidas apenas ao `dba`.

Se for necessário restringir mais objetos, você pode repetir o comando para **sequences** e **functions**:

sql

Copiar código

`ALTER DEFAULT PRIVILEGES IN SCHEMA starlov  GRANT ALL ON SEQUENCES TO dba;  ALTER DEFAULT PRIVILEGES IN SCHEMA starlov  GRANT EXECUTE ON FUNCTIONS TO dba;`

---

### **4. Opcional: Conceder acesso a outros usuários (quando necessário)**

Se outro usuário precisar acessar o schema, você pode conceder permissões específicas de forma granular. Por exemplo:

- Para leitura:
    
    sql
    
    Copiar código
    
    `GRANT USAGE ON SCHEMA starlov TO user_name; GRANT SELECT ON ALL TABLES IN SCHEMA starlov TO user_name;`
    
- Para leitura e escrita:
    
    sql
    
    Copiar código
    
    `GRANT USAGE ON SCHEMA starlov TO user_name; GRANT SELECT, INSERT, UPDATE, DELETE ON ALL TABLES IN SCHEMA starlov TO user_name;`