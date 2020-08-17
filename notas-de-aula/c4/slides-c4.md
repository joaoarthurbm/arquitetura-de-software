
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

<img align="center" style="width: 70%;" src="figures/c4-containers.png"/>

---

# Nível 3: Componentes

- Componentes: abstrações com responsabilidades específicas, coesas e delimitadas.
	- Componente de envio de email, componente de segurança, componente de estatísticas, *controllers*, fachadas... 

<img align="center" style="width: 70%;" src="figures/c4-componentes.png"/>


---

# Nível 4: Código

- Proximidade com o design de baixo-nível.
	- Classes, interfaces, padrões de projeto...

<img align="center" style="width: 85%;" src="figures/c4-codigo.png"/>

---

# Alguns outros diagramas

### Diagrama dinâmico

<img align="center" style="width: 82%;" src="figures/c4-dinamico.png"/>

???

Descreve como os elementos estáticos colaboram em tempo de execução para implementar um caso de uso / user story / requisito funcional.

Semelhante ao diagrama de sequência ou de comunicação de UML.

---


# Alguns outros diagramas

### Diagrama de implantação

<img align="right" style="width: 82%;" src="figures/c4-implantacao.png"/>

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




