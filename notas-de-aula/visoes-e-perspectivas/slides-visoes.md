background-image: url(figures/capa.jpg)

<br>
# Arquitetura de Software

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
### Visões, Pontos de Vista e *Sketches* arquiteturais
joao.arthur@computacao.ufcg.edu.br
---

# Relembrando

<blockquote>É inviável documentar a arquitetura em um único artefato.</blockquote>
<b>Documentação é comunicação.</b>
<br>
<img align="center" style="width: 100%;margin-left: 5px;margin-top: 18px" src="figures/visoes.png"/>
<p style="font-size:8px;position:absolute;left:80%">Copyright @ 2008 by Bredmeyer Consulting</p>

---

# Visões Arquiteturais

Viewpoints, Views, and Perspectives.

<img class="img-center" src="figures/livro-texto.jpg"/>

---

# Visões e Pontos de Vista

Uma **visão arquitetural** é a descrição de um aspecto do sistema.

**Ponto de vista** é uma coleção de padrões, templates e convenções que servem de guia para a construção das visões.

<img class="img-center" style="width: 80%;" src="figures/visao.jpg"/>

???

Aqui é importante frisar o conceito de divisão e conquista. As visões são criadas porque diminuem o problema. Juntas elas são capazes de descrever a arquitetura.

Pontos de vista agregam conhecimento legado para a construção de descrições arquiteturais. Há sim formalismos envolvidos, por exemplo, UML como linguagem de descrição pode uniformizar a maneira de descrever determinados aspectos da arquitetura. Contudo, na prática há uma heterogeneidade na maneira de descrever aspectos arquiteturais.

---

# Pontos de vista

- **Funcional**, **Informação** e **Concorrência** caracterizam a organização fundamental do sistema;
<br>
<br>
- **Desenvolvimento** existe para apoiar a construção do sistema; e
<br>
<br>
- **Implantação** e **Operação** caracterizam o sistema uma vez implantado em seu ambiente de execução.

???

O modelo de visões/pontos de vista é flexível o suficiente para você não precisar descrever usar todos os pontos de vista, por exemplo. Essa é a vantagem de ter um modelo com visões independentes. Além disso, cabe ao arquiteto decidir, em conjunto com stakeholders, o que e quanto descrever.

---

# Funcional

<blockquote>Descreve os elementos funcionais do sistema, suas responsabilidades, interfaces e relacionamentos. Tipicamente é o primeiro aspectos que stekeholders estão interessados.</blockquote>

<img class="img-center" style="width: 80%;" src="figures/funcional.jpg"/>

---

# Funcional: visão geral

Preocupações: interfaces externas, organização interna e conceitos de projeto.

Modelos: Funcionais.

Problemas e armadilhas: interfaces e responsabilidades mal definidas, infraestrutura modelada como elementos funcionais, muitas dependências, *"god" elements* etc.

Stakeholders: todos.

Aplicabilidade: todos os sistemas.

---

# Funcional: elementos

**Elementos funcionais:** parte bem definida do sistema com uma responsabilidade particular e interface bem definida. Exemplo: módulo responsável por login, módulo reponsável por log etc.

**Interfaces:** define as funções que podem ser acessadas por outros elementos. Definem entrada, saída e semântica das funções.

**Conectores:** pedaços da arquitetura que permite a conexão entre dois elementos. A diferença para a interfaces é que conectores são complexos o suficiente para demandarem uma especificação mais detalhada. 

**Entidades externas:** outros sistemas, programas, dispositivos, serviços que estão além da fronteira do sistema.

**Exemplo de Notação formal:** diagrama de componentes.

---

# Funcional: Monitor

Importante: nem todos os exemplos são bons exemplos de descrição funcional. Vamos discutí-los um a um.

<img class="img-center" style="width: 80%;" src="figures/componentes.png"/>
<p style="font-size:10px;text-align:center">Copyright - 2005 by Eoin Woods and Nick Rozanski</p>

---

# Funcional: Webshop

<img class="img-center" style="width: 80%;" src="figures/componentes-2.png"/>
<p style="font-size:10px;text-align:center;">Copyright - 2005 by Eoin Woods and Nick Rozanski</p>

---

# Funcional: Webshop

UML não é a única forma. Na verdade, vamos trabalhar com Sketeches Arquiteturais. Lembre-se: o objetivo é **comunicar**. Notação é meio, não fim.

<img class="img-center"  src="figures/sketch.png"/>


---

# Funcional: Bash


<img class="img-center" style="width: 60%;" src="figures/bash.png"/>
<p style="font-size:10px;text-align:center;">Copyright - 2005 by Eoin Woods and Nick Rozanski</p>

---

# Funcional: Eclipse

Este é um bom modelo funcional?

<img class="img-center" style="width: 60%;" src="figures/eclipse.png"/>
<p style="font-size:10px;text-align:center;">Copyright - http://aosabook.org/en/eclipse.html</p>

---

# Diretrizes para descrição da visão funcional

- Identifique os componentes -- elementos de alto-nível com responsabilidades claras.

- Identifique os relacionamentos desses elementos -- dependência, generalização, composição, uso, chamada etc.

- Diferencie grupos de componentes com diferentes formas.

- Especifique protocolos de comunicação, quando possível/preciso.  

- Seja consistente na notação. Componentes e relacionamentos similares devem ter a mesma forma.

- Evite modelar infraestrutura na visão funcional.

- Cuidado para não tornar essa visão a visão de todas as outras.

---

# Por que esta não é uma boa descrição?

<img class="img-center" style="width: 80%;" src="figures/modelo-ruim.png"/>
<p style="font-size:10px;text-align:center;">Copyright - 2005 by Eoin Woods and Nick Rozanski</p>
???

O que esse modelo comunica?

Não sabemos que componentes existem no servidor.

O que significa as linhas pontilhadas?

Elementos de hardware que não cabem como funcionais.

Aparentemente há uma decomposição em APPServer. Não sabemos qual, nem quais foram as decisões de projeto.

Muito importante: atente-se para as descrições funcionais.

---

# Decisões ruins

Por que este modelo denuncia decisões ruins?

<img class="img-center" style="width: 90%;" src="figures/god.png"/>
<p style="font-size:10px;text-align:center;">Copyright - 2005 by Eoin Woods and Nick Rozanski</p>

--

Vamos discutir um pouco sobre "god components/packages/classes", acoplamento e coesão.

---

# Informação

<blockquote>Descreve o modo como a arquitetura armazena, manipula, gerencia e distribui informação.</blockquote>

<img class="img-center" style="width: 80%;" src="figures/information.png"/>

---
# Informação: visão geral

Preocupações: estrutura, fluxo, controle de acesso, ciclo de vida, transações, qualidade, volume etc.

Modelos: diagrama de classes, diagrama de entidades e relacionamentos, diagrama de fluxo de dados, modelos estáticos de estruturas de dados, modelos de qualidade de dados etc.

Problemas e armadilhas: incompatibilidade, má qualidade, más definições de volume e esquemas.

Stakeholders: usuários, desenvolvedores, DBAs, entre outros.

Aplicabilidade: todo sistema que possui requisitos não-triviais de gerenciamento de informação.

---

# Informação: modelos estáticos de estruturas de dados

- Entidades
- Atributos
- Relacionamentos (associações)
- Cardinalidade

<img class="img-center" style="width: 70%;" src="figures/entidade-relacionamento.png"/>
<p style="font-size:10px;text-align:center;">Copyright - 2005 by Eoin Woods and Nick Rozanski</p>

---

# Informação: modelos estáticos de estruturas de dados

<img class="img-center" style="width: 90%;" src="figures/classe.png"/>
<p style="font-size:10px;text-align:center;">Copyright - 2005 by Eoin Woods and Nick Rozanski</p>

---

# Informação: Twitter

Como seria?

---

# Informação: fluxo

Foco no movimento da informação. Quais são os principais elementos arquiteturais e como a informação flui entre eles.

Muito adequado para sistemas *data-intensive*.


---

# Informação: Diagrama de fluxo de dados

Notação: Setas, Retângulos, Retângulos abertos e Elipses.

<img class="img-center" style="width: 70%;" src="figures/data-flow.png"/>
<p style="font-size:10px;text-align:center;">Copyright - 2005 by Eoin Woods and Nick Rozanski</p>


---

# Informação: Diagrama de máquina de estados

<img class="img-center" style="width: 90%;" src="figures/maquina-de-estados-uml.png"/>
<p style="font-size:10px;text-align:center;">Copyright - 2005 by Eoin Woods and Nick Rozanski</p>


---

# Informação: ePol

<img class="img-center" style="width: 90%;" src="figures/epol.png"/>
<p style="font-size:10px;text-align:center;">Copyright - 2020 by João Brunet</p>


???

Este diagrama tem relação forte com as regras de negócio do sistema. No caso do ePol, foi alvo de longas e profundas discussões até ser especificado em sua forma final. 

Hoje o diagrama serve de referência concreta para comunicar o ciclo de vida de um inquérito policial.

---

# Diretrizes para descrição da visão de informação

- Indentificar as entidades centrais em um sistema.

- Não é necessário detalhar toda e qualquer informação. Se seu modelo tem mais de 20 entidades e não cabe em uma página, ele não irá servir para o seu propósito, isto é, não irá comunicar.

- Você até pode, mas deve evitar diagramas de baixo-nível.

- Detalhes como acesso podem ser expressados como tabelas e comentários.

- Evitar detalhes desnecessários.

---

# Concorrência

<blockquote>Descreve a estrutura de concorrência do sistema. Identifica partes do sistema que são executadas concorrentemente e apresenta o controle dessa concorrência.</blockquote>

<img class="img-center" style="width: 40%;" src="figures/concorrencia.png"/>
<p style="font-size:10px;text-align:center;">Copyright - 2005 by Benjamin D. Esham</p>

---

# Concorrência: visão geral

Preocupações: organização das tarefas, mapeamento de elementos funcionais às tarefas, comunicação entre processos, gerenciamento de estado, sincronização, tolerância à falhas etc.

Modelos: modelos de estados e concorrência.

Problemas e armadilhas: complexidade, deadlock e condições de corrida.

Stakeholders: desenvolvedores, testadores e administradores.

Aplicabilidade: sistemas concorrentes.

---

# Concorrência

<img class="img-center" style="width: 75%;" src="figures/diagrama-concorrente.png"/>
<p style="font-size:10px;text-align:center;">Copyright - 2005 by Eoin Woods and Nick Rozanski</p>

???

Não há uma notação padrão em UML. O que se faz é reusar componentes e pacotes e anotar identificando processos e threads, além da comunicação entre esses elementos.

---

# Concorrência

<img class="img-center" style="width: 50%;" src="figures/threads.png"/>
<p style="font-size:10px;text-align:center;">Copyright - 2005 by Eoin Woods and Nick Rozanski</p>

---

# Concorrência


<img class="img-center" style="width: 50%;" src="figures/statechart.png"/>
<p style="font-size:10px;text-align:center;">Copyright - 2005 by Eoin Woods and Nick Rozanski</p>

???

Não é incomum o uso de diagrama de atividades.

---

# Diretrizes para descrição da visão de concorrência

- Seja consistente na notação.

- Identifique os estados.

- Identifique as transições e guardas.

- Se precisar detalhes, separe o ciclo de vida de algumas threads em outro modelo.

???

---

# Desenvolvimento

<blockquote>Modela a arquitetura que apoia o processo de desenvolvimento. </blockquote>


<div class="row">

<div class="column" style="width: 10px;">
<img src="figures/layers.png"/>
</div>

<div class="column" style="width: 10px;">
<img src="figures/mvc.jpg"/>
</div>
</div>

<div class = "row">
<div class="column" style="width: 10px;">
<img src="figures/pubsub.png"/>
</div>

<div class="column"  style="height: 1px">
<img src="figures/rest.png"/>
</div>

</div>

???

Aqui estão as decisões dos desenvolvedores e arquitetos em relação à organização do código. 

Abstrações, como elas estão organizadas e como se comunicação são as preocupações dessa visão. 

Aqui estamos falando de estilos e padrões arquiteturais.


---
# Desenvolvimento: visão geral

Preocupações: organização e decomposição dos módulos, padronização do projeto, padronização dos testes, organização do código-fonte.

Modelos: diagramas estruturais de módulos.

Problemas e armadilhas: muitos detalhes.

Stakeholders: desenvolvedores e testadores.

Aplicabilidade: todos os sistemas.

---

# Desenvolvimento

<img class="img-center" style="width: 65%;" src="figures/camadas.png"/>
<p style="font-size:10px;text-align:center;">Copyright - 2005 by Eoin Woods and Nick Rozanski</p>


---
# Desenvolvimento: ePol

<img class="img-center" style="width: 75%;" src="figures/epol-dev.png"/>
<p style="font-size:10px;text-align:center;">Copyright - 2020 by João Brunet</p>

---

# Desenvolvimento: perguntas

Na prática, focamos muito na organização em pacotes/módulos e na comunicação dessas partes. Contudo, outras perguntas são também importantes nessa visão:

- Como o código está organizado nos arquivos?
- Como os arquivos serão agrupados em módulos?
- Como será o build do código-fonte?
- Quais testes e como serão executados?
􏰀- Como será coordenado o desenvolvimento?

---

# Diretrizes para descrição da visão de desenvolvimento

- Identificar e classificar módulos e responsabilidades.

- Definir relacionamentos e dependências.

- Organizar visualmente as abstrações (camadas, por exemplo).

- Definir e explicitar regras entre camadas, grupos etc.

- Se precisar detalhes, separe o ciclo de vida de algumas threads em outro modelo.


---

# Implantação

<blockquote>Descreve o ambiente físico em que o sistema será implantado.</blockquote>

<img class="img-center" style="width: 75%;" src="figures/deployment.png"/>


???

Aqui estamos falando das máquinas, servidores, balanceadores de carga, dispositivos de armazenamentos etc.

---

# Implantação: visão geral

Preocupações: hardware necessário, sistemas externos, compatibilidade de tecnologia, requisitos de rede, restrições físicas etc.

Modelos: diagramas de implantação.

Problemas e armadilhas: preocupação tardia com o ambiente, falta de especialistas, incertezas na especificação do ambiente, etc. 

Stakeholders: Devops, Administradores de sistema, desenvolvedores e testadores.

Aplicabilidade: sistemas com implantação não tivial.


---

# Implantação

<img class="img-center" style="width: 73%;" src="figures/implantacao-uml.png"/>
<p style="font-size:10px;text-align:center;">Copyright - 2005 by Eoin Woods and Nick Rozanski</p>

---

# Implantação: rede

<img class="img-center" style="width: 85%;" src="figures/network.png"/>
<p style="font-size:10px;text-align:center;">Copyright - 2005 by Eoin Woods and Nick Rozanski</p>

---

Bom exemplo de deployment: https://medium.com/@lawrence143/red-hat-openshift-google-cloud-reference-architecture-a11ee5c6989d



---

# Atividade

- Procurar por boas descrições funcionais em projetos open source.
- Procurar descrições que podem ser melhoradas. Apontar problemas e sugerir soluções.




