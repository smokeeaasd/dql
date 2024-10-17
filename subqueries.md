# SUBQUERIES: Consultas Aninhadas no SQL

Uma subquery (ou subconsulta) é uma consulta SQL aninhada dentro de outra consulta. Elas são usadas para retornar dados que serão usados na consulta externa. As subqueries podem ser utilizadas em várias partes de uma consulta SQL, como na cláusula `SELECT`, `WHERE` ou `FROM`.

## Tipos de Subqueries

### 1. Subquery na Cláusula SELECT

Uma subquery pode ser utilizada para calcular um valor que será retornado na lista de seleção.

```sql
SELECT nome,
(SELECT COUNT(*)
FROM pedidos
WHERE pedidos.cliente_id = clientes.id) AS total_pedidos
FROM clientes;
```

### 2. Subquery na Cláusula WHERE

Uma subquery na cláusula `WHERE` pode ser usada para filtrar os resultados da consulta externa.

```sql
SELECT nome
FROM clientes
WHERE id IN (SELECT cliente_id
FROM pedidos
WHERE data > '2023-01-01');
```

### 3. Subquery na Cláusula FROM

Uma subquery pode ser utilizada na cláusula `FROM` para tratar o resultado como uma tabela temporária.

```sql
SELECT cidade, AVG(media_idade) AS media_idade
FROM (SELECT cidade, idade, AVG(idade) AS media_idade
FROM clientes
GROUP BY cidade) AS subquery
GROUP BY cidade;
```

## Considerações Finais

- As subqueries podem retornar um único valor, uma lista de valores ou um conjunto de resultados.
- As subqueries são úteis para consultas complexas que requerem a combinação de resultados de várias tabelas.
- As subqueries podem ser utilizadas em várias partes de uma consulta SQL, como na cláusula `SELECT`, `WHERE` ou `FROM`.
