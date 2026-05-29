## 17 AWS CLI

1. `AWS CLI`: ferramenta oficial de linha de comando para interagir com serviços AWS usando comandos estruturados em `aws serviço operação`.
2. `aws --version`: exibe a versão instalada da AWS CLI, confirmando se a ferramenta está acessível no terminal.
3. `aws help`: mostra ajuda geral com estrutura de comandos, serviços disponíveis e opções globais.
4. `aws serviço help`: exibe a documentação de linha de comando para um serviço específico, como `aws s3 help`.
5. `aws configure`: inicia assistente interativo para definir Access Key, Secret Key, região padrão e formato de saída.
6. `aws configure list`: mostra como a CLI está configurada, indicando de onde cada valor (perfil, variável de ambiente, arquivo) é carregado.
7. `aws configure get chave`: lê um valor específico da configuração atual, como região ou formato de saída.
8. `aws configure set chave valor`: grava um valor de configuração, por exemplo ajustar a região padrão sem interativo.
9. `--profile nome`: opção global que força o uso de um perfil de credenciais específico para aquele comando.
10. `--region codigo-regiao`: define explicitamente a região de execução para o comando atual, sobrescrevendo o padrão.

11. `~/.aws/credentials`: arquivo onde ficam armazenadas as chaves de acesso para perfis da AWS CLI no ambiente de usuário.
12. `~/.aws/config`: arquivo que guarda configurações de perfis, incluindo região e formato de saída.
13. `AWS_PROFILE`: variável de ambiente que indica qual perfil deve ser usado por padrão nos comandos.
14. `aws sts get-caller-identity`: retorna o ARN, ID da conta e usuário ou role associado às credenciais em uso.
15. `aws configure sso`: inicia configuração de acesso via Single Sign-On, criando estrutura de perfis SSO.
16. `aws sso login --profile nome`: realiza login SSO para o perfil especificado, permitindo uso temporário de credenciais.
17. `--output json|table|text`: parâmetro global que muda o formato do resultado apresentado no terminal.
18. `--query expressão`: permite filtrar e projetar campos de saída usando expressões JMESPath.
19. `aws ec2 describe-regions`: lista regiões disponíveis para uso com EC2 na conta atual.
20. `aws ec2 describe-availability-zones`: consulta zonas de disponibilidade em uma região, usadas para alta disponibilidade.

21. `aws s3 ls`: lista buckets S3 pertencentes à conta configurada, exibindo nomes e datas de criação.
22. `aws s3 ls s3://meu-bucket`: lista objetos dentro de um bucket específico, funcionando como listagem de diretório.
23. `aws s3 mb s3://novo-bucket`: cria um novo bucket S3 com o nome informado, respeitando regras globais de naming.
24. `aws s3 rb s3://bucket`: remove um bucket vazio do S3, apagando o contêiner de objetos.
25. `aws s3 cp arquivo s3://bucket/arquivo`: envia um arquivo local para um bucket S3, criando ou substituindo o objeto.
26. `aws s3 cp s3://bucket/arquivo .`: faz o download de um objeto do S3 para o diretório atual.
27. `aws s3 sync pasta-local s3://bucket/pasta`: sincroniza diretório local com caminho em bucket, enviando apenas mudanças.
28. `aws s3 sync s3://bucket/pasta pasta-local`: traz conteúdo do S3 para o ambiente local, espelhando arquivos.
29. `--exclude` e `--include`: filtros usados com `aws s3 cp` e `aws s3 sync` para controlar quais arquivos serão copiados.
30. `aws s3 rm s3://bucket/arquivo`: apaga um objeto no bucket S3, removendo permanentemente o arquivo.

31. `aws ec2 describe-instances`: lista instâncias EC2 existentes na região corrente, com detalhes de estado e configuração.
32. `aws ec2 describe-instances --filters Name=instance-type,Values=t2.micro`: filtra instâncias com base em tipo, retornando apenas as correspondentes.
33. `aws ec2 run-instances`: comando que cria novas instâncias EC2 com base em AMI, tipo e demais parâmetros fornecidos.
34. `aws ec2 terminate-instances --instance-ids id1 id2`: encerra instâncias específicas, liberando recursos de computação.
35. `aws ec2 start-instances --instance-ids id`: inicia instância parada, voltando a ser cobrada como instância em execução.
36. `aws ec2 stop-instances --instance-ids id`: para uma instância em execução, mantendo discos EBS associados.
37. `aws ec2 describe-images --owners self`: lista AMIs próprias da conta para reutilizar configurações de máquina.
38. `aws ec2 describe-key-pairs`: mostra pares de chaves cadastrados para acesso SSH às instâncias.
39. `aws ec2 describe-security-groups`: exibe grupos de segurança e suas regras de entrada e saída.
40. `aws ec2 create-tags --resources id --tags Key=Name,Value=Servidor`: adiciona tags descritivas a recursos, ajudando em organização.

41. `aws iam list-users`: lista usuários IAM existentes, permitindo revisar identidades configuradas na conta.
42. `aws iam list-roles`: mostra roles IAM que podem ser assumidas por serviços ou usuários federados.
43. `aws iam list-policies`: lista políticas gerenciadas disponíveis para anexar a usuários, grupos ou roles.
44. `aws logs describe-log-groups`: exibe grupos de logs do CloudWatch, base para consulta de eventos de aplicações.
45. `aws logs filter-log-events`: pesquisa eventos dentro de um grupo de logs com filtros de tempo e padrões de mensagem.
46. `aws cloudformation deploy`: aplica templates de infraestrutura como código, criando ou atualizando stacks.
47. `aws lambda list-functions`: lista funções Lambda na região atual, facilitando inventário de funções serverless.
48. `aws lambda invoke`: executa manualmente uma função Lambda e grava o resultado em arquivo de saída.
49. `aws configure import`: importa credenciais de um arquivo CSV exportado do console IAM para criar perfis na CLI.
50. `Boas práticas de segurança`: recomendação de usar perfis, IAM de mínimo privilégio, rotação de chaves e, sempre que possível, SSO ou roles temporárias em vez de chaves estáticas.
