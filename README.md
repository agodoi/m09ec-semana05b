# Apresentação dos conceitos envolvidos com a subcamada MAC (Medium Access Control)

## 1. Objetivos da Aula

Ao final desta prática/teórica, vocês deverão ser capazes de:

* Identificar o endereço MAC de diferentes interfaces de rede;
* Compreender a relação entre endereços IP e endereços MAC;
* Utilizar comandos de rede para visualizar tabelas ARP;
* Analisar dispositivos conectados a um roteador utilizando o MAC Address.
* Configurar filtro de MAC em um roteador Wi-Fi;
* Compreender limitações de segurança baseadas em MAC Filtering;
* Bloquear o host daquele seu parente que deve dinheiro para a sua mãe/pai;

## 2. Mecânica da Aula

* Formem duplas de 4;
* Pegue o seu cabo de rede crimpado na semana 02;
* Pegue o equipamentos com o prof;
* O quarteto deve seguir este relatório e responder as perguntas no Google Forms.
* No final, terá uma apresentação do grupo para os demais da sala.

## 3. Fundamentação teórica (parte conceitual)

A subcamada MAC (Medium Access Control) pertence à camada de ENLACE de dados do modelo OSI.

<img src="https://github.com/agodoi/m09ec-semana05b/blob/main/assets/modelo%20OSIvsTCP-IP.png" width="500">


Ela é responsável por:

* Identificar dispositivos na rede local;
* Controlar o acesso ao meio físico;
* Encapsular os dados em quadros Ethernet;
* Permitir que switches e roteadores identifiquem os dispositivos conectados;
* Cada interface de rede possui um endereço MAC único, composto por 48 bits, normalmente representado em formato hexadecimal.

Exemplo: ``` 00:1A:2B:3C:4D:5E```

### Curiosidade: 

Os três primeiros pares de hexadecimais (ex: 00:E0:4C) no endereço MAC do seu dispositivo (que é da forma XX:XX:XX:YY:YY:YY) informam quem fabricou o controlador de rede. Isso para uma investigação forence importa bastante.



