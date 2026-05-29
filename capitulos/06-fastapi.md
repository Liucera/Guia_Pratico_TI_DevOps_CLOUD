## 6 FastAPI

1. `from fastapi import FastAPI`: importa a classe principal usada para criar a aplicação web FastAPI.
2. `app = FastAPI()`: instancia o objeto da aplicação, ponto central onde as rotas e configurações são registradas.
3. `@app.get("/")`: define uma operação de rota HTTP GET para o caminho raiz, usada para retornar dados quando a URL é acessada.
4. `@app.post("/itens")`: registra uma rota HTTP POST para criação de recursos, geralmente para receber dados no corpo da requisição.
5. `@app.put("/itens/{id}")`: cria rota HTTP PUT para atualização completa de um recurso identificado por `id`.
6. `@app.delete("/itens/{id}")`: define rota HTTP DELETE que remove um recurso específico no servidor.
7. `@app.patch("/itens/{id}")`: implementa rota HTTP PATCH para atualizações parciais em recursos existentes.
8. `@app.api_route("/itens", methods=["GET","POST"])`: mapeia múltiplos métodos HTTP para o mesmo caminho, permitindo tratar várias operações em uma única função.
9. `async def endpoint():`: define uma função assíncrona de endpoint, permitindo operações não bloqueantes como chamadas a banco ou APIs.
10. `return {"mensagem": "ok"}`: retorna um dicionário Python que é convertido automaticamente em JSON na resposta HTTP.

11. `from pydantic import BaseModel`: importa a classe base usada para criar modelos de dados com validação automática.
12. `class Item(BaseModel):`: define um modelo Pydantic que descreve a estrutura do corpo da requisição e da resposta.
13. `nome: str`: campo obrigatório do modelo, indicando tipo string e participando da validação.
14. `preco: float | None = None`: campo opcional com tipo numérico, permitindo ausência no corpo da requisição.
15. `item: Item`: declaração de parâmetro de função de rota que indica que os dados devem ser lidos do corpo e validados pelo modelo.
16. `response_model=Item`: parâmetro no decorador da rota que define o modelo usado para filtrar e documentar a resposta.
17. `status_code=201`: define o código HTTP padrão retornado pela rota, como 201 para recursos criados.
18. `from typing import List`: permite declarar listas de modelos em parâmetros ou respostas, como `List[Item]`.
19. `tags=["itens"]`: agrupa a rota em uma categoria na documentação automática, facilitando navegação no Swagger.
20. `summary="Cria um item"`: adiciona um resumo curto à documentação da operação de rota.`uvicorn main:app --reload`: comando de terminal que inicia o servidor ASGI, carregando a aplicação `app` do módulo `main` com recarga automática.

21. `uvicorn main:app --reload`: comando de terminal que inicia o servidor ASGI, carregando a aplicação `app` do módulo `main` com recarga automática.
22. `uvicorn main:app --host 0.0.0.0 --port 8000`: executa a aplicação acessível em todas as interfaces de rede na porta 8000.
23. `fastapi run`: comando simplificado para iniciar o servidor recomendado pelo guia oficial, usando a aplicação configurada.
24. `pip install "uvicorn[standard]"`: instala o servidor Uvicorn com dependências extras recomendadas para produção.
25. `/docs`: rota gerada automaticamente que exibe a documentação interativa Swagger UI para testar endpoints.
26. `/redoc`: rota alternativa de documentação usando a interface ReDoc, útil para consulta das definições da API.
27. `openapi_url="/openapi.json"`: parâmetro na criação do `FastAPI()` que define o caminho do documento OpenAPI.
28. `title="Minha API"`: define o título da aplicação na documentação e nos metadados.
29. `version="1.0.0"`: registra a versão atual da API, importante para controle de evolução.
30. `description="Descrição da API"`: adiciona texto explicativo exibido na página de documentação.

31. `from fastapi import Depends`: importa o sistema de injeção de dependências do FastAPI, usado para reaproveitar lógica entre rotas.
32. `def get_db():`: função de dependência que cria ou recupera um recurso, como conexão de banco de dados.
33. `db = Depends(get_db)`: parâmetro que pede ao FastAPI para injetar automaticamente o retorno da função de dependência.
34. `Header`: tipo de parâmetro especial para extrair valores de cabeçalhos HTTP e usá-los como dependências ou validações.
35. `Query`: helper que define metadados e validação para parâmetros de consulta, como limites e valores padrão.
36. `Path`: especificador de parâmetros de rota que permite validação e documentação de variáveis na URL.
37. `Cookie`: tipo que lê valores vindos de cookies da requisição, útil para autenticação baseada em sessão.
38. `Body`: helper para configurar detalhes do corpo da requisição, como embed ou descrição adicional.
39. `BackgroundTasks`: recurso que permite agendar tarefas de fundo para rodar após a resposta ser enviada ao cliente.
40. `Security`: dependência especial para descrever e aplicar esquemas de segurança, como autenticação com tokens.

41. `APIRouter()`: classe usada para agrupar rotas relacionadas em módulos separados, facilitando a organização de grandes aplicações.
42. `router = APIRouter(prefix="/itens", tags=["itens"])`: cria um roteador com prefixo de caminho e grupo de documentação para endpoints de itens.
43. `@router.get("/")`: declara uma rota dentro de um roteador, que depois será incluída na aplicação principal.
44. `app.include_router(router)`: adiciona o conjunto de rotas do `APIRouter` à aplicação principal, integrando módulos separados.
45. `responses={404: {"description": "Não encontrado"}}`: personaliza respostas esperadas na documentação, descrevendo códigos específicos. [web:66]
46. `HTTPException(status_code=404, detail="Item não encontrado")`: lança exceções HTTP que são convertidas em respostas com código e mensagem apropriados.
47. `from fastapi.middleware.cors import CORSMiddleware`: importa middleware para configurar CORS, permitindo acesso da API por front-ends em outros domínios.
48. `app.add_middleware(CORSMiddleware, ...)`: registra middleware na aplicação, controlando origens, métodos e cabeçalhos permitidos.
49. `response_model_exclude_unset=True`: opção que faz a resposta omitir campos não definidos, retornando apenas dados efetivamente preenchidos.
50. `include_in_schema=False`: marca uma rota para não aparecer na documentação automática, embora continue acessível na API.
