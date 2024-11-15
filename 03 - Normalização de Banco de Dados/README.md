# 3. Normalização de Banco de Dados

A normalização é um processo usado no design de banco de dados relacional para eliminar redundâncias e inconsistências nos dados. Ela organiza os dados em tabelas de forma lógica, garantindo integridade e eficiência. As tabelas são divididas em estruturas menores e mais específicas, assegurando que cada uma armazene informações relevantes a um único contexto. Esse processo reduz duplicações desnecessárias, economiza espaço de armazenamento e facilita consultas e atualizações.

## 3.1. Primeira Forma Normal (1FN)

Uma tabela está na 1FN quando:

- Todos os valores em uma coluna são atômicos (ou seja, indivisíveis).
- Não existem grupos repetitivos ou atributos multivalorados.

**Exemplo sem normalização:**

