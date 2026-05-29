## 13 MySQL

1. `mysql -u usuario -p`: comando de terminal que abre o cliente MySQL para conexão com o servidor, solicitando a senha do usuário.
2. `SHOW DATABASES;`: lista todos os bancos de dados disponíveis no servidor, permitindo ver o que já está criado.
3. `CREATE DATABASE nome;`: cria um novo banco de dados vazio com o nome especificado, ponto de partida para tabelas e dados.
4. `DROP DATABASE nome;`: remove um banco de dados e todo o seu conteúdo definitivamente, devendo ser usado com extremo cuidado.
5. `USE nome;`: seleciona o banco de dados que será usado nas operações seguintes da sessão.
6. `SHOW TABLES;`: exibe a lista de tabelas existentes no banco de dados atualmente selecionado.
7. `DESCRIBE tabela;`: mostra estrutura de uma tabela, listando colunas, tipos de dados, se aceitam nulos e chaves.
8. `SHOW COLUMNS FROM tabela;`: alternativa para consultar o esquema de colunas de uma tabela específica.
9. `SHOW CREATE TABLE tabela;`: retorna o comando SQL completo usado para criar a tabela, útil para clonagem ou documentação.
10. `SHOW STATUS;`: exibe estatísticas de funcionamento do servidor MySQL, como conexões e consultas executadas.

11. `CREATE TABLE tabela (...);`: cria uma nova tabela, definindo colunas, tipos de dados e restrições básicas.
12. `INT`: tipo de dado numérico inteiro, geralmente usado para identificadores e contadores.
13. `VARCHAR(n)`: tipo de texto de tamanho variável, permitindo armazenar cadeias de caracteres até o limite definido.
14. `DECIMAL(p,s)`: tipo numérico exato com precisão e escala, adequado para valores monetários e cálculos financeiros.
15. `DATE`, `DATETIME` e `TIMESTAMP`: tipos de dados usados para armazenar datas e horários em diferentes granularidades.
16. `PRIMARY KEY`: restrição que define a chave primária da tabela, garantindo unicidade e indexação do identificador.
17. `AUTO_INCREMENT`: atributo que faz um campo numérico ser incrementado automaticamente a cada nova linha inserida.
18. `NOT NULL`: restrição que impede que a coluna receba valores nulos, exigindo preenchimento em cada registro.
19. `DEFAULT valor`: define um valor padrão para a coluna quando a inserção não informar explicitamente um valor.
20. `FOREIGN KEY`: restrição que cria relacionamento entre tabelas, ligando uma coluna a chave primária de outra.

21. `INSERT INTO tabela (colunas) VALUES (valores);`: adiciona um novo registro à tabela, preenchendo as colunas especificadas.
22. `INSERT INTO tabela VALUES (...);`: insere valores em todas as colunas na ordem em que foram definidas, exigindo alinhamento exato.
23. `INSERT INTO tabela (colunas) VALUES (...), (...);`: insere múltiplas linhas em um único comando, melhorando desempenho.
24. `SELECT * FROM tabela;`: retorna todas as colunas e linhas da tabela, usado como consulta básica de visualização.
25. `SELECT coluna1, coluna2 FROM tabela;`: busca apenas colunas específicas, reduzindo dados retornados e otimizando consultas.
26. `WHERE condição`: cláusula que filtra as linhas retornadas ou afetadas por comandos como SELECT, UPDATE e DELETE.
27. `AND`, `OR`, `NOT`: operadores lógicos usados em conjunto com WHERE para combinar múltiplas condições de filtro.
28. `ORDER BY coluna ASC|DESC;`: ordena os resultados de uma consulta pelas colunas escolhidas em ordem crescente ou decrescente. `LIMIT n`: restringe a quantidade de linhas retornadas por um SELECT, útil para paginação e testes.
29. `DISTINCT coluna`: elimina duplicatas na coluna selecionada, retornando apenas valores únicos.

30. `UPDATE tabela SET coluna=valor WHERE condição;`: modifica valores de uma ou mais colunas em linhas que satisfaçam a condição dada.
31. `UPDATE tabela SET coluna=coluna+1;`: exemplo de atualização baseada no valor atual, comum para contadores ou estatísticas.
32. `DELETE FROM tabela WHERE condição;`: remove registros específicos com base em critério definido na cláusula WHERE.
33. `DELETE FROM tabela;`: exclui todas as linhas da tabela, mantendo a estrutura, sendo equivalente a truncar dados.
34. `TRUNCATE TABLE tabela;`: apaga rapidamente todos os registros e reseta auto incrementos, preservando a definição da tabela.
35. `DROP TABLE tabela;`: remove completamente a tabela e seus dados do banco, operação destrutiva.
36. `ALTER TABLE tabela ADD coluna tipo;`: adiciona nova coluna à tabela existente, expandindo o esquema.
37. `ALTER TABLE tabela MODIFY coluna tipo;`: altera tipo ou atributos de uma coluna, como tamanho de texto ou possibilidade de nulos.
38. `ALTER TABLE tabela DROP COLUMN coluna;`: remove uma coluna da tabela, excluindo permanentemente seus dados.
39. `RENAME TABLE antiga TO nova;`: muda o nome de uma tabela, mantendo conteúdo e relacionamentos.

40. `CREATE INDEX idx_nome ON tabela(coluna);`: cria índice para acelerar consultas que filtram ou ordenam pela coluna especificada.
41. `CREATE UNIQUE INDEX idx_nome ON tabela(coluna);`: cria índice que garante unicidade dos valores, evitando duplicações.
42. `EXPLAIN SELECT ...;`: mostra plano de execução de uma consulta, ajudando a identificar gargalos e uso de índices.
43. `SHOW PROCESSLIST;`: lista conexões e consultas atualmente em execução no servidor, útil para diagnóstico de travamentos.
44. `CREATE USER 'usuario'@'host' IDENTIFIED BY 'senha';`: cria um novo usuário do MySQL com senha definida.
45. `GRANT PRIVILEGES ON banco.tabela TO 'usuario'@'host';`: concede permissões ao usuário, como SELECT, INSERT ou ALL PRIVILEGES.
46. `REVOKE PRIVILEGES ON banco.tabela FROM 'usuario'@'host';`: retira permissões anteriormente concedidas.
47. `FLUSH PRIVILEGES;`: recarrega as tabelas de privilégios, aplicando alterações em usuários e permissões.
48. `SHOW GRANTS FOR 'usuario'@'host';`: exibe as permissões atuais de um usuário específico no servidor.
49. `EXIT;` ou `QUIT;`: encerra a sessão no cliente MySQL, retornando ao shell do sistema operacional.
