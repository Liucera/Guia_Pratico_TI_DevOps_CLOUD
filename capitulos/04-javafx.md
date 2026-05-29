## 4 JavaFX

1. `extends Application`: faz a classe herdar de `javafx.application.Application`, habilitando o ciclo de vida padrão de uma aplicação JavaFX.
2. `launch(args);`: método estático que inicializa o toolkit JavaFX, cria o ambiente gráfico e dispara a chamada do método `start`.
3. `start(Stage primaryStage)`: método chamado após o `launch`, onde a janela principal é configurada e exibida ao usuário.
4. `Stage`: representa uma janela de nível superior, como a janela principal da aplicação ou diálogos adicionais.
5. `primaryStage.setTitle("Título");`: define o texto exibido na barra de título da janela, facilitando a identificação da tela.
6. `Scene`: container que agrupa todos os nós visuais, sendo a cena que é aplicada a um `Stage` para exibição.
7. `Scene scene = new Scene(root, largura, altura);`: cria uma nova cena a partir de um nó raiz e dimensões, preparando o conteúdo para ser exibido.
8. `primaryStage.setScene(scene);`: associa a cena à janela, fazendo com que o conteúdo especificado em `Scene` seja renderizado.
9. `primaryStage.show();`: torna o `Stage` visível na tela, efetivamente exibindo a janela ao usuário.
10. `Platform.exit();`: encerra a aplicação JavaFX de forma controlada, fechando todas as janelas e liberando recursos.

11. `Parent`: classe base para nós que podem conter outros nós, usada frequentemente como tipo de raiz da cena.
12. `Node`: classe abstrata que representa qualquer elemento visual no grafo de cena, como botões, textos ou contêineres.
13. `Button`: componente de botão clicável que dispara ações quando o usuário interage com ele.
14. `Label`: componente de texto não editável usado para exibir informações estáticas na interface.
15. `TextField`: campo de texto de linha única que permite entrada de dados pelo usuário.
16. `TextArea`: área de texto de múltiplas linhas para entrada ou exibição de textos mais longos.
17. `CheckBox`: componente de seleção com estado marcado ou desmarcado, útil para configurações booleanas.
18. `RadioButton`: botão de opção que costuma trabalhar em grupo, permitindo que apenas uma opção seja selecionada por vez.
19. `ToggleGroup`: agrupa `RadioButton` para garantir exclusividade de seleção em um conjunto de opções.
20. `ComboBox<T>`: lista suspensa que exibe opções quando clicada, permitindo a escolha de um item entre vários.

21. `VBox`: contêiner de layout que organiza filhos em uma coluna vertical, facilitando a montagem de formulários e listas simples.
22. `HBox`: contêiner que organiza nós em linha horizontal, útil para barras de ferramentas e agrupamento lateral.
23. `BorderPane`: layout que divide a tela em regiões (top, bottom, left, right, center), permitindo estruturas clássicas de aplicação.
24. `GridPane`: contêiner que organiza elementos em linhas e colunas, lembrando uma tabela flexível para formulários estruturados.
25. `StackPane`: layout que empilha nós uns sobre os outros, posicionando o conteúdo centralizado por padrão.
26. `AnchorPane`: contêiner que permite ancorar nós a bordas específicas, dando controle preciso de posicionamento.
27. `Pane`: contêiner básico sem política de layout sofisticada, usado para posicionamento absoluto ou cenários personalizados.
28. `SceneBuilder`: ferramenta visual que gera arquivos FXML arrastando e soltando componentes, acelerando o design da interface.
29. `Insets`: classe usada para definir margens internas e espaçamentos, controlando o respiro entre componentes.
30. `setPadding(new Insets(...))`: configura o preenchimento interno de um contêiner, afastando os nós da borda.

31. `FXMLLoader.load(...)`: carrega um arquivo `.fxml` e devolve a hierarquia de nós que representará a interface definida em XML.
32. `@FXML`: anotação que marca campos e métodos a serem injetados ou chamados pelo JavaFX a partir de um arquivo FXML.
33. `fx:controller`: atributo no FXML que liga o arquivo ao controlador Java responsável pela lógica da tela.
34. `onAction="#metodo"`: atributo FXML que associa eventos de clique ou ação a métodos no controlador, ligando interface e código.
35. `Controller`: classe Java que implementa a lógica da interface descrita em FXML, manipulando eventos e atualizações de dados.
36. `initialize()`: método opcional do controlador chamado após o carregamento do FXML, usado para configuração inicial de componentes.
37. `root.getScene().getWindow()`: obtém a janela (`Stage`) a partir de um nó presente na cena, comum ao trocar telas.
38. `stage.setScene(novaScene);`: troca a cena atual da janela por outra, permitindo navegação entre telas diferentes.
39. `button.setOnAction(event -> { ... });`: define um manipulador de evento para clique no botão usando expressão lambda.
40. `scene.setRoot(novoRoot);`: altera o nó raiz da cena atual, trocando a interface inteira sem substituir o `Stage`.

41. `Image`: classe que representa imagens carregadas de arquivos ou URLs, usadas em componentes visuais.
42. `ImageView`: nó que exibe uma `Image` na cena, com propriedades de tamanho e escala.
43. `setImage(new Image(url));`: troca a imagem exibida em um `ImageView`, permitindo atualizar conteúdo visual dinamicamente.
44. `ProgressBar`: componente que mostra progresso contínuo de uma tarefa numa barra preenchida.
45. `ProgressIndicator`: indicador circular de progresso, geralmente usado para tarefas indeterminadas.
46. `Alert`: classe para exibir caixas de diálogo de aviso, erro, informação ou confirmação ao usuário.
47. `Timeline`: mecanismo de animação baseado em tempo, permitindo alterar propriedades de nós em intervalos definidos.
48. `KeyFrame`: representa um ponto no tempo em uma `Timeline`, especificando valores de propriedades nesse instante.
49. `setOnCloseRequest(event -> { ... });`: registra um manipulador para o evento de fechamento da janela, permitindo confirmar saída ou salvar dados.
50. `Css`: uso de arquivos `.css` aplicados à cena através de `scene.getStylesheets().add(...)`, controlando visual e temas da aplicação.
