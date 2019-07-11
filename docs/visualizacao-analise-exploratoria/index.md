---

layout: project

---

# Visualização de dados na apuração: análise exploratória
##### Rodrigo Menegat

Usualmente, vemos os gráficos como uma forma de apresentar informações **para o leitor**. No fluxo de trabalho usual do jornalismo de dados, sistematizado por Paul Bradshaw (2011) como [“A Pirâmide Invertida do Jornalismo de Dados”](https://onlinejournalismblog.com/2011/07/07/the-inverted-pyramid-of-data-journalism/), a visualização é a última etapa de um processo que começa com a coleta de dados e passa pela limpeza e contextualização do material antes de chegar à comunicação do conteúdo.

Entretanto, é comum usarmos técnicas de visualização com um objetivo diferente, ainda na fase inicial de um projeto. Como vimos em [outro texto deste módulo](http://meneg.at/dataviz-1/introducao-visualizacao-de-dados/), gráficos são ótimas ferramentas para organizar e extrair conhecimento de informações complexas. E o que é apurar uma matéria se não obter conhecimento sobre o tema da reportagem?

O processo de visualizar um conjunto de dados para conhecê-lo melhor se chama **visualização exploratória** ou **análise exploratória**. No restante desse texto, vou dar um exemplo prático de como isso funciona e de que forma pode ajudar no trabalho de reportagem.

### Visualizar para reportar

Não é bom começar a produzir qualquer material sem antes saber **qual cara** os dados têm. Dá até para ter alguma ideia de como são as centenas de milhares de linhas de um banco de dados usando **estatística descritiva** – ou seja, calculando valores como média, desvio padrão e mediana. Ainda assim, números são mais difíceis de compreender que imagens – e, em muitos aspectos, mais limitados. Elaborar visualizações logo na largada de uma reportagem ajuda a entender melhor com o que estamos lidando.

Suponha que estamos trabalhando em uma série de reportagens que usa os resultados do Enem 2018. **Queremos saber como os estudantes do Brasil foram no exame**. Há várias maneiras de responder à essa pergunta. Poderíamos, por exemplo, apenas reportar qual foi a nota média de todos os alunos. Isso faz sentido?

De certa forma, sim. A média é uma maneira de resumir a distribuição dos valores em um banco de dados. Usamos matemática para encontrar um valor que representa, de forma aproximada, a experiência de todos os estudantes que fizeram a prova. Entretanto, trata-se apenas disso: um resumo, um modelo, um aproximação. Será que esse cálculo retrata a realidade de forma adequada?

Para ter certeza, precisamos dar uma olhada nas notas de **todos os estudantes**. Fazer isso com uma tabela parece uma ideia péssima: imagina ter de ler e contar as pontuações de cada um dos milhões de alunos que fizeram a prova? Só de imaginar, já sinto meu cérebro derreter. 

Por sorte, há um tipo de gráfico que mostra o formato de todos os nossos dados, ou seja, mostra a **distribuição** dos valores de um banco de dados. É o histograma. 
![alt text](../imgs/histograma-enem.png "Histograma de notas do Enem 2018")

O que ele faz é contar **quantos alunos tiraram cada nota** e representar esse valor com uma barra. Nesse caso, cerca de 175 mil estudantes tiraram uma nota próxima da média – cerca de 532 pontos, valor destacado pela traço pontilhado. (Achou difícil de entender mesmo com essa explicação? [Aqui](https://pt.khanacademy.org/math/ap-statistics/quantitative-data-ap/histograms-stem-leaf/v/histograms-intro) tem uma explicação mais detalhada.) 

Veja como há barras mais altas do lado esquerdo da linha. Isso significa que a maioria dos alunos teve notas inferiores do que média aritmética simples de todas as provas. 

Isso acontece, provavelmente, porque há uma minoria de alunos com notas muito altas – ou seja, *outliers* (pontos fora da curva) que fazem com que esse indicador acabe inflacionado. Eles estão representados no gráfico pelas barras pequenas que se acumulam no canto inferior direito.

Com esse histograma simples, já descobrimos coisas que não veríamos usando estatísticas descritivas simples. Isso já é suficiente para enriquecer qualquer tipo de reportagem. Entretanto, podemos ir além. E se criarmos um desses gráficos para cada região do país?

![alt text](../imgs/multiplos-Centro-Oeste.png "Histograma de notas do Enem 2018 – Centro Oeste")
![alt text](../imgs/multiplos-Norte.png "Histograma de notas do Enem 2018 – Norte")
![alt text](../imgs/multiplos-Nordeste.png "Histograma de notas do Enem 2018 – Nordeste")
![alt text](../imgs/multiplos-Sudeste.png "Histograma de notas do Enem 2018 – Sudeste")
![alt text](../imgs/multiplos-Sul.png "Histograma de notas do Enem 2018 – Sul")

Vejamos: há um acúmulo de notas menores nas regiões Centro-Oeste, Nordeste e Norte. No Sul e no Sudeste, o pico fica deslocado para a direita, o que revela que as notas tendem a ser mais altas nessas regiões

Seguindo em frente com a exploração, podemos criar gráficos semelhantes agrupando os alunos pela cor de pele que declararam no questionário de inscrição.

![alt text](../imgs/multiplos-Amarelo.png "Histograma de notas do Enem 2018 – Amarelo")
![alt text](../imgs/multiplos-Indígena.png "Histograma de notas do Enem 2018 – Indígena")
![alt text](../imgs/multiplos-Branco.png "Histograma de notas do Enem 2018 – Branco")
![alt text](../imgs/multiplos-Preto.png "Histograma de notas do Enem 2018 – Preto")
![alt text](../imgs/multiplos-Pardo.png "Histograma de notas do Enem 2018 – Pardo")

Assim como no caso anterior, é possível observar diferenças na forma dos histogramas. Dessa vez, perceba que os alunos brancos costumam ter notas mais altas que os demais.

Poderíamos seguir fazendo recortes por um bom tempo: por gênero, faixa de renda, tipo de instituição de ensino em que o estudante está matriculado… 

Cada conjunto de visualizações proporciona um pouco mais de conhecimento sobre a base de dados com que estamos lidando – e, por consequência, mais conhecimento sobre o tema de nossas reportagens. 

Agora, em vez de simplesmente responder se os alunos brasileiros estão indo bem ou mal no Enem, podemos investigar temas como o impacto de diferenças regionais, econômicas e sociais na qualidade da educação. Saímos de uma história simplista e chegamos a uma pauta que reflete melhor a complexidade dos dados.

Vale ressaltar que o histograma é apenas um de muitos tipos de gráfico, embora seja extremamente útil para compreender aspectos diversos de uma base de dados. É possível explorar os números visualmente de várias outras maneiras, que variam desde um simples gráfico de linhas até coisas mais técnicas como um [diagrama de caixa](https://pt.wikipedia.org/wiki/Diagrama_de_caixa).

Nesse módulo, não vamos conseguir detalhar todo o potencial da visualização de dados como uma ferramenta de exploração. Entretanto, já conseguimos o essencial: perceber que gráficos podem nos ajudar a aprender mais sobre um conjunto de informações e, com isso, elaborar reportagens melhores.

Se você se interessou pelo tema, minha maior recomendação é o livro [The Trutfhful Art](https://www.amazon.com.br/Truthful-Art-Data-Charts-Communication/dp/0321934075), do Alberto Cairo. A obra toda é incrível, mas o capítulo sobre análise exploratória é o ponto mais alto do texto.