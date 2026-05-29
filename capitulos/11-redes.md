## 11 Redes

1. `endereço IP`: identificador numérico de um host em uma rede, usado para rotear pacotes entre origem e destino.
2. `máscara de rede`: valor que define qual parte do endereço IP representa a rede e qual representa os hosts, determinando o tamanho da sub-rede.
3. `gateway padrão`: endereço do roteador que encaminha tráfego para fora da rede local, sendo o salto de saída padrão.
4. `servidor DNS`: serviço que converte nomes de domínio em endereços IP, permitindo acessar hosts por nomes legíveis.
5. `porta`: número que identifica serviços específicos em um host, permitindo que vários aplicativos usem o mesmo IP sem conflito.
6. `protocolo TCP`: protocolo orientado a conexão que garante entrega confiável e ordenada de dados entre hosts.
7. `protocolo UDP`: protocolo sem conexão, usado para transmissões rápidas em que alguma perda de pacotes é aceitável, como streaming.
8. `localhost`: endereço que aponta para a própria máquina, geralmente associado ao IP 127.0.0.1 em IPv4.
9. `sub-rede`: divisão lógica de uma rede maior em blocos menores, usada para organização e controle de tráfego.
10. `latência`: tempo que um pacote leva para ir de um ponto a outro, medido em milissegundos e relevante para desempenho de rede.

11. `ping host`: envia pacotes ICMP para testar conectividade e medir tempo de resposta entre a máquina local e outro host.
12. `ping -c 4 host`: envia um número específico de pacotes ICMP, encerrando o comando após esse total.
13. `ping 8.8.8.8`: teste comum de conectividade com um servidor DNS público, útil para verificar acesso à internet.
14. `traceroute host`: mostra o caminho percorrido pelos pacotes até o destino, listando cada salto intermediário na rota.
15. `mtr host`: ferramenta que combina funções de `ping` e `traceroute`, apresentando estatísticas contínuas de perda e latência por salto.
16. `pathping host`: comando similar no ecossistema Windows que une análises de ping e rota em um único relatório.
17. `ip addr`: comando moderno que exibe endereços IP e detalhes das interfaces de rede na máquina.[web:115]
18. `ip link`: lista interfaces de rede e seus estados, permitindo ver se estão ativas ou inativas.
19. `ip route`: mostra a tabela de rotas usada pelo kernel para encaminhar pacotes entre redes.
20. `ip neigh`: exibe a tabela ARP, associando IPs a endereços MAC de dispositivos vizinhos na rede local.

21. `ifconfig`: comando tradicional para exibir e configurar interfaces de rede, ainda presente em muitas distribuições.
22. `ifconfig eth0 up`: ativa uma interface de rede específica, permitindo que ela passe a enviar e receber pacotes.
23. `ifconfig eth0 down`: desativa a interface, interrompendo temporariamente sua participação na rede.
24. `nslookup dominio`: consulta servidores DNS para obter o endereço IP associado a um domínio ou verificar registros.
25. `dig dominio`: ferramenta avançada de consulta DNS que permite analisar registros detalhados, como A, MX ou TXT.
26. `host dominio`: utilitário simples para resolver nomes de domínio e exibir IPs correspondentes.
27. `whois dominio`: consulta informações de registro de domínio, como responsável, datas e servidores associados.
28. `telnet host porta`: tenta abrir uma conexão simples em uma porta TCP específica, verificando se o serviço está acessível.
29. `nc host porta`: usa netcat para testar conexões TCP ou UDP, enviar dados e diagnosticar serviços de rede.
30. `curl http://host`: realiza uma requisição HTTP e mostra a resposta, permitindo testar APIs e servidores web.

31. `netstat -tulpn`: lista conexões de rede e portas em escuta, indicando quais processos estão ouvindo em cada porta.
32. `ss -tulpn`: substituto moderno do `netstat`, mais rápido e rico em detalhes para conexões e sockets.
33. `route -n`: exibe a tabela de roteamento em formato numérico, detalhando gateways, máscaras e interfaces.
34. `arp -a`: mostra as entradas da tabela ARP, correlacionando IPs locais a endereços MAC associados.
35. `tcpdump`: captura pacotes de rede em tempo real, permitindo análise profunda de tráfego em nível de pacote.
36. `tcpdump -i eth0`: inicia captura na interface `eth0`, filtrando pacotes desse link específico.
37. `nmap host`: escaneia portas de um host para descobrir quais serviços estão disponíveis e acessíveis.
38. `nmap -sV host`: além de listar portas abertas, tenta identificar a versão dos serviços em execução.
39. `ethtool interface`: exibe e altera configurações de interfaces Ethernet, como velocidade e modo duplex.
40. `iwconfig`: mostra e ajusta parâmetros de interfaces sem fio, como SSID e modo de operação.

41. `hostname`: exibe ou configura o nome da máquina, usado para identificação na rede.
42. `hostname -I`: lista os endereços IP atribuídos às interfaces da máquina.
43. `nmcli`: ferramenta de linha de comando para gerenciar conexões de rede via NetworkManager.
44. `systemctl restart network` ou serviço equivalente: reinicia serviços de rede, aplicando mudanças de configuração.
45. `resolv.conf`: arquivo de configuração que define servidores DNS usados pelo sistema para resolver nomes.
46. `hosts`: arquivo local que mapeia nomes de host para endereços IP, permitindo overrides de DNS.
47. `firewall`: conceito de filtro de tráfego que permite ou bloqueia pacotes com base em regras definidas.
48. `ufw`: utilitário simples de firewall em distribuições baseadas em Ubuntu para criar regras de entrada e saída.
49. `iptables`: ferramenta mais granular de firewall e NAT, operando em baixo nível sobre tabelas de filtragem de pacotes.
50. `VPN`: rede privada virtual que cria túnel criptografado sobre a internet, permitindo acesso seguro a redes remotas como se fosse local.
