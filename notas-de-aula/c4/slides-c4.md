
background-image: url(figures/c4-livro.png)

### O Modelo C4 para Visualização de Arquitetura de Software

---

# A metáfora dos mapas

<img align="center" style="width: 100%;" src="figures/c4-mapas.jpg"/>

- Diferentes níveis de detalhes.
- Diferentes visões.
- O foco inicial está na estrutura estática.


---

## C4: <b>C</b>ontexto, <b>C</b>ontainers, <b>C</b>omponentes e <b>C</b>ódigo


<img align="center" style="width: 100%;" src="figures/c4-overview.png"/>

---

# Nível 1: Diagrama de Contexto

<img align="right" style="width: 90%;" src="figures/c4-context.png"/>

---

# Nível 2: Containers

- Containers: algo implantável.
	- *single-page application*, *datastore*, aplicação desktop, aplicação mobile, microserviços, aplicação do lado do servidor... 

<img class="center" style="width: 70%;" src="figures/c4-containers.png"/>

---

# Nível 3: Componentes

- Componentes: abstrações com responsabilidades específicas, coesas e delimitadas.
	- Componente de envio de email, componente de segurança, componente de estatísticas, *controllers*, fachadas... 

<img class="center" style="width: 70%;" src="figures/c4-componentes.png"/>


---

# Nível 4: Código

- Proximidade com o design de baixo-nível.
	- Classes, interfaces, padrões de projeto...

<img class="center" style="width: 85%;" src="figures/c4-codigo.png"/>

---

# Alguns outros diagramas

### Diagrama dinâmico

<img class="center" style="width: 82%;" src="figures/c4-dinamico.png"/>

???

Descreve como os elementos estáticos colaboram em tempo de execução para implementar um caso de uso / user story / requisito funcional.

Semelhante ao diagrama de sequência ou de comunicação de UML.

---


# Alguns outros diagramas

### Diagrama de implantação

<img class="center" style="width: 82%;" src="figures/c4-implantacao.png"/>

???

Mapeia os containers para elementos de hardware.
---

# Notação


<div class="row">

<div class="column">
<figure>
<img style="width: 70%" src="figures/notation-software-system.png"/>
<figure>
</div>

<div class="column">
<figure>
<img style="width: 70%;" src="figures/notation-container.png"/>
</figure>
</div>

</div>

<div class="row">

<div class="column">
<figure>
<img style="width: 70%" src="figures/notation-component.png"/>
<figure>
</div>

<div class="column">
<figure>
<img style="width: 70%;" src="figures/notation-relationship.png"/>
</figure>
</div>

</div>

???

O texto tem um papel importante na notação c4.

---

# Notação

<figure>
<img style="width: 100%;" src="figures/c4-todos.png"/>
</figure>


---

# Um caso concreto: Parlametria

Serviço no twitter para um sistema já desenvolvido.


<figure>
<img class="center" style="width: 40%;" src="figures/parlametria-contexto.png"/>
</figure>

???

O objetivo do sistema é analisar e monitorar discursos de deputados no twitter. Além de interagir com o twitter, interage também um sistema desenvolvido previamente para monitorar outros aspectos dos deputados.

Primeiro aspecto importante: não há interação com pessoas. Trata-se de um sistema ou sub-sistema que irá fornecer informações ao Leggo.

Poderíamos ver como um container dentro do contexto do parlametria? Sim. Como já discutimos várias vezes, não há fórmula exata.
---

# Um caso concreto: Parlametria

Serviço no twitter para um sistema já desenvolvido.


<figure>
<img class="center" style="width: 65%;" src="figures/parlametria-container.png"/>
</figure>


---

# Um caso concreto: Parlametria

Serviço no twitter para um sistema já desenvolvido.


<figure>
<img class="center" style="width: 65%;" src="figures/parlametria-implantacao.png"/>
</figure>

---

# Um caso concreto: Parlametria

Mais detalhes: <a style="font-size:20px" href="https://docs.google.com/document/d/1V3LzmH-uhWgbTMHvlyv3UDklVGQk4AWA5B518_LnN0o/edit?usp=sharing">documento de descrição arquitetural.</a>

---

# Referências

<div class="row">

<div class="column">
<figure>
<img style="width: 70%" src="figures/c4-livro.png"/>
<figure>
</div>

<div class="column">	
</div>

</div>


- https://c4model.com/
- https://www.infoq.com/articles/C4-architecture-model