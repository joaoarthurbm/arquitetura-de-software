+++
title = "Rodrigo Duarte: Autenticação e Autorização no OpenStack"
date = 2019-10-23
tags = []
categories = []
ppt = "https://drive.google.com/file/d/1SCwxr-uOxhvY2vvDWpBhA5S97p7W51M1/view?usp=sharing"
+++

***

Neste bate-papo **Rodrigo Duarte** nos apresenta dois aspectos arquiteturais do OpenStack. Em primeiro lugar, a migração de monilito para microsserviços e, depois, a evolução do esquema de tokens para autenticação e autorização no OpenStack. 

É muito interessante a maneira como cada escolha tomada ao longo do tempo possui um tradeoff. Nós discutimos bastante a respeito desses tradeoffs, além de outros aspectos arquiteturais, como evolução de monolito para microsserviços, documentação arquitetural, avaliação das decisões e metodologia científica, além do papel do arquiteto.

Importante: o primeiro comentário do vídeo possui um índice, caso você queira pular direto para algum desses temas.

<center>
<iframe width="560" height="315" src="https://www.youtube.com/embed/PuCSjWzWRuQ" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</center>

***

## Minhas notas (com traços de opiniões)

Decisões arquiteturais são transversais, firmes e de grande impacto.

Toda decisão expõe um tradeoff.

Migrar para microsserviços resolve muita coisa, mas também implica em uma nova gama de problemas e complexidade adicional.

O modelo como as estratégias de tokens foram avaliadas foi "coloca para executar e monitora".

Rodrigo citou a importância de se avaliar com uma metodologia adequada. Em particular, é uma bandeira interna dele essa preocupação. Segundo ele, houve casos em que as conclusões não eram adequadas porque não se usou intervalo de confiação, por exemplo.

Rodrigo citou que o "modelo de RFC" é usado para documentação arquitetural. Na prática, um documento colaborativo para discussão das decisões.

O código tende a caminhar de maneira muito mais veloz do que a documentação.

Chamei a atenção para o fato de que a descrição arquitetural deve se basear no conceito de visões. Isto é, para quem estou descrevendo? Aspectos diferentes e níveis de detalhes diferentes para diferentes stakeholders.

Também chamei a atenção para manter a documentação arquitetural apenas com aspectos realmente importantes. Esconder detalhes desnecessários.

Discutimos brevemente o conceito de walking architecture e truck-factor. Lembrei que é um problema que as decisões fiquem concentradas em apenas alguns membros. Rodrigo citou que isso acontece.

Rodrigo lembrou que, gradativamente, foi percebendo que suas decisões não eram locais. Aliado ao fato de que em alguns momentos ele era *fullstack developer*, esse cenário o fez "mais solidário", uma vez que o impacto da mudança poderia afetar, por exemplo, a implantação e ele era quem também cuidava dessa etapa.











