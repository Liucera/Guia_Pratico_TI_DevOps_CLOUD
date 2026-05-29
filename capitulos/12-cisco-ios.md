## 12 Cisco IOS

1. `Router>`: prompt do modo EXEC usuário, nível inicial de acesso em que apenas comandos básicos de monitoramento podem ser executados.
2. `enable`: comando que eleva o usuário para o modo EXEC privilegiado, permitindo acesso a configurações sensíveis.
3. `Router#`: prompt do modo EXEC privilegiado, de onde é possível executar comandos avançados e entrar na configuração global.
4. `configure terminal`: entra no modo de configuração global, permitindo alterar parâmetros permanentes do roteador ou switch.
5. `Router(config)#`: prompt que indica que o equipamento está no modo de configuração global.
6. `enable password senha`: configura senha simples para o comando `enable`, protegendo o acesso ao modo privilegiado.
7. `enable secret senha`: define senha criptografada para o modo privilegiado, considerada prática mais segura que `enable password`.
8. `line console 0`: entra na configuração da linha console física, por onde o equipamento costuma ser acessado localmente.
9. `password senha`: dentro da linha console, define a senha que será solicitada ao conectar fisicamente ao equipamento.
10. `login`: ativa a obrigatoriedade de senha na linha em configuração, garantindo que o usuário seja autenticado.

11. `hostname NOME`: altera o nome exibido no prompt do equipamento, facilitando a identificação em ambientes com vários dispositivos.
12. `no ip domain-lookup`: desativa a tentativa de resolver nomes digitados incorretos como se fossem domínios, evitando atrasos no terminal.
13. `clock set HH:MM:SS DIA MES ANO`: ajusta a data e a hora do equipamento, importante para logs e sincronização.
14. `service password-encryption`: aplica criptografia básica às senhas armazenadas na configuração, evitando visualização direta.
15. `banner motd #texto#`: define uma mensagem de dia (Message of the Day) exibida no login, geralmente com avisos legais.
16. `logging synchronous`: ajusta a linha de console ou VTY para que mensagens de log não interrompam a digitação de comandos.
17. `history size 20`: configura o tamanho do histórico de comandos armazenado para a sessão atual.
18. `terminal length 0`: desabilita a paginação de saída, fazendo com que comandos longos sejam exibidos de uma vez só.
19. `show history`: exibe os últimos comandos digitados na sessão, auxiliando na revisão de operações recentes.
20. `?`: mostra ajuda contextual com a lista de comandos válidos naquele modo ou após o texto já digitado.

21. `show running-config`: exibe a configuração em execução na memória RAM, refletindo o estado atual do equipamento.
22. `show startup-config`: mostra a configuração armazenada na NVRAM, que será aplicada na próxima inicialização. [web:124]
23. `copy running-config startup-config`: salva a configuração atual na NVRAM, garantindo que as mudanças sejam mantidas após reiniciar.
24. `copy run start`: forma abreviada muito usada do comando de salvamento de configuração em execução.
25. `reload`: reinicia o equipamento, recarregando a configuração de inicialização.
26. `write erase` ou `erase startup-config`: limpa a configuração salva, retornando o equipamento ao estado de fábrica lógico.
27. `show version`: exibe informações sobre a versão do IOS, tempo de funcionamento e detalhes de hardware.
28. `show ip interface brief`: mostra um resumo das interfaces IP com endereços e estados, útil para diagnóstico rápido.
29. `show interfaces`: apresenta detalhes completos de cada interface, incluindo estatísticas de erros e estado operacional.
30. `show arp`: exibe a tabela ARP, associando endereços IP a MACs conhecidos pelo roteador.

31. `interface GigabitEthernet0/0`: entra na configuração de uma interface física específica, como porta Ethernet do roteador.
32. `description texto`: configura uma descrição para a interface, documentando propósito ou conexão ligada.
33. `ip address IP mascara`: atribui um endereço IPv4 e máscara à interface, tornando-a parte de uma rede.
34. `no shutdown`: liga a interface, mudando o estado de administrativamente down para ativo.
35. `shutdown`: desativa administrativamente a interface, interrompendo tráfego naquela porta.
36. `interface VLAN1` ou outra VLAN: entra na interface lógica associada a uma VLAN, usada para gerenciamento ou inter-VLAN.
37. `switchport mode access`: configura a porta de switch para atuar como access, pertencendo a uma única VLAN.
38. `switchport access vlan 10`: coloca a porta como membro da VLAN especificada, segmentando a rede em domínio de broadcast.
39. `switchport mode trunk`: define a interface como tronco, transportando múltiplas VLANs pela mesma conexão.
40. `switchport trunk allowed vlan 10,20`: limita quais VLANs podem trafegar em uma porta trunk, reforçando segmentação.

41. `vlan 10`: entra na configuração de uma VLAN específica, permitindo nomear e ativar essa VLAN no switch.
42. `name VENDAS`: atribui um nome amigável à VLAN atual, facilitando identificação em grandes ambientes.
43. `show vlan brief`: exibe um resumo das VLANs configuradas e as portas associadas a cada uma.
44. `show interfaces status`: mostra status operacional das portas, incluindo VLAN associada e velocidade.
45. `ip route rede mascara next-hop`: adiciona rota estática para uma rede, definindo o próximo salto ou interface de saída.
46. `show ip route`: exibe a tabela de roteamento IPv4, incluindo rotas conectadas, estáticas e aprendidas por protocolos dinâmicos.
47. `access-list número regra`: cria listas de controle de acesso numeradas para filtrar tráfego com base em IPs e portas.
48. `ip access-group número in`: aplica uma ACL a uma interface na direção de entrada, filtrando pacotes recebidos.
49. `no access-list número`: remove uma lista de acesso, retirando suas regras de filtragem.
50. `exit` e `end`: comandos que retornam a níveis superiores de configuração ou direto ao modo EXEC privilegiado, finalizando seções de configuração.
