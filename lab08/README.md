
## Propostas de Mapeamento e Transformações
~~~
1. Criação de um mapeamento em que ingredientes se ligam a ingrediente por participação em receitas
2. Criação de uma rede similar à dos ingredientes, relacionando receitas através de uma projeção nas pessoas que as consomem
~~~

## Análises
1. Ingredientes que costumam aparecer juntos: o que clusters significam? Sabores parecidos?
   
-> Por meio da técnica de predição de links (Link Prediction), podemos identificar semelhanças entre nós. Uma resposta
plausível a ser encontrada é a presença de componentes químicos entre os ingredientes que os tornam complementares ou então
alguma relação que promove uma harmonização entre os sabores.

2. O que ingredientes considerados "hubs" têm em comum?

-> Utilizando a técnica de Centralidade, em especial a de grau (Degree), é possível identificar os ingredientes
 considerados "hubs" ou seja, que participam de muitas conexões. A resposta provável é que são ingredientes complementares
 e de grande difusão global, que "combinam" com diversas receitas.

3. Distância grande entre entre dois ingredientes implica em baixa compatibilidade/disponibilidade na mesma região?

-> A análise da distância entre dois ingredientes por meio da técnica de Centralidade, especialmente utilizando a medida de Betweenness, permite identificar a proximidade ou afastamento na presença de outros ingredientes em uma rede alimentar. Uma conclusão esperada é que uma grande distância entre ingredientes pode indicar baixa compatibilidade ou disponibilidade na mesma região.

Essa abordagem é valiosa para compreender não apenas possíveis interações químicas entre os ingredientes, mas também para considerar fatores geográficos e culturais. Por exemplo, a distância entre ingredientes como alga japonesa e dendê pode refletir não apenas diferenças de sabor, mas também as preferências culinárias regionais, indicando a disponibilidade local desses ingredientes.

Dessa forma, a análise de Betweenness na rede alimentar proporciona uma visão mais abrangente da relação entre ingredientes, considerando tanto aspectos químicos quanto geográficos, contribuindo para uma compreensão mais rica da complexidade da culinária e das interações alimentares.

4. Comunidades de receitas.

-> Analisando as comunidades que podem vir a se formar na rede de receitas, podemos identificar receitas que costumam ser apreciadas pelas mesmas pessoas. Ademais, utilizando essa rede e aplicando técnicas de link prediction, podemos desenvolver um algoritmo que, baseado no gosto de uma pessoa, sugira receitas que ela provavelmente irá apreciar
