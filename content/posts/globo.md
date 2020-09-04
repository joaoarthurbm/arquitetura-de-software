+++
title = "globo.com: Streaming via P2P"
date = 2019-10-22
tags = []
categories = []
youtube = "https://youtu.be/tJ_ns20SIaU"
ppt = "https://docs.google.com/presentation/d/13lwkQJQqt23MN79vjpLo_BMdRslYqELPPat6q_bdWmY/edit?usp=sharing"
+++

***

Neste encontro, Flávio Ribeiro fala sobre como aplicou o estilo arquitetural peer-to-peer (P2P) na globo.com para entregar streaming de melhor qualidade.

<b>*Importante.*</b> O primeiro comentário do vídeo possui um índice, caso você queira pular direto para algum desses temas.

<center>
<iframe width="560" height="315" src="https://www.youtube.com/embed/tJ_ns20SIaU" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

### Motivação para adotar P2P

São vários os bons momentos que podem ser extraídos dessa conversa. Em particular, gostei bastante do fato de que a motivação de Flávio teve relação com a falta de recursos (banda) na região em que morava. Ou seja, a decisão arquitetural foi tomada tendo como norte o requisito não-funcional latência e foi provocada pelo ambiente em que vivia. 

O sistema foi desenvolvido em forma de plugin para facilitar implantação, testes e experimentação.

### Migração de monolito para componentes/plugin

Também foi interessante o modo como ele remodelou o *player* de vídeo da globo.com. A arquitetura inicial era monolito e foi migrada para o conceito de componentes/plugin (<a class="external" href="http://blog.flavioribeiro.com/clappr-an-extensible-media-player-for-the-web/">clappr</a>). Isso possibilitou a troca de ângulos nos jogos da Copa do Mundo de 2014 sem a necessidade de redesenhar todos os componentes na tela. Isso o player, suas funções e o local onde o vídeo é exibido são diferentes componentes. 

***

## Minhas notas (com traços de opiniões)

<b>*Criatividade.*</b> O caso apresentado por Flávio me lembrou uma máxima: a ausência de recursos te faz criativo. Isso tem muita relação com arquitetura de software também. Fávio optou pelo estilo arquitetural P2P porque havia restrições de banda larga.

<b>*Melhoria na infraestrutura vs. Aumento no consumo de recursos dos software.*</b> Uma pergunta natural é: "a banda não melhorou significativamente ao longo do tempo?". A resposta é: sim, mas o conteúdo passou a ser mais rico e exigir mais. Ou seja, a máxima "mais recursos computacionais não resolveram o problema". O software precisou também resolver.

<b>*Arquitetura híbrida.*</b> Flávio optou por um modelo hierárquivo de P2P. Ou seja, há classes de nós dentro da rede. Nem todos estão no mesmo nível. Os pontos de presença, que possuem mais recursos, fazem parte da rede, mas estão em um nível acima dos "clientes finais".

P2P foi uma estratégia adotada para aproveitar banda de pares "mais privilegiados" estão "disperdiçando". 

<b>*Uma decisão traz um conjunto de preocupações.*</b> Decidir pelo estilo P2P trouxe preocupações adicionas:

- Como avaliar pares na rede? Fávio criou um esquema de pontuação para eleger pares com boas conexões.

- Como fazer com que os pares não se aproveitem da rede para distribuir outro conteúdo?



