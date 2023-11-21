# Modelo para Apresentação do Lab08 - Modelo Lógico e Análise de Dados em Grafos

Estrutura de pastas:

~~~
├── README.md  <- arquivo apresentando a tarefa
│
└── images     <- arquivos de imagem usados na tarefa
~~~

# Equipe `VASKO`

# Subgrupo `VASCO`
* Gabriel de Carvalho Silva Nascimento - 222103
* Breno Shigeki Guimarães Nishimoto - 220599
* Mateus da Costa e Silva Rios Alves de Andrade - 230806

## Modelo Lógico do Banco de Dados de Grafos
> Coloque aqui o modelo lógico.
> Coloque a imagem do PNG do seu modelo lógico como ilustrado abaixo (a imagem estará na pasta `image`):
>
><img src="images\grafo.png" width="400px" height="auto">
>

## Propostas de Mapeamento e Transformações

>1. Criação de um mapeamento em que ingredientes se ligam a ingrediente por participação em receitas
>2. Criação de uma rede similar à dos ingredientes, relacionando receitas através de uma projeção nas pessoas que as consomem

## Perguntas de Pesquisa/Análise Combinadas e Respectivas Análises

> Liste aqui as perguntas de pesquisa/análise e respectivas análises.
>
### Pergunta/Análise 1
> * 1. Distância grande entre entre dois ingredientes implica em baixa compatibilidade/disponibilidade na mesma região?
>   
>   * -> A análise da distância entre dois ingredientes por meio da técnica de Centralidade, especialmente utilizando a medida de Betweenness, permite identificar a proximidade ou afastamento na presença de outros ingredientes em uma rede alimentar. Uma conclusão esperada é que uma grande distância entre ingredientes pode indicar baixa compatibilidade ou disponibilidade na mesma região.
Essa abordagem é valiosa para compreender não apenas possíveis interações químicas entre os ingredientes, mas também para considerar fatores geográficos e culturais. Por exemplo, a distância entre ingredientes como alga japonesa e dendê pode refletir não apenas diferenças de sabor, mas também as preferências culinárias regionais, indicando a disponibilidade local desses ingredientes.
Dessa forma, a análise de Betweenness na rede alimentar proporciona uma visão mais abrangente da relação entre ingredientes, considerando tanto aspectos químicos quanto geográficos, contribuindo para uma compreensão mais rica da complexidade da culinária e das interações alimentares.

### Pergunta/Análise 2
> * 2. Análise da formação de comunidades de receitas.
>   
>   * -> Ao realizar uma análise das comunidades emergentes na complexa rede de receitas, é possível identificar padrões intrínsecos de preferências gastronômicas, elucidando quais receitas apresentam maior compatibilidade entre si. Esta abordagem revela-se crucial para a expansão estratégica dos cardápios, fundamentada na interconectividade entre as receitas existentes e a busca por sinergias alimentares. A utilização de técnicas sofisticadas de previsão de links possibilita a concepção de um algoritmo inovador, capacitado a sugerir receitas aos usuários com base em seus históricos alimentares, transcendo a mera recomendação óbvia. Assim, viabiliza-se a proposição de receitas inexploradas por determinado usuário, mas que ostentam elevada probabilidade de agradar, alinhada ao seu perfil gastronômico distintivo.

### Pergunta/Análise 3
> * 3. O que ingredientes considerados "hubs" têm em comum?
>   
>   * -> Ao empregar a técnica de centralidade, notadamente a centralidade de grau (Degree), podemos observar ingredientes que se comportam como "hubs", ou seja, aqueles que participam de inúmeras conexões na rede de receitas. Um boa motivo para sua ocorrência reside na caracterização desses ingredientes como elementos complementares e amplamente difundidos globalmente, conferindo-lhes a capacidade de "combinação" versátil com uma variedade de receitas distintas. Esses ingredientes, ao ostentarem elevada centralidade de grau, emergem como peças-chave na interconectividade da rede, desempenhando um papel significativo na coesão e diversidade gastronômica das receitas analisadas.

