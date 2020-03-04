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
- **Deploy** e **Operação** caracterizam o sistema uma vez implantado em seu ambiente de execução.

???

O modelo de visões/pontos de vista é flexível o suficiente para você não precisar descrever usar todos os pontos de vista, por exemplo. Essa é a vantagem de ter um modelo com visões independentes. Além disso, cabe ao arquiteto decidir, em conjunto com stakeholders, o que e quanto descrever.

---

# Funcional

Descreve os elementos funcionais do sistema, suas responsabilidades, interfaces e relacionamentos. Tipicamente é o primeiro aspectos que stekeholders estão interessados.

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

???

Bom exemplo de deployment: https://medium.com/@lawrence143/red-hat-openshift-google-cloud-reference-architecture-a11ee5c6989d



---

# Atividade

- Procurar por descrições funcionais em projetos open source. Vamos 




