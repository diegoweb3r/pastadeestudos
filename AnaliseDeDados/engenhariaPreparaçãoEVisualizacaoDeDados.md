<h1>📘 Engenharia, preparação e visualização de dados.</h1>
<p align="justify">
O estudo de distribuições estatisticas não é recente. A análise de dados parte do pressuposto de que os individuos são capazes de expressar suas preferencias básicas quando enfrentam situações de decisão simples. Com base nisso, a metodologiadesenvolvida pela Análise de decisão permitira a resolução de problemas de decisão mais complexos.
</p>

<h2>💡 Representação do conhecimento</h2>
<p align="justify">
A disponibilidade de dados é de grande volume (big data) esão obtidos de diversas maneiras: web, rede social, bases cientificas e etc. Porém, a quantidade de dados naão significa conhecimento, é necessário trata-los, aplicando tecnicas para mineirar dados gerando conhecimentos uteis. O tratamento de dados para por processo que requer a utilização de computadores. Tencincas adotando metodos estatisticos e IA tem possibilitado as analises de dados para tais fins.
</p>
<p align="justify">A economia baseada no conhecimento, que tem o conhecimento como arma de competitividade, ganha importancia, é patrimonico indispensavel. Dessa forma, administrar o conhecimento para adquirir vantagens competitivas, tornou-se um foco central da estratégia de concorrencia.</p>

### Descoberta de conhecimentos em base de dados

<p align="justify">O numero de dados produzidos pela sociedade tem aumentado a cada dia e nesse contexto, insere-se a área de mineiração de dados, que se dedica a explira-los e analisa-los, dando origem ao nome <b>Big Data</b>.</p>
<p align="justify">A analise de dados expliratória é uma subárea da estatistica á qual a mineração de dados está relacionada. A mineração de dados emergiu da intersecção de três areas, estatistitca clássica, inteligencia artificial e aprendizado de maquina. <p>
<p align="justify">Também conhecido como KDD (knowledge-discovery in databases) a descoberta de conhecimentos em bases de dados visa encontrar padrões em grandes volumes de dados e, a partir desses padõres, identificar novos conhecimentos. Dentre as caracteristicas masi importantes do KDD, está o grande volume de dados e a capacidade de mudança de escala com relação ao tamanho dos dados, mas o processo é mais complexo, geralmente os dados tem ruimdo ou estão incompletos, de modo que a confiabildiade seja baixa, logo o analista precisa tomar a decisão sobre quais tipos de algoritmos são necessarios, aplicando-os em  conjunto de amostra de dados especificos e sintetizando resultados. É um processo de varias etapas, não trivial, interativo e iterativo, para a identificação de padrões compreensiveis e potecilamente uteis.</p>
<p align="justify">A característica “não trivial” diz respeito à complexidade existente na execução e na manutenção dos processos de KDD: interativo: representa a relevância de conter um elemento que controle o processo; iterativo: indica a possibilidade de repetições em qualquer uma das etapas do processo; e conhecimento útil: aponta para a indicação de que o objetivo foi alcançado. As etapas do KDD apresentado por Fayyad, Piatetsky-Shapiro e Smyth (1996) estão ilustradas na figura a seguir.</p>

<div align="center">

🟪 **Seleção dos Dados**  
⬆️  
🟦 **Transformação e Pré-processamento**  
⬆️  
🟩 **Escolha da técnica de _Machine Learning_**  
⬆️  
🟨 **Treino Teste Validação**  
⬆️  
🟧 **Interpretação**

</div>

> 🔁 Processo iterativo — cada etapa pode retroalimentar as anteriores.

<p align="justify"><b>Seleção de dados:</b> Nesta etapa, são realizadas consultas em base de dados que estão relacionadas ao negócio, geralmente, grandes volumes de dados, até que sejam escolhidos todos os registros que farão parte da modelagem.</p>
<p align="justify"><b>Transformação e pré-processamento:</b> Tpecnicas de anaálise matemática estatistica são aplicadas nos dados selecionados. O objetivo é muddar a natureza de alguns dados. Esta etapa prepara o registro para os algoritmos de Machine Learning que serão aplicados</p>
<p align="justify"><b>Aprendizagem de máquina:</b> Visa extrair, de forma automática, padrões em grandes repositórios de dados. Utilizadas em grandes volumes de dados com objetivo de descorbir padrões que, a principio não poderiam ser percebidos por uma analise trivial. Nesse momento, algoritmos de aprendizagem de maquina, utilizam os dados que foram preaprados na etapa anterior. O objetivo é extrair padrões entre os dados. Nessa fase, tem custo de processamento elevado, uma vez que os algoritmos precisam validar uma grande quantidade de paramentros. Principais abordagens que podem ser utilizadas nessa fase do KDD:
<ul>
<li>Redes neurais: Rede neural Artifical (RNA) é uma técnica computacional que constroi um modelo matemático inspirado em um sistema neural biologico simplificado, com capacidade de aprendizado, generalização, associacao, robustez e abstração. Tentam aprender padrões diretamente dos dados por meio de um processo de repetidas apresentação dos dados.</li>
<li> Logica nebulosa: É uma técnica que permite construia sistemas que lidem com informações imprecisas ou subjetivas. Diferente da logica classia, oferece flexibilidade na definição e na avaliação de conceitos</li>
<li> Algoritmo genetico: É uma tecnica utilizada para a solução de problemas de busca e otimização, inspirada na teoria da evolução por seleção natural e na genetica. Problemas de otimização tipicamente envolvem tres componentes, variaveis, restrições e funções-objetivos. As variaveis descrevem os vários aspectos do problema, as restrições indicam os valores que as variavies podem assumir, e as funções objetivo são utilizadas para avaliar a solução. </li>
<li>Tecnicas estatisticas: A estatistica fornece diversos modelos e tecnicas tradicionais para a analise e interpretação de dados.
</ul>

<p align="justify"><b>Conjunto de treino, teste e validação:</b> Nessa fase, o conjunto de dados é separado em subconjuntos de treino, teste e validação, para que sejam aplicadas as técnicas mapeadas na etapa anterior. Essa fase é primordial em projetos de ciencias de dados, pois é responsavel por verificar quais modelos são mais aderentes as necessidades do negocio.</p>
</p>
<p align="justify"><b>Interpretação:</b> Os padroes obtidos serão validados pela area de negocio, assim, o cliente valida se os resultados estão de acordo com os requisitos apresentados.</p>

<p align="justify">O papel do usuário na condução de aplicações KDD é de grande importancia no processo, exemplos de fatores que controle a condução de aplicações KDD:</p>
<ul>
<li> Necessidade de formulação precisa dos objetivos a serem alcançados em um processo</li>
<li> Escolha de algoritmo de mineração de dados com potencial para geração de dados</li>
<li> Escolha entre alternativas de pré processamento dos dados.</li>
<li> Parametrização adequada de diversos algoritmos diante de cada nova situação</li>
</ul>
<p align="justify">Cabe ao analista de KDD a tarefa de orientar a execução do processo, diante de cada cenário, esse profissional utiliza de experiencias anteriores, conhecimentos para interpretar e decidir a estrategia a ser adotada. O usuario sempre tem intereação com as etapas do KDD, sendo seu papel fundamental, uma vez que detem mais conhecimento sobre o negocio.</p>

<h2>Big Data</h2>
<p align="justify">O termo refere-se a um grande conjunto de dados gerados e armazenados, no qual os aplicativos de processamento desses dados tradicionais ainda nao conseguem atuar em um tempo aceitavel. Na atualidade, o big data se tornou essencial para as relações economicas e sociais.</p>
<ul>
<li> Volume: Capacidade de coletar, processar e armazenar conjuntos de dados muito grandes.</li>
<li> Velocidade: Velocidade de geração de dados e frequencia de entrega.</li>
<li> Variedade: Referem-se os dados de diferentes fontes e tipos que podem ser estruturados ou não.</li>
<li> Variabilidade: Refere-se a estabelecer se a estrutura de contextualização do fluxo de dados é regular e confiavel. Define a necessidade de obter dados significativos, considerando todas as circunstancias possiveis</li>
<li>Veracidade: Referem-se a vieses, ruidos e anormalidades nos dados. É aqui que precisamos ser capazes de identificar a relevancia dos dados e garantir que a limpeza de dados seja feita para armazenar apenas dados valiosos.</li>
<li> Valor: Refere-se ao proposito, cenario ou resultado comercial que a solução analitica deve abordar.</li>
</ul>

<p align="justify">Os dados estruturados são dados de formato fixo e com tipos bem definidos. Números, textos, datas, entre outros organizados rigidamente na forma de tabelas com linhas e colunas em bancos de dados ou arquivos do Excel.Já os dados não estruturados são dados armazenados em um formato que facilita a leitura por seres humanos, mas que são dificilmente compreendidos por um computador, dado as suas irregularidades e ambiguidades. </p>

<h2>Governança e proteção de dados</h2>

<p align="justify">É um consenso as implicações éticas de data science, no que diz respeito a propriedade, privacidade e uso de dados. Inclusive é tema de lei, com a LGPD. A lei, tem diversos principios:</p>
<ul>
<li> Finalidade: Tratamento para propositos legitimos, especificos e informados ao titular. Sem a possibilidade de tratamento de forma incompativel com essas finalidades.</li>
<li> Adequação: Compatibildiade do tratamento com as finalidades informadas ao titular.</li>
<li> Necessidade: Limitação do tratamento ao minimo necessario para realização de suas finalidades.</li>
<li>Livre acesso: Garantia, aos titulares, de consulta aos dados. </li>
<li>Qualidade dos dados: Garantia aos titulares, da exatidadao, clareza e relevancia e atualizacao dos dados.</li>
<li> Segurança: Utilização de medidas tecnicas e administrativas a porteger os dados pessoais de acessos nao autorizados.</li>
<li> Transparencia: Garantia de inofrmações claras, precisas e facilmente acessiveis sobre a realização do tratamento e os respecitvos agentes</li>
<li> Prevenção: Adoção de medidas para prevenir a ocorrencia de danos em viture do tratamento de dados pessoais.</li>
<li> Não discriminação: Impossibilidade de realização do tratamento para fins discriminatorios </li>
<li> Responsabilidade e prestação de contas: Demonstração, pelo agente, deadoção de medidas eficazes e capazes de comprovar a observancia e o cumprimento das normas de proteção de dados pessoais.</li>
</ul>