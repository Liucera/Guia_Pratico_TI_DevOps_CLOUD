## 15 Salesforce

1. `Salesforce`: plataforma de CRM em nuvem usada para gerenciar vendas, atendimento, marketing e aplicativos personalizados com dados centralizados.
2. `Objeto padrão`: estrutura de dados fornecida pela plataforma, como Account, Contact, Opportunity e Case, já preparada para uso em negócios.
3. `Objeto personalizado`: objeto criado pelo administrador ou desenvolvedor para representar entidades específicas do negócio, como Projeto ou Contrato.
4. `Campo personalizado`: atributo adicional criado em objetos para armazenar informações específicas além dos campos padrão.
5. `Registro`: instância concreta de um objeto, semelhante a uma linha de tabela em banco de dados relacional.
6. `Relacionamento master-detail`: vínculo forte entre dois objetos, em que o detail depende do master para existir e herda configurações.
7. `Relacionamento lookup`: relacionamento mais flexível entre objetos, permitindo associação sem dependência rígida de vida útil.
8. `Layout de página`: configuração que define quais campos, seções e componentes aparecem na tela de um registro.
9. `Registro de configuração (Custom Setting/Custom Metadata)`: estrutura usada para armazenar parâmetros que controlam comportamento de automações.
10. `Trigger`: gatilho de Apex que executa lógica antes ou depois de operações de banco, como insert, update e delete.

11. `SOQL`: Salesforce Object Query Language, linguagem de consulta usada para buscar dados em objetos da plataforma.
12. `SELECT campos FROM Objeto`: sintaxe básica de consulta SOQL, retornando campos de registros daquele objeto.
13. `SELECT Name FROM Account`: exemplo de consulta que traz o nome de todas as contas cadastradas.
14. `WHERE condição`: cláusula que filtra registros que atendam a critérios específicos, como status ou data.
15. `ORDER BY campo ASC|DESC`: ordena resultados de uma consulta SOQL por um campo em ordem crescente ou decrescente.
16. `LIMIT n`: restringe o número de registros retornados pela consulta, evitando trazer mais dados que o necessário.
17. `SELECT Name FROM Contact WHERE AccountId = 'id'`: exemplo de consulta filtrando contatos por conta relacionada.
18. `SELECT Name, (SELECT Name FROM Contacts) FROM Account`: consulta com subselect de relacionamento filho, retornando contas com seus contatos.
19. `SELECT Account.Name, Name FROM Contact`: exemplo de uso de relacionamento pai em SOQL, acessando campo do objeto Account a partir de Contact.
20. `COUNT()`: função agregada em SOQL que retorna a quantidade de registros que atendem ao filtro.

21. `SUM(campo)`, `AVG(campo)`, `MIN(campo)`, `MAX(campo)`: funções agregadas em SOQL usadas para somar, calcular média e obter mínimo ou máximo de valores numéricos.
22. `GROUP BY campo`: agrupa resultados ao usar funções agregadas, produzindo totais por valor do campo agrupador.
23. `HAVING condição`: filtra grupos após agregação, por exemplo mantendo apenas somas acima de certo valor.
24. `Bind variables`: uso de variáveis Apex dentro da cláusula WHERE, permitindo consultas dinâmicas com parâmetros seguros.
25. `List<Objeto> lista = [SELECT ... FROM Objeto];`: sintaxe em Apex que executa uma consulta SOQL e armazena resultado em lista tipada.
26. `FOR registro : [SELECT ... FROM Objeto]`: laço for que itera diretamente sobre resultados de uma consulta SOQL no Apex.
27. `Developer Console Query Editor`: ferramenta da plataforma para executar SOQL e SOSL, visualizar resultados e testar consultas.
28. `SOSL`: Salesforce Object Search Language, linguagem de pesquisa para procurar texto em múltiplos objetos de uma vez.
29. `SELECT Id FROM User WHERE IsActive = true`: consulta comum para recuperar usuários ativos na organização.
30. `LIMIT 1`: combinação frequente para buscar apenas um registro específico quando se espera resultado único.

31. `Apex`: linguagem de programação fortemente tipada da Salesforce, similar a Java, usada para lógica de negócio no servidor. [][web:162]
32. `public class NomeClasse { }`: forma básica de declarar uma classe Apex, onde são colocados métodos e atributos. [][web:162]
33. `public static void metodo() { }`: define um método estático chamável sem instanciar a classe, muito usado em utilitários.
34. `List<Tipo> lista = new List<Tipo>();`: cria uma lista em Apex para armazenar coleções de registros ou valores.
35. `insert registros;`: comando Apex que insere uma lista de registros no banco de dados da plataforma.
36. `update registros;`: atualiza registros já existentes com novos valores de campos.
37. `delete registros;`: remove registros da base de dados, respeitando regras de integridade definidas.
38. `Database.saveResult`: estrutura que retorna resultado detalhado de operações DML feitas via Database, incluindo erros.
39. `System.debug(valor);`: comando de log usado para registrar informações de depuração no log de execução Apex.
40. `Test.startTest()` / `Test.stopTest()`: métodos usados em classes de teste para isolar trechos de código e medir limites de recursos.

41. `Salesforce CLI`: ferramenta de linha de comando que gerencia orgs, código-fonte e automação de tarefas de desenvolvimento.[web:163]
42. `sf update`: comando que atualiza a Salesforce CLI para a versão mais recente disponível.
43. `sf org login web`: abre o navegador para login em uma organização Salesforce e autoriza a CLI a acessar essa org.
44. `sf org list --all`: lista todas as organizações nas quais a CLI tem sessão gravada, incluindo orgs temporárias.
45. `sf org create scratch`: cria uma org temporária (scratch org) para desenvolvimento isolado com configuração definida em projeto.
46. `sf org delete scratch`: remove uma scratch org quando não é mais necessária, liberando limites de criação.
47. `sf project deploy start`: envia metadados e código do projeto local para a org selecionada, efetivando implantação.
48. `sf project retrieve start`: traz metadados da org para o projeto local, sincronizando código-fonte com o que está em produção ou sandbox.
49. `sf apex run`: executa blocos de código Apex anônimo a partir do terminal, útil para testes rápidos e scripts de manutenção.
50. `sf apex test run`: roda classes e métodos de teste Apex via CLI, gerando relatórios de cobertura e resultados.
