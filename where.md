# WHERE: Filtrando Resultados

O comando `WHERE` em SQL é utilizado para filtrar registros com base em uma ou mais condições. Ele é frequentemente usado em conjunto com o comando `SELECT` para restringir os resultados da consulta.

## Sintaxe Básica

```sql
SELECT coluna1, coluna2, ... FROM nome_da_tabela WHERE condição;
```

- `coluna1`, `coluna2`, ...: As colunas que você deseja buscar.
- `nome_da_tabela`: O nome da tabela de onde os dados serão extraídos.
- `condição`: A condição que os registros devem atender para serem incluídos nos resultados.

## Exemplo Simples

Vamos considerar a tabela `clientes`, que contém as colunas `id`, `nome`, `idade`, `cidade`.

Para buscar clientes que moram na cidade de "São Paulo":

```sql
SELECT * FROM clientes WHERE cidade = 'São Paulo';
```

## Operadores de Comparação

Você pode usar diferentes operadores de comparação nas condições do `WHERE`:

- `=`: Igual a
- `!=` ou `<>`: Diferente de
- `>`: Maior que
- `<`: Menor que
- `>=`: Maior ou igual a
- `<=`: Menor ou igual a

Exemplo utilizando o operador `>`:

```sql
SELECT * FROM clientes WHERE idade > 30;
```

## Operadores Lógicos

Os operadores lógicos `AND`, `OR` e `NOT` podem ser usados para combinar várias condições:

- **AND**: Ambas as condições devem ser verdadeiras.
- **OR**: Pelo menos uma das condições deve ser verdadeira.
- **NOT**: Inverte o resultado da condição.

Exemplo utilizando `AND`:

Retorna clientes que moram em São Paulo e têm mais de 25 anos.

```sql
SELECT * FROM clientes WHERE cidade = 'São Paulo' AND idade > 25;
```

Exemplo utilizando `OR`:

Retorna clientes que moram em São Paulo ou no Rio de Janeiro.

```sql
SELECT * FROM clientes WHERE cidade = 'São Paulo' OR cidade = 'Rio de Janeiro';
```

## Filtrando com IN e BETWEEN

Você também pode usar os operadores `IN` e `BETWEEN` para simplificar suas consultas.

### IN

Retorna clientes que moram em São Paulo ou no Rio de Janeiro.

```sql
SELECT * FROM clientes WHERE cidade IN ('São Paulo', 'Rio de Janeiro');
```

### BETWEEN

Retorna clientes com idade entre 20 e 30 anos.

```sql
SELECT * FROM clientes WHERE idade BETWEEN 20 AND 30;
```

## Considerações Finais

- A cláusula `WHERE` é essencial para filtrar os resultados de uma consulta SQL.
- Você pode usar operadores de comparação e lógicos para criar condições complexas.
- Os operadores `IN` e `BETWEEN` podem ser úteis para simplificar suas consultas.
- O comando `WHERE` é frequentemente combinado com o comando `SELECT` para buscar dados específicos de uma tabela.
- A correta utilização do `WHERE` permite obter resultados mais precisos e relevantes em suas consultas SQL.