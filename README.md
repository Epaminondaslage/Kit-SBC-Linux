<td style="width: 20%;"><img src="https://github.com/Epaminondaslage/Automacao-industrial-e-residencial-Ecossistema-didatico/blob/main/img/Logo_CEFET-MG.png" width="20%" /></td>
<p><strong><span style="color: #0000ff;"> Kit SBC Linux</span></strong></p>
<p><strong><span style="color: #0000ff;">Prof Epaminondas Lage</span></strong></p>
<a href="http://lattes.cnpq.br/7787341723868111"> Currículo Lattes LAGE, E. S.</a> 

# Índice 

* [Introdução](#Introdução)
* [O Kit SBC Linux](#O-Kit-SBC-Linux)
* [Sistema Operacional](#Sistema-Operacional)
* [Espansão do conector de 40 pinos](#Espansão-do-conector-de-40-pinos)
* [Módulo relé](#Módulo-Relé)
* [Módulo chave digital](#Módulo-chave-digital)
* [Status do Projeto](#Status-do-Projeto) 
* [Referências](#Referências)

# Introdução

O coração do Kit SBC Linux é o OrangePi One. O Orange Pi, que é mais uma SBC (Single-Board Computers) disponibilizada no mercado, conta com um processador ARM e pode ser utilizada com varias distribuições do sistema operacional GNU/Linux. Ele foi desenhanda para ter um extrema performance e baixo custo, ela conta com o processador H3 que é o mesmo das suas irmãs mais potentes, possui memoria ram (512), não tem eMMC e nem wifi. É uma excelente escolha e é tão potente quanto uma raspberry pi ou outras do mercado com um custo excelente, conforme é mostrado na figura 1.

<table border="0">
<tbody>
<tr>
<td><img style="display: block; margin-left: auto; margin-right: auto;" src="/img/orangepionecabo.jpg" alt="" width="20%" /></td>
</tr>
<tr>
<td style="text-align: center;">Figura 1: OrangePi One.</td>
</tr>
</tbody>
</table>

Veja as principais características do Orange Pi One:

    SoC – Allwinner H3 quad core Cortex A7 1.2 GHz com GPU ARM Mali-400MP2 de 600 MHz
    RAM – 512 MB DDR3
    Slot para cartão micro SD
    Saída de vídeo/audio e HDMI
    Conectivitidade porta RJ45 Ethernet
    1 USB 2.0 host, 1x micro USB OTG port
    Câmera – CSI Interface
    40 pinos compatíveis com a Raspberry Pi
    Debugging – 3 pinos UART
    Botão Power
    Alimentação – 5V/2A
     
    
# O Kit SBC Linux

A base de sustentação para as placas foi desenvovolvida construida em uma impressora 3D. Possui dimensões de 245x180x15 mm e possui um slot para o OrangePi One, uma placa de conexões, um módulo de 8 relés e um módulo de 5 push-botons conforpe apresenta a figura 2. 

<table border="0">
<tbody>
<tr>
<td><img style="display: block; margin-left: auto; margin-right: auto;" src="/img/base_kit.jpg" alt="" width="40%" /></td>
</tr>
<tr>
<td style="text-align: center;">Figura 2: Impressão 3D do Kit SBC Linux.</td>
</tr>
</tbody>
</table>

A figura 3 apresenta o kit SBC Linux com os dispositivos eletrônicos montados sobre a base.

<table border="0">
<tbody>
<tr>
<td><img style="display: block; margin-left: auto; margin-right: auto;" src="/img/kit-sbclinux.png" alt="" width="80%" /></td>
</tr>
<tr>
<td style="text-align: center;">Figura 3: Kit SBC Linux.</td>
</tr>
</tbody>
</table>

# GPIO

Existem duas maneiras de controlar e configurar os pinos GPIO. A primeira é usar uma biblioteca apropriada (C, C++, Python ou outra linguagem de programação) e a segunda é controlar GPIO do Shell de usuário do Linux. Maiores informações podem ser obtitos no <a href="https://github.com/orangepi-xunlong">Github da Orange Pi</a>. O diagrama abaixo é uma reprodução extraída do git da OrangePi.

    +------+-----+----------+------+---+OrangePiH3+---+------+----------+-----+------+
    | GPIO | wPi |   Name   | Mode | V | Physical | V | Mode | Name     | wPi | GPIO |
    +------+-----+----------+------+---+----++----+---+------+----------+-----+------+
    |      |     |     3.3V |      |   |  1 || 2  |   |      | 5V       |     |      |
    |   12 |   0 |    SDA.0 |  OUT | 0 |  3 || 4  |   |      | 5V       |     |      |
    |   11 |   1 |    SCL.0 |  OUT | 0 |  5 || 6  |   |      | GND      |     |      |
    |    6 |   2 |      PA6 |  OUT | 0 |  7 || 8  | 0 | OUT  | TXD.3    | 3   | 13   |
    |      |     |      GND |      |   |  9 || 10 | 0 | OUT  | RXD.3    | 4   | 14   |
    |    1 |   5 |    RXD.2 |  OUT | 0 | 11 || 12 | 0 | OUT  | PD14     | 6   | 110  |
    |    0 |   7 |    TXD.2 |  OUT | 0 | 13 || 14 |   |      | GND      |     |      |
    |    3 |   8 |    CTS.2 |  OUT | 0 | 15 || 16 | 0 | OUT  | PC04     | 9   | 68   |
    |      |     |     3.3V |      |   | 17 || 18 | 0 | OUT  | PC07     | 10  | 71   |
    |   64 |  11 |   MOSI.0 |  OUT | 0 | 19 || 20 |   |      | GND      |     |      |
    |   65 |  12 |   MISO.0 |  OUT | 0 | 21 || 22 | 0 | OUT  | RTS.2    | 13  | 2    |
    |   66 |  14 |   SCLK.0 |  OUT | 0 | 23 || 24 | 0 | OUT  | CE.0     | 15  | 67   |
    |      |     |      GND |      |   | 25 || 26 | 0 | OUT  | PA21     | 16  | 21   |
    |   19 |  17 |    SDA.1 |  OUT | 0 | 27 || 28 | 0 | OUT  | SCL.1    | 18  | 18   |
    |    7 |  19 |     PA07 |  OUT | 0 | 29 || 30 |   |      | GND      |     |      |
    |    8 |  20 |     PA08 |  OUT | 0 | 31 || 32 | 0 | OUT  | RTS.1    | 21  | 200  |
    |    9 |  22 |     PA09 |  OUT | 0 | 33 || 34 |   |      | GND      |     |      |
    |   10 |  23 |     PA10 |  OUT | 0 | 35 || 36 | 0 | OUT  | CTS.1    | 24  | 201  |
    |   20 |  25 |     PA20 |  OUT | 0 | 37 || 38 | 0 | OUT  | TXD.1    | 26  | 198  |
    |      |     |      GND |      |   | 39 || 40 | 0 | OUT  | RXD.1    | 27  | 199  |
    +------+-----+----------+------+---+----++----+---+------+----------+-----+------+
    | GPIO | wPi |   Name   | Mode | V | Physical | V | Mode | Name     | wPi | GPIO |
    +------+-----+----------+------+---+OrangePiH3+---+------+----------+-----+------+

## Controle os pinos GPIO usando uma biblioteca

Se você deseja controlar os pinos GPIO de uma placa Orange Pi usando uma biblioteca apropriada, o primeiro passo é escolher a biblioteca certa. Então você tem que decidir qual linguagem de programação você quer usar. Na lista a seguir estão algumas das bibliotecas mais utilizadas:

<ul class="list-normal">
<li><a class="external-link" title="Open external link in new window" href="https://github.com/zhaolei/WiringOP" target="_blank" rel="noopener noreferrer">WiringOP </a>(C library)</li>
<li><a class="external-link" title="Open external link in new window" href="https://github.com/duxingkei33/orangepi_PC_gpio_pyH3" target="_blank" rel="noopener noreferrer">GPIO_pyH3</a> (Python library for H3 boards)</li>
<li><a class="external-link" title="Open external link in new window" href="https://opi-gpio.readthedocs.io/en/latest/index.html" target="_blank" rel="noopener noreferrer">OPi.GPIO</a> (Python library for Orange Pi )ne)</li>
</ul>

## Controle os pinos GPIO através de Shell Script Linux

A segunda maneira de gerenciar os pinos GPIO é usando os comandos do Shell Script do kernel do Linux . O primeiro passo é habilitar esta opção na configuração do kernel. Em geral, nas imagens oficiais, isso é feito por padrão. Se você usa um kernel personalizado, pode usar a ferramenta menuconfig para habilitá-lo. Vá para Device Drivers, habilite GPIO Support e então no menu GPIO Support habilite /sys/class/gpio/... (sysfs interface).

<table border="0">
<tbody>
<tr>
<td><img style="display: block; margin-left: auto; margin-right: auto;" src="/img/Orange-Pi-One-01-478x418.png" alt="" width="80%" /></td>
</tr>
<tr>
<td style="text-align: center;">Figura 4: H3 SoC Gpio do orange Pi One .</td>
</tr>
</tbody>
</table>

# Sistema Operacional 

Nos nossos kits optamos em utilizar o Ubuntu para a programação em Shell Script e o Debian para a instalação do OpenPLC runtime. Veja como intalar as duas distribuições.

## Repositórios Disponíveis

* <a href="https://github.com/Epaminondaslage/SO_Ubuntu_SBC_OrangePI">SO Ubuntu SBC OrangePI</a> 
* <a href="https://github.com/Epaminondaslage/SO-Debian-SBC-OrangePI">SO Debian SBC OrangePI</a> 

# Espansão do conector de 40 pinos

<table border="0">
<tbody>
<tr>
<td><img style="display: block; margin-left: auto; margin-right: auto;" src="/img/Espansao40pinos.png" alt="" width="80%" /></td>
</tr>
<tr>
<td style="text-align: center;">Figura 5: Espansão do conector de 40 pinos .</td>
</tr>
</tbody>
</table>

# Módulo relé

    * Descrição do produto: Módulo de relé de 8 canais
    Carga máxima: AC 250V/10A, DC 30V/10A
    Corrente de gatilho: 5mA
    Tensão de trabalho: 3,3V
    Tamanho do módulo: 50 x 26 x 18,5 mm (C x L x A)
    Quatro furos de parafusos de montagem, diâmetro 3,1 mm
    Dc+: fonte de alimentação positiva (VCC)
    Dc-: fonte de alimentação negativa (GND)
    In: pode ser relé de controle de alto ou baixo nível
    Na: interface de relé normalmente aberta
    Com: Relés da Interface comum
    Nc: interface de relé fechada normalmente
    Dimensões: 135mm (comprimento) * 53mm (L) * 18,5 (A)
    Peso:. 31g 
    Cor do PCB: azul
    8 optoaclopladores e anti-jamming 
    Acionamento com sinal baixo. LED indicadore de status de funcionamento. 
    Vcc da energia do sistema. Entrada de energia do relé de fonte de alimentação separada do JD-VCC. Você pode conectar jampers 
    
    * Parâmetros elétricos: 
    Tensão de fornecimento: 3,3VDC 
    Corrente: maior de 100mA 
    Carga: 250V 10A AC,125V 10A AC ou 30V 10A DC 
 
    * Fiação: 
    Vcc: sistema de alimentação positiva 
    Gnd: Potência do sistema negativa 
    In1 - IN8: portas de controle de relé

<table border="0">
<tbody>
<tr>
<td><img style="display: block; margin-left: auto; margin-right: auto;" src="/img/modulorele.jpg" alt="" width="40%" /></td>
</tr>
<tr>
<td style="text-align: center;">Figura 6: Módulo relé.</td>
</tr>
</tbody>
</table>

<p>Informa&ccedil;&otilde;es de funcionamento deste m&oacute;dulo pode ser encontradas <a href="https://github.com/Epaminondaslage/Kit-SBC-Linux/tree/main/M%C3%B3dulo%20rel%C3%A9">aqui</a>.</p>

# Módulo chave digital

Este Módulo desenvolvido em montagens experimentais em protoboard, ele vem com pinos +VCC,out,GND e capa colorida para facilitar o manuseio. Apresenta
as seguintes características:

    Tamanho: 11*22mm (Mais detalhes via foto)
    Cor: Branco, Vermelho, Amarelo, Verde, Azul, e Verde.
    Tensão: 3.3 até 5 v
    Saída: nível digital (Sinal alto, se quiser Sinal baixo inverter GND e VCC na ligação)
    Contem um resistor de 10K entre GND e OUT (resistor de pull-down)
    Plataforma: Compatível com qualquer plataforma, Arduíno, OrangePi, RaspberryPI e outras.

<table border="0">
<tbody>
<tr>
<td><img style="display: block; margin-left: auto; margin-right: auto;" src="/img/modulochave.jpg" alt="" width="40%" /></td>
</tr>
<tr>
<td style="text-align: center;">Figura 7: Módulo chave.</td>
</tr>
</tbody>
</table>

<p>Informa&ccedil;&otilde;es de funcionamento deste m&oacute;dulo pode ser encontradas <a href="https://github.com/Epaminondaslage/Kit-SBC-Linux/tree/main/M%C3%B3dulo-chave">aqui</a>.</p>

# Status do Projeto

![Badge em Desenvolvimento](http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=GREEN&style=for-the-badge)

# Referências

https://uthings.uniud.it/control-gpio-pins-of-orange-pi-boards







