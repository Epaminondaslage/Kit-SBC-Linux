<td style="width: 20%;"><img src="https://github.com/Epaminondaslage/Automacao-industrial-e-residencial-Ecossistema-didatico/blob/main/img/Logo_CEFET-MG.png" width="20%" /></td>
<p><strong><span style="color: #0000ff;"> Kit SBC Linux</span></strong></p>
<p><strong><span style="color: #0000ff;">Prof Epaminondas Lage</span></strong></p>
<a href="http://lattes.cnpq.br/7787341723868111"> Currículo Lattes LAGE, E. S.</a> 

# Índice 

* [Introdução](#Introdução)
* [O que é o Orange Pi?](#O-que-é-o-Orange-Pi)
* [Aplicações do Orange Pi](#Aplicações-do-Orange-Pi)
* [O Kit SBC Linux](#O-Kit-SBC-Linux)
* [Sistema Operacional](#Sistema-Operacional)
* [Espansão do conector de 40 pinos](#Espansão-do-conector-de-40-pinos)
* [Módulo relé](#Módulo-Relé)
* [Módulo botão](#Módulo-botão)
* [Status do Projeto](#Status-do-Projeto) 
* [Referências](#Referências)

# Introdução

Computador de placa única (SBC) é um computador onde todos os componentes electrônicos necessários para o seu funcionamento estão situados numa única placa de circuito impresso. Estes computadores são geralmente usados em sistemas de controle, alarmes, sistemas de medidas, entre outros. Atualmente, a oferta de SBC (Single-Board Computers) é grande. Para citar somente alguns, temos acesso facilmente no mercado de sistemas embarcados a: Raspberry Pi, BeagleBone Black, BeagleBone Green, Linkit Smart 7688, Intel Edison, CubieBoard, Arduino Mega 2560, Odroid, Orange Pi, Asus Tinker Board, etc. 

Com esta oferta crescente, os fabricantes se diferenciam principalmente em dois aspectos: configurações de hardware cada vez mais robustas e preços cada vez menores. É justamente nestes dois pontos que a empresa Orange Pi focou para a fabricação da Orange Pi One. Esta placa possui características extremamente atraentes em hardware a um preço muito competitivo. Entre outras características, esta máquina também incorpora um conector de 40 pins, porta USB, uma porta Gigabit Ethernet e HDMI. 

O coração do Kit SBC Linux é o OrangePi One. O Orange Pi, que é mais uma SBC (Single-Board Computers) disponibilizada no mercado, conta com um processador ARM e pode ser utilizada com varias distribuições do sistema operacional GNU/Linux. Ele foi desenhanda para ter um extrema performance e baixo custo, ela conta com o processador H3 que é o mesmo das suas irmãs mais potentes, possui memoria ram (512), não tem eMMC e nem wifi. É uma excelente escolha e é tão potente quanto uma raspberry pi ou outras do mercado com um custo excelente, conforme é mostrado na figura 1

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

Estas placas rodam o SO Linux  e possuem os pinos I/O  disponíveis para acesso através de Shell script, Pynton, etc. Uma vez configurados a direção do pino de I/O pode-se ler ou alterar o estado do pino de I/O resultado em leituras de sensores externos, atuação de relés, etc. 

# O que é o Orange Pi?
<table style="border-collapse: collapse; width: 100%;" border="1">
<tbody>
<tr>
<td style="width: 50%;"><img src="/img/Imagem1.jpg" alt="" width="200" /></td>
<td style="width: 50%;">Figura 2. Orange Pi &eacute; um computador de uma placa &uacute;nica e de c&oacute;digo aberto. Percence a uma nova gera&ccedil;&atilde;o de placa de desenvolvimento, pode executar o Android 4.4, Android 7.0, Ubuntu e Debian e outros sistemas operacionais. A placa de desenvolvimento Orange Pi One usa o sistema em chip Allwinner H3 e possui 512 MB de mem&oacute;ria DDR3.</td>
</tr>
</tbody>
</table>

# Aplicações do Orange Pi
Praticamente qualquer outra coisa, porque Orange Pi é de código aberto. Podemos usá-lo para construir:
<ul>
<li>Um computador</li>
<li>Um servidor sem fio</li>
<li>Jogos</li>
<li>Música e sons</li>
<li>Vídeo HD</li>
<li>Desenvolvimento de IoT</li>
<li>Firewall</li>
<li>Roteadores</li>
<li>Android</li>
</ul>

## As vistas superior e inferior do Orange Pi One

<table style="border-collapse: collapse; width: 100%;" border="1">
<tbody>
<tr>
<td style="width: 50%;"><img src="/img/Imagem1.jpg" alt="" width="300" /></td>
<td style="width: 50%;"><img src="/img/Imagem2.jpg" alt="" width="300" /></td>
</tr>
<tr>
<td style="text-align: center;">Figura 4: OrangePi One- Vista superior e inferior.</td>

</tr>
</tbody>
</table>

## As conex&otilde;es externas do Orange Pi One

<table style="border-collapse: collapse; width: 100%;" border="1">
<tbody>
<tr>
<td style="width: 50%;"><img src="/img/Imagem3.jpg" alt="" width="400" /></td>
</tr>
<tr>
<td style="text-align: center;">Figura 5: OrangePi One-Conexões Externas.</td>
</tr>
</tbody>
</table>


* Veja as principais características do Orange Pi One:

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

A base de sustentação para as placas foi desenvovolvida construida em uma impressora 3D. Possui dimensões de 245x180x15 mm e possui um slot para o OrangePi One, uma placa de conexões, um módulo de 8 relés e um módulo de 5 push-botons é apresentado pela figura 6. 

<table border="0">
<tbody>
<tr>
<td><img style="display: block; margin-left: auto; margin-right: auto;" src="/img/base_kit.jpg" alt="" width="40%" /></td>
</tr>
<tr>
<td style="text-align: center;">Figura 6: Impressão 3D do Kit SBC Linux.</td>
</tr>
</tbody>
</table>

A figura 7 apresenta o kit SBC Linux com os dispositivos eletrônicos montados sobre a base.

<table border="0">
<tbody>
<tr>
<td><img style="display: block; margin-left: auto; margin-right: auto;" src="/img/kit-sbclinux.png" alt="" width="80%" /></td>
</tr>
<tr>
<td style="text-align: center;">Figura 7: Kit SBC Linux.</td>
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
<td style="text-align: center;">Figura 8: H3 SoC Gpio do orange Pi One .</td>
</tr>
</tbody>
</table>

# Sistema Operacional 

Nos nossos kits optamos em utilizar o Ubuntu para a programação em Shell Script e o Debian para a instalação do OpenPLC runtime. Veja como instalar as duas distribuições utilizadas.

## Repositórios Disponíveis

* <a href="https://github.com/Epaminondaslage/SO_Ubuntu_SBC_OrangePI">SO Ubuntu SBC OrangePI</a> 
* <a href="https://github.com/Epaminondaslage/SO-Debian-SBC-OrangePI">SO Debian SBC OrangePI</a> 

# Expansão do conector de 40 pinos

A Placa de Expansão de GPIO - 40 Pinos é a solução ideal para expandir a utilização dos pinos de GPIO da Rasbeprry, podendo extender a conexao de 40 pinos, sendo compatível com os modelos de raspberry/orangePI.

O módulo em tipo T facilita a conexão dos GPIO a uma protoboard, permitindo a prototipagem rápida durante o desenvolvimento de circuitos eletrônicos.

<table border="0">
<tbody>
<tr>
<td><img style="display: block; margin-left: auto; margin-right: auto;" src="/img/placaexpansao.jpg" alt="" width="40%" /></td>
</tr>
<tr>
<td style="text-align: center;">Figura 9: Expansão do conector de 40 pinos .</td>
</tr>
</tbody>
</table>

# Módulo relé

Relés são componentes atuam como interruptores, acionando ou parando a ação de um circuito por meio da (re)transmissão de corrente elétrica. Por isolar sinais, é muito útil para a segurança de um circuito. Relés são ativados por correntes elétricas bem inferiores àquelas empregadas no circuito principal, que pode ser controlado por componentes como transistores e fotoresistores. Assim, não é necessário operar com cargas elevadas.

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
    Corrente: maior de 30mA para cada acionamento 
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
<td style="text-align: center;">Figura 10: Módulo com 1,2,4 e 8 relés.</td>
</tr>
</tbody>
</table>

<p>Informa&ccedil;&otilde;es de funcionamento deste m&oacute;dulo assim como o uso do pino JD-VCC podem serem encontradas <a href="https://github.com/Epaminondaslage/Kit-SBC-Linux/tree/main/M%C3%B3dulo%20rel%C3%A9">aqui</a>.</p>

# Módulo botão

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
<td style="text-align: center;">Figura 11: Módulo chave.</td>
</tr>
</tbody>
</table>

<p>Informa&ccedil;&otilde;es de funcionamento deste m&oacute;dulo pode ser encontradas <a href="https://github.com/Epaminondaslage/Kit-SBC-Linux/tree/main/Módulobotão">aqui</a>.</p>

# Status do Projeto

![Badge em Desenvolvimento](http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=GREEN&style=for-the-badge)

# Referências

https://uthings.uniud.it/control-gpio-pins-of-orange-pi-boards







