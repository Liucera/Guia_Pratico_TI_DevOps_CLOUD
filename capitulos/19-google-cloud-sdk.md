## 19 Google Cloud SDK

1. `Google Cloud SDK`: conjunto de ferramentas de linha de comando para interagir com o Google Cloud, incluindo `gcloud`, `gsutil` e `bq`.
2. `gcloud`: ferramenta principal da CLI para gerenciar projetos, recursos e autenticação no Google Cloud.
3. `gsutil`: ferramenta de linha de comando para trabalhar com Cloud Storage, como buckets e objetos.
4. `bq`: ferramenta de linha de comando para BigQuery, usada para criar datasets, tabelas e executar consultas SQL.
5. `kubectl`: ferramenta incluída no SDK para gerenciar clusters do Kubernetes Engine (GKE).
6. `gcloud --version`: exibe a versão instalada da CLI gcloud, confirmando instalação correta.
7. `gcloud help`: mostra ajuda geral com grupos de comandos e opções globais.
8. `gcloud <grupo> help`: exibe ajuda específica para um grupo, como `gcloud auth help` ou `gcloud compute help`.
9. `gcloud init`: inicia assistente interativo para configurar projeto, região e zona padrão.
10. `gcloud auth login`: abre o navegador para autenticação com conta Google, criando credenciais locais.

11. `gcloud auth list`: lista contas com credenciais armazenadas localmente, indicando qual está ativa.
12. `gcloud config configurator`: abre interface interativa para selecionar configurações de projeto e região.
13. `gcloud config get-value propriedade`: consulta valor atual de uma propriedade de configuração.
14. `gcloud config set propriedade valor`: define valor de configuração, como projeto, zona ou região padrão.
15. `gcloud config set project ID_projeto`: muda o projeto padrão usado pelos comandos subsequentes.
16. `gcloud config set compute/zone zona`: define zona padrão para operações de Compute Engine.
17. `gcloud config set compute/region regiao`: define região padrão para recursos como VMs e discos.
18. `gcloud config list`: exibe todas as configurações atuais do SDK, incluindo projeto, zona e região.
19. `gcloud projects list`: lista projetos disponíveis na conta atual, com IDs e nomes.
20. `gcloud projects create ID_projeto --name="Nome"`: cria um novo projeto no Google Cloud.

21. `gcloud compute instances list`: lista instâncias de VM no projeto e região/zona configurados.
22. `gcloud compute instances create nome --image=ubuntu --machine-type=e2-micro`: cria uma nova instância VM com imagem e tamanho especificados.
23. `gcloud compute instances start nome`: inicia uma instância VM parada.
24. `gcloud compute instances stop nome`: para uma instância VM em execução, mantendo discos.
25. `gcloud compute instances delete nome`: remove uma instância VM do projeto.
26. `gcloud compute instances describe nome`: mostra detalhes completos de uma instância, incluindo IPs e configurações.
27. `gcloud compute ssh nome`: abre sessão SSH em uma instância VM diretamente pela CLI.
28. `gcloud compute scp arquivo:nome:/caminho`: copia arquivos localmente entre máquina local e VM.
29. `gcloud compute zones list`: lista zonas de disponibilidade disponíveis para a região.
30. `gcloud compute regions list`: lista regiões disponíveis para provisionamento de recursos.

31. `gsutil ls`: lista buckets e objetos no Cloud Storage, similar ao `ls` do sistema de arquivos.
32. `gsutil mb gs://nome-bucket`: cria um novo bucket no Cloud Storage.
33. `gsutil rm -r gs://bucket`: remove um bucket e todo o seu conteúdo.
34. `gsutil cp arquivo gs://bucket/caminho`: copia arquivo local para o Cloud Storage.
35. `gsutil cp gs://bucket/arquivo .`: baixa objeto do Cloud Storage para o diretório atual.
36. `gsutil cp -r pasta gs://bucket/pasta`: copia diretório recursivamente para o Cloud Storage.
37. `gsutil rsync -r pasta gs://bucket/pasta`: sincroniza diretório local com bucket, atualizando apenas diferenças.
38. `gsutil cat gs://bucket/arquivo`: exibe conteúdo de um objeto no terminal.
39. `gsutil mv gs://bucket/origem gs://bucket/destino`: move ou renomeia objeto dentro do Cloud Storage.
40. `gsutil acl`: conjunto de comandos para gerenciar permissões de acesso em buckets e objetos.

41. `bq --version`: exibe versão da ferramenta BigQuery instalada no SDK.
42. `bq ls`: lista datasets disponíveis no projeto atual.
43. `bq mk dataset`: cria um novo dataset no BigQuery.
44. `bq query --use_legacy_sql=false "SELECT 1"`: executa consulta SQL padrão no BigQuery.
45. `bq mk --table dataset.tabela`: cria uma tabela no dataset especificado.
46. `bq load dataset.tabela arquivo.csv`: carrega dados de arquivo local para tabela no BigQuery.
47. `bq show dataset.tabela`: exibe esquema e metadados de uma tabela.
48. `bq rm dataset`: remove um dataset e todas as tabelas contidas.
49. `gcloud components list`: lista todos os componentes do SDK instalados e disponíveis.
50. `gcloud components install nome_componente`: instala ou atualiza um componente específico do Cloud SDK.
