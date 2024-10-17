# Funções Agregadas

As funções agregadas são utilizadas para realizar cálculos em um conjunto de valores e retornar um único valor. Elas são frequentemente usadas em conjunto com a cláusula `GROUP BY`. Abaixo estão algumas das funções agregadas mais comuns em SQL.

## Funções Agregadas Comuns

### 1. COUNT()

Retorna o número de linhas que correspondem a uma condição específica.

```sql
SELECT COUNT(*) FROM clientes;
```

### 2. SUM()

Calcula a soma de uma coluna numérica.

```sql
SELECT SUM(idade) FROM clientes;
```

### 3. AVG()

Calcula a média dos valores de uma coluna numérica.

```sql
SELECT AVG(idade) FROM clientes;
```

### 4. MAX()

Retorna o maior valor de uma coluna.

```sql
SELECT MAX(idade) FROM clientes;
```

### 5. MIN()

Retorna o menor valor de uma coluna.

```sql
SELECT MIN(idade) FROM clientes;
```

## Usando Funções Agregadas com GROUP BY

As funções agregadas são frequentemente usadas em conjunto com a cláusula `GROUP BY` para calcular valores em grupos específicos.

### Exemplo

Para calcular a média de idade dos clientes por cidade:

```sql
SELECT cidade, AVG(idade) AS media_idade
FROM clientes
GROUP BY cidade;
```

## Considerações Finais

- As funções agregadas são essenciais para realizar cálculos em conjuntos de dados.
- Elas permitem obter informações resumidas sobre os dados, como contagem, soma, média, máximo e mínimo.
- As funções agregadas são frequentemente usadas em conjunto com a cláusula `GROUP BY` para calcular valores em grupos específicos.
- É importante entender o propósito e a sintaxe de cada função agregada para utilizá-las corretamente em consultas SQL.