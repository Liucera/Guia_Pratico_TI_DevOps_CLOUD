## 1 HTML

1. `<html>`: delimita o documento HTML inteiro e indica ao navegador que o conteúdo será interpretado como página web, servindo como elemento raiz da árvore de elementos.
2. `<!DOCTYPE html>`: informa ao navegador que o documento segue o padrão HTML5, ajudando a evitar diferenças de renderização entre navegadores.
3. `<head>`: agrupa metadados da página, como título, folhas de estilo, scripts e informações usadas por navegadores e buscadores, e não aparece diretamente para o usuário.
4. `<body>`: contém todo o conteúdo visível da página para o usuário, como textos, imagens, links e formulários, sendo a área principal renderizada pelo navegador.
5. `<title>`: define o título exibido na aba do navegador e usado por motores de busca, ajudando na identificação da página.
6. `<meta>`: armazena metadados como charset, descrição, autor e configurações de viewport, apoiando SEO e comportamento responsivo.
7. `<link>`: referencia recursos externos como arquivos de estilo CSS ou ícones, permitindo modularizar e reutilizar configurações visuais.
8. `<style>`: permite incluir regras CSS diretamente dentro do documento HTML, aplicando estilos sem depender de arquivo externo.
9. `<script>`: embute ou referencia código JavaScript que adiciona interatividade, lógica de negócios e integração com APIs na página.
10. `<!-- comentário -->`: insere comentários no código HTML que são ignorados pelo navegador, servindo para documentação e notas internas. [web:15]

11. `<h1>`: representa o título principal da página ou seção, com maior peso semântico e de hierarquia para acessibilidade e SEO.
12. `<h2>`: indica subtítulos de nível imediatamente abaixo do `<h1>`, estruturando o conteúdo em seções organizadas.
13. `<h3>`: marca subtítulos de terceiro nível, aprofundando a hierarquia de tópicos dentro de uma seção.
14. `<h4>`: define um título de quarto nível, refinando ainda mais a divisão do conteúdo.
15. `<h5>`: representa títulos menos importantes na hierarquia, geralmente usados para subdivisões específicas.
16. `<h6>`: define o nível mais baixo de cabeçalho, útil para detalhes bem específicos dentro da estrutura de seções.

17. `<p>`: delimita parágrafos de texto, organizando blocos de conteúdo corrido de forma semântica.
18. `<br>`: insere uma quebra de linha simples dentro de um parágrafo ou outro conteúdo, sem iniciar um novo parágrafo.
19. `<hr>`: desenha uma linha horizontal que representa uma separação temática entre seções de conteúdo.
20. `<span>`: agrupa pequenas partes de texto ou elementos inline para aplicar estilos ou atributos específicos sem quebrar o fluxo do parágrafo. `<div>`: cria um contêiner genérico em bloco para agrupar outros elementos, facilitando layout, estilização e organização lógica do conteúdo.
22. `<strong>`: indica que o texto tem importância forte, geralmente exibido em negrito e interpretado semanticamente por leitores de tela.
23. `<em>`: marca texto com ênfase, normalmente renderizado em itálico, com significado semântico para acessibilidade.
24. `<b>`: aplica destaque visual em negrito sem acrescentar significado semântico, sendo mais voltado à formatação.
25. `<i>`: exibe texto em itálico com foco em estilo, muitas vezes usado para termos técnicos ou estrangeiros.
26. `<u>`: sublinha o texto, devendo ser usado com cuidado para não confundir com links clicáveis.

27. `<a>`: cria links para outras páginas, seções internas ou recursos externos, usando o atributo `href` para definir o destino.
28. `<img>`: insere imagens no documento, exigindo pelo menos o atributo `src` com o caminho da imagem e `alt` para texto alternativo acessível.
29. `<figure>`: agrupa conteúdo ilustrativo como imagens ou gráficos juntamente com sua legenda, dando um bloco semântico próprio.
30. `<figcaption>`: define a legenda descritiva associada a uma `<figure>`, explicando o conteúdo visual para o usuário.
31. `<video>`: embute vídeos na página, com controles de reprodução e atributos para definir fonte, tamanho e comportamento.
32. `<audio>`: incorpora conteúdo de áudio como músicas ou podcasts com controles de reprodução.
33. `<source>`: especifica arquivos de mídia alternativos para `<audio>` ou `<video>`, permitindo oferecer diferentes formatos compatíveis.
34. `<track>`: adiciona faixas de legenda ou descrição para mídias, melhorando a acessibilidade de vídeos e áudios.
35. `<embed>`: insere conteúdo interativo ou plugins externos, como animações ou documentos incorporados.
36. `<object>`: incorpora objetos externos como arquivos PDF ou aplicações, permitindo conteúdo enriquecido dentro da página.

37. `<ul>`: cria listas não ordenadas, em que os itens aparecem com marcadores, usada para coleções sem prioridade numérica.
38. `<ol>`: constrói listas ordenadas, numerando automaticamente os itens para representar sequências ou rankings.
39. `<li>`: representa cada item dentro de listas `<ul>` ou `<ol>`, contendo texto ou outros elementos.
40. `<dl>`: define uma lista de definição, usada para termos e suas descrições, útil em glossários e dicionários.
41. `<dt>`: indica o termo a ser definido dentro de uma lista de definição, destacando o nome do conceito.
42. `<dd>`: descreve o termo correspondente em um `<dt>`, armazenando a definição ou explicação.

43. `<table>`: cria tabelas de dados estruturados, organizadas em linhas e colunas.
44. `<thead>`: agrupa o cabeçalho da tabela, contendo as colunas descritivas principais.
45. `<tbody>`: reúne o corpo da tabela, onde ficam os dados principais separados do cabeçalho e rodapé.
46. `<tfoot>`: define o rodapé da tabela, geralmente com totais, resumos ou observações.
47. `<tr>`: representa uma linha da tabela, agrupando células de dados ou cabeçalhos em uma linha horizontal.
48. `<th>`: cria células de cabeçalho em uma tabela, com significado semântico e, em geral, texto em negrito centralizado.
49. `<td>`: define células de dados dentro de uma linha de tabela, armazenando os valores ou textos exibidos.
50. `<nav>`: identifica uma área de navegação com links importantes do site, como menus ou barras de navegação principal.
