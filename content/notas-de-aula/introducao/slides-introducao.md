background-image: url(figures/2.jpg)
count: false
<p align="center" style="color:#585B50;font-size:30px">
	<b>Introdução à Arquitetura de Software</b>
</p>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<p align="center">
	<b>joao.arthur@computacao.ufcg.edu.br</b>
</p>

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
<br>
<br>
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

???

TODO: procurar aqui por exemplos concretos que mostrem essas preocupações.

Decisões arquiteturais são tomadas tendo como norte o atendimento a requisitos não-funcionais/ atributos qualitativos. 

*Exemplo.* Optar por utilizar o MVC tem como motivação separar a lógica de negócio da apresentação e do fluxo da aplicação. Essa motivação tem uma razão de existir. 
É mais fácil manter e evoluir código cuja separação entre módulos é clara e cujos módulos são coesos. Ou seja, favorece a manutenabilidade.

*Exemplo.* Adotar uma estratégia de cache é uma decisão que está relacionada ao desempenho e latência.

*Exemplo.* Adotar microsserviços é uma decisão relacionada a vários atributos de qualidade. Por exemplo, impacta na manutenção e evolução do sistema porque permite que diferentes times evoluam separadamente os diferentes serviços oferecidos pelo sistema. Impacta também na testabilidade do sistema, pois permite testes em serviços isolados e, por consequência, mais simples. Também permite que uma indiponibilidade em um serviço não resulte na indisponibilidade de todo o sistema. Além disso, a implantação de um mesmo serviço pode ser feita em diferentes servidores para favorecer a escalabilidade do sistema.

---

## Consenso

<blockquote>Há consenso sobre o que importa e sobre não existir um único modelo para representar a arquitetura.</blockquote>
<br>

<img class="img-center" src="figures/consenso.jpeg"/>
--
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

<div class="column">
<img style="width: 100%" src="figures/41-model.png"/>
</div>

<div class="column">
<img style="width: 100%;" src="figures/siemens41.jpg"/>
</div>

</div>

<p style="font-size:10px;position:absolute;left:7%;top:70%"><b>Kruchten, Philippe B. "The 4+ 1 view model of architecture." IEEE software, 1995.</b>
</p>
<p style="font-size:10px;position:absolute;left:53%;top:70%"><b>D. Soni et. al. "Software architecture in industrial applications". ICSE, 1995.</b>
</p>









