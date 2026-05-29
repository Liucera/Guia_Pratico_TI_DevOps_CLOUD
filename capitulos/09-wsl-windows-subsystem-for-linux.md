## 9 WSL - Windows Subsystem for Linux

1. `WSL`: sigla para Windows Subsystem for Linux, recurso que permite rodar distribuições Linux diretamente dentro do Windows via terminal.
2. `wsl`: comando básico que inicia a distribuição Linux padrão configurada no sistema, abrindo um shell no ambiente WSL.
3. `wsl.exe`: forma explícita do mesmo comando usada em scripts ou quando se deseja garantir que o executável do sistema seja chamado.
4. `wsl --install`: instala automaticamente o WSL e uma distribuição Linux padrão, simplificando a configuração inicial no Windows moderno.
5. `wsl --install -d NomeDistribuicao`: instala uma distribuição específica como Ubuntu ou Debian, permitindo escolher o ambiente Linux desejado.
6. `wsl --list --online`: lista as distribuições disponíveis para instalação, mostrando nomes que podem ser usados com `--install`.
7. `wsl --list --verbose`: exibe as distribuições instaladas localmente com informações de estado e versão de WSL usada.
8. `wsl --set-default NomeDistribuicao`: define qual distribuição será aberta ao executar apenas `wsl` sem parâmetros.
9. `wsl --set-version NomeDistribuicao 2`: altera a distribuição informada para rodar em WSL 2, melhorando compatibilidade e desempenho.
10. `wsl --set-default-version 2`: define WSL 2 como versão padrão para novas distribuições instaladas no futuro.

11. `wsl --status`: mostra o estado geral do WSL, incluindo versão padrão e se os recursos necessários estão habilitados.
12. `wsl --shutdown`: encerra todas as instâncias WSL ativas, liberando memória e aplicando alterações de configuração.
13. `wsl --terminate NomeDistribuicao`: encerra apenas a instância da distribuição especificada, útil para reiniciar um ambiente isolado.
14. `wsl --export NomeDistribuicao arquivo.tar`: exporta o sistema de arquivos da distribuição para um arquivo, permitindo backup ou migração.
15. `wsl --import NomeDistribuicao pasta arquivo.tar`: cria nova distribuição a partir de um arquivo exportado e de um diretório de destino.
16. `wsl --unregister NomeDistribuicao`: remove completamente a distribuição informada, apagando o sistema de arquivos e configurações.
17. `wsl --help`: lista todas as opções disponíveis do comando WSL, servindo como referência rápida em linha de comando.
18. `wsl --mount disco`: monta um disco físico ou partição no WSL, permitindo acessar sistemas de arquivos adicionais.
19. `wsl --unmount disco`: desmonta um disco previamente montado, garantindo que o sistema de arquivos seja fechado corretamente.
20. `wslconfig`: utilitário legado para gerenciar distribuições WSL em versões mais antigas do Windows, ainda útil em alguns cenários.

21. `.wslconfig`: arquivo de configuração no diretório do usuário Windows que ajusta parâmetros globais do WSL 2, como memória e uso de processador.
22. `[wsl2]`: seção do `.wslconfig` onde são definidas opções específicas para máquinas virtuais WSL 2, como limites de recursos.
23. `memory=4GB`: configuração possível em `.wslconfig` que limita a memória máxima utilizada pelo WSL 2.
24. `processors=4`: parâmetro que define quantos núcleos de CPU o WSL 2 pode usar, controlando impacto no sistema.
25. `cd ~` dentro do WSL: comando que leva ao diretório home do usuário Linux, base do ambiente dentro da distribuição.
26. `explorer.exe .`: abre o diretório atual do WSL no Explorador de Arquivos do Windows, facilitando trabalho misto com arquivos.
27. `code .`: quando o VS Code está instalado, abre o diretório atual do WSL no editor, integrando desenvolvimento Linux com IDE no Windows.
28. `wslpath`: comando que converte caminhos entre formatos Windows e Unix, ajudando a interoperar scripts dos dois ambientes.
29. `/mnt/c`: ponto de montagem padrão onde o WSL expõe a unidade C: do Windows, permitindo acesso aos arquivos do sistema hospedeiro.
30. `\\wsl$`: caminho de rede que permite acessar o sistema de arquivos das distribuições WSL a partir de aplicativos Windows.

31. `sudo apt update`: comando típico dentro do WSL baseado em Debian/Ubuntu para atualizar a lista de pacotes disponíveis.
32. `sudo apt upgrade`: instala atualizações dos pacotes já instalados na distribuição WSL, mantendo o ambiente Linux em dia.
33. `sudo apt install pacote`: instala um novo pacote de software dentro da distro, por exemplo compiladores, linguagens ou ferramentas de rede.
34. `uname -a`: exibe informações sobre o kernel Linux em execução dentro do WSL, ajudando a verificar versão e arquitetura.
35. `lsb_release -a`: mostra detalhes da distribuição Linux como nome, versão e codinome.
36. `wsl --set-default NomeDistro`: reforça o conceito de definir distribuição padrão, importante quando múltiplas distros coexistem.
37. `hostname -I`: lista endereços IP da instância WSL, útil para expor serviços para o Windows ou outras máquinas na rede.
38. `ping`: teste básico de conectividade disponível dentro da distro WSL, verificando acesso a hosts internos e externos.
39. `curl`: ferramenta de linha de comando frequentemente usada no WSL para testar APIs e downloads via HTTP.
40. `ssh usuario@servidor`: comando usado no WSL para conectar-se a servidores Linux remotos, aproveitando o ambiente Unix completo.

41. `PowerShell como administrador`: requisito comum para executar comandos de instalação e ativação do WSL e recursos de virtualização.
42. `dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart`: comando usado para habilitar o recurso WSL em versões mais antigas do Windows.
43. `dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart`: ativa a plataforma de máquina virtual necessária para WSL 2.
44. `wsl --update`: atualiza componentes do WSL, incluindo o kernel Linux, garantindo correções e melhorias de desempenho.
45. `wsl --version`: exibe informações sobre a versão do WSL instalada, incluindo kernel e detalhes do sistema.
46. `wsl --help --advanced`: opção usada para exibir parâmetros adicionais de linha de comando, incluindo recursos mais avançados.
47. `configurações de proxy no WSL`: ajuste necessário em algumas redes corporativas para permitir que o WSL acesse a internet por meio de variáveis de ambiente.
48. `integração com Docker`: cenário em que o Docker Desktop usa o WSL 2 como backend, permitindo containers Linux com melhor desempenho.
49. `VS Code Remote - WSL`: extensão do VS Code que permite abrir diretórios e depurar código diretamente dentro da distribuição WSL.
50. `instalar Ubuntu pelo Microsoft Store`: alternativa gráfica para adicionar distribuições WSL, oferecendo instalação facilitada para usuários menos experientes.
