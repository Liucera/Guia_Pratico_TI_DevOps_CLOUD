## 8 Docker

1. `docker version`: exibe as versões do cliente e do servidor Docker, verificando se a instalação está funcional.
2. `docker info`: mostra informações detalhadas do daemon, como número de imagens, containers e configurações do host.
3. `docker help`: lista comandos disponíveis e opções de ajuda, servindo como referência rápida no terminal.
4. `docker login`: autentica o usuário em um registro de imagens como Docker Hub, permitindo push e pull privados.
5. `docker logout`: encerra a sessão com o registro, removendo credenciais salvas localmente.
6. `docker search nome`: procura imagens disponíveis em registries públicos com base em um termo, ajudando a encontrar bases prontas.
7. `docker pull imagem:tag`: baixa uma imagem do registro remoto para uso local, com tag específica ou padrão `latest`.
8. `docker images`: lista as imagens armazenadas no host, mostrando repositório, tag, ID e tamanho.
9. `docker rmi imagem`: remove uma imagem local, liberando espaço e evitando acúmulo de versões antigas.
10. `docker image prune -a`: apaga imagens não utilizadas, inclusive as que não têm containers associados, limpando o ambiente.

11. `docker run imagem`: cria e inicia um container a partir de uma imagem, executando o comando padrão configurado.
12. `docker run -it imagem bash`: inicia um container interativo com shell, permitindo executar comandos diretamente dentro dele.
13. `docker ps`: lista containers em execução, mostrando ID, imagem, comandos e portas expostas.
14. `docker ps -a`: lista todos os containers, inclusive parados, facilitando limpeza e inspeção.
15. `docker stop container`: envia sinal para parar um container em execução, permitindo desligamento gracioso.
16. `docker start container`: inicia novamente um container que estava parado sem recriá-lo, aproveitando configuração existente.
17. `docker restart container`: reinicia um container em uma única operação, útil para aplicar mudanças de ambiente.
18. `docker rm container`: remove um container parado do host, liberando recursos associados.
19. `docker container ls`: comando equivalente moderno para listar containers em execução, com sintaxe mais explícita.
20. `docker attach container`: conecta o terminal local ao processo principal do container, permitindo interagir com a execução.

21. `docker exec -it container comando`: executa um comando dentro de um container em execução, frequentemente usado para abrir um shell ou rodar scripts.
22. `docker logs container`: exibe logs do container, ajudando na análise de erros e comportamento da aplicação.
23. `docker logs -f container`: segue os logs em tempo real, semelhante ao `tail -f` em arquivos de log.
24. `docker inspect recurso`: mostra detalhes em formato JSON sobre containers, imagens, volumes ou redes especificados.
25. `docker top container`: lista processos em execução dentro de um container, facilitando diagnóstico de uso de recursos.
26. `docker stats`: exibe uso de CPU, memória e IO de containers em tempo real, funcionando como monitor de recursos.
27. `docker system df`: mostra consumo de espaço por imagens, containers e volumes, indicando onde o ambiente está mais pesado.
28. `docker system prune`: remove recursos não utilizados como containers parados, imagens dangling e redes não usadas.
29. `docker system events`: acompanha eventos do daemon Docker, como criação e remoção de containers, para monitoramento.
30. `docker history imagem`: mostra o histórico de camadas usadas na construção da imagem, facilitando auditoria e otimização.

31. `docker build -t nome:tag .`: constrói uma nova imagem com base em um Dockerfile no diretório atual, aplicando a tag especificada.
32. `Dockerfile`: arquivo de definição de imagem que descreve base, comandos de instalação, cópias de arquivos e instruções de execução.
33. `FROM imagem:tag`: instrução que define a imagem base a partir da qual a nova imagem será construída.
34. `WORKDIR /caminho`: define o diretório de trabalho padrão para as instruções seguintes e para o container em execução.
35. `COPY origem destino`: copia arquivos do contexto de build para dentro da imagem no caminho de destino.
36. `COPY --from=estagio origem destino`: copia arquivos de outro estágio no mesmo Dockerfile, permitindo builds em múltiplos estágios.
37. `RUN comando`: executa comandos durante o build da imagem, como instalação de dependências ou configuração do ambiente.
38. `EXPOSE porta`: documenta a porta em que o container espera receber conexões, ajudando ferramentas e orquestradores.
39. `CMD ["comando","arg"]`: define o comando padrão executado quando o container é iniciado sem comandos adicionais.
40. `ENTRYPOINT ["comando","arg"]`: define o processo principal fixo do container, podendo receber argumentos extras via linha de comando.

41. `docker volume create nome`: cria um volume nomeado para persistir dados fora do ciclo de vida do container.
42. `docker volume ls`: lista todos os volumes existentes no host Docker, permitindo gerenciamento e limpeza.
43. `docker volume rm nome`: remove um volume não utilizado por containers ativos, liberando espaço.
44. `docker volume prune`: apaga volumes órfãos que não estão conectados a containers, reduzindo lixo de dados.
45. `docker network create nome`: cria uma rede Docker personalizada, permitindo comunicação isolada entre containers.
46. `docker network ls`: lista redes definidas no host, incluindo a bridge padrão e redes personalizadas.
47. `docker network inspect nome`: mostra detalhes de configuração e containers conectados a uma rede específica.
48. `docker-compose up`: lê o arquivo `docker-compose.yml` e cria além de iniciar todos os serviços definidos.
49. `docker-compose down`: encerra e remove containers, redes e recursos criados pelo `docker-compose up`.
50. `docker-compose build`: realiza apenas o build das imagens definidas no arquivo de composição, sem iniciar os serviços.
