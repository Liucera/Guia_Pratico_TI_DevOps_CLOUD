## 23 Conceitos de Cloud

1. `Computação em nuvem`: entrega de recursos de TI sob demanda pela internet, com preço conforme o uso, sem necessidade de data centers próprios.
2. `Pagamento conforme o uso`: modelo de cobrança em que se paga apenas pelos recursos consumidos, reduzindo custos fixos.
3. `Elasticidade`: capacidade de expandir ou reduzir recursos automaticamente conforme a demanda, sem intervenção manual pesada.
4. `Escalabilidade`: capacidade de aumentar capacidade de forma suave para atender crescimento de carga de trabalho.
5. `Alta disponibilidade`: projeto de sistemas para garantir tempo de atividade elevado, com redundância e failover automático.
6. `Fortalecimento por serviços gerenciados`: provedor cuida de manutenção, patches e operação de infraestrutura e serviços.
7. `Pool de recursos`: conjunto virtualizado de recursos como CPU, memória, armazenamento e rede, compartilhado entre múltiplos clientes.
8. `On-demand`: provisionamento de recursos quase instantâneo, sem necessidade de capex e longo ciclo de compra.
9. `IaaS`: Infraestrutura como Serviço, oferecendo VMs, armazenamento, redes e sistema operacional sob demanda.
10. `PaaS`: Plataforma como Serviço, fornecendo ambiente para desenvolvimento, deploy e execução de aplicações sem gerenciar infraestrutura.

11. `SaaS`: Software como Serviço, entregando aplicativos completos pela internet, hospedados e gerenciados pelo provedor.
12. `Serverless`: modelo onde o provedor gere alocação e escalabilidade de recursos, cobrando apenas pelo tempo de execução de funções ou serviços.
13. `Nuvem pública`: infraestrutura compartilhada entre múltiplos clientes, oferecida por provedores como AWS, Azure e Google Cloud.
14. `Nuvem privada`: infraestrutura dedicada a uma única organização, podendo ser on-premise ou hospedada por terceiros.
15. `Nuvem híbrida`: combinação de nuvens públicas e privadas, integradas para permitir portabilidade de dados e aplicações.
16. `Multicloud`: uso simultâneo de múltiplos provedores de nuvem para evitar vendor lock-in e distribuir carga.
17. `Data center`: instalação física que abriga servidores, redes e sistemas de armazenamento usados por provedores de nuvem.
18. `Zona de disponibilidade`: data center isolado dentro de uma região, com energia e refrigeração independentes, usado para alta disponibilidade.
19. `Região`: área geográfica contendo múltiplas zonas de disponibilidade, usada para definir localização de recursos.
20. `Latência`: tempo de ida e volta de um pacote entre cliente e servidor, influenciando escolha de região.

21. `Throughput`: capacidade de transferência de dados por unidade de tempo, importante para redes e armazenamento na nuvem.
22. `CDN`: Content Delivery Network, rede distribuída de servidores que entrega conteúdo próximo ao usuário, reduzindo latência.
23. `Load Balancer`: serviço que distribui tráfego entre múltiplas instâncias, melhorando disponibilidade e desempenho.
24. `Auto scaling`: ajuste automático de número de instâncias com base em métricas como CPU e tráfego.
25. `Disaster Recovery`: estratégias para recuperação de sistemas e dados após falhas, desastres ou ataques.
26. `Backup em nuvem`: cópia de dados para armazenamento remoto, com versionamento e recuperação pontual.
27. `Snapshots`: captura pontual do estado de discos ou volumes, usada para backup e recuperação rápida.
28. `Storage object`: armazenamento de objetos, como arquivos em buckets, escalável e acessível por HTTP/API.
29. `Blob storage`: armazenamento de blocos binários grandes, usado para arquivos, imagens, vídeos e backups.
30. `File system como serviço`: sistema de arquivos gerenciado na nuvem, acessível por múltiplas instâncias como montagem de rede.

31. `Rede virtual`: rede lógica isolada dentro da nuvem, com sub-redes, rotas e segurança definidas pelo usuário.
32. `Sub-rede`: divisão lógica de uma rede virtual, permitindo segmentação de recursos e controle de tráfego.
33. `Peering`: conexão entre redes virtuais diferentes, permitindo comunicação privada entre elas.
34. `VPN`: tunelamento criptografado entre rede local e nuvem, para acesso seguro e privado.
35. `Dedicated Connection`: link físico dedicado entre data center local e provedor de nuvem, com maior desempenho e segurança.
36. `IAM`: Identity and Access Management, gerencia usuários, grupos, roles e permissões de acesso a recursos.
37. `Role`: conjunto de permissões que pode ser atribuído a usuários, serviços ou recursos.
38. `Política`: definição de permissões em JSON ou formato nativo, que especifica quem pode fazer o quê em quais recursos.
39. `MFA`: autenticação multifator, exigindo mais de uma prova de identidade para acesso, aumentando segurança.
40. `Criptografia em repouso`: proteção de dados armazenados, como discos e objetos, com chaves de criptografia.

41. `Criptografia em trânsito`: proteção de dados enquanto trafegam entre cliente e servidor ou entre serviços, usando TLS/SSL.
42. `KMS`: Key Management Service, serviço gerenciado para criar, gerenciar e rotacionar chaves de criptografia.
43. `Logging`: registro de eventos e atividades de recursos, usado para auditoria, diagnóstico e compliance.
44. `Monitoring`: acompanhamento de métricas como CPU, memória e latência, com alertas e dashboards.
45. `Alertas`: notificações automáticas quando métricas ultrapassam limites definidos, indicando problemas ou eventos importantes.
46. `Automated provisioning`: criação de infraestrutura por meio de código e APIs, sem intervenção manual.
47. `Infrastructure as Code (IaC)`: uso de arquivos de configuração para definir e versionar infraestrutura, como Terraform e CloudFormation.
48. `DevOps`: conjunto de práticas que unem desenvolvimento e operações, usando automação e CI/CD na nuvem.
49. `CI/CD`: integração contínua e entrega contínua, pipeline automatizado para build, teste e deploy de aplicações na nuvem.
50. `Provedores principais`: AWS, Microsoft Azure e Google Cloud Platform são os três maiores provedores de nuvem pública, com portfólio amplo de serviços.
