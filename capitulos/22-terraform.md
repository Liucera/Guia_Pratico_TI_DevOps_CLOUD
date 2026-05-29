## 22 Terraform

1. `Terraform`: ferramenta de Infrastructure as Code (IaC) que permite definir, provisionar eVersionar infraestrutura em nuvem e sistemas locais usando arquivos declarativos `.tf`.
2. `HCL`: HashiCorp Configuration Language, linguagem de configuração usada nos arquivos `.tf` para descrever recursos, variáveis e saídas.
3. `arquivo .tf`: arquivo de texto que contém módulos, recursos, variáveis e saídas definidos em HCL para uma infraestrutura.
4. `provider`: bloco que define o provedor de nuvem ou serviço (AWS, Azure, GCP), carregando plugin e configuração para interagir com a API.
5. `resource`: bloco que descreve um componente de infraestrutura, como instância, bucket ou rede, com tipo, nome e atributos.
6. `terraform init`: inicializa o diretório de trabalho, baixando provedores e módulos especificados nos arquivos `.tf`.
7. `terraform init -upgrade`: re-inicializa o projeto atualizando provedores e módulos para as versões mais recentes permitidas.
8. `terraform init -reconfigure`: re-inicializa sem reutilizar configurações anteriores, forçando redescoberta de estado e provedores.
9. `terraform validate`: verifica se os arquivos `.tf` são sintaticamente válidos e internamente consistentes, sem depender de estado ou provedores.
10. `terraform fmt`: formata automaticamente os arquivos `.tf` no diretório, aplicando estilo padrão e melhorando legibilidade.

11. `terraform plan`: gera um plano de execução mostrando o que será criado, modificado ou destruído se `apply` for executado.
12. `terraform plan -out=tfplan`: salva o plano gerado em um arquivo binário (`tfplan`) para ser aplicado depois.
13. `terraform apply`: executa o plano, aplicando mudanças na infraestrutura conforme definido nos arquivos `.tf`.
14. `terraform apply -auto-approve`: aplica mudanças sem solicitar confirmação interativa, útil em pipelines de CI/CD.
15. `terraform apply tfplan`: executa exatamente o plano salvo anteriormente, garantindo que mudanças aplicadas correspondam ao que foi planejado.
16. `terraform destroy`: remove todos os recursos criados pelo Terraform na configuração atual, destruindo a infraestrutura.
17. `terraform destroy -auto-approve`: executa destruição sem confirmação, geralmente usado em ambientes de teste ou pipelines.
18. `terraform show`: exibe o estado atual da infraestrutura conhecida pelo Terraform, incluindo valores de atributos.
19. `terraform refresh`: sincroniza o estado local com o estado real da infraestrutura, atualizando valores de atributos.
20. `Terraform Cloud`: serviço gerenciado para armazenar estado, executar planos e gerenciar equipes e workspaces de forma centralizada.

21. `estado (`terraform.tfstate`)`: arquivo que contém o estado atual da infraestrutura, mapeando recursos do mundo real aos recursos do código.
22. `backend`: configuração que define onde o estado será armazenado, como S3, Azure Blob ou Terraform Cloud.
23. `terraform state list`: lista recursos registrados no estado atual, mostrando os IDs lógicos de recursos gerenciados.
24. `terraform show -json`: exibe o estado atual em formato JSON, facilitando processamento por scripts.
25. `terraform state mv SRC DEST`: move um recurso dentro do estado, atualizando a referência sem recriar a infraestrutura.
26. `terraform state rm recurso`: remove um recurso do estado, fazendo com que o Terraform pare de gerenciá-lo, sem destruir na nuvem.
27. `terraform state import recurso ID`: importa um recurso existente na nuvem para o estado do Terraform, gerenciando-o de agora em frente.
28. `terraform taint recurso`: marca um recurso como corrompido, forçando recriação na próxima execução de `apply`.
29. `terraform untaint recurso`: desmarca um recurso como corrompido, removendo o sinalizador de `taint`.
30. `lock state`: bloqueio de estado que impete que múltiplas pessoas ou processos apliquem mudanças simultaneamente, evitando conflitos.

31. `variável (variable)`: bloco que define parâmetros de entrada, como nome de ambiente ou região, permitindo reutilização de código.
32. `output`: bloco que define valores de saída, como IP de uma VM ou URL de um serviço, expostos para outros módulos ou usuários.
33. `terraform output`: exibe os valores de saída atuais da infraestrutura gerenciada pelo projeto.
34. `-var "nome=valor"`: flag usada na linha de comando para definir valor de variável em `plan` ou `apply`.
35. `-var-file="arquivo.tfvars"`: carrega valores de variáveis a partir de um arquivo `.tfvars`, centralizando configurações.
36. `locals`: bloco que define valores locais derivados de outras variáveis, simplificando expressões e evitando repetição.
37. `terraform console`: abre um shell interativo para testar expressões HCL e funções antes de usar em arquivos `.tf`.
38. `function`: função do HCL, como `concat`, `lookup` ou `element`, usada para manipular dados em expressões.
39. `depends_on`: atributo que define dependência explícita entre recursos, garantindo ordem de criação.
40. `count`: recurso especial que permite replicar um recurso múltiplas vezes com base em número ou tamanho de lista.

41. `for_each`: similar ao `count`, mas itera sobre mapas ou conjuntos, criando recursos com chaves identificadas.
42. `módulo`: conjunto de arquivos `.tf` organizados em um diretório, encapsulando recursos e expostos via chamadas de módulo.
43. `module "nome" { source = "..." }`: bloco que chama um módulo, podendo usar provedores, variáveis e saídas.
44. `módulo raiz`: diretório principal onde o Terraform é iniciado, contendo o arquivo `main.tf` e chamadas de módulos.
45. `módulo remoto`: módulo hospedado em repositório Git, Terraform Registry ou outro backend, não no diretório local.
46. `PoR (Plan-Only Review)`: prática de revisar o plano antes de aplicar, garantindo que mudanças sejam corretas e seguras.
47. `CI/CD`: integração contínua e entrega contínua, onde `terraform plan` e `apply` são executados em pipelines automatizados.
48. `Terraform Registry`: repositório oficial de módulos públicos e privados, facilitando reutilização de componentes de infraestrutura.
49. `provedor com versão`: prática de travar versão do provedor para garantir consistência entre ambientes, como `version = ">= 5.0"`.
50. `Boas práticas com Terraform`: usar versionamento de estado, repositório Git, revisão de plano, módulos reutilizáveis e separar ambientes (dev, staging, prod) em workspaces ou diretórios distintos.
