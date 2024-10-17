# ORDER BY: Ordenação de Resultados

A cláusula `ORDER BY` é usada em consultas SQL para ordenar os resultados de acordo com uma ou mais colunas especificadas. Por padrão, a ordenação é feita em ordem crescente (ASC), mas também pode ser alterada para ordem decrescente (DESC).

## Sintaxe Básica

A sintaxe básica para a cláusula `ORDER BY` é a seguinte:

```sql
SELECT coluna1, coluna2
FROM tabela
ORDER BY coluna1 [ASC|DESC], coluna2 [ASC|DESC];
```

## Exemplos

### 1. Ordenar em Ordem Crescente

Para ordenar os resultados pela coluna `nome` em ordem crescente:

```sql
SELECT * FROM clientes
ORDER BY nome ASC;
```

### 2. Ordenar em Ordem Decrescente

Para ordenar os resultados pela coluna `idade` em ordem decrescente:

```sql
SELECT * FROM clientes
ORDER BY idade DESC;
```

### 3. Ordenar por Múltiplas Colunas

Você pode ordenar os resultados por várias colunas. Por exemplo, para ordenar primeiro pela `cidade` e depois pela `idade`:

```sql
SELECT * FROM clientes
ORDER BY cidade ASC, idade DESC;
```

### 4. Ordenação com NULLs

Por padrão, os valores `NULL` aparecem no final quando você usa `ORDER BY` em ordem crescente e no início em ordem decrescente. Para controlar a posição dos `NULLs`, você pode usar `NULLS FIRST` ou `NULLS LAST` (dependendo do banco de dados).

```sql
SELECT * FROM clientes
ORDER BY idade ASC NULLS LAST;
```

## Considerações Finais

- A cláusula `ORDER BY` é essencial para ordenar os resultados de uma consulta SQL.
- Você pode ordenar os resultados em ordem crescente (ASC) ou decrescente (DESC).
- É possível ordenar por múltiplas colunas, especificando a ordem de cada uma delas.
- Os valores `NULL` podem ser controlados na ordenação usando `NULLS FIRST` ou `NULLS LAST`.