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
<td><img style="display: block; margin-left: auto; margin-right: auto;" src="/img/orangepionecabo.jpg" alt="" width="40%" /></td>
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

Existem duas maneiras de controlar e configurar os pinos GPIO. A primeira é usar uma biblioteca apropriada (C, C++, Python ou outra linguagem de programação) e a segunda é controlar GPIO do Shell de usuário do Linux.

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
<table border="0">
<tbody>
<tr>
<td><img style="display: block; margin-left: auto; margin-right: auto;" src="/img/modulorele" alt="" width="80%" /></td>
</tr>
<tr>
<td style="text-align: center;">Figura 6: Módulo relé.</td>
</tr>
</tbody>
</table>

# Módulo chave digital

<table border="0">
<tbody>
<tr>
<td><img style="display: block; margin-left: auto; margin-right: auto;" src="/img/modulochave.jpg" alt="" width="80%" /></td>
</tr>
<tr>
<td style="text-align: center;">Figura 7: Módulo chave.</td>
</tr>
</tbody>
</table>



# Status do Projeto

![Badge em Desenvolvimento](http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=GREEN&style=for-the-badge)

# Referências

https://uthings.uniud.it/control-gpio-pins-of-orange-pi-boards







