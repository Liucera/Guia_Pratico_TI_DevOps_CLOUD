## 7 Git e GitHub

1. `git init`: cria um novo repositório Git no diretório atual, iniciando o controle de versão do projeto.
2. `git status`: mostra o estado atual do repositório, listando arquivos modificados, não rastreados e prontos para commit.
3. `git add arquivo`: adiciona um arquivo específico à área de stage, preparando-o para ser incluído no próximo commit.
4. `git add .`: adiciona todas as modificações e novos arquivos da pasta atual e subpastas à área de stage.
5. `git commit -m "mensagem"`: registra um snapshot das alterações no histórico com uma mensagem descritiva.
6. `git log`: exibe o histórico de commits, incluindo autor, data e mensagens, permitindo auditar a evolução do projeto.
7. `git diff`: mostra as diferenças entre o estado atual dos arquivos e a última versão commitada, útil para revisão antes do commit.
8. `git diff --staged`: compara o que está na área de stage com o último commit, mostrando exatamente o que será incluído no próximo snapshot.
9. `git config --global user.name "Nome"`: define o nome do autor usado em novos commits em todos os repositórios da máquina.
10. `git config --global user.email "email"`: configura o e-mail associado aos commits, usado para identificação no GitHub e outras plataformas.

11. `git clone url`: copia um repositório remoto inteiro para a máquina local, incluindo histórico e configurações.
12. `git remote -v`: lista os repositórios remotos configurados, mostrando URLs para fetch e push.
13. `git remote add origin url`: adiciona um remoto chamado `origin`, normalmente apontando para um repositório no GitHub.
14. `git push -u origin main`: envia a branch `main` local para o remoto e define a relação de acompanhamento para futuros pushes.
15. `git push`: envia commits locais da branch atual para o repositório remoto configurado, atualizando o histórico compartilhado.
16. `git pull`: baixa alterações do repositório remoto e integra com a branch atual, combinando `fetch` e `merge`.
17. `git fetch`: busca novas referências e commits do remoto sem mesclar automaticamente, permitindo revisar antes de integrar.
18. `git push origin nome-branch`: envia uma branch específica para o remoto, compartilhando trabalho em andamento com a equipe.
19. `git remote remove origin`: remove a configuração do remoto `origin`, útil ao trocar URLs ou repositórios.
20. `git remote set-url origin nova-url`: atualiza a URL do remoto sem perder o histórico de commits ou branches.

21. `git branch`: lista branches locais e indica qual está ativa, ajudando a visualizar o fluxo de desenvolvimento.
22. `git branch nome-branch`: cria uma nova branch baseada na posição atual, normalmente usada para desenvolver novas features isoladas.
23. `git checkout nome-branch`: muda a branch ativa, atualizando a árvore de arquivos para a versão correspondente.
24. `git switch nome-branch`: comando moderno para trocar de branch, oferecendo interface mais clara que `checkout` para este uso.
25. `git checkout -b nova-branch`: cria uma nova branch e muda para ela em um único passo.
26. `git branch -d nome-branch`: apaga uma branch local já integrada, mantendo o histórico preservado em outras branches.
27. `git merge nome-branch`: junta o histórico de outra branch na branch atual, criando um commit de merge se necessário.
28. `git rebase nome-branch`: reaplica commits da branch atual sobre outra, produzindo um histórico linear e mais limpo.
29. `git stash`: guarda temporariamente alterações não commitadas em uma pilha, limpando a árvore de trabalho sem perder progresso.
30. `git stash pop`: recupera as alterações salvas no stash e remove o registro da pilha, retomando o trabalho interrompido.

31. `git reset --soft HEAD~1`: desfaz o último commit mantendo as alterações na área de stage, permitindo ajustar mensagem ou incluir mais arquivos.
32. `git reset --mixed HEAD~1`: desfaz o último commit e remove os arquivos da área de stage, preservando mudanças no diretório de trabalho.
33. `git reset --hard HEAD~1`: desfaz o último commit e descarta completamente as alterações, voltando o código ao estado anterior.
34. `git revert hash`: cria um novo commit que desfaz as alterações do commit informado, preservando o histórico sem sobrescrever.
35. `git log --oneline --graph --all`: mostra o histórico de forma compacta e em gráfico, visualizando branches e merges.
36. `git show hash`: exibe detalhes de um commit específico, incluindo diffs e metadados.
37. `git blame arquivo`: lista, linha a linha, qual commit alterou cada parte do arquivo, útil para rastreio de bugs.
38. `git tag nome`: cria uma tag leve apontando para o commit atual, usada para marcar versões importantes.
39. `git tag -a v1.0 -m "versão 1.0"`: cria uma tag anotada com mensagem, autor e data, ideal para releases.
40. `git push origin --tags`: envia tags locais para o repositório remoto, sincronizando marcações de versão com a equipe.

41. `fork` (no GitHub): cria uma cópia de um repositório na conta do usuário, permitindo experimentar e contribuir sem alterar o original.
42. `pull request`: proposta de mudança enviada a um repositório remoto para revisão e merge, central no fluxo colaborativo do GitHub.
43. `git fork-flow`: prática onde contribuições para projetos open source são feitas via fork e pull request, sem acesso direto de escrita.
44. `git flow`: modelo de branches com `develop`, `feature`, `release` e `hotfix`, usado em projetos com ciclos formais de release.
45. `GitHub Actions`: sistema de automação que executa workflows como testes e deploys quando há push ou pull request.
46. `.github/workflows/arquivo.yml`: diretório e arquivo onde são definidos fluxos de trabalho automatizados no GitHub.
47. `gitignore`: arquivo que lista padrões de arquivos a serem ignorados pelo Git, evitando que artefatos de build entrem no repositório.
48. `README.md`: arquivo de documentação principal de um repositório GitHub, descrevendo projeto, instalação e uso.
49. `git submodule`: recurso para incluir outro repositório Git como subdiretório, permitindo compartilhar componentes entre projetos.
50. `HEAD`: ponteiro simbólico que indica o commit atual e normalmente aponta para a ponta da branch ativa, base para muitas operações.
