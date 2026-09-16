## Capítulo 01
### 1.1 O desenvolvimento de software
<p align="justify">
Software é representado pelas instruções e dados que algum ser humano definiu e executados por alguma máquina, cumprindo algum objetivo. 
</p>
<p align="justify">
Os dados são organizados em um computador de acordo com sua representação binária. E o objetivo de um computador é extrair informações destes dados. É importante observar a diferença entre informação e dado: o dado por si só é um valor qualquer, e informação representa interpretação desse dado. Os dados fornecidos para a máquina é denominada dados de entrada, por outro lado, os fornecidos ao ser humano, é conhecido como dados de saída.
</p>
<p align="justify">
É importante notar que o objetivo do software é que motiva sua construção, podendo ser uma necessidade humana, por exemplo. A construção de um programa é dada em etapas, um cliente ou pessoa interessada, deve especificar o que ele deve conter e realizar, essa etapa é chamada de <b> requisitos </b>. Outras etapas são:
<ul>
<li><b>Análise:</b> criam-se as especificações que detalham como o software vai funcionar</li>
<li><b>Projeto:</b> criam-se especificações que detalham o resultado da análise em termo mais próximos da implementação do software</li>
<li><b>Implementação:</b> utilizando-se uma linguagem de programação e as especificações de projeto, o software é construído.</li>
<li><b>Teste:</b> após a construção do software, são realizados testes para conferir a conformidade com os requisitos.</li>
</ul>
</p>
<p align="justify">
Após as etapas, o software é implantado, podendo ser em minutos ou semanas a depender do projeto, mas, mesmo finalizado o software não é livre de erros. É um fato que parte do investimento é gasta na correção de erros do que na elaboração do programa, surgindo a necessidade de um processo bem definido através da engenharia de software.
</p>

### 1.2 Algoritmos e lógica de programação
<p align="justify">
O estudo de algoritmo e lógica de programação é essencial no contexto de processo de criação de software. Ligada diretamente com a etapa de projeto de um software em que, mesmo sem saber qual será a linguagem, especifica-se o programa a um ponto que na implementação pode ser utilizada qualquer linguagem. Nessa etapa, é possível averiguar se o programa vai atender as especificações propostas.
</p>

#### 1.2.1 Significado de algoritmo
<p align="justify">
Um algoritmo representa um conjunto de regras para a solução de um problema, podendo ser aplicada a qualquer circunstância. É importante notar que a ordem do passo a passo é importante, então o algoritmo especifica com clareza e de forma correta as instruções de um software e que ao ser executado, fornece o resultado esperado.
</p>
<p align="justify">
Em primeiro lugar, deve-se entender o problema a ser resolvido pelo programa, depois, deve-se extrair todas as informações deste problema e relacionar com conhecimento atual, esta fase é chamada de modelagem. A modelagem do problema é resultante de um processo mental de abstração. Depois de entender o problema e como resolver, a próxima tarefa é descrever claramente os passos para chegar á solução. Além disso, é importante que essa descrição possua regras, para que todas as pessoas envolvidas consigam entende-las.
</p>
<p align="justify">
Outro fator importante nesse contexto é entender que um problema pode ser resolvido com vários algoritmos diferentes, mas, alguns são mais eficientes que outros.
</p>

### 1.3 A formalização de um algoritmo
<p align="justify">
A tarefa de especificar algoritmos para representar um programa consiste em detalhar os dados que serão processados pelo programa e as instruções executadas e para isso, pode-se fazer de forma livre, mas é altamente recomendada que seja feita seguindo alguma convenção, para que quem ler, consiga entender. É necessário definir conjuntos de regras que regulem  escrita, isso é a <b>sintaxe</b>, depois, é estabelecer as regras que permitam interpretar um algoritmo, isso é a <b>semântica</b>
</p>

#### 1.3.1 Sintaxe de um algoritmo
<p align="justify">A sintaxe de um algoritmo resume-se nas regras de escrita. Essas regras indicam quais são os tipos de comando que pode ser utilizado para escrever expressões, que realizam algum tipo de operação com os dados envolvidos.
</p>
<p align="justify">Os tipos de comandos são denominados estruturas de programação e existem três tipos: estruturas <b>sequenciais</b>, <b>decisão</b> e <b>repetição</b>. 
</p>
<p align="justify">As expressões que são escritas em estrutura de programação envolvem dados e existem vários tipos de dados: valores lógicos, números inteiros e etc, que são traduzidos em valores binários. A manipulação desses dados é feira através de variáveis e valores constantes, que representam no texto do algoritmo os dados que serão armazenados na memoria do computador.
</p>

#### 1.3.3 Semântica de um algoritmo
<p align="justify">
A semântica de um algoritmo estabelece regras para a sua interpretação. A semântica sempre acompanha a sua sintaxe, fornecendo significados, e a junção da formalização do algoritmo, com a sintaxe e semântica serve para:
<ul>
<li> Evitar ambiguidades: pois definem regras para sempre serem interpretadas da mesma forma
<li> Impedir criação de símbolos ou comandos desnecessários: representam um conjunto mínimo de regras que pode ser utilizada em qualquer algoritmo.
<li> Permitir uma aproximação com as regras de uma linguagem de programação fazendo uma fácil tradução de um algoritmo para sua implementação.
</ul>
</p>

### 1.4 Como resolver problemas
<p align="justify">
A criação de um algoritmo é uma tarefa intelectual. A partir do enunciado de um problema, deseja-se obter um algoritmo que o resolva. Pode-se afirmar que a tarefa de escrever um algoritmo seja resolver um problema.
</p>

#### 1.4.1 A análise de a síntese de um problema
<p align="justify">
A resolução de um problema envolve duas grandes fases: a análise e a síntese da solução.
</p>
<p align="justify">
Na fase de análise, o problema é entendido de forma que se descubra o que deve ser solucionado, quais são os dados necessários e as condições para resolve-lo. Depois, parte-se para sua modelagem e como resultado dessa fase tem-se a elaboração de um plano de ação, no qual a experiência em problemas similares vistos anteriormente é utilizada, fazendo abstrações e mapas mentais do problema.
</p>
<p align="justify">
Na etapa de síntese, executa-se o plano definido na fase de análise, representando os passos por meio de um algoritmo escrito em uma representação formal. 
</p>


#### 1.4.2 Modelagem de problemas
<p align="justify">
A modelagem é a principal responsável pela facilidade ou dificuldade da resolução de um problema. Na matemática e na engenharia o uso da linguagem matemática é fundamental, principalmente pela eliminação de duplo sentido.
</p>
<p align="justify">
Ocorre também na computação, com o emprego de linguagens de descrição de algoritmos e de linguagens de programação.
</p>

#### 1.4.3 O papel da lógica de programação
<p align="justify">
Lógica é uma área da matemática cujo objetivo é investigar a veracidade de suas proposições, exemplo:
<ol>
<li> Se estiver chovendo, eu pegarei meu guarda chuva.
<li> Esta chovendo
</ol>

</p>
<p align="justify">
Conclui-se que eu pegarei o guarda chuva, pois segue-se o fato que existe uma implicação lógica na primeira proposição, a qual afirma que "se estiver chovendo" implica em "eu pegarei o meu guarda chuva". Essa implicação age como uma rega que conduz a dedução do fato. Mas e se a proposição fosse:
<ol>
<li>Se estiver chovendo, eu pegarei meu guarda 
<li>Eu pegarei meu guarda chuva
</ol>
O que se conclui? Provável que esteja chovendo. 
</p>
<p align="justify">
Exemplos que fornecem uma ideia, embora simplificada, do que a lógica se preocupa em estudar. Toda lógica proposta também deve ser formalizada em elemento sintáticos e elementos semânticos.
</p>
<p align="justify">
O papel da lógica em programação de computadores está relacionado com a correta sequência de instruções que devem ser definidas para que o programa atinja seu  objetivo. Serve como verificação do programa escrito. Um algoritmo correto é aquele que, a partir de um estado inicial, suas variáveis, consegue, com a execução de suas instruções, chegar a um estado final, no qual valores das variáveis estão de acordo com a solução esperada.
</p>

### 1.5 Como se portar em um curso de computação
<p align="justify">
Uma das maiores dificuldades é de abstrair e descrever as soluções de problemas contado apenas com poucas e simples estruturas. Em carreiras de computação, as tarefas intelectuais são sempre envolvidas para a solução de problemas, que podem inclusive, gerar novos problemas, então, entende-se que é um erro decorar soluções, mas sim, entender a solução para adaptar a novos problemas. Não existe uma formula mágica, mas consegue aproveitar a experiencia em novos problemas, mas tem-se um conjunto de dicas que podem ajudar:
<ul>
<li>Tente entende-lo: O que se deve descobrir ou calcular? Quais são os dados disponíveis? Quais condições necessárias e suficientes para resolver?</li>
<li>Crie um plano pra solução: Consulte se ja resolveu um problema parecido e tente aproveitar pro analogia. Tente quebrar em problemas menores, ou enxergar em outras perspectivas.</li>
<li>Formalize a solução</li>
<li>Exame dos resultados</li>
<li>Otimize a solução</li>
</p>
