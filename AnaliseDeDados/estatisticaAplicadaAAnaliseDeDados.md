<h1>📘 Estatística Aplicada à Análise de Dados </h1>
<p align="justify">
Em analise de dados, a estatistica tem se tornado mais valiosa e tem avançado com os computadores mais potentes, com algoritmos mais eficientes e empoderando a estatistica computacional. Reflexo dessa abordagem são as diversas aplicações, tais como: Programação estatistica, econometria entre outras.
</p>
<h2>💡 Análise Estatistica de decisão</h2>
<p align="justify">
Essa análise parte do pressuposto que os individuos são capoazes de expressar suas preferencias básicas quando enfrentam situações de decisão simples e a analise estatistica de decisão resolve problemas de decisão mais complexos, nos quais o agente, também chamaod de decisor, mantém suas preferencias básicas, mas é incapaz de manipular a complexidade da sitaução.
</p>

#### Aprendizado supervisionado
<p align="justify">
O aprendizado supervisionado utiliza um conjunto de dados de entrada para treinamento do algoritmo, depois, outro conjunto de dados é utilizado para validação.
</p>

#### Aprendizado não supervisionado
<p align="justify">
O aprendizado não supervisionado ocorre sem a necessidade de um conjunto de dados para treinamento, o algoritmo aprende sem a intervenção humana.
</p>

<h2>💡 Análise Estatistica</h2>
<p align="justify">
É representada pelo conjunto de metodos e processos quantitativos que servem para medir e estudar os fenomenos coletivos. Nos ultimos tempos, o aprendizado de maquina (ML) e a ciencia de dados ganharam popularidade. Espera-se que esse canpo cresça exponenciamente nos proximos anos. Mas o que é aprendizado de maquina? è um ramo de estudo no qual um modelo pode aprender automaticamente a partir de experiencias baseadas em dados sem ser modelado exclusivamente em modelos estatisticos.
</p>
<p align="justify">
A primeira etapa de um processo de aprendizagem de maquina visa entender a natureza de cada informaçao no banco de dados, para então avaliar como cada informação sera util para a solução a ser construida. 
</p>

### 🧩 Etapas do Processo

#### 1. 📥 Coleta
> É a etapa em que os dados são **capturados** de diferentes fontes, como bancos de dados, sensores, planilhas ou APIs.

- Exemplo: registros de vendas, dados de clientes, acessos a um site.

---

#### 2. 🧹 Pré-processamento
> Nessa fase, os dados são **limpos e organizados** para eliminar inconsistências, valores ausentes ou duplicados.

- Exemplo: remover linhas com erros, padronizar formatos de datas, corrigir outliers.

---

#### 3. 🔄 Transformação
> Aqui, os dados são **convertidos ou normalizados** para adequar-se à análise.

- Exemplo: converter variáveis categóricas em numéricas, criar novas colunas derivadas (como média, soma, etc.).

---

#### 4. ⛏️ Mineração de Dados
> Aplicam-se **técnicas estatísticas e algoritmos** para encontrar **padrões** ou **relações** ocultas.

- Exemplo: identificar quais produtos são comprados juntos, prever comportamento de clientes.

---

#### 5. 🧠 Avaliação e Interpretação
> Os resultados da mineração são **avaliados e interpretados** para gerar **conhecimento útil**.

- Exemplo: transformar padrões em i

<h2>💡 Amostra</h2>
<p align="justify">
Uma amostra é qualquer subconjunto de uma população. Representa um conjunto de dados da base, que possui todas as classes a serem estudadas. Definir esse conjunto é importante e crucial durante um projeto de ML, porque os dados a serem processados farão parte do subconjunto. Durante a analise, dados com ruidos são excluidos.</p>

<h2>💡 Valores médios</h2>
<p align="justify">
Os valores que, em estatistica, caracteriazm os valores médios são chamados de medidas de tendencia central. Entre as principais medidas de tendencia central destacam-se a media aritmetica e a mediana. </p>
<p align="justify">
A média aritmetica simples é o prototipo das medidas de tendencia central definido como quociente entre a soma de todos os valores da variavel e o numero de elementos desta. Ela representa abscissa do centro de gravidade do sistema formado pelos valores da variavel com massas iguais as respectivas frequencias absolutas. Geralmente é um valor que nao pertence ao conjunto original de dados.</p>

<p align="justify">
A mediana é o valor que representa centro de um conjunto de valores ordenados, ou seja, que o divide em duas partes iguais. Existem três casos a considerar:
<ol>
<li>A variável em estudo é discreta e n (número de termos) é ímpar: nesse caso, a mediana será o valor da variável que ocupa o posto de ordem.</li>
<li>A variável em estudo é discreta e n (número de termos) é par: nesse caso, não existirá no conjunto ordenado um valor que ocupe o valor central, isto é, a mediana será indeterminada.</li>
<li>A variável é contínua: em tal caso, a mediana é calculada sem considerar se o número de termos da distribuição é par ou ímpar. A fórmula empregada para seu cálculo é a mesma utilizada para os percentis.</li>
</ol></p>

<h2>💡 Medidas de dispersão</h2>
<p align="justify">
São medidas utilizadas pra avaliar o grau de variabilidade dos valores de uma variavel em torno da média, ou seja, são medidas que servem para avaliar a representativadade da media. A amplitude total de um conjunto de valores é a diferencça entre o maior e o menor valor da variavel. O desvio padrão é o prototipo das medidas de dispersão em virtude de suas propriedades matematicas de seu uso na teoria da amostragem.</p>

<h2>💡 Separar em amostra de treino e teste</h2>
<p align="justify">
Separar o conjunto de dados em amostra de treio e teste visa realizar uma segmentação dos dados cujo objetivo é utilizar a amostra de treino para ensinar o algoritmo um determinado padrão e depois, verificar com a amostra de teste se o algortimo conseguiu identificar todos os padrões necessarios para resolver o problema.</p>

<h2>💡 Validação do modelo de aprendizado de máquina</h2>
<p align="justify">
<b> Precisão</b><br>
É representada pela quantidade de verdadeiros positivos dividida pelo numero de positivos estimados pelo modelo (verdadeiro positivo + falso positivo). Também chamado de Positive Predictive Value (PPV). A expressão matemática:

```
Precisão = tp / tp + fp
tp = verdadeiros positivos, frações dos resultados que podem ser considerados corretos
tn = verdadeiros negativos, frações dos resultados que ja esperava como falso
fp = Falso possitivo
fn = Falso negativos
``` 

<b> Acurácia</b><br>
Representada pela proporção de resuldatos corretos. Raão entre as predições corretas pelo total. A seguir é apresentada a expressão matemática para seu calculo.

```
Acuracia = tp + fn / tp + tn + fp + fn
tp = verdadeiros positivos, frações dos resultados que podem ser considerados corretos
tn = verdadeiros negativos, frações dos resultados que ja esperava como falso
fp = Falso possitivo
fn = Falso negativos
```
<b> Matriz de confusão</b><br>
Em problema de classificação, uma matriz de confusão é uma tabela que permite a visualização do desempenho do algoritmo. Nas linhas, são representadas as instancias verdaderias, enquanto, nas colunas as preditas.
</p>