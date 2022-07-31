# resistor pull-down /pull-up

# Pull-up

O esquema de ligação padrão para esta configuração é ilustrado pela Figura 1. Quando o botão estiver solto, o Vcc fluirá pelo resistor R1 chegando na porta digital. Quando o botão for pressionado, o Gnd fluirá pelo contato da chave — sem maiores resistências — alcançando o pino do microcontrolador.

Na prática, quando o botão estiver solto, o microcontrolador reconhecerá nível lógico 1, por isso a nomenclatura pull-up (puxar para cima): normalmente para cima/nível lógico High. Todavia, enquanto a chave for pressionada, o microcontrolador reconhecerá nível lógico 0.

<table border="0">
<tbody>
<tr>
<td><img style="display: block; margin-left: auto; margin-right: auto;" src="/Resistor pull up-pull down/img/pull-up.jpg" alt="" width="80%" /></td>
</tr>
<tr>
<td style="text-align: center;">Figura 1: Resistor de Pull-Up.</td>
</tr>
</tbody>
</table>

# Pull-down

A Figura 2 ilustra o esquema de ligação padrão para esta configuração. Quando o botão estiver solto, o Gnd fluirá pelo resistor R1 chegando na porta digital. Quando o botão for pressionado, o Vcc fluirá pelo contato da chave — sem maiores resistências — alcançando o pino do microcontrolador. 

Na prática, quando o botão estiver solto, o microcontrolador reconhecerá nível lógico 0 (Gnd), por essa razão a nomenclatura pull-down (puxar para baixo): normalmente para baixo/nível lógico 0. Contudo, enquanto a chave for pressionada, o microcontrolador identificará nível lógico 1 .

<table border="0">
<tbody>
<tr>
<td><img style="display: block; margin-left: auto; margin-right: auto;" src="/Resistor pull up-pull down/img/Pull-down.jpg" alt="" width="80%" /></td>
</tr>
<tr>
<td style="text-align: center;">Figura 2: Resistor de Pull-down.</td>
</tr>
</tbody>
</table>
