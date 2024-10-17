# Operadores de Comparação e Lógicos

Os operadores de comparação e lógicos são fundamentais para a construção de condições em SQL, permitindo filtrar e manipular dados de forma eficaz. Abaixo, estão os principais operadores utilizados nas consultas SQL.

## Operadores de Comparação

Os operadores de comparação permitem comparar valores em uma consulta SQL.

### 1. Igual a (=)
Compara se dois valores são iguais.

```sql
SELECT * FROM clientes WHERE idade = 30;
```

### 2. Diferente de (<>)
Compara se dois valores são diferentes.

```sql
SELECT * FROM clientes WHERE idade <> 30;
```

### 3. Maior que (>)
Verifica se um valor é maior que outro.

```sql
SELECT * FROM clientes WHERE idade > 30;
```

### 4. Menor que (<)
Verifica se um valor é menor que outro.

```sql
SELECT * FROM clientes WHERE idade < 30;
```

### 5. Maior ou igual a (>=)
Verifica se um valor é maior ou igual a outro.

```sql
SELECT * FROM clientes WHERE idade >= 30;
```

### 6. Menor ou igual a (<=)
Verifica se um valor é menor ou igual a outro.

```sql
SELECT * FROM clientes WHERE idade <= 30;
```

## Operadores Lógicos

Os operadores lógicos permitem combinar várias condições em uma consulta SQL.

### 1. AND
Retorna verdadeiro se ambas as condições forem verdadeiras.

```sql
SELECT * FROM clientes WHERE cidade = 'São Paulo' AND idade > 25;
```

### 2. OR
Retorna verdadeiro se pelo menos uma das condições for verdadeira.

```sql
SELECT * FROM clientes WHERE cidade = 'São Paulo' OR cidade = 'Rio de Janeiro';
```

### 3. NOT
Inverte o resultado da condição, retornando verdadeiro se a condição for falsa.

```sql
SELECT * FROM clientes WHERE NOT cidade = 'São Paulo';
```

## Exemplos Combinando Operadores

Você pode combinar operadores de comparação e lógicos para criar condições complexas.

```sql
SELECT * FROM clientes WHERE (cidade = 'São Paulo' OR cidade = 'Rio de Janeiro') AND idade >= 30;
```

Esse comando retornará clientes que moram em São Paulo ou no Rio de Janeiro e têm 30 anos ou mais.

## Considerações Finais

- Os operadores de comparação e lógicos são essenciais para a construção de condições em consultas SQL.
- Eles permitem filtrar dados com base em critérios específicos, tornando as consultas mais poderosas e flexíveis.
- Ao combinar diferentes operadores, você pode criar condições complexas para atender às necessidades de sua consulta.
- Pratique a utilização desses operadores em consultas SQL para aprimorar suas habilidades de manipulação de dados.