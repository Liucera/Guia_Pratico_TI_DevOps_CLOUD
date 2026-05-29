## 14 PostgreSQL

1. `psql`: cliente de linha de comando do PostgreSQL, usado para conectar ao servidor, executar consultas e meta-comandos.
2. `psql -U usuario -d banco`: conecta ao banco especificado com o usuário indicado, abrindo prompt interativo. [][web:151]
3. `psql -f script.sql -U usuario`: executa um arquivo de script SQL inteiro no servidor, automatizando criação de estruturas.
4. `\?`: exibe ajuda de meta-comandos disponíveis dentro do `psql`, como atalhos para listar bancos, tabelas e usuários.
5. `\l` ou `\list`: lista todos os bancos de dados disponíveis no servidor PostgreSQL.
6. `\c nome_banco`: troca a conexão atual para outro banco de dados, mantendo o mesmo usuário.
7. `\dt`: mostra as tabelas do esquema atual, listando nome, tipo e proprietário.
8. `\d tabela`: exibe detalhes da estrutura de uma tabela, incluindo colunas, tipos, chaves e índices.
9. `\du`: lista os papéis (roles) e usuários cadastrados, com informações de privilégios.
10. `\q`: sai do `psql`, encerrando a sessão com o servidor.

11. `createdb nome_banco`: utilitário de shell que cria um novo banco de dados vazio no servidor PostgreSQL.
12. `dropdb nome_banco`: remove completamente um banco de dados existente, apagando objetos e dados.
13. `CREATE DATABASE nome_banco;`: comando SQL equivalente para criar banco dentro de uma sessão `psql`.
14. `DROP DATABASE nome_banco;`: remove o banco através de comando SQL, exigindo que não haja conexões ativas.
15. `ALTER DATABASE nome_banco RENAME TO novo_nome;`: renomeia um banco de dados, ajustando seu identificador.
16. `ALTER DATABASE nome_banco OWNER TO novo_dono;`: muda o proprietário do banco para outro usuário ou role.
17. `CREATE SCHEMA nome;`: cria um novo esquema dentro do banco, agrupando tabelas e objetos relacionados.
18. `SET search_path TO esquema;`: define o esquema padrão de busca, simplificando o uso de nomes de tabelas.
19. `SHOW search_path;`: exibe a ordem de esquemas que serão consultados ao buscar objetos sem qualificação.
20. `DROP SCHEMA nome CASCADE;`: remove um esquema e todos os objetos contidos nele, como tabelas e views.

21. `CREATE TABLE tabela (...);`: cria uma tabela com colunas, tipos de dados e restrições definidos.
22. `SERIAL`: tipo especial que cria coluna inteira auto incrementada, geralmente usada para chaves primárias.
23. `BIGSERIAL`: variante de maior capacidade para valores muito grandes de chave.
24. `BOOLEAN`: tipo lógico nativo do PostgreSQL para armazenar verdadeiro, falso ou nulo.
25. `TEXT`: tipo de dado para textos longos sem tamanho máximo predeterminado.
26. `PRIMARY KEY(coluna)`: define a chave primária de uma tabela, garantindo unicidade e indexação.
27. `UNIQUE(coluna)`: assegura que não existam valores repetidos na coluna ou combinação de colunas.
28. `CHECK (condicao)`: cria regra de validação na tabela para garantir que valores inseridos obedeçam a um critério.
29. `FOREIGN KEY (coluna) REFERENCES outra_tabela(coluna)`: implementa integridade referencial entre duas tabelas.
30. `DROP TABLE tabela;`: exclui a tabela e seus dados do banco de dados.

31. `INSERT INTO tabela (colunas) VALUES (valores);`: insere uma nova linha com os valores definidos para as colunas selecionadas.
32. `SELECT * FROM tabela;`: consulta todas as colunas e linhas da tabela, sendo a forma mais simples de leitura.
33. `SELECT colunas FROM tabela WHERE condição;`: retorna apenas determinadas colunas e linhas que atendam à condição especificada.
34. `UPDATE tabela SET coluna=valor WHERE condição;`: altera valores de linhas existentes com base em filtro definido.
35. `DELETE FROM tabela WHERE condição;`: remove registros específicos da tabela, respeitando a condição.
36. `SELECT coluna, COUNT(*) FROM tabela GROUP BY coluna;`: agrupa dados por coluna e conta o número de registros em cada grupo.
37. `HAVING condição`: aplica filtros após o agrupamento, restringindo quais grupos aparecerão no resultado.
38. `ORDER BY coluna ASC|DESC`: ordena os resultados de uma consulta em ordem crescente ou decrescente.
39. `LIMIT n OFFSET m`: pagina resultados, retornando n linhas a partir da posição m.
40. `JOIN`: palavra-chave que combina linhas de duas tabelas baseadas em uma condição de relacionamento.

41. `CREATE ROLE usuario WITH LOGIN PASSWORD 'senha';`: cria um novo papel com permissão de login, funcionando como usuário.
42. `ALTER ROLE usuario WITH SUPERUSER;`: concede privilégios de superusuário ao papel, permitindo administração completa.
43. `GRANT privilégio ON tabela TO usuario;`: dá permissões como SELECT, INSERT ou ALL em objetos específicos.
44. `REVOKE privilégio ON tabela FROM usuario;`: remove permissões anteriormente concedidas.
45. `\password usuario`: comando do `psql` para alterar a senha de um usuário interativamente.`\dn`: lista esquemas existentes no banco de dados atual.
46. `\df`: mostra funções definidas no banco, incluindo funções SQL e de linguagem procedural.
47. `\dv`: lista views disponíveis, que são consultas salvas reutilizáveis.
48. `EXPLAIN SELECT ...;`: exibe plano de execução de uma consulta, permitindo analisar desempenho e uso de índices.
49. `ANALYZE`: atualiza estatísticas usadas pelo otimizador de consultas, melhorando escolhas de planos de execução.
