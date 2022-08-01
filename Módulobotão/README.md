<td style="width: 20%;"><img src="https://github.com/Epaminondaslage/Automacao-industrial-e-residencial-Ecossistema-didatico/blob/main/img/Logo_CEFET-MG.png" width="20%" /></td>
<p><strong><span style="color: #0000ff;"> Módulo Botão</span></strong></p>
<p><strong><span style="color: #0000ff;">Prof Epaminondas Lage</span></strong></p>
<a href="http://lattes.cnpq.br/7787341723868111"> Currículo Lattes LAGE, E. S.</a> 

# Índice 

* [Resistor Pull-up](#Resistor-Pull-up)
* [Resistor Pull-down](#Resistor-Pull-down)
* [Referências](#Referências)
* [Status do Projet](#-Status-do-Projeto)

Se o pino do microcontrolador não estiver conectado a nada, ele pode entender tanto HIGH como LOW (e isso pode mudar aleatoriamente). Assim sendo não conseguimos detectar um mero estado de botão com confiabilidade. Para contornar o problema, utilizaremos resistores nas configurações Pull-up/Pull-down.

# Resistor Pull-up

O esquema de ligação padrão para esta configuração é ilustrado pela Figura 1. Quando o botão estiver solto, o Vcc fluirá pelo resistor R1 chegando na porta digital. Quando o botão for pressionado, o Gnd fluirá pelo contato da chave — sem maiores resistências — alcançando o pino do microcontrolador.

Na prática, quando o botão estiver solto, o microcontrolador reconhecerá nível lógico 1, por isso a nomenclatura pull-up (puxar para cima): normalmente para cima/nível lógico High. Todavia, enquanto a chave for pressionada, o microcontrolador reconhecerá nível lógico 0.

<table border="0">
<tbody>
<tr>
<td><img style="display: block; margin-left: auto; margin-right: auto;" src="https://github.com/Epaminondaslage/Kit-SBC-Linux/blob/main/M%C3%B3dulobot%C3%A3o/img/pull-up.jpg" alt="" width="80%" /></td>
</tr>
<tr>
<td style="text-align: center;">Figura 1: Resistor de Pull-Up.</td>
</tr>
</tbody>
</table>

# Resistor Pull-down

A Figura 2 ilustra o esquema de ligação padrão para esta configuração. Quando o botão estiver solto, o Gnd fluirá pelo resistor R1 chegando na porta digital. Quando o botão for pressionado, o Vcc fluirá pelo contato da chave — sem maiores resistências — alcançando o pino do microcontrolador. 

Na prática, quando o botão estiver solto, o microcontrolador reconhecerá nível lógico 0 (Gnd), por essa razão a nomenclatura pull-down (puxar para baixo): normalmente para baixo/nível lógico 0. Contudo, enquanto a chave for pressionada, o microcontrolador identificará nível lógico 1 .

<table border="0">
<tbody>
<tr>
<td><img style="display: block; margin-left: auto; margin-right: auto;" src="https://github.com/Epaminondaslage/Kit-SBC-Linux/blob/main/M%C3%B3dulobot%C3%A3o/img/Pull-down.jpg" alt="" width="80%" /></td>
</tr>
<tr>
<td style="text-align: center;">Figura 2: Resistor de Pull-down.</td>
</tr>
</tbody>
</table>

# Referências

* https://blog.eletrogate.com/entendendo-os-resistores-de-pull-up-e-pull-down/?gclid=Cj0KCQjw852XBhC6ARIsAJsFPN22xGMaY3AThOyW9cVYgKx-9HBHwOiBQLjScbkCeFj_dYLZKObz_tsaAlayEALw_wcB

# Status do Projeto

![Badge em Desenvolvimento](http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=GREEN&style=for-the-badge)













