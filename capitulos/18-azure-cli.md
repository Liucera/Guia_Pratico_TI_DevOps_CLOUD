## 18 Azure CLI

1. `Azure CLI`: ferramenta de linha de comando multiplataforma para gerenciar recursos do Azure com comandos `az grupo subcomando`.
2. `az --version`: exibe a versão instalada da CLI e dependências, confirmando que a ferramenta está disponível.
3. `az -h` ou `az --help`: mostra ajuda geral, listando grupos de comandos e opções globais.
4. `az <grupo> -h`: exibe ajuda específica para um grupo de comandos, como `az vm -h` ou `az group -h`.
5. `az login`: abre o fluxo de autenticação no navegador para entrar com sua conta do Azure.
6. `az login --use-device-code`: inicia login via código de dispositivo quando não há navegador disponível.
7. `az account show`: mostra os detalhes da assinatura e usuário atualmente ativos no contexto da CLI.
8. `az account list`: lista todas as assinaturas associadas à conta logada, com IDs e estados.
9. `az account set --subscription ID`: define qual assinatura será usada como padrão para os próximos comandos.
10. `az logout`: encerra a sessão da CLI, removendo tokens de autenticação locais.

11. `az config set chave=valor`: configura opções da CLI, como padrão de localização ou saída.
12. `az config get chave`: obtém o valor atual de uma configuração específica da CLI.
13. `AZURE_DEFAULTS_LOCATION`: variável usada para definir localização padrão de recursos na CLI.
14. `--output json|table|tsv`: parâmetro que escolhe o formato da saída de um comando, como JSON completo ou tabela resumida.
15. `--query expressão`: aplica uma expressão JMESPath à saída JSON para filtrar e projetar campos.
16. `az vm show --query "[name,location]"`: exemplo que retorna apenas nome e localização da VM em uma lista.
17. `az vm show --query "osProfile.adminUsername"`: extrai apenas o usuário administrador de uma máquina virtual.
18. `az vm show --query "[name, osProfile.adminUsername, osProfile.linuxConfiguration.ssh.publicKeys[0].keyData]"`: seleciona múltiplas propriedades aninhadas em uma única consulta.
19. `--subscription ID`: parâmetro que força o uso de uma assinatura específica em um comando isolado.
20. `--only-show-errors`: opção que reduz mensagens de saída, exibindo apenas erros e resultados essenciais.]

21. `az group create --name nome --location região`: cria um novo grupo de recursos, contêiner lógico para recursos Azure.
22. `az group list`: lista grupos de recursos existentes na assinatura atual.
23. `az group show --name nome`: exibe detalhes de um grupo específico, incluindo localização e tags.
24. `az group delete --name nome --yes --no-wait`: exclui um grupo de recursos e todos os recursos associados.
25. `resource group`: conceito de agrupamento lógico de recursos para organização, controle de acesso e lifecycle.
26. `location` (região): parâmetro que define a região geográfica onde recursos físicos serão provisionados.
27. `tags`: pares chave-valor atribuídos a recursos e grupos para organizar, filtrar e controlar custos.
28. `az tag create` / `az tag list`: comandos usados para gerenciar definições de tags em nível de assinatura.
29. `az resource list --resource-group nome`: lista todos os recursos de um grupo, independentemente do tipo.
30. `az resource show --ids ID`: retorna detalhes de um recurso específico usando seu ID completo.

31. `az vm create`: comando que cria uma máquina virtual, combinando vários parâmetros de imagem, tamanho e autenticação.
32. `az vm create --resource-group rg --name nome --image UbuntuLTS --admin-username user --generate-ssh-keys`: exemplo comum de criação de VM Linux com chave SSH.
33. `--size`: parâmetro que especifica o tamanho da VM, como `Standard_B1s` ou `Standard_D2s_v3`.
34. `az vm list`: lista VMs do escopo atual, retornando detalhes em JSON.
35. `az vm list -d -o table`: lista VMs com detalhes (IP, status) em formato de tabela legível.
36. `az vm show --resource-group rg --name vm`: mostra configurações completas de uma VM específica.
37. `az vm start --resource-group rg --name vm`: inicia uma VM parada, reativando a cobrança de computação.
38. `az vm stop --resource-group rg --name vm`: faz shutdown da VM mantendo o recurso alocado.
39. `az vm deallocate --resource-group rg --name vm`: desaloca a VM, liberando hardware e reduzindo custos, mantendo discos.
40. `az vm delete --resource-group rg --name vm --yes`: exclui a VM, podendo manter discos ou recursos relacionados dependendo dos parâmetros.

41. `az storage account create`: cria uma conta de armazenamento, pré-requisito para containers e blobs.
42. `az storage account list`: lista contas de armazenamento na assinatura ou grupo especificado.
43. `az storage container create --account-name conta --name nome`: cria um container de blobs dentro de uma conta de armazenamento.
44. `az storage blob upload --account-name conta --container-name c --name arquivo --file caminho`: envia arquivo local para blob no Azure Storage.
45. `az storage blob download`: baixa um blob de um container para o sistema de arquivos local.
46. `az network vnet create`: cria uma rede virtual, definindo espaço de endereços e sub-redes.
47. `az network nsg create`: cria um Network Security Group para controlar tráfego em portas e protocolos.
48. `az network public-ip create`: provisiona IP público para associar a VMs ou balanceadores de carga.
49. `az network nic create`: cria interface de rede associada a VNet, sub-rede, NSG e IP público.
50. `Boas práticas com Azure CLI`: usar `az login` seguro, limitar permissões via RBAC, separar recursos em grupos coerentes e aproveitar `--query`/tags para governança e automação.
