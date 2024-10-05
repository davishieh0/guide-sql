# MySQL Comandos Essenciais

### Consulta SQL

```sql
SELECT * FROM avaliacoes;
/*Operadores*/
WHERE  nota>=4;
WHERE  nota=4;
WHERE  nota<>4; /* Simbolo de diferente != */
WHERE nome_aluno >'C'; /*Letras de c para frente */

WHERE país_de_origem = 'China';
WHERE Idade > 30 AND Sexo <> 'Masculino';
WHERE NOT status = 'reprovado';
WHERE Nome LIKE 'computador';
WHERE data_de_envio BETWEEN '2023-08-01' AND '2023-09-01';

SELECT DISTINCT cliente FROM tabelapedidos
/* Traz dados distintos*/

```

### Consulta SQL em ordem

```sql
SELECT * FROM avaliacoes;

WHERE preco_de_compra BETWEEN 200 AND 600 ORDER BY nome_produto;
Mostrando os preços entre 200 e 600 em nome do produto alfabeticamente

WHERE preco_de_compra BETWEEN 200 AND 600 ORDER BY nome_produto DESC;
/* Comando DESC inverte a ordem do filtro*/
```

### Adicionando linhas INSERT

```sql
INSERT INTO tabelaclientes
(id_cliente,
 nome_cliente,
 informacoes_de_contato,
 endereco_cliente)
 VALUES
 ('1','Ana Silva','ana.silva@gmail.com','rua flores -casa 1);
```

### Alterando tabelas

```sql
ALTER table tabelafornecedores ADD endereco_cliente VARCHAR(250);
/* Cria  nova coluna*/

DROP TABLE tabela_clientes;
Apaga tudo
```

### Alterando dados

```sql
UPDATE tabelapedidos SET status = 'enviado' WHERE status = 'Processando'
UPDATE 
```

### Excluindo dados

```sql
DELETE FROM tabelafornecedores WHERE país_de_origem = 'Turquia';
```