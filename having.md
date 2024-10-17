# HAVING: Filtrando Grupos em SQL

A cláusula `HAVING` é usada em consultas SQL para filtrar grupos de resultados criados pela cláusula `GROUP BY`. Enquanto a cláusula `WHERE` filtra linhas individuais antes da agregação, `HAVING` filtra os resultados após a aplicação das funções agregadas.

## Sintaxe Básica

A sintaxe básica para a cláusula `HAVING` é a seguinte:

```sql
SELECT coluna1, função_agregada(coluna2)
FROM tabela
GROUP BY coluna1
HAVING condição;
```

## Exemplos

### 1. Filtrando Grupos com HAVING

Para mostrar apenas cidades que têm mais de 10 clientes:

```sql
SELECT cidade, COUNT(*) AS total_clientes
FROM clientes
GROUP BY cidade
HAVING COUNT(*) > 10;
```

### 2. Usando HAVING com Múltiplas Condições

Você pode usar múltiplas condições na cláusula `HAVING`. Por exemplo, para mostrar cidades com mais de 10 clientes e uma média de idade acima de 30:

```sql
SELECT cidade, COUNT(*) AS total_clientes, AVG(idade) AS media_idade
FROM clientes
GROUP BY cidade
HAVING COUNT(*) > 10 AND AVG(idade) > 30;
```

### 3. Comparando Resultados de Funções Agregadas

Para filtrar grupos com base em resultados de funções agregadas, como encontrar estados onde a soma das idades dos clientes é superior a 100:

```sql
SELECT estado, SUM(idade) AS soma_idade
FROM clientes
GROUP BY estado
HAVING SUM(idade) > 100;
```

## Considerações Finais

- A cláusula `HAVING` sempre deve ser usada após a cláusula `GROUP BY`.
- É comum usar `HAVING` em consultas que incluem funções agregadas, pois permite filtrar os resultados com base em condições aplicáveis aos dados agregados.