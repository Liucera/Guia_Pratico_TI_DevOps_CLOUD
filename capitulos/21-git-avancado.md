## 21 Git Avançado

1. `git reflog`: exibe o histórico de todas as atualizações do HEAD local, permitindo recuperar commits perdidos ou redefinir para estados anteriores.
2. `git reflog show branch`: mostra o histórico de updates para uma branch específica, útil para rastrear rewrites de histórico.
3. `git reset --soft HEAD@{1}`: redefine HEAD para um estado anterior do reflog, mantendo alterações na área de stage, ideal para reorganizar commits.
4. `git reset --mixed HEAD@{5}`: volta ao estado há 5 registros no reflog, removendo alterações da área de stage mas preservando no diretório.
5. `git reset --hard HEAD@{2}`: restaura o repositório ao estado exato de 2 registros atrás no reflog, descartando todas as mudanças locais.
6. `git rebase -i HEAD~n`: inicia rebase interativo nos últimos `n` commits, permitindo reordenar, editar, esbagar ou apagar commits.
7. `pick`: instrução em rebase interativo que mantém o commit como está, sem alterações.
8. `reword`: instrução que mantém o commit mas permite editar a mensagem.
9. `edit`: instrução que pausa o rebase no commit indicado, permitindo ajustes antes de continuar com `git rebase --continue`.
10. `squash`: instrução que mescla o commit atual com o anterior, unindo mensagens e conteúdo.

11. `fixup`: instrução que une o commit ao anterior, mantendo apenas a mensagem do primeiro.
12. `drop`: instrução que remove o commit completamente do histórico durante o rebase.
13. `git rebase --continue`: continua um rebase após resolver conflitos ou editar commits.
14. `git rebase --abort`: cancela o rebase atual, voltando ao estado antes de iniciar.
15. `git rebase --skip`: pula o commit atual em rebase interativo e continua com os próximos.
16. `git cherry-pick commit`: aplica as mudanças de um commit específico em cima da branch atual.
17. `git cherry-pick -n commit`: aplica mudanças sem criar commit automático, permitindo editar antes de confirmar.
18. `git cherry-pick A..B`: aplica todos os commits no intervalo entre A e B na branch atual.
19. `git bisect`: inicia processo de busca binária para encontrar commit que introduziu um bug.
20. `git bisect start`: marca o início de uma sessão de bisect, sem aplicação de filtro ainda.

21. `git bisect good`: marca o commit atual como "bom", sem defeito, restringindo a busca para commits anteriores.
22. `git bisect bad`: marca o commit atual como "ruim", com defeito, definindo a ponta alta do intervalo de busca.
23. `git bisect reset`: encerra sessão de bisect, retornando à branch e estado anterior.
24. `git bisect skip`: ignora o commit atual no processo de bisect, útil quando não é possível testá-lo.
25. `git bisect log`: exibe o histórico de marcações de bisect, permitindo recriar a sessão em outro lugar.
26. `git worktree add pasta branch`: cria um novo diretório de trabalho associado a uma branch, permitindo trabalhar em várias branches simultaneamente.
27. `git worktree list`: exibe todos os worktrees ativos e suas branches associadas.
28. `git worktree remove pasta`: remove um worktree existente, limpando o diretório de trabalho.
29. `git worktree prune`: remove registros de worktrees já inexistentes do repositório.
30. `git worktree add -b nova-branch pasta`: cria e adiciona um worktree com nova branch a partir do HEAD atual.

31. `git hook`: script executado automaticamente em eventos como commit, merge ou push, no cliente ou servidor.
32. `pre-commit`: hook executado antes de criar um commit, útil para linting e testes rápidos.
33. `commit-msg`: hook que valida a mensagem do commit, podendo rejeitar formatos incorretos.
34. `post-commit`: hook executado após o commit ser criado, usado para notificações ou gatilhos externos.
35. `pre-push`: hook executado antes de enviar commits para o remoto, permitindo testes antes de compartilhar.
36. `.git/hooks`: diretório que contém hooks locais, desativados por padrão, precisam ser nomeados sem extensão e executáveis.
37. `git blame arquivo`: mostra quem modificou cada linha de um arquivo e em qual commit, útil para rastrear origem de bugs.
38. `git blame -L 10,20 arquivo`: limita o blame a linhas 10 a 20 do arquivo.
39. `git blame --reverse`: mostra quem introduziu o que em ordem inversa, útil para entender evolução de código.
40. `git shortlog`: resume commits por autor, mostrando quantos commits cada pessoa fez.

41. `git shortlog -sn`: exibe autores ordenados por número de commits,`-n` por quantidade e `-s` resumido.
42. `git log --all --graph --decorate --oneline`: mostra histórico completo de todas as branches em forma de gráfico.
43. `git log --grep="texto"`: busca commits cuja mensagem contenha o texto especificado.
44. `git log --author="nome"`: filtra commits por autor, mostrando apenasmodificações de determinada pessoa.
45. `git log --since="2024-01-01" --until="2024-12-31"`: restringe log a um intervalo de datas, útil para auditoria.
46. `git log -p`: exibe diffs de cada commit durante o log, mostrando mudanças de conteúdo.
47. `git log --stat`: mostra estatísticas de arquivos alterados por commit, sem diffs completos.
48. `git log --oneline --graph --all --decorate --source`: combinação para visualizar histórico completo, com branches e fontes.
49. `git replace`: cria substituições temporárias de objetos, permitindo corrigir commits sem reescrever histórico permanentemente.
50. `Fluxos avançados de Git`: práticas como Git Flow, trunk-based development, rebase contínuo, pull requests com squash e uso de tags semânticas para releases.
