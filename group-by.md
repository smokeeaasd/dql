# GROUP BY: Agrupando Dados em SQL

A cláusula `GROUP BY` é utilizada em consultas SQL para agrupar linhas que têm valores iguais em colunas especificadas em conjuntos de resumo. Geralmente, é usada em conjunto com funções agregadas para calcular valores resumidos para cada grupo.

## Sintaxe Básica

A sintaxe básica para a cláusula `GROUP BY` é a seguinte:

```sql
SELECT coluna1, função_agregada(coluna2)
FROM tabela
GROUP BY coluna1;
```

## Exemplos

### 1. Agrupando por uma Coluna

Para contar o número de clientes em cada cidade:

```sql
SELECT cidade, COUNT(*) AS total_clientes
FROM clientes
GROUP BY cidade;
```

### 2. Agrupando por Múltiplas Colunas

Você pode agrupar por várias colunas. Por exemplo, para contar o número de clientes por cidade e estado:

```sql
SELECT cidade, estado, COUNT(*) AS total_clientes
FROM clientes
GROUP BY cidade, estado;
```

### 3. Usando Funções Agregadas com GROUP BY

Para calcular a média de idade dos clientes agrupados por cidade:

```sql
SELECT cidade, AVG(idade) AS media_idade
FROM clientes
GROUP BY cidade;
```

## Considerações Finais

- A cláusula `GROUP BY` é essencial para agrupar dados em conjuntos de resumo.
- Você pode agrupar por uma ou mais colunas, dependendo da sua necessidade.
- Funções agregadas são frequentemente usadas em conjunto com `GROUP BY` para calcular valores resumidos para cada grupo.
- A cláusula `GROUP BY` é frequentemente usada em conjunto com `HAVING` para filtrar grupos de resultados.