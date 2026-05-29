## 5 React

1. `React`: biblioteca JavaScript usada para construir interfaces de usuário baseadas em componentes reutilizáveis, focada em atualização eficiente da tela.
2. `JSX`: sintaxe que mistura JavaScript com marcação parecida com HTML, permitindo descrever a interface de forma declarativa dentro do código.
3. `create-react-app`: ferramenta de linha de comando que cria um projeto React já configurado com bundler, transpiler e servidor de desenvolvimento.
4. `npm create vite@latest`: comando moderno para criar projetos React com Vite, oferecendo build mais rápido e ambiente enxuto.
5. `npm start`: inicia o servidor de desenvolvimento do projeto React, recompilando e recarregando a aplicação a cada alteração de código.
6. `npm run build`: gera a versão otimizada para produção da aplicação React, produzindo arquivos estáticos para deploy.
7. `npm test`: executa a suíte de testes configurada no projeto, validando o comportamento dos componentes.
8. `import React from "react";`: importação tradicional do objeto React, necessária em alguns ambientes para interpretar JSX corretamente.
9. `export default Componente;`: torna o componente disponível para importação em outros arquivos, facilitando a reutilização.
10. `import Componente from "./Componente";`: traz um componente definido em outro arquivo para uso na árvore de componentes.

11. `function Componente() { ... }`: define um componente de função, forma recomendada para criar interfaces em React moderno.
12. `return (<div>...</div>);`: retorna o JSX que descreve o que o componente deve renderizar na tela.
13. `props`: objeto recebido como parâmetro de componentes que contém valores passados pelo componente pai, permitindo personalização.
14. `Componente prop="valor" />`: exemplo de uso de props, enviando dados para o componente filho através de atributos JSX.
15. `children`: propriedade especial que representa elementos aninhados entre a abertura e o fechamento de um componente.
16. `fragment <>...</>`: sintaxe para agrupar múltiplos elementos JSX sem adicionar uma div extra na árvore DOM.
17. `className`: atributo JSX equivalente ao `class` do HTML, usado para aplicar classes de CSS a elementos.
18. `onClick={função}`: adiciona um manipulador de evento de clique a um elemento JSX, disparando lógica quando o usuário interage.
19. `onChange={função}`: associa lógica a mudanças de valor em inputs, permitindo formular e controlar formulários.
20. `style={{ chave: valor }}`: define estilos inline usando um objeto JavaScript, com propriedades em camelCase.

21. `useState(valorInicial)`: hook que cria um estado reativo no componente de função, retornando o valor atual e uma função para atualizá-lo.
22. `const [estado, setEstado] = useState(...)`: padrão de desestruturação usado para trabalhar com o valor do estado e sua função de atualização.
23. `setEstado(novoValor)`: atualiza o estado, disparando uma nova renderização do componente com os dados atualizados.
24. `useEffect(() => { ... }, [deps])`: hook que executa efeitos colaterais como chamadas de API, timers ou integração com código externo.
25. `useEffect(() => { ... }, [])`: executa o efeito apenas uma vez, após a primeira renderização, geralmente usado para buscar dados iniciais.
26. `useEffect(() => { ... })`: executa o efeito após toda renderização, útil para monitorar mudanças sem controle de dependências.
27. `useContext(Contexto)`: hook que acessa um valor fornecido por um `Context.Provider` sem passar props manualmente por muitos níveis.
28. `useRef(valorInicial)`: cria uma referência mutável que persiste entre renderizações, usada para acessar elementos DOM ou guardar valores sem re-renderizar.
29. `useMemo(() => cálculo, [deps])`: memoriza o resultado de um cálculo caro, recalculando apenas quando as dependências mudam.
30. `useCallback(() => função, [deps])`: memoriza funções para evitar recriações desnecessárias, melhorando performance em componentes filhos.

31. `createContext(valorDefault)`: cria um contexto que permite compartilhar dados como tema ou usuário logado por toda a árvore de componentes.
32. `<Context.Provider value={valor}>`: componente que fornece um valor de contexto para todos os descendentes que usarem `useContext`.
33. `<Context.Consumer>`: componente que consome valores de contexto usando render props, abordagem mais antiga em relação ao `useContext`.
34. `key={valorUnico}`: atributo obrigatório em listas de elementos para ajudar o React a identificar qual item foi alterado, adicionado ou removido.
35. `{lista.map(item => <Elemento key={item.id} />)}`: padrão para renderizar listas de componentes a partir de arrays de dados.
36. `conditional && <Componente />`: renderização condicional que exibe o componente apenas quando a expressão booleana é verdadeira.
37. `conditional ? <A /> : <B />`: expressão ternária usada para alternar entre dois blocos de JSX com base em uma condição.
38. `defaultProps`: propriedade estática de componentes que define valores padrão para props não informadas.
39. `propTypes`: especificação de tipos e obrigatoriedade de props, usada em desenvolvimento para validar uso de componentes.
40. `memo(Componente)`: função que envolve um componente e evita renderizações desnecessárias quando as props não mudam.

41. `BrowserRouter`: componente que habilita rotas baseadas em histórico de navegador, geralmente importado de bibliotecas como React Router.
42. `Route path="..." element={<Componente />}`: define uma regra de rota que associa uma URL específica a um componente de página.
43. `Link to="/caminho"`: componente que cria links de navegação interna sem recarregar a página inteira.
44. `useNavigate()`: hook que permite navegar programaticamente entre rotas, útil após ações como login ou envio de formulário.
45. `useParams()`: hook que lê parâmetros dinâmicos da URL, como IDs de recursos acessados na rota.
46. `Suspense fallback={<Loading />}`: componente que exibe um fallback enquanto partes da interface são carregadas de forma assíncrona.
47. `lazy(() => import("./Componente"))`: função que permite carregamento dinâmico de componentes sob demanda, reduzindo o tamanho inicial do bundle.
48. `StrictMode`: componente que ativa verificações adicionais em desenvolvimento para detectar padrões problemáticos nos componentes.
49. `ReactDOM.createRoot(element).render(<App />);`: inicializa a aplicação React na versão moderna, associando a árvore de componentes ao elemento raiz do HTML.
50. `Regras de Hooks`: conjunto de boas práticas que exigem chamar hooks apenas no topo de componentes de função e nunca dentro de loops ou condicionais, garantindo ordem consistente de execução.
