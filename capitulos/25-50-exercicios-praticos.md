## 25 50 Exercícios Práticos

### 1–10: Terminal Linux e WSL

1. `Navegação e criação de diretórios`: use `cd`, `ls`, `mkdir` para criar estrutura `projeto/{src,docs,tests}` e listar conteúdo recursivamente com `tree`.

2. `Criação e edição de arquivos`: crie `README.md` e `main.py` usando `touch` e `nano`, depois imprima o conteúdo com `cat`.

3. `Busca de arquivos`: use `find . -name "*.py"` para listar todos os arquivos Python no diretório atual e seus subdiretórios.

4. `Contagem de linhas`: use `wc -l` para contar linhas em todos os arquivos `.py` e identifique o maior arquivo.

5. `Redirecionamento e pipes`: use `ls -l | grep "^-" > arquivos.txt` para salvar apenas arquivos regulares em um arquivo de texto.

6. `Compactação`: use `tar -czf backup.tar.gz projeto/` para comprimir um diretório e depois extraia com `tar -xzf`.

7. `Permissões`: use `chmod 755 script.sh` e `chmod 644 arquivo.txt` para ajustar permissões e verifique com `ls -l`.

8. `Execução de scripts`: crie um script `saudacao.sh` que imprime "Olá, mundo!" e execute com `bash saudacao.sh`.

9. `Ambiente WSL`: instale uma distribuição Linux via Microsoft Store, configure usuário e senha, e execute `apt update && apt upgrade`.

10. `Interligação Windows–WSL`: use `\\wsl$` no Explorer para acessar arquivos do Linux a partir do Windows.



### 11–20: Git e GitHub

11. `Inicialização de repositório`: use `git init`, `git add .` e `git commit -m "Initial commit"` para criar primeiro commit.

12. `Clone de repositório`: use `git clone https://github.com/usuario/repo.git` para baixar um projeto remoto.

13. `Branching básico`: crie branch `feature/login` com `git checkout -b`, faça alterações e mescle com `git merge`.

14. `Histórico e diff`: use `git log --oneline --graph` e `git diff HEAD~1` para ver mudanças entre commits.

15. `Rebase interativo`: use `git rebase -i HEAD~3` para reordenar e squash de commits.

16. `Cherry-pick`: use `git cherry-pick abc123` para aplicar um commit específico de outra branch.

17. `stash`: use `git stash` para salvar mudanças temporárias, depois `git stash pop` para restaurar.

18. `.gitignore`: crie um arquivo `.gitignore` ignorando `*.pyc`, `__pycache__`, `.env` e `node_modules/`.

19. `Ação de tag`: use `git tag v1.0.0` e `git push origin v1.0.0` para marcar e empurrar uma versão.

20. `Resolução de conflitos`: provoque conflito em merge e resolva manualmente, depois finalize com `git commit`.



### 21–30: Docker e Containers

21. `Hello World Docker`: execute `docker run hello-world` para confirmar instalação e funcionamento do Docker.

22. `Imagem oficial Python`: use `docker run -it python:3.11-slim bash` para entrar em container interativo com Python.

23. `Dockerfile básico`: crie Dockerfile com `FROM python:3.11-slim`, `COPY . /app` e `CMD ["python", "main.py"]`.

24. `Build de imagem`: use `docker build -t meu-app .` para criar imagem a partir do Dockerfile.

25. `Execução de container`: use `docker run -d -p 8000:8000 meu-app` para rodar em segundo plano com porta mapeada.

26. `Listagem e inspeção`: use `docker ps`, `docker images` e `docker inspect container_id` para ver detalhes.

27. `Logs de container`: use `docker logs container_id` e `docker logs -f container_id` para acompanhar saída.

28. `Entrada interativa`: use `docker exec -it container_id bash` para entrar em container em execução.

29. `Rede Docker`: use `docker network create auth-net` e `docker run --network auth-net` para conectar containers.

30. `Docker Compose`: crie `docker-compose.yml` com serviços `app` e `db`, depois use `docker-compose up -d`.



### 31–40: AWS, Azure, GCP e IaC

31. `AWS: listagem de buckets`: use `aws s3 ls` para listar buckets e `aws s3 mb s3://teste-unico` para criar um.

32. `AWS: upload e download`: use `aws s3 cp arquivo.txt s3://teste-unico/` e depois `aws s3 cp s3://teste-unico/arquivo.txt .`.

33. `AWS: listagem de EC2`: use `aws ec2 describe-instances` e filtre por `--filters Name=instance-state-name,Values=running`.

34. `AWS: criação de instância`: use `aws ec2 run-instances --image-id ami-xxxxxxxx --count 1 --instance-type t2.micro`.

35. `Azure: login e projeto`: use `az login` e `az account set --subscription ID` para definir conta e assinatura.

36. `Azure: criação de VM`: use `az vm create --resource-group rg --name vm --image UbuntuLTS --admin-username user --generate-ssh-keys`.

37. `Azure: listagem de VMs`: use `az vm list -d -o table` para ver VMs com IP e status.

38. `GCP: autenticação e projeto`: use `gcloud auth login` e `gcloud config set project ID_projeto`.

39. `GCP: criação de VM`: use `gcloud compute instances create vm --image=ubuntu --machine-type=e2-micro`.

40. `Terraform init/plan/apply`: use `terraform init`, `terraform plan` e `terraform apply` para criar infraestrutura AWS simples (bucket S3).



### 41–50: Kubernetes, Cloud e Integrações



41. `kubectl config`: use `kubectl config current-context` e `kubectl config use-context minikube` para trocar de contexto.
42. `Listagem de pods`: use `kubectl get pods`, `kubectl get pods -A` para ver pods em todos os namespaces.
43. `Criação de deployment`: use `kubectl create deployment nginx --image=nginx` e `kubectl get deployments`.
44. `Escala de deployment`: use `kubectl scale deployment nginx --replicas=3` e confirme com `kubectl get pods`.
45. `Service tipo NodePort`: use `kubectl expose deploy/nginx --port=80 --type=NodePort` e verifique com `kubectl get svc`.
46. `Logs e exec`: use `kubectl logs deploy/nginx` e `kubectl exec -it deploy/nginx -- bash`.
47. `Conceito de zona e região`: ligue na console da AWS/Azure/GCP e compare como zonas e regiões aparecem em diferentes provedores.
48. `Auto scaling`: configure um auto scaling group ou scale set para VMs e observe ajuste automático sob carga simulada.
49. `CI/CD básico`: crie um pipeline simples que, ao fazer push no GitHub, roda testes e faz deploy em um container ou VM.
50. `Projeto final integrado`: crie um repositório com app Python, Dockerfile, docker-compose, Terraform para infraestrutura e um pipeline CI/CD que executa testes, constrói imagem e deploy em cluster Kubernetes.







**Autor**:  Liucera

**Versão**:   Edição 2026 · v1.0
