
## Propostas de Mapeamento e Transformações
~~~
1. Criação de um mapeamento em que ingredientes se ligam a ingrediente por participação em receitas
2. Desenvolvimento de um mapeamento em que os ingredientes se liguem por pertencerem a um grupo
~~~

## Análises
~~~
1. Ingredientes que costumam aparecer juntos: o que clusters significam? Sabores parecidos?
-> Por meio da técnica de predição de links (Link Prediction), podemos identificar semelhanças entre nós. Uma resposta
plausível a ser encontrada é a presença de componentes químicos entre os ingredientes que os tornam complementares ou então
alguma relação que promove uma harmonização entre os sabores.

2. O que ingredientes considerados "hubs" têm em comum?
-> Utilizando a técnica de Centralidade, em especial a de grau (Degree), é possível identificar os ingredientes
 considerados "hubs" ou seja, que participam de muitas conexões. A resposta provável é que são ingredientes complementares
 e de grande difusão global, que "combinam" com diversas receitas.

3. Distância grande entre entre dois ingredientes implica em baixa compatibilidade/disponibilidade na mesma região?
-> Nesse caso a técnica de Centralidade, em específico a de Betweenness, conseguimos identificar a distância entre ingredientes.
A conclusão esperada é a presença de componentes químicos antagonistas, como açúcar e sal, ou então a própria disponibilidade regional
como a distância entre alga japonesa e o dendê.
~~~