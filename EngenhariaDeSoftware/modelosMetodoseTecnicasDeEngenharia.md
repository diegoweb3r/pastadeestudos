<div style="max-width: 900px; margin: auto; text-align: justify; font-family: Arial, sans-serif; line-height: 1.6;">

  <h1>⚙️ Modelos, métodos e técnicas da engenharia de software</h1>

  <h2>📚 Sumário</h2>
  <ul>
    <li><a href="#engenharia-de-software">Engenharia de Software</a></li>
    <li><a href="#qualidade-de-software">Qualidade de Software</a></li>
    <li><a href="#processo-de-software">Processo de Software</a></li>
    <li><a href="#modelos-de-processos-de-software">Modelos de processos de software</a></li>
    <li><a href="#metodos-ageis">Métodos ágeis</a></li>
    <li><a href="#engenharia-de-requisitos">Engenharia de Requisitos</a></li>
  </ul>

  <hr>

  <h2 id="engenharia-de-software">Engenharia de Software</h2>
  <p>
    É uma disciplina da computação que aplica princípios de engenharia ao desenvolvimento de sistemas computacionais e visa criar programas de alta qualidade, de forma sistemática, controlada, eficiente e previsível.  
    Em 1960, muitas empresas enfrentavam problemas com projetos atrasados, ultrapassavam o orçamento, o sistema com muitos erros e de manutenção difícil. A resposta a isso foi a criação de métodos, modelos e técnicas para organizar o processo de desenvolvimento, nascendo a Engenharia de Software.
  </p>

  <h2 id="qualidade-de-software">Qualidade de Software</h2>
  <p>De acordo com a ISO/IEC 25010, a qualidade de um produto de software pode ser medida em alguns aspectos:</p>
  <ul>
    <li>Funcionalidade</li>
    <li>Confiabilidade</li>
    <li>Usabilidade</li>
    <li>Eficiência de desempenho</li>
    <li>Segurança</li>
    <li>Manutenibilidade</li>
    <li>Portabilidade</li>
  </ul>

  <h2 id="processo-de-software">Processo de Software</h2>
  <p>
    Conjunto estruturado de atividades e resultados associados para produzir um produto de software, definindo as etapas pelas quais um sistema passa do início ao fim:
  </p>
  <ul>
    <li><b>Levantamento de requisitos:</b> entender o problema do cliente, determinar a solução e definir o que precisa ser feito.</li>
    <li><b>Projeto (design):</b> desenvolvimento de modelos do sistema em diferentes níveis de abstração, definição da arquitetura, componentes e design detalhado.</li>
    <li><b>Implementação (codificação):</b> criação do software por meio da codificação, verificação e testes.</li>
    <li><b>Testes:</b> verificação dinâmica se o programa prevê o comportamento esperado para os casos de teste.</li>
    <li><b>Entrega e implementação:</b> passagem do software para produção, instalação e ativação.</li>
    <li><b>Manutenção:</b> correções de erros, evolução do ambiente e adaptação a novos requisitos.</li>
  </ul>

  <h2 id="modelos-de-processos-de-software">Modelos de processos de software</h2>

  <h3>Modelo cascata</h3>
  <p>Idealizado em 1970, conhecido como top-down, caracterizado por uma sequência de atividades, sendo que cada uma deve ser finalizada completamente antes que outra inicie.</p>
  <p>🟢 Vantagens:</p>
  <ul>
    <li>Documentação produzida em cada fase</li>
    <li>Aderência a outros modelos de software</li>
    <li>Boa opção em casos que os requisitos estejam bem compreendidos</li>
  </ul>
  <p>🔴 Desvantagens:</p>
  <ul>
    <li>Próxima fase só inicia após a anterior</li>
    <li>Dificuldade de adaptar mudanças</li>
    <li>Envolvimento do cliente apenas no início e fim</li>
    <li>Cliente só terá a versão final</li>
  </ul>

  <h3>Modelo de prototipação</h3>
  <p>Consiste na criação de um modelo antes da implementação completa do sistema, atendendo a limitação do cascata (dificuldade de alterar requisitos).</p>
  <p>🟢 Vantagens:</p>
  <ul>
    <li>Solução para sistemas grandes e complexos</li>
    <li>Maior comunicação entre cliente e desenvolvedor</li>
    <li>Testado em ambiente real</li>
    <li>Pode ser usado em outros modelos como técnica</li>
  </ul>
  <p>🔴 Desvantagens:</p>
  <ul>
    <li>Protótipo pode não tratar segurança</li>
    <li>Cliente pode querer usar como produto final</li>
  </ul>

  <h3>Modelo espiral</h3>
  <p>Tentativa de unir o melhor dos modelos cascata e prototipação acrescentando a análise de riscos. Composto por quatro etapas:</p>
  <ul>
    <li><b>Planejamento:</b> determinação dos objetivos, alternativas e restrições.</li>
    <li><b>Análise de risco:</b> identificação e resolução dos riscos.</li>
    <li><b>Engenharia:</b> desenvolvimento do produto.</li>
    <li><b>Avaliação do cliente:</b> avaliação dos resultados.</li>
  </ul>
  <p>🔴 Desvantagens:</p>
  <ul>
    <li>Exige competência considerável na avaliação dos riscos.</li>
  </ul>

  <h3>Modelo baseado em componentes</h3>
  <p>Caracterizado pela criação de uma aplicação a partir de componentes previamente construídos, levando ao reuso de software.</p>
  <ul>
    <li><b>Análise de componentes:</b> busca de componentes que atendam os requisitos.</li>
    <li><b>Modificação de requisito:</b> possibilidade de ajustar um requisito para corresponder a um componente disponível.</li>
    <li><b>Projeto de sistema com reuso:</b> definição ou reutilização de frameworks.</li>
    <li><b>Desenvolvimento e integração:</b> construção das partes não fornecidas e integração.</li>
  </ul>
  <p>🟢 Vantagens:</p>
  <ul>
    <li>Redução da quantidade de software a ser produzido</li>
    <li>Maior rapidez</li>
    <li>Reuso de software</li>
  </ul>
  <p>🔴 Desvantagens:</p>
  <ul>
    <li>Controle de versão dos componentes</li>
    <li>Efeito cascata de alterações</li>
  </ul>

  <h3>Modelo RAD</h3>
  <p>Caracterizado como um processo de software incremental que enfatiza ciclo de desenvolvimento curto, acelerando a criação de sistemas funcionais.</p>
  <ol>
    <li><b>Comunicação:</b> entender os problemas de negócio e identificar características necessárias.</li>
    <li><b>Planejamento:</b> essencial pois várias equipes trabalham paralelamente.</li>
  </ol>
  <p>🔴 Desvantagens:</p>
  <ul>
    <li>Projetos grandes exigem bastante pessoal</li>
    <li>Comprometimento da equipe e cliente para manter o ciclo rápido</li>
  </ul>

  <h3>Iterações e incremento</h3>
  <h4>Desenvolvimento iterativo</h4>
  <ul>
    <li>Repetição em pequenos períodos de tempo</li>
    <li>Cada iteração pode passar por especificação, projeto, validação e evolução</li>
  </ul>
  <h4>Desenvolvimento incremental</h4>
  <ul>
    <li>Entrega em incrementos separados</li>
    <li>Cada incremento possui funcionalidades solicitadas</li>
  </ul>

  <h2 id="metodos-ageis">Métodos ágeis</h2>
  <p>São abordagens iterativas e incrementais que valorizam a flexibilidade, colaboração e entrega contínua.</p>

  <h3>Manifesto Ágil</h3>
  <ol>
    <li>Indivíduos e interações mais que processos e ferramentas</li>
    <li>Software em funcionamento mais que documentação</li>
    <li>Colaboração com cliente mais que negociação de contratos</li>
    <li>Responder a mudanças mais que seguir um plano</li>
  </ol>

  <h3>Principais métodos ágeis</h3>
  <table border="1" cellspacing="0" cellpadding="6">
    <tr>
      <th>Método</th>
      <th>Descrição resumida</th>
      <th>Características</th>
    </tr>
    <tr>
      <td>Scrum</td>
      <td>Organiza o trabalho em sprints (ciclos curtos de entregas)</td>
      <td>Papéis definidos, reuniões diárias, backlog priorizado</td>
    </tr>
    <tr>
      <td>XP</td>
      <td>Foco em qualidade técnica e feedback rápido</td>
      <td>Programação em par, testes automatizados, integração contínua</td>
    </tr>
    <tr>
      <td>Kanban</td>
      <td>Fluxo visual de tarefas</td>
      <td>Limite de tarefas em andamento, melhoria contínua</td>
    </tr>
  </table>

  <h3>Diferenças entre métodos ágeis e tradicionais</h3>
  <table border="1" cellspacing="0" cellpadding="6">
    <tr>
      <th>Aspecto</th>
      <th>Tradicionais</th>
      <th>Ágil</th>
    </tr>
    <tr>
      <td>Planejamento</td>
      <td>Detalhado no início</td>
      <td>Evolutivo e contínuo</td>
    </tr>
    <tr>
      <td>Entregas</td>
      <td>Única, ao final</td>
      <td>Frequentes e incrementais</td>
    </tr>
    <tr>
      <td>Mudanças</td>
      <td>Evitadas</td>
      <td>Bem-vindas</td>
    </tr>
    <tr>
      <td>Documentação</td>
      <td>Extensa e formal</td>
      <td>Leve e necessária</td>
    </tr>
    <tr>
      <td>Comunicação</td>
      <td>Formal</td>
      <td>Informal e colaborativa</td>
    </tr>
  </table>

  <h3>Scrum</h3>
  <p>Organiza o trabalho em Sprints, promove entrega incremental e colaboração. Papéis principais:</p>
  <ul>
    <li><b>Product Owner:</b> representa cliente, define backlog, aceita entregas.</li>
    <li><b>Scrum Master:</b> facilitador, remove impedimentos, garante processo.</li>
    <li><b>Time de desenvolvimento:</b> multidisciplinar, transforma backlog em entregas.</li>
  </ul>

  <h4>Artefatos do Scrum</h4>
  <ul>
    <li><b>Product Backlog:</b> lista priorizada de funcionalidades.</li>
    <li><b>Sprint Backlog:</b> itens selecionados para a sprint.</li>
    <li><b>Incremento:</b> soma dos itens concluídos, pronto para entrega.</li>
  </ul>

  <h4>Eventos no Scrum</h4>
  <table border="1" cellspacing="0" cellpadding="6">
    <tr>
      <th>Evento</th>
      <th>Objetivo</th>
    </tr>
    <tr>
      <td>Sprint</td>
      <td>Ciclo de desenvolvimento (1~4 semanas)</td>
    </tr>
    <tr>
      <td>Sprint Planning</td>
      <td>Planejar o que será entregue</td>
    </tr>
    <tr>
      <td>Daily Scrum</td>
      <td>Reunião diária de sincronização</td>
    </tr>
    <tr>
      <td>Sprint Review</td>
      <td>Apresentação do que foi feito</td>
    </tr>
    <tr>
      <td>Sprint Retrospective</td>
      <td>Refletir e melhorar o processo</td>
    </tr>
  </table>

  <h2 id="engenharia-de-requisitos">Engenharia de Requisitos</h2>
  <p>Requisitos definem o comportamento e propriedades de um sistema.</p>

  <h3>Tipos de requisitos</h3>
  <table border="1" cellspacing="0" cellpadding="6">
    <tr>
      <th>Requisitos</th>
      <th>Descrição</th>
      <th>Exemplo</th>
    </tr>
    <tr>
      <td>Funcionais</td>
      <td>Especificam funcionalidades</td>
      <td>Permitir cadastro e enviar e-mail</td>
    </tr>
    <tr>
      <td>Não funcionais</td>
      <td>Especificam atributos de qualidade</td>
      <td>Disponível 24h, em conformidade com LGPD</td>
    </tr>
  </table>

  <h3>Técnicas de elicitação</h3>
  <table border="1" cellspacing="0" cellpadding="6">
    <tr>
      <th>Técnica</th>
      <th>Descrição</th>
      <th>Vantagem</th>
      <th>Limitação</th>
    </tr>
    <tr>
      <td>Entrevista</td>
      <td>Conversa com stakeholders</td>
      <td>Contato direto</td>
      <td>Sujeito a interpretação</td>
    </tr>
    <tr>
      <td>Questionário</td>
      <td>Perguntas abertas e fechadas</td>
      <td>Escalável</td>
      <td>Respostas superficiais</td>
    </tr>
    <tr>
      <td>Observação direta</td>
      <td>Análise de ambiente de trabalho</td>
      <td>Evita lacunas</td>
      <td>Demanda tempo</td>
    </tr>
    <tr>
      <td>Brainstorm</td>
      <td>Geração de ideias em grupo</td>
      <td>Ideias ricas</td>
      <td>Requer moderação</td>
    </tr>
    <tr>
      <td>Prototipação</td>
      <td>Representação inicial do sistema</td>
      <td>Facilita entendimento</td>
      <td>Pode criar expectativas irreais</td>
    </tr>
  </table>

  <h3>Escolha da técnica</h3>
  <table border="1" cellspacing="0" cellpadding="6">
    <tr>
      <th>Técnica</th>
      <th>Descrição</th>
    </tr>
    <tr>
      <td>Muitos usuários</td>
      <td>Questionários</td>
    </tr>
    <tr>
      <td>Projeto inovador</td>
      <td>Brainstorm + Prototipação</td>
    </tr>
    <tr>
      <td>Requisitos vagos</td>
      <td>Entrevista + Observação direta</td>
    </tr>
    <tr>
      <td>Clientes remotos</td>
      <td>Entrevistas + Questionário</td>
    </tr>
  </table>


<h3>Especificação de requisitos</h3>
<p>Especificar requisitos significa documenta-los de forma clara, completa e compreensivel para todos os envolvidos no projeto. Serve como base de comunicação entre cliente e desenvolvedores, ajuda a evitar mal entendidos e ambuiguidades, trona os requisitos testáveis e validados. Formas de representar requisitos:</p>
<p><b>Liguagem natural estruturada:</b> Escrever requisitos de fomra textual, com liguagem clara e regras de estilo</p>
<p><b>Casos de uso:</b> Um caso de uso descreve como o usuário interage com sistema para atingir um objetivo</p>
<p><b>Cenários:</b> São narrativas informais, que mostram como um usuário realiza uma tarefa.</p>
<p> A validação verifica se os requisitos estão corretos, consistntes, commpreensiveis e viaveis e as tecnicas de validação são:</p>
<ol>
<li>Revisão com o cliente</li>
<li>Prototipação</li>
<li>Analise de consistencia e completude</li>
<li>Casos de teste derivados dos requisitos</li>
</ol>
<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th>Método de Validação</th>
    <th>Descrição</th>
    <th>Exemplo</th>
    <th>Pontos Positivos</th>
    <th>Pontos Negativos</th>
  </tr>

  <tr>
    <td><b>1 - Revisão com o Cliente</b></td>
    <td>
      Reunião entre analistas e cliente para revisar a documentação dos requisitos e garantir que representam corretamente as necessidades do usuário.
    </td>
    <td>
      Após a escrita dos requisitos, o analista apresenta cada item ao cliente, que confirma se as funcionalidades descritas atendem às suas expectativas.
    </td>
    <td>
      • Garante o alinhamento entre cliente e equipe. <br>
      • Identifica mal-entendidos logo no início.
    </td>
    <td>
      • Pode ser demorado se o cliente não estiver disponível. <br>
      • Requer boa comunicação e clareza técnica.
    </td>
  </tr>

  <tr>
    <td><b>2 - Prototipação</b></td>
    <td>
      Criação de modelos visuais ou funcionais (protótipos) do sistema para validar a compreensão dos requisitos antes da implementação.
    </td>
    <td>
      Uma tela de cadastro é criada em um software de prototipagem (como Figma ou Adobe XD) e apresentada ao cliente para feedback sobre layout e funcionalidades.
    </td>
    <td>
      • Facilita o entendimento dos requisitos abstratos. <br>
      • Permite ajustes antes da codificação.
    </td>
    <td>
      • Pode gerar expectativa de que o protótipo já é o produto final. <br>
      • Exige tempo e ferramentas específicas.
    </td>
  </tr>

  <tr>
    <td><b>3 - Análise de Consistência e Completude</b></td>
    <td>
      Verifica se os requisitos não possuem contradições, lacunas ou redundâncias e se cobrem todos os aspectos necessários do sistema.
    </td>
    <td>
      Durante a análise, é identificado que um requisito diz “o sistema deve permitir alterar o cadastro”, enquanto outro afirma “os dados do cadastro não podem ser alterados”.
    </td>
    <td>
      • Melhora a qualidade e a confiabilidade do documento de requisitos. <br>
      • Reduz riscos de erros na fase de desenvolvimento.
    </td>
    <td>
      • Exige leitura detalhada e conhecimento técnico do domínio. <br>
      • Pode ser difícil detectar inconsistências em sistemas grandes.
    </td>
  </tr>

  <tr>
    <td><b>4 - Casos de Teste Derivados dos Requisitos</b></td>
    <td>
      Transforma requisitos em casos de teste que comprovam, na prática, se cada funcionalidade cumpre o que foi especificado.
    </td>
    <td>
      Requisito: “O sistema deve autenticar usuários com login e senha.” <br>
      → Caso de teste: “Verificar se o sistema nega acesso quando a senha estiver incorreta.”
    </td>
    <td>
      • Torna os requisitos mensuráveis e verificáveis. <br>
      • Facilita a detecção de falhas antes da entrega final.
    </td>
    <td>
      • Exige tempo para criar e manter os casos de teste. <br>
      • Pode não capturar requisitos subjetivos (como usabilidade).
    </td>
  </tr>
</table>
<h3> Gestão de requisitos</h3>
<p> É o conjunto de atividades que garantem que os requisitos seja, documentados, rastreados, priorizados e atualizados durante o cliclo de vida do sistema. Inclui: Registro e organização dos requisitos, controle de mudanças, rastreabilidade e priorização.</p>
<p> Em projetos reais, nem sempre é possivel implementar todos os requisitos ao mesmo tempo, a priorização ajuda a entregar valor rapidamente, focar no que é mais importante e gerenciar restrições de tempo e recurso.</p>
<p>Tecnicas de priorização:</p>
<p><b>MoSCoW:</b> Classifica os requisitos em: Must have (M): Essencial, Should have (S): Importante, mas nao essencial, Could have (C): Desejavel, Won't Have (W): Não sera implementado agora.</p>
<p> Rastreabilidade é a capacidade de acompanhar cada requisito ao longo de todo o cliclo de vida do projeto para garantir nenhum requisito se perca e que todas as mudanças possam ser rastreadas.
</P>
</div>
