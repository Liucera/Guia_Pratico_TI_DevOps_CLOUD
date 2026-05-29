## 10 Linux - Comandos Essenciais

1. `pwd`: exibe o caminho completo do diretório atual, ajudando a saber exatamente onde você está no sistema de arquivos.
2. `ls`: lista arquivos e pastas do diretório atual, mostrando o conteúdo básico da pasta em que você está.
3. `ls -l`: exibe a lista de arquivos em formato longo, incluindo permissões, proprietário, tamanho e data de modificação.
4. `ls -a`: mostra todos os arquivos, incluindo arquivos ocultos que começam com ponto, como `.git`.
5. `cd pasta`: muda para o diretório indicado, permitindo navegar pela estrutura de pastas.
6. `cd ..`: retorna ao diretório pai, subindo um nível na hierarquia de diretórios.
7. `cd ~`: vai direto para o diretório home do usuário, servindo como atalho para o ponto de partida pessoal.
8. `mkdir nome`: cria um novo diretório com o nome especificado, organizando arquivos em pastas.
9. `rmdir nome`: remove um diretório vazio, usado para apagar pastas que não contêm arquivos.
10. `rm arquivo`: apaga um arquivo simples, removendo-o do sistema de arquivos.

11. `rm -r pasta`: remove um diretório e todo o seu conteúdo recursivamente, devendo ser usado com cuidado.
12. `cp origem destino`: copia arquivos de um local para outro, preservando o original.
13. `cp -r pasta destino`: copia diretórios inteiros com seu conteúdo, inclusive subpastas.
14. `mv origem destino`: move arquivos ou diretórios para outro local ou renomeia quando destino é apenas um novo nome.
15. `touch arquivo`: cria um arquivo vazio ou atualiza a data de modificação de um arquivo existente.
16. `cat arquivo`: exibe o conteúdo de um arquivo de texto diretamente no terminal, útil para arquivos pequenos.
17. `less arquivo`: abre o arquivo em um visualizador paginado, permitindo rolar para cima e para baixo confortavelmente.
18. `head arquivo`: mostra as primeiras linhas de um arquivo, por padrão as dez primeiras.
19. `tail arquivo`: exibe as últimas linhas de um arquivo, geralmente usado para acompanhar logs.
20. `tail -f arquivo`: segue o crescimento do arquivo em tempo real, ideal para monitorar logs de serviços.

21. `echo texto`: imprime uma linha de texto na saída padrão, frequentemente usado em scripts para mensagens simples.
22. `grep padrão arquivo`: procura linhas que contenham o padrão dentro do arquivo, retornando apenas as correspondências.
23. `grep -r padrão pasta`: busca recursivamente por um padrão em todos os arquivos de uma pasta e subpastas.
24. `find caminho -name "padrão"`: localiza arquivos e diretórios por nome a partir de um caminho inicial.
25. `history`: lista os comandos executados recentemente no shell, permitindo reaproveitar ou revisar ações.
26. `clear`: limpa o conteúdo visível do terminal, deixando a tela pronta para novos comandos.
27. `man comando`: exibe o manual completo de um comando, descrevendo opções, uso e exemplos.
28. `which comando`: mostra o caminho do executável usado quando o comando é chamado, útil para saber qual versão está sendo usada.
29. `alias nome="comando"`: cria um atalho para um comando ou conjunto de opções, personalizando o ambiente de terminal.
30. `unalias nome`: remove um alias previamente criado, restaurando o comportamento original do comando.

31. `chmod modo arquivo`: altera permissões de leitura, escrita e execução de um arquivo ou diretório.
32. `chown usuario:grupo arquivo`: muda o proprietário e o grupo de um arquivo, controlando quem pode acessá-lo.
33. `sudo comando`: executa o comando com privilégios elevados, normalmente de superusuário, exigindo autenticação.
34. `ps aux`: lista todos os processos em execução, com informações detalhadas de consumo e dono.
35. `top`: mostra em tempo real os processos mais ativos, consumo de CPU e memória, funcionando como monitor do sistema.
36. `htop`: versão interativa do top, quando instalada, permitindo filtrar e encerrar processos com interface colorida.
37. `kill pid`: envia um sinal para encerrar o processo identificado pelo número de PID.
38. `df -h`: exibe o uso de espaço em disco de forma legível, mostrando partições e porcentagem utilizada.
39. `free -h`: apresenta o uso de memória RAM e swap em formato amigável, indicando quanto está livre ou usado.
40. `uptime`: mostra há quanto tempo o sistema está ligado e a carga média nos últimos minutos.

41. `ping host`: testa a conectividade de rede com um host, medindo tempo de resposta e perdas de pacote.
42. `curl url`: realiza uma requisição HTTP simples, exibindo a resposta no terminal, útil para testar APIs e sites.
43. `wget url`: baixa arquivos da internet diretamente para o diretório atual usando HTTP, HTTPS ou FTP.
44. `ifconfig` ou `ip addr`: exibe configurações de interface de rede, como endereços IP e status de conexões.
45. `ssh usuario@servidor`: conecta-se a um servidor remoto via protocolo SSH, abrindo um terminal seguro.
46. `scp origem destino`: copia arquivos de forma segura entre máquinas usando SSH como transporte.
47. `tar -czf arquivo.tar.gz pasta`: compacta uma pasta em um arquivo tar.gz, combinando empacotamento e compressão.
48. `tar -xzf arquivo.tar.gz`: descompacta um arquivo tar.gz, restaurando os arquivos e pastas contidos.
49. `apt update`: em distribuições baseadas em Debian ou Ubuntu, atualiza a lista de pacotes disponíveis no repositório.
50. `apt upgrade`: instala as versões mais recentes dos pacotes já instalados, mantendo o sistema atualizado.
