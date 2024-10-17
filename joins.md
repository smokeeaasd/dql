# JOINS: Combinando linhas de tabelas

Os `JOINS` em SQL são utilizados para combinar linhas de duas ou mais tabelas com base em uma condição relacionada entre elas. Existem diferentes tipos de `JOINS`, e cada um tem suas particularidades.

## Tipos de JOINS

### 1. INNER JOIN

O `INNER JOIN` retorna apenas as linhas que têm correspondência em ambas as tabelas.

´´´sql
SELECT clientes.nome, pedidos.data
FROM clientes
INNER JOIN pedidos ON clientes.id = pedidos.cliente_id;
´´´

### 2. LEFT JOIN

O `LEFT JOIN` retorna todas as linhas da tabela à esquerda e as linhas correspondentes da tabela à direita. Se não houver correspondência, os resultados da tabela da direita serão `NULL`.

´´´sql
SELECT clientes.nome, pedidos.data
FROM clientes
LEFT JOIN pedidos ON clientes.id = pedidos.cliente_id;
´´´

### 3. RIGHT JOIN

O `RIGHT JOIN` é o oposto do `LEFT JOIN`. Ele retorna todas as linhas da tabela à direita e as correspondências da tabela à esquerda. Se não houver correspondência, os resultados da tabela da esquerda serão `NULL`.

´´´sql
SELECT clientes.nome, pedidos.data
FROM clientes
RIGHT JOIN pedidos ON clientes.id = pedidos.cliente_id;
´´´

## Considerações Finais

- Os `JOINS` são essenciais para combinar dados de várias tabelas em uma única consulta.
- Existem diferentes tipos de `JOINS`, como `INNER JOIN`, `LEFT JOIN` e `RIGHT JOIN`, cada um com suas próprias características.
- Ao usar `JOINS`, é importante definir corretamente as condições de correspondência para obter os resultados desejados.
- Ao usar `JOINS`, sempre serão usados dois IDs de tabelas diferentes, sendo uma chave estrangeira e uma chave primária.