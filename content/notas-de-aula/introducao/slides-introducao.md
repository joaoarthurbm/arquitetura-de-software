background-image: url(figures/capa.jpg)
---

<br>

<blockquote>Não há definição única de Arquitetura de Software.</blockquote>
<br>
<br>
<img align="center" style="width: 100%;" src="figures/books.jpg"/>

???

Arquitetura de Software é um conceito chave na área de Engenharia de Software e vem sendo discutida com mais profundidade desde a década de 90, quando vários pesquisadores concentraram-se em definir e explorar suas diversas formas de especificação e representação.

Embora muito esforço tenha sido empregado, não existe atualmente uma definição universal de Arquitetura de Software. Pesquisadores e engenheiros de software divergem no conteúdo, na forma e em que momento a arquitetura deve ser especificada. De fato, atualmente, a abordagem mais aceita é a que relativiza o papel da arquitetura. Isto é, não existe ‘A arquitetura’, mas sim um conjunto de visões arquiteturais que abordam os pontos de interesses de diferentes stakeholders.

---

## Arquitetura de Software: partes e relacionamentos

<blockquote>Arquitetura é um conjunto de <b>partes</b> que compõem o sistema e o <b>ambiente</b> em que está inserido, suas <b>responsabilidades</b> e seus <b>relacionamentos</b>.</blockquote>
<br>

- *Partes*: componentes, pacotes, subsistemas, camadas...

- *Ambiente*: infraestrutura, stakeholders, configuração...

- *Responsabilidades*: não-funcionais e funcionais

- *Relacionamentos*: interação entre as partes

???

### Partes

Algumas diferentes visões sobre o mesmo conjunto de artefatos estão em jogo aqui. Neste momento vamos detalhar mais os elementos de software, por enquanto.

Não quero encerrar a discussão do que é um componente, um módulo ou pacote. O importante é termos noção de que estamos falando de uma parte (*chunk*) de software e como ela se relaciona com as outras partes. Vamos chamar de componente como sinônimo de parte, não de componente formalmente definido em Engenharia de Software.

Esses componentes precisam ter alta **coesão** e precisam ser acopladas umas às outras de maneira adequada.

Alta Coesão: o componente é formado por elementos fortemente relacionados. O Componente faz **uma** coisa e faz bem.

Acoplamento: os componentes devem ser acoplados de maneira adequada. Acoplamento alto dificulta a manutenção, pois aumenta o efeito "gelatina".


Outras perspectivas, pontos de visão e visões que veremos com mais detalhes tentam responder as questões:

* Como esses elementos interagem com o ambiente. Onde e como serão implantados?

* Qual é o fluxo da informação? Como é gerenciada, armazenada e apresentada?

* Que funcionalidades serão providas?

* E do ponto de vista do processo de desenvolvimento e implantação?

Os pontos de vista, visões arquiteturais e perspectivas arquiteturais serão assunto para as próximas aulas. Contudo, o que estou querendo deixar claro aqui é que há diferentes aspectos da arquitetura que interessam a diferentes stakeholders.

### Ambiente

O software é implantado e executa em plataformas, sevidores etc. Pessoas interagem com o software. Outros sistemas também. É sobre isso que estamos falando quando usamos o termo ambiente. É parte importante da arquitetura definir esse ecossistema porque permite a diferentes stakeholders ter noção exata do que, como e onde estão os seus pontos de interesse.

### Relacionamentos

As partes precisam se relacionar. Não somente as partes relacionadas ao software, mas ao hardware e, inclusive, stakeholders. Faz parte da arquitetura também descrever como se dão esses relacionamentos. Os protocolos utilizados nessa comunicação definem o modo como as interações são realizadas, bem como suas capacidades e limitações.

Stakeholder é o nome dado a qualquer pessoa ou organização que é relacionada ou está interessada no projeto. Isso inclui arquiteto, analista, desenvolvedor, cliente, usuário, entre outros.


---
name: definicao
## Arquitetura de Software: partes e relacionamentos

<blockquote>Arquitetura é um conjunto de <b>partes</b> que compõem o sistema e o <b>ambiente</b> em que está inserido, suas <b>responsabilidades</b> e seus <b>relacionamentos</b>.</blockquote>

Na prática...

---
template: definicao

<img class="img-center" src="figures/eclipse.png" alt="eclipse"/>

<a href="http://aosabook.org/en/eclipse.html" style="position:absolute;left:33%">The Architecture of Open Source Applications: Eclipse.</a>


---
template: definicao

<img class="img-center" src="figures/eclipse33features.png" alt="eclipse"/>

<a href="http://aosabook.org/en/eclipse.html" style="position:absolute;left:33%">The Architecture of Open Source Applications: Eclipse.</a>


---

template: definicao

<img class="img-center" src="figures/eclipse-deploy.png" alt="eclipse"/>

<a href="http://aosabook.org/en/eclipse.html" style="position:absolute;left:33%">The Architecture of Open Source Applications: Eclipse.</a>


---

template: definicao

<img class="img-center" src="figures/puppet-dataflow.png" alt="puppet"/>

<a href="http://aosabook.org/en/puppet.html" style="position:absolute;left:33%">The Architecture of Open Source Applications: Puppet.</a>

---

template: definicao

<img class="img-center" src="figures/puppet-dataflow2.png" alt="puppet"/>

<a href="http://aosabook.org/en/puppet.html" style="position:absolute;left:33%">The Architecture of Open Source Applications: Puppet.</a>

---

## Arquitetura de Software: conjunto de decisões

<blockquote>Arquitetura é um conjunto de <b>decisões firmes</b> e de <b>grande impacto</b>.</blockquote>
<br>

- Linguagens, persistência, integração, padrões, estilos, protocolos de comunicação, interfaces etc.

- Princípios e diretrizes.

--
count: false
<img class="img-center" src="figures/catedral.jpg" alt="drawing"/>

???
Os termos-chave aqui são "firmes" e "grande impacto". Uma decisão arquitetural é uma decisão estratégica e não se altera facilmente sem haver profundas discussões sobre o seu custo e impacto. 

*Exemplo.* Decidir por usar o estilo arquitetural REST é uma decisão arquitetural. Com o software em evolução, trocar de estilo/padrão é uma mudança complexa e de alto impacto.

*Exemplo.* Adotar um modelos relacional ao invés de um modelo não-relacional para gerenciar os dados é também uma decisão arquitetural porque tem profundo impacto em como o software será implementado e mantido.

*Exemplo.* Definir as interfaces dos subsistemas é uma decisão arquitetural. Os serviçõs que serão expostos devem ser cuidadosamente definidos e, se constantemente modificados, podem geram impacto muito grande em outros sussistemas e componentes que se relacionam com o mesmo.

*Exemplo.* A escolha de uma estrutura de dados **não** é uma decisão arquitetural. Embora importante para o projeto de baixo-nível, essa escolha não tem um impacto global no sistema. Ainda, caso seja necessário trocar uma lista por um mapa, por exemplo, a mudança não é cara do ponto de vista codificação, testes e impacto em outras partes do sistema.

---

## Arquitetura de Software: requisitos não-funcionais como norte

<blockquote>Requisitos não-funcionais norteiam decisões arquiteturais.</blockquote>
<br>


Desempenho, manutenabilidade, escalabilidade, segurança, latência, tolerância à falhas, reuso, entre outros.

- Cache e suas estratégias
- MapReduce
- MVC
- Microsserviços
- Escalabilidade horizontal
- Balanceamento de carga
- ...

???

Decisões arquiteturais são tomadas tendo como norte o atendimento a requisitos não-funcionais/ atributos qualitativos. 

*Exemplo.* Optar por utilizar o MVC tem como motivação separar a lógica de negócio da apresentação e do fluxo da aplicação. Essa motivação tem uma razão de existir. 
É mais fácil manter e evoluir código cuja separação entre módulos é clara e cujos módulos são coesos. Ou seja, favorece a manutenabilidade.

*Exemplo.* Adotar uma estratégia de cache é uma decisão que está relacionada ao desempenho e latência.

*Exemplo.* Adotar microsserviços é uma decisão relacionada a vários atributos de qualidade. Por exemplo, impacta na manutenção e evolução do sistema porque permite que diferentes times evoluam separadamente os diferentes serviços oferecidos pelo sistema. Impacta também na testabilidade do sistema, pois permite testes em serviços isolados e, por consequência, mais simples. Também permite que uma indiponibilidade em um serviço não resulte na indisponibilidade de todo o sistema. Além disso, a implantação de um mesmo serviço pode ser feita em diferentes servidores para favorecer a escalabilidade do sistema.

*Exemplo.* Adotar MapReduce para processamento de parte dos dados é uma decisão relacionada ao desepenho.

---

## Consenso

<blockquote>Há consenso sobre o que importa e sobre não existir um único modelo para representar a arquitetura.</blockquote>
<br>

<img class="img-center" src="figures/consenso.jpeg"/>
--
count: false
<p style="font-size:16px">
<b>O que importa?</b> Estrutura, responsabilidades, relacionamentos, decisões, padrões, diretrizes e atendimento a atributos de qualidade.
<br>
<br>
<b>Representação?</b> A arquitetura é vista e especificada em diferentes formas, variando de acordo com os <i>stakeholders</i>. Por exemplo, os pontos de interesse dos desenvolvedores são, certamente, diferentes dos projetistas e analistas. 
</p>

???
Essa concordância vem da impossibilidade de se descrever a arquitetura seguindo um único modelo ou, em outras palavras, uma única visão. Nesse modelo de visões arquiteturais, a arquitetura é vista e especificada em diferentes formas, variando de acordo com os stakeholders. Por exemplo, os pontos de interesse dos desenvolvedores são, certamente, diferentes dos projetistas e analistas.

É importante destacar, contudo, que as várias definições não são conflitantes do ponto de vista conceitual. De fato, há uma convergência sobre o que importa: estrutura, responsabilidades, relacionamentos, decisões e atendimento a atributos de qualidade.

---

# Visões Arquiteturais

<blockquote>É inviável documentar a arquitetura em um único artefato.</blockquote>
<b>Documentação é comunicação.</b>
<br>
<img align="center" style="width: 100%;margin-left: 5px;margin-top: 18px" src="figures/visoes.png"/>
<p style="font-size:8px;position:absolute;left:80%">Copyright @ 2008 by Bredmeyer Consulting</p>
???

Um único modelo seria muito confuso e teria que abordar muitos aspectos que são irrelevantes dependendo do stakeholder. Para agradar muitos, acabaria não agradando ninguém.

<b>Documentação é comunicação.</b> Deve ser direta, concisa, coesa e ter público alvo bem definido.

---

# Visões Arquiteturais

<blockquote>Há diferentes visões sobre a arquitetura.</blockquote>
<br>

<div class="row">
<p style="font-size:8px"><b>Kruchten, Philippe B. "The 4+ 1 view model of architecture." IEEE software, 1995.</b>
</p>

<p style="font-size:8px"><b>D. Soni et. al. "Software architecture in industrial applications". ICSE, 1995.</b>
</p>

<p style="font-size:8px"><b>Bass et. al. "Software architecture in practice." Addison-Wesley Professional, 2003.</b>
</p>

</div>

<div class="row">

<div class="column">
<img style="width: 100%" src="figures/41-model.png"/>
</div>

<div class="column">
<img style="width: 100%;" src="figures/siemens41.jpg"/>
</div>

<div class="column">
<img style="width: 100%;" src="figures/sei.png"/>
</div>

</div>

--

Em resumo:


- Como o software é decomposto do ponto de vista estrutural?
- Como se dá a comunicação dos componentes, bibliotecas e subsistemas em tempo de execução?
- Como os elementos de software se relacionam com elementos do ambiente (e. g. hardware)?


???

A ideia de entender a arquitetura como um conjunto de visões arquiteturais não é nova. Em 1974, Parnas já entendia a arquitetura como um conjunto de várias estruturas parciais e que o sistema é o conjunto dessas várias estruturas. Desde então esse conceito parte-todo permeia os relatos teóricos e práticos na área. Em 1995, Kruchten publicou um artigo influente descrevendo o modelo de visões aplicado na Rational Software. Esse modelo possui 4 visões principais e uma adicional que une essas principais: o modelo 4 + 1. As visões definidas são:

**Visão Lógica.** Essa visão captura as abstrações (classes, interfaces etc) e seus relacionamentos. Tipicamente utiliza-se diagramas de classes e de estado para descrever esses elementos. Muitas vezes envolve as principais abstrações do sistema que estão relacionadas com o domínio do problema e os padrões de baixo-nível utilizados, por exemplo, Observer, Strategy, entre outros.

**Visão de Processo.** Lida com aspectos dinâmicos do sistema, o que inclui, em essência, o controle da execução do sistema. Detalhes relacionados à concorrência, controle de threads, distribuição e tolerância à falhas são preocupações que devem ser descritas nesta visão.

**Visão de desenvolvimento.** Contempla a visão do desenvolvedor sobre o sistema. Está muito relacionada ao gerenciamento do software. A organização dos módulos, bibliotecas e subsistemas é uma das principais preocupações descritas nesta visão, que se utiliza de diagramas de componentes e de pacote para tal fim.

**Visão Física.** Pode ser vista como a visão de deploy do sistema. Nos dias atuais, o stakeholder nessa visão seria o *devops*, uma vez que ele controla onde os elementos de software serão executados. Essa visão mostra, por exemplo, em quais e quantos servidores os dados estão distribuídos e em que máquinas os serviços estão executando.

A quinta visão é a que, de certa forma, une todas as outras. Isso é feito através de Casos de Uso. Além de explicitarem requisitos funcionais, Casos de Uso capturam também requisitos para a arquitetura e, portanto, podem estar relacionados a mais de uma visão.

Durante a mesma época, engenheiros da Siemens também publicaram o modelo de visões arquiteturais utilizado na empresa. Nesse modelo há 4 visões: conceitual, visão de módulos, visão da execução e visão do código. 

**A visão conceitual** descreve as principais abstrações de alto-nível do projeto e seus relacionamentos. Nessa visão é muito comum utilizar "componente-conector" para descrever os elementos de interesse. O objetivo é apresentar os módulos de alto-nível e como se dá a comunicação entre eles. Essa visão é independente de implementação. 

 A **visão de módulos** descreve como os módulos são decompostos, isto é, decomposição funcional e camadas. Essa visão deixa claro as decisões que foram ou serão tomadas durante a implementação. Estamos falando aqui de estilos arquiteturais, por exemplo.

 A **visão de execução** descreve os aspectos dinâmicos do software, como threads, tarefas e processos. A preocupação aqui está nos atributos de qualidade como desempenho, escalabilidade e monitoramento. 

Por fim, **a visão de código** descreve como o código, bibliotecas e subsistemas estão organizados no ambiente de desenvolvimento.

Houve também um esforço do Instituto de Engenharia de Software (SEI), documentado no livro *Software Architecture In Practice*, para definição de visões arquiteturais que capturam o modelo arquitetural.  Na verdade, o termo usado é Tipos de Visão (Viewtypes). *Viewtypes* definem um conjunto de elementos e de relacionamentos que são usados para descrever a arquitetura de um determinado ponto de vista. Podemos pensar em Viewtypes como um metamodelo para as visões. Nessa contexto, há 3 grandes preocupações:

- Como o software é decomposto do ponto de vista estrutural?

- Como se dá a comunicação dos componentes, biblitecas e subsistemas em tempo de execução?

- Como os elementos de software se relacionam com elementos do ambiente (e. g. hardware)?

Ou seja, as unidades de implementação, as unidades de execução e o mapeamento dos elementos de software nos elementos de hardware.

As visões propostas são: módulo, componentes e conectores e alocação.

**Módulo.** Representa a visão estrutural da arquitetura. Aqui são descritas as abstrações e os relacionamentos entre essas abstrações. Essa visão responde a primeira pergunta acima.

**Componentes e Conectores.** Descreve os aspectos comportamentais da arquitetura. Processos, tasks, threads e objetos são colocados em perspectiva, além da forma como se comunicam. Essa visão responde a segunda pergunta acima.

**Alocação.** Descreve o mapeamento dos processos nos elementos de hardware. Essa visão é semelhante à visão física do modelo 4 + 1. Essa visão responde a terceira pergunta acima.

---

# O Modelo que adotaremos

Viewpoints, Views, and Perspectives.

<img class="img-center" src="figures/livro-texto.jpg"/>

???

# Perguntas na prática

Quais são os principais componentes e como se comunicam?
Onde esses componentes, módulos e subsistemas estão implantados?
Como a informação é gerenciada, armazenada e apresentada?
Como os atributos de qualidade são abordados?

---

# Definições

<blockquote>Stakeholder: pessoa "afetada" pelo sistema.</blockquote>

<blockquote>Visão arquitetural é a descrição de um aspecto da arquitetura do sistema.</blockquote>

<blockquote>Visão arquitetural é a descrição de um aspecto da arquitetura do sistema.</blockquote>


---

# Discussões importantes


O Arquiteto de Software não pode ser responsável por tudo.

Há equipes sem arquiteto de software. Há software sem arquitetura?









