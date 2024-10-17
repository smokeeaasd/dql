# SELECT: Buscando Dados

O comando `SELECT` em SQL é utilizado para buscar dados de uma ou mais tabelas em um banco de dados. Ele é um dos comandos mais usados na **Data Query Language (DQL)**, permitindo a recuperação de dados de forma estruturada.

## Sintaxe Básica

```sql
SELECT coluna1, coluna2, ... FROM nome_da_tabela;
```

- `coluna1`, `coluna2`, ...: Especifica as colunas que você deseja buscar.
- `nome_da_tabela`: O nome da tabela de onde os dados serão extraídos.

## Exemplo Simples

Vamos supor que temos uma tabela chamada `clientes` com as seguintes colunas: `id`, `nome`, `idade`, `cidade`.

Para buscar todas as colunas:

```sql
SELECT * FROM clientes;
```

Para buscar apenas os nomes e idades dos clientes:

```sql
SELECT nome, idade FROM clientes;
```

## Alias para Colunas

Você pode usar aliases para renomear as colunas retornadas na consulta:

```sql
SELECT nome AS 'Nome do Cliente', idade AS 'Idade do Cliente' FROM clientes;
```

Neste exemplo, as colunas `nome` e `idade` serão renomeadas para `Nome do Cliente` e `Idade do Cliente`, respectivamente.

## Considerações Finais

- O comando `SELECT` é essencial para recuperar dados de um banco de dados.
- Você pode buscar todas as colunas de uma tabela ou apenas as colunas desejadas.
- Aliases podem ser usados para renomear as colunas retornadas na consulta.
- O comando `SELECT` é frequentemente usado em conjunto com outros comandos SQL para realizar consultas mais complexas.