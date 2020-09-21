+++
title = "Deepmind: Arquitetura de Software e Aprendizagem de Máquina"
date = 2019-10-23
tags = []
categories = []
youtube = "https://youtu.be/qluVuMYWQrM" 
ppt = "https://drive.google.com/file/d/1GGR_yAkJ31adk0YnE7iiphcl8jt5K21b/view?usp=sharing"
+++

***

Neste bate-papo, **Marianne Monteiro** fala sobre as preocupações arquiteturais envolvidas no desenvolvimento de sistemas que utilizam aprendizagem de máquina. Algumas preocupações arquiteturais são trazidas para a discussão mais detalhada. Entre elas, destaco decisões sobre escalabilidade de maneira geral e sobre paralelismo de dados e de modelos. Por fim, foi muito interessante debater sobre propriedade intelectual de modelos, uma vez que há também a possibilidade de executá-los do lado do cliente.


<b>*Importante.*</b> O primeiro comentário do vídeo possui um índice, caso você queira pular direto para algum desses temas.

<center>
<iframe width="560" height="315" src="https://www.youtube.com/embed/qluVuMYWQrM" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</center>

***

## Minhas notas (com traços de opiniões)

Marianne traz para discussão preocupações arquiteturais que emergem quando estamos tratando de aplicações que usam aprendizagem de máquina. Eu separei algumas delas para escrever mais detalhadamente.

<b>A separação treino/modelo.</b> O treino não possui as mesmas restrições do modelos. Em primeiro lugar, sua execução pode demorar horas, dias e até semanas. Por não se tratar de código de produção, esse código pode executar em linguagens "mais lentas", em máquinas diferentes das de produção etc. Por outro lado, o código do modelo tem requisitos bem estritos sobre desempenho. Nesse sentido, Marianne destacou, por exemplo, que o código de treino pode ser em Python e o de modelo em C++, que permite melhor controle sobre o desempenho e uso de memória. Marianne aponta vários exemplos de como separar treino e modelo. Desde os mais simples (cliente-servidor) até organizações mais complexas, discutindo detalhadamente os trade-offs envolvidos.

Um ponto interessante aqui é a possibilidade de enviar o modelo para o cliente. Embora, como toda decisão arquitetual, haja vantagens em sua adoção, alguns pontos importantes foram levantados para discussão. Por exemplo, o modelo é, de certa forma, a chave do negócio de muitas empresas. Então é importante manter o sigilo e propriedade intelectual. Isso é muito dificultado se o modelo estiver sendo executado do lado do cliente. Aqui há uma clara decisão arquitetural a ser tomada tendo requisitos não-funcionais conflitantes, como simplicidade, desempenho, sigilo e propriedade intelectual.

<b>Escalando modelos.</b> Marianne discute detalhadamente abordagens sobre como escalar o treinamento de modelos. Naturalmente, tudo depende das restrições impostas pelos dados. Por exemplo, se os dados couberem em memória, é lá que são pré-processados. A execução do modelo pode ser, por exemplo, em CPU, GPUs ou em um conjunto desses componentes. Tanto escala vertical como horizontal são discutidas por Marianne em sua apresentação. 

Marianne debate muito bem sobre o conceito de paralelismo de dados e de modelos. As decisões arquiteturais giram em torno de paralelizar dados, modelos ou ambos. Lembrando sempre que isso traz complexidade ao sistema e, por isso, as decisões devem ser analisadas com cuidado antes.

<b>Perguntas importantes.</b> Uma lista de perguntas importantes apontadas por Marianne descreve bem as preocupações arquiteturais. Exemplos:

- Onde estão os dados? Qual o formato?
- Modelo cabe em memória?
- Quantas GPUs preciso para treinar o modelo de forma eficiente?
- Quanto tempo posso levar para treinar um modelo?
- Como pré-processo meus dados?
- Quais métricas são importantes?