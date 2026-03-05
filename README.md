# Apresentação dos conceitos envolvidos com a subcamada MAC (Medium Access Control)

## Objetivos da Aula

Ao final desta prática/teórica, vocês deverão ser capazes de:

* Identificar o endereço MAC de diferentes interfaces de rede;
* Compreender a relação entre endereços IP e endereços MAC;
* Utilizar comandos de rede para visualizar tabelas ARP;
* Analisar dispositivos conectados a um roteador utilizando o MAC Address.
* Configurar filtro de MAC em um roteador Wi-Fi;
* Compreender limitações de segurança baseadas em MAC Filtering;
* Bloquear o host daquele seu parente que deve dinheiro para a sua mãe/pai;

## Mecânica da Aula

* Formem duplas de 4;
* Pegue o seu cabo de rede crimpado na semana 02;
* Pegue os equipamentos com o prof;
* O quarteto deve seguir este relatório e responder as perguntas no Google Forms;
* No final, terá uma apresentação do grupo para os demais da sala.

## PREPARAÇÃO

* Conecte o roteador na tomada mais próxima do rack de equipamentos onde está o professor. Motivo: vamos ter que usar o seu cabo para conectar o roteador ao switch;
* Atenção, este roteador ainda está sem acesso à Internet e possui a rede padrão ```192.168.0.1```. Precisamos mudar este IP para o respectivo valor da tabela;
* Para acessar a parte administrativa do roteador, não precisa de usuário e nem senha. Basta digitar o IP de Rede no seu navegador;
* Cada grupo deve pesquisar a tela do roteador e se conectar ao SSID de acordo com o rotador que você recebeu. As senhas são bem parecidas, logo, tome cuidado para não entrar no roteador errado:
  
| IP de Rede   | SSID     | Senha    |
|---------------|----------|----------|
| 192.168.1.1   | grupo1ec | grupo1ec |
| 192.168.2.1   | grupo2ec | grupo2ec |
| 192.168.3.1   | grupo3ec | grupo3ec |
| 192.168.4.1   | grupo4ec | grupo4ec |
| 192.168.5.1   | grupo5ec | grupo5ec |
| 192.168.6.1   | grupo6ec | grupo6ec |
| 192.168.7.1   | grupo7ec | grupo7ec |
| 192.168.8.1   | grupo8ec | grupo8ec |

## ARQUITETURA DA AULA

<img src="https://github.com/agodoi/m09ec-semana05b/blob/main/assets/semana05b-fig2.png" width="1000">




# PARTE 1 - Fundamentação teórica: Entendendo o Endereço MAC

A subcamada MAC (Medium Access Control) pertence à camada de ENLACE de dados do modelo OSI.

<img src="https://github.com/agodoi/m09ec-semana05b/blob/main/assets/modelo%20OSIvsTCP-IP.png" width="1000">


Ela é responsável por:

* Identificar dispositivos na rede local;
* Controlar o acesso ao meio físico;
* Encapsular os dados em quadros Ethernet;
* Permitir que switches e roteadores identifiquem os dispositivos conectados;
* Cada interface de rede possui um endereço MAC único, composto por 48 bits, normalmente representado em formato hexadecimal.

Exemplo: ``` 00:1A:2B:3C:4D:5E```

### Curiosidade: 

Os três primeiros pares de hexadecimais (ex: 00:E0:4C) no endereço MAC do seu dispositivo (que é da forma XX:XX:XX:YY:YY:YY) informam quem fabricou o controlador de rede. Isso para uma investigação forence importa bastante. Use esse link para confirmar quem é o seu fabricante: [https://macvendors.com](https://macvendors.com)


## RESPONDA A PARTE 1 - Descobrindo o endereço MAC do computador [FORMS AQUI](https://forms.gle/4HL77ReE4azrnPgZ7)


# PARTE 2 - Fundamento Teórico: Observando a relação entre IP e MAC

Os dispositivos da rede precisam descobrir o MAC correspondente a um IP. Isso é feito pelo protocolo ARP (Address Resolution Protocol).

**(2.1)** Execute no terminal: ```arp -a``` ou ```ip neigh```

Exemplo de resultado:

* 192.168.0.1 x 84-16-F9-11-22-33
* 192.168.0.10 x 3C-22-FB-10-20-30

**(2.2)** Caso não esteja enxegando IPs que comecem com ```192.168```, dê um PING nos computadores do seu grupo e execute novamente o **(2.2)**. Certifique-se que os hosts do seu grupo estejam conectados no roteador do grupo.

## RESPONDA A PARTE 2 - Observando a relação entre IP e MAC [FORMS AQUI](https://forms.gle/4HL77ReE4azrnPgZ7)

# PARTE 3 - Fundamento Teórico: Identificando dispositivos conectados ao roteador

* Todo roteador possui uma tabela de hosts conectados nele e o respectivo endereço MAC;
* Acesso endereço do seu roteador usando o seu navegador preferido;
* Deixe os campos usuário e senha em branco e confirme.
* Seu desafio é encontrar a tela que mostra os hosts conectados. Dica: busque por QoS ou DHCP. Isso depende do modelo do roteador;

## RESPONDA A PARTE 3 - Identificando dispositivos conectados ao roteador [FORMS AQUI](https://forms.gle/4HL77ReE4azrnPgZ7)

# PARTE 4 - Fundamento Teórico: Filtragem de MAC no roteador

* Todo rotedor tem uma lista de bloqueio de endereços MAC;
* Essa lista é bem útil quando você precisa bloquear totalmente um acesso de um host sem ter que se preocupar em mudar senha do roteador, ou esconder o SSID;
* Mesmo que o computador plug um cabo Ethernet ou tenha a senha de acesse do SSID do roteador, esse bloqueio vai acontecer na camada mais baixa do modelo TCP/IP;

## RESPONDA A PARTE 4 - Filtragem de MAC no roteador [FORMS AQUI](https://forms.gle/4HL77ReE4azrnPgZ7)

# PARTE 5 - Fundamento Teórico: Como clonar endereço MAC

* O endereço MAC é gravado na placa de rede pelo fabricante, porém o sistema operacional pode alterar o endereço apresentado ao sistema e à rede;
* Esse processo é chamado de **MAC Spoofing**;
* O hardware continua tendo o MAC original, mas o sistema passa a anunciar outro MAC na rede.
* Esse site explica como: [https://technitium.com/tmac/](https://technitium.com/tmac/)
* Por motivos óbvios, não vamos avançar deste ponto. Qualquer mudança de MAC do seu computador é de inteira responsabilidade sua.

## RESPONDA A PARTE 5 - Como clonar endereço MAC [FORMS AQUI](https://forms.gle/4HL77ReE4azrnPgZ7)


