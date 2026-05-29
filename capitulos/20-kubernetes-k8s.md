## 20 Kubernetes (k8s)

1. `Kubernetes`: sistema de orquestração de contêineres que gerencia escala, rede, deploy e automação de pods em clusters.
2. `k8s`: abreviação comum para Kubernetes, usada amplamente na comunidade e documentação.
3. `cluster`: conjunto de máquinas (nós) que executam contêineres gerenciados pelo Kubernetes.
4. `nó (node)`: máquina física ou virtual que roda containers dentro do cluster Kubernetes.
5. `pod`: unidade mínima do Kubernetes, contendo um ou mais containers compartilhando rede e armazenamento.
6. `kubectl`: ferramenta de linha de comando oficial para interagir com o Kubernetes, executando comandos como `kubectl get pods`.
7. `kubectl version`: exibe versão do cliente e do servidor Kubernetes, confirmando compatibilidade.
8. `kubectl cluster-info`: mostra informações sobre o cluster, incluindo endpoints da API e versão.
9. `kubectl config`: grupo de comandos para gerenciar contextos e configurações de conexão com clusters.
10. `kubectl config current-context`: mostra o contexto atual usado pelo kubectl para direcionar comandos.

11. `kubectl config use-context nome`: altera o contexto para outro cluster ou namespace configurado.
12. `~/.kube/config`: arquivo que armazena configurações de clusters, usuários e contextos usados pelo kubectl.
13. `namespace`: mecanismo de isolamento lógico dentro do cluster, separando recursos por equipe ou ambiente.
14. `kubectl get namespaces`: lista namespaces existentes no cluster, incluindo o padrão `default`.
15. `kubectl get pods`: lista todos os pods no namespace atual, mostrando estado e reinícios.
16. `kubectl get pods -A`: lista pods em todos os namespaces simultaneamente.
17. `kubectl get deployments`: lista deployments no namespace atual, mostrando status de réplicas.
18. `kubectl get services`: lista serviços de rede, expondo portas e endereços dentro do cluster.
19. `kubectl get all`: exibe todos os recursos principais do namespace atual em uma única chamada.
20. `kubectl describe recurso nome`: mostra detalhes completos de um recurso, como eventos e condições de pod.

21. `kubectl logs pod`: exibe logs de contêineres em um pod, útil para diagnóstico de falhas.
22. `kubectl logs -f pod`: segue logs em tempo real, similar ao `tail -f` em arquivos.
23. `kubectl exec -it pod -- bash`: abre um terminal interativo dentro do contêiner do pod.
24. `kubectl apply -f arquivo.yaml`: cria ou atualiza recursos conforme definidos em um arquivo YAML.
25. `kubectl create`: comando que cria um recurso novo a partir de YAML ou definição inline.
26. `kubectl delete recurso nome`: remove um recurso do cluster, como pod, deployment ou service.
27. `kubectl delete pod --ignore-not-found`: remove pod sem erro se ele já não existir.
28. `kubectl patch recurso nome --patch '{"chave":"valor"}'`: atualiza parcialmente um recurso sem reescrever o YAML completo.
29. `kubectl edit recurso nome`: abre o recurso em editor de texto para modificação direta.
30. `kubectl rollout status deploy/nome`: mostra o progresso de um rollout de deployment.

31. `deployment`: recurso que declara estado desejado de pods, gerenciando atualizações e rollbacks.
32. `kubectl create deployment nome --image=imagem`: cria um deployment com imagem e réplicas padrões.
33. `kubectl scale deploy/nome --replicas=3`: ajusta número de réplicas de um deployment.
34. `kubectl set image deploy/nome container=imagem:nova-atualizacao`: atualiza imagem de container em deployment.
35. `kubectl rollout undo deploy/nome`: reverte deployment para versão anterior, fazendo rollback.
36. `replicaSet`: controlador que mantém conjunto estável de pods réplicas, geralmente gerenciado por deployment.
37. `pod template`: seção dentro de deployment ou replicaSet que define a configuração do pod a ser criado.
38. `spec`: parte do YAML que define comportamento esperado do recurso, como imagens e portas.
39. `metadata`: seção do YAML que contém nome, labels, namespace e outros metadados do recurso.
40. `labels`: pares chave-valor usados para identificar e agrupar recursos como pods e serviços.

41. `selectors`: filtros baseados em labels usados por serviços e deployments para identificar pods.
42. `service`: recurso que define acesso de rede estável a um conjunto de pods, com IP e porta.
43. `ClusterIP`: tipo de serviço que expõe recurso apenas dentro do cluster, sem acesso externo.
44. `NodePort`: tipo que expõe serviço em porta fixa em cada nó, permitindo acesso externo.
45. `LoadBalancer`: tipo que provisiona balanceador de carga na nuvem, expondo serviço externamente.
46. `kubectl expose deploy/nome --port=80 --type=NodePort`: cria um serviço expondo um deployment.
47. `configmap`: objeto que armazena dados de configuração para serem injetados em pods.
48. `secret`: objeto similar ao ConfigMap, mas para dados sensíveis como senhas e chaves.
49. `kubectl apply -f - <<EOF`: cria recursos a partir de YAML inline usando heredoc.
50. `Boas práticas com k8s`: usar namespaces por ambiente, labels consistentes, deployments com réplicas, health checks (liveness/readiness) e evitar pods standalone fora de controladores.
