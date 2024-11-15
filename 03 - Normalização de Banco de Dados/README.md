# 3. Normalização de Banco de Dados

A normalização é um processo usado no design de banco de dados relacional para eliminar redundâncias e inconsistências nos dados. Ela organiza os dados em tabelas de forma lógica, garantindo integridade e eficiência. As tabelas são divididas em estruturas menores e mais específicas, assegurando que cada uma armazene informações relevantes a um único contexto. Esse processo reduz duplicações desnecessárias, economiza espaço de armazenamento e facilita consultas e atualizações.

## 3.1. Primeira Forma Normal (1FN)

Uma tabela está na 1FN quando:

- Todos os valores em uma coluna são atômicos (ou seja, indivisíveis).
- Não existem grupos repetitivos ou atributos multivalorados.

**Exemplo sem normalização:**

| id_aluno | nome  | telefone | endereço |
| -------- | ----- | -------- | -------- |
| 1        | João  | 48 1111111111, 21 2222222222 | Rua A, 101, Bairro X, Curitiba |
| 2        | Maria | 11 3333333333 | Rua C, 202, Centro, São Paulo |

**Problemas:**

- A coluna `endereço` armazena informações compostas.
- A coluna `telefone` contém múltiplos valores, dificultando consultas.

**Solução (1FN aplicada):**

| id_aluno | nome  | rua   | numero | bairro   | cidade    |
| -------- | ----- | ----- | ------ | -------- | --------- |
| 1        | João  | Rua A |  101   | Bairro X | Curitiba  |
| 2        | Maria | Rua C |  202   | Centro   | São Paulo |

Tabela aluno_telefone:

| id_aluno | telefone      |
| -------- | ------------- |
| 1        | 48 1111111111 |
| 1        | 21 2222222222 |
| 2        | 11 3333333333 |

## 3.2. Segunda Forma Normal (2FN)

Uma tabela está na 2FN quando:

- Atende à 1FN.
- Todos os atributos que não são chave dependem unicamente da chave primária.

**Exemplo sem normalização:**

| id_venda | data_compra | valor_compra | id_curso | curso  |
| -------- | ----------- | ------------ | -------- | ------ |
| 1        |  02/05/2024 | 280.00       |  2       | Python |
| 2        |  03/08/2024 | 349.00       |  5       | Java   |

**Problemas:**

- A coluna `curso` depende de `id_curso`, não de `id_venda`.

**Solução (2FN aplicada):**

1. Criar uma tabela para os cursos:

| id_curso | curso  |
| -------- | ------ |
| 2        | Python |
| 5        | Java   |

2. Ajustar a tabela de vendas:

| id_venda | data_compra | valor_compra | id_curso |
| -------- | ----------- | ------------ | -------- |
| 1        |  02/05/2024 | 280.00       |  2       |
| 2        |  03/08/2024 | 349.00       |  5       |