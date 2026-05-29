## 2 Python

1. `python`: comando de terminal que inicia o interpretador interativo, permitindo executar instruções Python linha a linha para testes rápidos.
2. `python arquivo.py`: executa um script salvo em arquivo, rodando o código do início ao fim em modo não interativo.
3. `python -m módulo`: executa um módulo como script, útil para rodar pacotes ou ferramentas internas como `python -m http.server`.
4. `python --version`: exibe a versão instalada do interpretador, ajudando a confirmar compatibilidade de código.
5. `pip install pacote`: instala um pacote Python do repositório PyPI, adicionando bibliotecas externas ao ambiente de desenvolvimento.
6. `pip list`: mostra os pacotes instalados no ambiente atual, permitindo auditar dependências do projeto.
7. `pip uninstall pacote`: remove um pacote previamente instalado, limpando dependências não utilizadas.
8. `pip freeze`: gera uma lista de pacotes e versões instaladas, normalmente usada para criar arquivos `requirements.txt`.
9. `pip install -r requirements.txt`: instala todos os pacotes listados em um arquivo de requisitos, reproduzindo o ambiente de outro desenvolvedor.
10. `venv`: módulo que cria ambientes virtuais isolados, permitindo separar dependências de projetos diferentes.
11. `print(valor)`: envia informações para o console, servindo como comando básico de saída e depuração.
12. `input(mensagem)`: lê uma entrada do usuário como texto, exibindo uma mensagem opcional antes da leitura.
13. `type(objeto)`: retorna o tipo do objeto informado, ajudando a inspecionar valores em tempo de execução.
14. `int(texto)`: converte um valor para inteiro, quando possível, permitindo transformar entradas de texto em números.
15. `float(texto)`: converte um valor em número de ponto flutuante, útil para cálculos com casas decimais.
16. `str(valor)`: converte um valor para string, facilitando a concatenação e exibição de dados.
17. `len(sequencia)`: retorna o tamanho de listas, strings ou outras coleções, sendo muito usado em laços e validações.
18. `range(inicio, fim, passo)`: gera uma sequência numérica, normalmente utilizada em laços `for` para controlar o número de iterações.
19. `help(objeto)`: abre a documentação interativa de um módulo, função ou tipo, ajudando a consultar rapidamente parâmetros e uso.
20. `dir(objeto)`: lista atributos e métodos disponíveis em um objeto, útil para descoberta de funcionalidades em bibliotecas.
21. `if condição:`: cria um bloco condicional que executa comandos apenas se a expressão booleana for verdadeira, controlando fluxos de decisão.
22. `elif condição:`: adiciona uma nova condição a uma estrutura `if`, permitindo múltiplos caminhos de execução exclusivos.
23. `else:`: define o bloco executado quando nenhuma das condições anteriores é satisfeita, cobrindo o caso padrão.
24. `for variável in iterável:`: percorre sequências como listas, strings ou ranges, executando um bloco de código para cada elemento.
25. `while condição:`: repete um bloco de comandos enquanto a condição for verdadeira, ideal para laços de iteração indefinida.
26. `break`: interrompe imediatamente o laço `for` ou `while` mais interno, saindo do ciclo atual.
27. `continue`: pula o restante do bloco no laço atual e segue para a próxima iteração, mantendo o laço ativo.
28. `pass`: atua como comando vazio, reservado para lugares onde a sintaxe exige um bloco, mas ainda não há implementação.
29. `try:`: inicia um bloco de tratamento de exceções, tentando executar código que pode gerar erros.
30. `except Erro:`: captura uma exceção específica e executa um bloco de tratamento, evitando a interrupção abrupta do programa.
31. `def nome_função(parâmetros):`: declara uma função, encapsulando um conjunto reutilizável de comandos com parâmetros opcionais.
32. `return valor`: encerra a execução de uma função e devolve um resultado para quem a chamou.
33. `lambda parâmetros: expressão`: cria funções anônimas pequenas, normalmente usadas em operações de alta ordem como `map` e `filter`.
34. `import módulo`: torna um módulo externo disponível no código, permitindo usar suas funções e classes.
35. `from módulo import nome`: importa apenas símbolos específicos de um módulo, evitando prefixos longos em chamadas.
36. `as apelido`: define um alias para módulo ou função importada, simplificando o nome usado no código.
37. `class NomeClasse:`: cria uma nova classe, definindo estrutura de dados e comportamentos orientados a objeto.
38. `__init__(self, ...)`: método construtor chamado ao criar uma instância, inicializando atributos da classe.
39. `self`: referência à própria instância dentro de métodos de classe, usada para acessar atributos e outros métodos.
40. `super()`: acessa a implementação da classe pai, permitindo reutilizar ou estender comportamentos herdados.
41. `lista = [elementos]`: cria uma lista mutável, adequada para coleções ordenadas de itens que podem mudar de tamanho.
42. `tupla = (elementos)`: cria uma tupla imutável, ideal para grupos de valores que não devem ser alterados.
43. `conjunto = {elementos}`: define um conjunto, coleção sem ordem e sem itens duplicados, útil para operações de pertença e diferença.
44. `dicionario = {"chave": valor}`: cria um dicionário, estrutura de pares chave–valor para acesso rápido por chave.
45. `lista.append(item)`: adiciona um elemento ao final da lista, expandindo a coleção.
46. `lista.remove(item)`: remove a primeira ocorrência do item na lista, lançando erro se não existir.
47. `lista.sort()`: ordena os elementos da lista in-place em ordem crescente padrão, quando possível.
48. `dicionario.get(chave, padrão)`: obtém o valor de uma chave, retornando um padrão se a chave não existir, evitando erro.
49. `with open(caminho, modo) as arquivo:`: abre um arquivo garantindo fechamento automático ao final do bloco, evitando vazamentos de recursos.
50. `raise Erro("mensagem")`: dispara explicitamente uma exceção, permitindo sinalizar condições de erro nas regras de negócio.
