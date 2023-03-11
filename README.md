# Uma Análise de Correspondência dos Top 100 movies IMDb
Análise de Correspondência Aplicada aos dados do IMDb

# Os filmes com maior arrecadação são os mais bem avaliados?

Resumo: A  paixão mundial e a importância da indústria, seja para o mercado financeiro ou população, fica evidente a necessidade de estudos quanto a esse mercado e tentar encontrar insights. Deste modo, esse estudo está concentrado em tirar algumas conclusões em volta dessa indústria bilionária chamada de cinema. O estudo pretende verificar se os filmes com maior arrecadação são os que detém as melhores notas visto que são os que mais atraem público. O objetivo é entender a relação das variáveis do dataset trabalhado, nele contém os 100 maiores filmes que obtiveram uma maior nota em avaliação da população no site da IMDb, os filmes estão entre os anos de 1932 e 2015, esses dados foram retirados do site Kaggle e foram disponibilizados de forma pública. Utilizando do método chamado de análise de correspondência ou ANACOR, junto ao software R-Studio para realizar os cálculos necessários. O método consiste em verificar a relação entre as variáveis, no estudo será utilizado a arrecadação do filme, número de votos e a nota média do filme dentro do site. Utilizando dos percentis para que as variáveis numéricas tornem-se categóricas, visto que a ANACOR é um estudo para esse tipo de variável. Dessa forma foi possível verificar através da estatística aplicada que temos evidências para acreditar que quanto maior a arrecadação maior é o número de votos e maior é a nota do filme quando comparado ao número de votantes.

Palavras-chave: Coleta de dados. Ciência de dados. Análise de dados. Análise de correspondência. Estatística aplicada.

Abstract: The worldwide passion and importance of the industry, whether for the financial market or population, it is evident the need to study this market and try to find insights. In this way, this study is focused on drawing some conclusions around this billionaire industry called cinema. The study intends to verify if the films with the highest collection are those with the best grades, since they are the ones that attract the most public. The objective is to understand the relationship of the variables of the dataset worked, it contains the 100 greatest films that obtained a higher score in population evaluation on the IMDb website, the films are between the years 1932 and 2015, this data was taken from the Kaggle website and were made publicly available. Using the method called correspondence analysis or ANACOR, together with the R-Studio software to perform the necessary calculations. The method consists of verifying the relationship between the variables, in the study the film's collection, number of votes and the average score of the film within the site will be used. Using the percentiles so that numerical variables become categorical, since ANACOR is a study for this type of variable. In this way, it was possible to verify through applied statistics that we have evidence to believe that the greater the collection, the greater the number of votes and the greater the film's score when compared to the number of voters.

Keywords: Data collect. Data science. Data analysis. Correspondence analysis. Applied statistics.

 
## Introdução
A indústria de entretenimento é um dos que mais crescem dentro do mercado mundial, corro o risco de errar afirmando que é o maior opioide da população que necessita de uma distração para manter o discernimento necessário para o cotidiano e esse fato demonstra um possível motivo desse crescimento.
Dentre os assuntos abordados pelos estudos do lazer, a história deste fenômeno está certamente entre as mais negligenciadas. Além do número reduzido de trabalhos sobre o assunto, há também uma certa precariedade empírica nos resultados apresentados. (DIAS, 2018)
Entre o entretenimento temos as mais diversas opções, segundo o Cambridge Dictionary o entretenimento engloba entre outros, shows, filmes e televisão. Ainda poderíamos adicionar os esportes como um dos fatores que abrangem esse arcabouço. Neste artigo em questão vamos abordar sobre os filmes e o mercado dele como um todo.
A Motion Picture Association – MPA emitiu em 2021 o seu relatório anual falando sobre o cenário do entretenimento audiovisual informou que em 2021 arrecadou U$ 99,7 bilhões, isso significa um crescimento de 24% em relação ao ano anterior. O crescimento que mais chama atenção é do digital, em 2019 arrecadou U$ 28,7 bilhões e em 2021 U$ 71,9 bilhões que corresponde a um crescimento de 151%.
A crescente exponencial dos streamings é evidente e esclarecer de forma mais palpável os 151%, o maior destaque e propulsor para esse “bom” foi a Netflix que foi fundada em 1997 e hoje conta mais de 200 milhões de assinantes, para ficar mais claro a dimensão desse número, é como se todos os brasileiros tivessem assinado um dos pacotes deles. Hoje podemos enxergar “n” streamings e de todo tipo seja sobre luta, futebol, filmes, estudos, entre outros.
Visto a paixão mundial e a importância da indústria, seja para o mercado financeiro ou população, fica evidente a necessidade de estudos quanto a esse mercado e tentar encontrar insights. Deste modo, esse estudo está concentrado em tirar algumas conclusões em volta dessa indústria bilionária chamada de cinema.
No cenário brasileiro, a produção cinematográfica brasileira foi intensificada durante os anos 1970 e 1980, graças à intensa e direta ação do Estado. Antes de tudo, porque o regime militar, dentro de seus princípios de centralização político-administrativa, instaurou um projeto de institucionalização cultural de extensão nacional (AMANCIO, 2007).
Após longa crise que se estendeu por praticamente toda a década de 1980, a Embrafilme – principal instrumento das ações do governo federal para o campo cinematográfico – foi fechada em um dos primeiros atos do presidente Fernando Collor de Mello (AUTRAN, 2009).
Ainda segundo Autran, Esta situação perdurou até 1993, quando já no governo Itamar Franco foi aprovada a Lei do Audiovisual, instrumento que bem ou mal permitiu o início do reaquecimento da produção de longas-metragens, a qual em alguns anos voltou a um patamar significativo em termos numéricos.
Percebemos a evolução do cinema brasileiro e podemos citar filmes que fizeram sucesso dentro e fora do Brasil como Central do Brasil, Tropa de Elite e Cidade de Deus. Esse último aliás foi considerado o filme mais visto em uma pesquisa do site americano Internet Movie Database - IMDb e é importante citar que também foi indicado a quatro Oscar.

## Material e Métodos
Os dados foram retirados Kaggle que é uma subsidiária da Google LLC, é uma comunidade on-line de cientistas de dados e profissionais de aprendizado de máquina (WIKIPEDIA, 2022). Lá você pode fazer o download de alguns bancos de dados e até competir por soluções em que os donos do banco de dados premiam em dinheiro a melhor solução para o caso dela.Esse dataset em questão foi feito upload pelo usuário Mrityunjay Pathak, ele fez um web scraping através do python e disponibilizou esses dados de forma pública.
Nesse banco de dados contém os 100 filmes mais bem avaliados na plataforma IMDb de 1931 a 2015, dentre as variáveis existem os index, nome, ano de lançamento, categoria, tempo, gênero, nota, números de votantes e valor arrecadado.
O objetivo é fazer uma análise de correspondência simples entre a variável votos e as notas, também chamada de ANACOR, ela se utiliza de variáveis categóricas em tabelas de contingência, analisando a correspondência das matrizes.
Assim, são construídos gráficos com os componentes principais das linhas e das colunas permitindo a visualização da relação entre os conjuntos, onde a proximidade dos pontos referentes à linha e a coluna indicam associação e o distanciamento, uma repulsão (PSICOMETRIAONLINE, 2023).
Existem dois tipos de análise de correspondência a simples (AC), que iremos usar, ela é para duas variáveis categóricas e a múltipla (ACM) que será realizada quando o dataset tiver mais de duas variáveis.
Para esse experimento iremos utilizar o software estatístico R Studio, que agora faz parte da posit, ele é famoso no meio estatístico e principalmente com avanço da ciência de dados. É uma ferramenta open source que irá nos auxiliar com a análise dos dados.
A análise de correspondência é relativamente complexa, mas tentarei explicar da melhor forma possível para que seja compreendido de uma forma mais simples diante desse estudo. Para iniciar faremos uma limpeza na base que vem com algumas sujeiras que podem vir a atrapalhar nossa análise.
Uma outra mudança que precisa fazer é a alteração do tipo de variável, a análise de correspondência é para variáveis categórica e estamos comparando o número de votos com a nota média dos votantes. Isso significa que estamos falando de uma base numérica e para realizar essa alteração faremos uma divisão percentual.
Ambas as variáveis serão divididas em 3 categorias, menores_notas/menores_votos que irá conter os menores 25% dos valores, depois teremos notas_medias/votos_medios que conterá as os valores maiores que os 25% e menor que 75% geral, a última serão as 25% maiores notas, para facilitar observe a tabela abaixo. 

![image](https://user-images.githubusercontent.com/91537585/224507792-4161ff27-0ecf-428e-a159-293368a976d1.png)
         
Feito as alterações necessárias para iniciar, significa que podemos partir para a tabela de contingência que tem a responsabilidade de demonstrar alguns itens de suma importância para a sequência da nossa análise. Ela irá demonstrar a importância da categoria para o modelo, o peso de cada linha ou coluna para dimensão e a importância da dimensão para o modelo. Além do teste qui-quadrado e o p-valor que indicará se faz sentido continuarmos até plotarmos os dados ou não.

Tabela 2 – Tabela de contigência Notas x Votos

![image](https://user-images.githubusercontent.com/91537585/224507819-dcc8f875-2046-4cb6-bdab-1973adb102b8.png)
         
O primeiro valor da tabela(em preto) são os valores observados e o segundo são os valores esperados, as porcentagem corresponde aos percentuais por linha e coluna respectivamente. As estatísticas que temos que analisar melhor é o p-valor que foi menor 0,05 e isso demonstra que podemos continuar o nosso trabalho visto que estamos no cenário “ideal”. A segunda estatística a observar é a Cramer’s V que retornou 0,445. Segundo (Acastat, 2023) o grau de associação pode ser mensurado através da tabela.
Logo nossos dados têm uma associação de nível médio e detém uma qualificação para continuarmos os estudos e podemos plotar os dados para verificarmos de forma mais contundente como funciona essa relação entre as variáveis estudadas.
Imagem 1 – Mapa Perceptual Notas x Votos

![image](https://user-images.githubusercontent.com/91537585/224507829-def772f0-c1b7-40cc-ba87-63d2d6c6c775.png)

Podemos observar claramente que as menores notas ficaram mais próximas dos menos votados, as notas médias dos que tiveram uma votação média e por último os mais votados próximo das maiores notas.
É um resultado interessante visto que quanto maior o número de votantes esperamos uma variabilidade maior e consequentemente uma nota mais ao meio, mas também estatisticamente falando esperamos uma distribuição mais próxima da normal quanto maior o número de votos.
Então podemos teorizar que as pessoas que mais gostam dos filmes são as que mais vão até a plataforma votar e consequentemente os filmes que atraem um menor público acabam por sofrer as consequências de um número de votos menor e podemos comprovar através dos dados que quanto maior a arrecadação maior é o número de votantes como pode ser visto na imagem abaixo.

Imagem 2 – Mapa Perceptual Arrecadação x Votos

![image](https://user-images.githubusercontent.com/91537585/224507846-46f3905c-9132-4000-aaeb-868e8055fd58.png)

Se quisermos tirar o tira-teima quanto a arrecadação e a nota, podemos rodar o script para a tabela de contingência entre as variáveis em questão e assim identificar se existe uma correspondência direta entre elas. Como podemos observar abaixo, aceitamos H0, logo a arrecadação não tem correspondência estatisticamente falando com a média da nota dos filmes.

Tabela 3 – Tabela de contigência Arrecadação x Notas

![image](https://user-images.githubusercontent.com/91537585/224507854-61b66c77-9c6f-48af-a0ac-189a7437d457.png)

## Conclusão
O que podemos perceber com o estudo é que quanto maior a arrecadação que em geral significa levar mais pessoas a assistir e podemos considerar isso sinônimo de sucesso, os filmes que atingem uma maior arrecadação levam mais pessoas a votarem no site e por consequência pessoas que gostaram do filme dando a ele uma nota mais alta e poderíamos concluir que quanto maior o número de votos maior o sucesso de um filme.
Entretanto, percebemos que uma maior arrecadação não significa dizer que esse filme tem uma nota maior, visto que rejeitamos essa alternativa na tabela de contingência. Logo podemos concluir que quanto maior o número de espectadores maior é o número de votantes, mas que não temos como provar estatisticamente que o filme terá uma nota maior ou menor devido ao sucesso de bilheteria.

##Referências

acastat. (23 de 01 de 2023). acastat. Fonte: acastat: https://www.acastat.com/statbook/chisqassoc.htm#:~:text=between%20the%20variables.-,It%20is%20interpreted%20as%20a%20measure%20of%20the%20relative%20(strength,substantive%20relationship%20between%20two%20variables.
Amancio, T. (Jul/dez de 2007). Pacto cinema-Estado: os anos Embrafilme. ALCEU, p. 173 a 184.
Análise de correspondência para avaliação do perfil de mulheres na pós-menopausa e o uso da terapia de reposição horm o n a. (jan-fev de 2004). Cad. Saúde Pública, Rio de Janeiro, pp. 100-108.
Análise de Correspondência: Uma Aplicação do Método à Avaliação de Serviços de Vacinação. (jul/set de 1992). Cad. Saúde Públi., Rio de Janeiro, pp. 287-301.
Autran, A. (jul/dez de 2009). O cinema brasileiro contemporâneo diante do público e do mercado exibidor. Significação: revista de cultura audiovisual, vol. 36, núm. 32, pp. 119-135.
Canal Tech. (21 de 01 de 2023). Canal Tech. Fonte: Canal Tech: https://canaltech.com.br/empresa/netflix/
Dias, C. (jan/jun de 2018). HISTÓRIA E HISTORIOGRAFIA DO LAZER. Revista de História do Esporte, pp. 1-26.
Gonçalves, M. T., & dos Santos, S. R. (20-23 de 10 de 2009). APLICAÇÃO DA ANÁLISE DE CORRESPONDÊNCIA À AVALIAÇÃO INSTITUCIONAL DA FECILCAM. Encontro de produção Científica e Tecnológica.
Motion Picture Associantion - MPA. (21 de 01 de 2023). Theme Report. Fonte: motionpictures: https://www.motionpictures.org/wp-content/uploads/2022/03/MPA-2021-THEME-Report-FINAL.pdf
Pereira, C. (2001). Análise de Dados Qualitativos Aplicados às Representações Sociais. Psicologia, Vol. XV, pp. 177-204.
R CORE TEAM. R: A language and environment for statistical computing. R Foundation for Statistical Computing, Vienna, Austria. 2013. ISBN 3-900051-07-0, URL http://www.R-project.org/.
