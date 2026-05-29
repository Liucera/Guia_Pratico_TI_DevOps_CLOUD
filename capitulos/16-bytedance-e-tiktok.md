## 16 ByteDance e TikTok

1. `ByteDance`: empresa de tecnologia responsável por plataformas de conteúdo como TikTok, que oferece APIs oficiais para integrações e análise de dados.
2. `TikTok for Business`: conjunto de ferramentas e APIs voltado para anunciantes e parceiros, permitindo gerenciar campanhas, criativos e relatórios.
3. `TikTok Developer Platform`: portal para desenvolvedores se registrarem, criarem aplicações, obterem credenciais e acessarem documentação técnica.
4. `App ID`: identificador único da aplicação registrada na plataforma de desenvolvedores, usado em fluxos de autenticação e chamadas de API.
5. `App secret`: chave secreta associada ao App ID, usada para assinar solicitações e trocar códigos de autorização por tokens de acesso. [][web:170]
6. `Access token`: credencial de curto prazo enviada em cabeçalhos HTTP para autorizar chamadas às APIs TikTok.
7. `Refresh token`: token usado para obter novos access tokens sem exigir novo login do usuário ou anunciante.
8. `OAuth2`: protocolo de autorização utilizado pelas APIs TikTok para permitir que usuários concedam acesso limitado a dados da conta.
9. `Scope`: lista de permissões específicas que uma aplicação solicita no fluxo OAuth2, como ler campanhas ou publicar conteúdo.
10. `Rate limit`: limite de chamadas permitido em determinado período para cada aplicação ou token, controlando uso da infraestrutura.

11. `TikTok Research API`: interface oficial para pesquisadores consultarem dados públicos de contas e vídeos, com foco em transparência e estudo.
12. `POST /v2/research/user/info`: endpoint da Research API que retorna dados públicos de uma conta TikTok a partir do username informado.
13. `fields` (Research API): parâmetro que define quais atributos de usuário ou vídeo devem ser retornados, como nome, bio e contagens.
14. `username`: campo usado em chamadas da Research API para indicar o identificador público da conta a ser consultada.
15. `POST /v2/research/video/query`: endpoint usado para buscar vídeos públicos com filtros por período, idioma ou outras características.
16. `Video metrics`: métricas como visualizações, curtidas, comentários e compartilhamentos, retornadas por endpoints de pesquisa de vídeos.
17. `Pagination`: mecanismo que distribui resultados de consultas em páginas, controladas por parâmetros como `cursor` e `page_size`.
18. `cursor`: ponteiro para a próxima página de resultados em algumas APIs TikTok, usado para continuar iterações.
19. `page_size`: quantidade máxima de itens retornados por página em uma chamada de listagem, ajustável pelo cliente.
20. `Error codes`: códigos numéricos ou textuais retornados pela API para indicar erros de autorização, parâmetros inválidos ou limites excedidos.

21. `TikTok Content Posting API`: conjunto de endpoints que permitem subir vídeos e fotos programaticamente para contas autorizadas.
22. `source=FILE_UPLOAD`: modo da Content Posting API em que o cliente envia o arquivo de vídeo diretamente em upload para os servidores TikTok.
23. `source=PULL_FROM_URL`: modo de postagem em que o TikTok baixa o vídeo de uma URL fornecida, sem upload direto do cliente.
24. `upload_url`: URL temporária retornada pela Content Posting API para onde o cliente deve enviar o arquivo de vídeo usando requisição PUT.
25. `publish_id`: identificador de publicação retornado ao iniciar upload, usado para acompanhar processamento e status do vídeo.
26. `post_mode`: campo requerido na requisição de postagem que define o tipo de publicação, como rascunho ou publicação imediata.
27. `media_type`: parâmetro que especifica se o conteúdo enviado é vídeo, foto ou outro formato suportado.
28. `caption`: texto de legenda enviado junto à mídia, respeitando limites de tamanho e políticas de conteúdo.
29. `privacy_level`: configuração de visibilidade da publicação, indicando se é pública, privada ou limitada a determinados públicos.
30. `scheduled_time`: parâmetro utilizado para agendar a publicação de conteúdo em um horário futuro, quando disponível.

31. `TikTok API for Business`: API destinada a anunciantes para gerenciar contas de anúncios, campanhas, grupos de anúncios e criativos.
32. `advertiser_id`: identificador do anunciante ou conta de anúncios usado como parâmetro obrigatório em chamadas da Ads API.
33. `POST /open_api/v1.2/oauth2/access_token/`: endpoint da Ads API que troca um código de autorização por access token.
34. `auth_code`: código temporário obtido após o usuário conceder acesso, usado na solicitação de access token da Ads API.
35. `GET /open_api/v1.2/campaign/get/`: endpoint que retorna campanhas de uma conta de anúncios, com suporte a filtros e paginação.
36. `GET /open_api/v1.2/adgroup/get/`: endpoint que lista grupos de anúncios associados a campanhas, podendo ser filtrado por `campaign_ids`.
37. `filtering={"campaign_ids":[...]}`: parâmetro JSON usado nas URLs para filtrar resultados de grupos de anúncios por campanhas específicas.
38. `GET /open_api/v1.2/ad/get/`: endpoint que retorna anúncios individuais, incluindo criativos e estados de veiculação.
39. `GET /open_api/v1.2/reports/integrated/get`: endpoint que gera relatórios integrados de desempenho de campanhas, grupos e anúncios.
40. `data_level=AUCTION_AD`: configuração de relatório que pede dados em nível de anúncio individual, permitindo análises detalhadas de performance.

41. `display API`: categoria de API usada para renderizar ou exibir conteúdo TikTok de forma integrada em outros aplicativos e sites, conforme diretrizes.
42. `Register application`: processo inicial na Developer Platform em que são definidos nome, descrição, permissões e URLs de callback da aplicação.
43. `Callback URL`: endereço para o qual o TikTok redireciona o usuário após autorização, passando códigos e parâmetros de autenticação.
44. `Authorization header`: cabeçalho HTTP `Authorization: Bearer token` utilizado em praticamente todas as chamadas autenticadas às APIs.
45. `Content-Type: application/json`: cabeçalho que indica que o corpo da requisição está em JSON, formato padrão para parâmetros das APIs.
46. `Retry strategy`: prática de repetir requisições com falha transitória respeitando backoff e limites, recomendada em integrações com a API. []
47. `Sandbox environment`: ambiente de testes fornecido para alguns produtos TikTok, permitindo validar integrações sem impactar contas reais. []
48. `Webhooks`: mecanismo que permite ao TikTok enviar notificações de eventos para URLs registradas, como mudanças de status em vídeos ou anúncios.
49. `Compliance e políticas`: conjunto de termos de uso e regras que exigem que aplicações respeitem privacidade, limites de uso e direitos autorais.
50. `Monitoramento de API`: prática de registrar logs de requisições, respostas e erros para garantir estabilidade de integrações com TikTok e ByteDance.
