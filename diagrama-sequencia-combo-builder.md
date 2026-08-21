# Diagrama de Sequência — Padrão Builder (Combo de Fast-Food)

![Diagrama de sequência do padrão Builder](./diagrama_sequencia_combo_builder.svg)

## Quem aparece no desenho

**Cliente** (o bonequinho à esquerda)
É a pessoa que chega no balcão querendo comprar um combo. É ela quem começa toda a história.

**Atendente (Diretor)** (a bolinha azul)
É quem trabalha no caixa. Ele não faz o combo com as próprias mãos, ele só dá as ordens: "bota isso", "bota aquilo". No mundo da programação, esse "dar ordens" tem um nome chique: **Diretor**. Mas pode pensar nele só como o atendente mesmo.

**ComboBuilder** (a caixinha azul escrito «interface»)
Pensa nele como uma "receita em branco" ou um "moldezinho" que sabe montar um combo, passo a passo. Ele é tipo um funcionário invisível que fica junto do atendente, prontinho pra receber as ordens de "bota o lanche", "bota a batata"...

**Combo** (a última bolinha, à direita)
É o produto final. O saquinho pronto, fechado, com tudo dentro, pra entregar pro cliente.

As linhas pontilhadas descendo de cada um são só pra mostrar "o tempo passando" pra aquele personagem — é assim que se desenha esse tipo de diagrama.

As barrinhas azuis em cima das linhas mostram quando cada um está "ocupado fazendo alguma coisa".

## Passo a passo do que acontece

**1 — O cliente cria o moldezinho do combo**
Antes de tudo, o cliente prepara um builder específico pra fast-food. É como se ele dissesse "quero montar um combo, e vou usar esse moldezinho aqui pra isso".

**1.1 — O cliente entrega o pedido pro atendente**
O cliente passa esse moldezinho pra mão do atendente e fala "monta esse pedido pra mim".

**1.1.1 — Atendente pede o lanche**
O atendente vira pro moldezinho e fala "bota um hambúrguer aí".

**1.1.2 — Atendente pede a batata**
Mesma coisa, agora pedindo a batata frita.

**1.1.3 — Atendente pede a bebida**
Pede o refrigerante.

**1.1.4 — Atendente pede o brinde**
Pede o brinquedinho ou brinde que acompanha o combo.

Repara que essas quatro chamadas são bem parecidas — é o atendente falando, um de cada vez e na ordem certa, tudo que precisa entrar no combo.

**1.2 — Atendente pede o combo pronto**
Depois de pedir tudo, o atendente fala "agora me dá o combo montado".

**1.2.1 — O moldezinho cria o combo de verdade**
Aí sim, o moldezinho junta tudo que foi pedido (lanche, batata, bebida, brinde) e cria o combo, o produto de verdade, prontinho.

**1.3 — O combo volta pro atendente**
O moldezinho entrega esse combo pronto de volta na mão do atendente. (Essa seta é tracejada porque é uma "resposta", não um pedido novo.)

**1.4 — O atendente entrega pro cliente**
Por fim, o atendente entrega o combo prontinho na mão do cliente. Fim da história.

## Por que isso é interessante (o "pulo do gato")

O atendente nunca fica mexendo direto no combo. Ele só vai dando ordens simples, uma de cada vez, pro moldezinho. Quem realmente monta o combo, junta as peças e entrega pronto é o moldezinho (o builder).

Isso é útil porque, se um dia quiserem criar um combo diferente — tipo um combo vegetariano ou um combo infantil — só precisam trocar o moldezinho por outro. O jeito de o atendente pedir as coisas continua exatamente igual, ele nem percebe a diferença.
