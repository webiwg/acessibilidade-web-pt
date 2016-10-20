---
layout: translation
date: 2010-01-01 # Data de ultima atualização do original
title: "É possível escrever de forma Simples e Clara" # Titulo traduzido
description: "The task of writing clearly and simply has never been either clear or simple.
In fact, it can be one of the most difficult of all writing tasks.
Clear and simple writing is an art to which many aspire and few achieve."

copyright: 'Copyright WebAIM' # Quem tem direitos de cópia
license: null # Caso seja uma licença padrão (MIT, GPL...) por aqui
license-custom: null # Caso a licença não seja uma padrão, por uma descrição curta dela aqui
authors: [{
    name: "WebAIM",
    link: "http://webaim.org/"
}]
translators: [{
    name: "Isadora Coffani",
    link: "https://github.com/icoffani"
}]
reviewers: []
discussion: https://github.com/webiwg/acessibilidade-web-pt/issues/29
original: {
    title: "Writing Clearly and Simply", # Titulo original, no idioma origial
    link: "http://webaim.org/techniques/writing/", # Link para documento original
    dateOfTranslation: "2016-10-09" # Data em que a tradução foi finalizada
}
isDraft: true
isReleaseCandidate: false
---

<!--
 N.T: Temos um problema, que precisa ser visto com autor original.
      Neste artigo, não tem uma data de ultima atualização. (fititnt, 2016-10-09 19:15)
-->

<!-- Geração automática de índice, inicio -->
<nav markdown="1">

## Índice de tópicos
{:.no_toc}

- Indice de Tópicos. Esta linha será substituída
{:toc}

</nav>
<!-- Geração automática de índice, fim -->

<style>
/*
  NOTA: tags styles dentro do corpo de forma provisória. Melhorar no futuro (fititnt, 2016-09-22 22:59)
*/
.programlisting {
    border: 1px dashed #990000;
    border-radius: 4px;
    background-color: #ffffc1;
    width: auto;
    margin: 0 0 1em 0;
    padding: 2px;
    overflow: auto;
}
.note {
    background-color: #F1F5F7;
    border: 1px solid #CCCCCC;
}
.example {
    background-color: #F1F5F7;
    border: 1px solid #CCCCCC;
}
.important, .tip, .note, .example {
    padding: 4px 1.5em 0px 1.5em;
    margin: 1em auto 1em auto;
    width: 85%;
    border-radius: 4px;
}
.example .title {
    background: url(media/bg.png) 0px -1700px no-repeat;
}
.note .title {
    background: url(media/bg.png) 0px -1800px no-repeat;
}
.important .title, .tip .title, .note .title, .example .title {
    padding: 3px 0 15px 35px;
    display: block;
    font-size: 1.25em;
    font-family: 'Kameron',Georgia,Times,serif;
}
.important {
    background-color: #fafaae;
    border: 1px solid #CCCCCC;
}
.important .title {
    background: url(media/bg.png) 0px -1600px no-repeat;
}
.important, .tip, .note, .example {
    padding: 4px 1.5em 0px 1.5em;
    margin: 1em auto 1em auto;
    width: 85%;
    border-radius: 4px;
}
.programlisting  code {
  background-color: transparent;
}
h3 code {
  font-size: 26px;
  font-weight: 400;
}
h4 code {
  margin-top: 1em;
  font-size: 20px;
  font-weight: 400;
}

</style>

<!--
  N.T.: Não estou certa se "Clearly and Simply" possui um significado subjetivo além do literal 
        (@icoffani, 2016-10-11 15:24)
-->

É *possível* escrever de forma "Simples e Clara"?
-----------------------------------------------

A tarefa de escrever de forma clara e simples nunca foi nem clara e nem simples.
Na verdade, ela pode ser uma das tarefas mais difíceis relacionadas à escrita.
Escrita clara e simples é uma arte à qual muitos se aspiram, porém poucos a atingem.
Ainda assim, o entendimento do conteúdo da web depende de uma escrita clara e simples.
A escrita, quando não é clara e é confusa, é uma barreira de acessibilidade a todos os leitores,
mas pode ser ainda mais difícil para pessoas que tenham dislexia ou pessoas com distúrbios
cognitivos.

<!--
  N.T.: As traduções das citações foram retiradas das traduções já realizadas por terceiros por
  se tratarem de sentenças de pessoas famosas já traduzidas anteriormente.
        (@icoffani, 2016-10-18 23:36)
-->

> "O meu objetivo é colocar no papel aquilo que vejo e aquilo que sinto da mais simples 
e melhor maneira." <br>
> —Ernest Hemingway

> "A menos que você seja um gênio, dedique-se a ser inteligível." <br>
> —Anthony Hope Hawkins

**Diferenças culturais e de linguagem importam.**
Para complicar a situação, as “regras” para escrita de forma clara e simples em inglês podem não se aplicar de
forma alguma a outras línguas, ou até mesmo entre culturas que falam a mesma língua.
Em muitos países em que se fala o Inglês, é valorizada uma comunicação escrita que seja direta e explícita.
Outras culturas sentem que esse estilo seja muito grosseiro, e até mesmo ofensivo aos leitores.

Apesar das dificuldades em definir o significado da escrita “clara e simples”,
as sugestões nesta seção ainda podem beneficiar redatores de conteúdo para web.
As sugestões servem como orientações generais para escrever em Inglês de forma clara e simples,
primeiramente a partir de uma perspectiva do Inglês Americano.
Aqueles que escrevem em outras línguas deverão procurar recursos que se apliquem especificamente àquelas
línguas.

**Habilidades cognitivas importam.**
Nem todo mundo tem o mesmo nível de leitura ou tem a habilidade de entender os conteúdos dos textos,
mesmo quando estes são apresentados de forma clara e simples.
Dislexia, distúrbios de memória, distúrbios de déficit de atenção,
e outras condições que afetam os processos cognitivos do cérebro podem comprometer a habilidade de uma 
pessoa de se beneficiar com o texto.
As orientações apresentadas abaixo vão melhorar a leitura para muitas pessoas, mas pode não ser 
aplicável para todas.

Orientações Gerais
------------------

As orientações apresentadas aqui não são uma lista completa,
também não se aplicam a toda situação, mas são um bom ponto de partida. 
Escritores que levam estas orientações a sério têm maior probabilidade de escrever de forma clara e simples.

### 1. Organize suas ideias em um esboço lógico – antes e durante o processo de escrita

Esta pode ser a orientação mais importante de todas.
Você tem de pensar claramente sobre um tópico a fim de poder comunicá-lo claramente.
O processo de organização é contínuo,
começando antes de qualquer palavra ser escrita e continuando através de todo o processo.
Não há nada de errado em reorganizar um papel conforme você o escreve.
Quando você acredita ter terminado,
aproveite a oportunidade de analisá-lo mais uma vez para ver se a organização faz sentido para você.
Se ela faz, ótimo! Se não fizer, tente novamente!

Aqui estão algumas ideias de escritores bem-sucedidos sobre a necessidade de organizar as ideias:

> "Se qualquer homem deseja escrever de forma clara, deixe-o antes ser claro em seus pensamentos." <br>
> —Johann Wolfgang von Goethe

> "Escrever é mais fácil se você tiver algo a dizer." <br>
> —Sholem Asch

### 2. Diga aos seus leitores o que você irá dizer a eles; diga a eles; depois diga a eles o que você disse a eles

A fórmula a ser seguida é começar com uma introdução ou uma visão geral das ideias do artigo, 
explicar as ideias no corpo principal do texto e, então, resumir ou revisar as ideias no final.

<div class="example" markdown="1">
<div class="title">Exemplo</div>

De forma simplificada, aqui está uma análise estrutural de ideias para um artigo sobre calvície:

<div style="border:gray solid 1px;padding:20px;margin:20px;" markdown="1">
**Introdução (Diga aos leitores o que você irá dizer a eles)**

Nem todo mundo aprecia a calvície da forma como deveriam.
Há vantagens em ser calvo.

**Corpo (Diga a eles)**

**Ideia Principal 1:**
Pessoas calvas não têm de se preocupar com o custo de cortes de cabelo.
Eles podem cortar seu próprio cabelo (o que tiver sobrado dele) com uma tesoura ou navalha.

<!--
  N.T.: o verbo "style" possui diversas aplicações no português no contexto inserido, tais como: pentear,
  fazer escova, realizar um penteado, etc. Dessa forma, foi escolhida a palavra que mais se aproxima do 
  sentido de todos os aplicáveis ao verbo citado.
        (@icoffani, 2016-10-18 00:03)
-->

**Ideia Principal 2:**
Pessoas calvas não precisam pentear seu cabelo.
Eles só têm de secar a sua cabeça com uma toalha após o banho,
e estão então livres para seguir para outras atividades mais relevantes,
tais como ler quadrinhos, praticar ioga ou escalar árvores.

**Ideia Principal 3:**
Mesmo em dias de vento, as pessoas calvas nunca têm cabelos caindo em seus olhos ou em suas bocas,
ao menos não os seus próprios,
o que torna dias de vento mais suportáveis para a vasta maioria das pessoas que não gosta do sabor
de cabelo.

**Revisão e Conclusão (Diga a eles o que você disse a eles)**

A calvície permite algumas conveniências na vida que normalmente são pouco apreciadas,
em termos de cortes de cabelo, estilo e em dias de vento. Você deveria considerar a possibilidade
de ser calvo.

</div>
</div>

### 3. Atenha-se ao ponto

Quando mais você se afasta de seu ponto principal, menor será a probabilidade de as pessoas
lembrarem dele.

### 4. Torne-o interessante

Prenda a atenção dos seus leitores através da inclusão de detalhes relevantes que os motivem a 
continuar lendo.

Aqui estão algumas ideias de indivíduos famosos sobre a importância de tornar as coisas interessantes:

> "Se você não quer ser esquecido quando morrer, escreva coisas que valham a pena serem lidas ou faça coisas
que valham a pena escrever a respeito." <br>
> —Benjamin Franklin

> "A imaginação é mais importante que o conhecimento.” "
> —Albert Einstein

> "O que queremos é uma história que comece com um terremoto e que chegue ao clímax pouco a pouco." <br>
> —Samuel Goldwyn

### 5. Escreva para seu público-alvo

Você deve escrever de modo diferente para uma classe de alunos de primeira série e para um comitê de
estudantes pós-graduados. 
Além disso, você deve levar em conta as áreas de competência das pessoas,
mesmo que elas tenham o mesmo nível de educação ou de inteligência.
Diferenças culturais e de gênero também podem desempenhar um papel ao definir o público-alvo.
À medida que você seguir em sua escrita, mantenha as características de seu público em mente
e escreva de acordo.

### 6. Assuma que seus leitores são inteligentes, mas não assuma que eles saibam sobre o tema tão bem quanto você

A quantidade de explicação que você necessita dar depende de quão familiar o seu público é com o
tópico em questão. 
Explicar conceitos não é um insulto; é benéfico,
desde que as explicações mostrem que você respeita o leitor.
Algumas pessoas com distúrbios cognitivos podem necessitar de mais explicação do que outras,
mas quando você escreve para o público em geral, assuma um nível de inteligência genérico a eles.

Alguns especialistas dizem que os escritores devem almejar uma linguagem em sua escrita de “nível
de oitava série”.
É difícil determinar com certeza o que isso significa. Muitas revistas populares,
tais como a “Reader’s Digest” e a “Ladies’ Home Journal” são escritas em torno desse nível. 
Fontes de notícias, como a “Newsweek”, são escritas em um nível ligeiramente maior, aproximando-se de 
linguagem do primeiro ano do ensino médio (décimo ano de estudo).

<!--
  N.T.: o décimo ano de estudo (10th grade) corresponde ao primeiro ano do ensino médio no Brasil.
        (@icoffani, 2016-10-18 00:17)
-->


### 7. Escreva parágrafos com coesão, construídos em torno de uma ideia única e principal

Todas as ideias de um parágrafo devem remeter ao ponto principal.
Se possível, coloque a ideia principal do parágrafo na primeira frase.

<div class="example" markdown="1">
<div class="title">Exemplo</div>

O parágrafo a seguir apresenta uma ideia sobre equipes.
A primeira frase claramente aponta a ideia principal do parágrafo (“Obstáculos são uma
realidade constante para as equipes”). 
Conforme você prosseguir com a leitura deste parágrafo,
note como as outras frases dele reforçam a ideia principal da primeira frase.

> **Obstáculos são uma realidade constante para as equipes.**
Eles ocorrem a partir do momento que uma equipe em potencial se junta até o final desta equipe.
Obstáculos também diferem tanto quanto as equipes, os desafios de performance, os ambientes 
organizacionais e os contextos de negócios que os produzem.
A equipe “Burlington Northern Intermodal”, por exemplo, encontrou pouco apoio da gestão,
políticas contra publicidade, falta de confiança de caminhoneiros e o talento medíocre no departamento intermodal.
Ela também confrontou mau tempo, competição intensa e uma economia empobrecida quando teve de provar sua estratégia
com os dois novos núcleos. 
Quaisquer desses obstáculos poderia impedir o progresso e a performance da equipe.
Nenhum deles o fez. De fato, trabalhar com os obstáculos tornou a equipe mais forte.

(De “A Sabedoria das Equipes”, por Jon R. Katzenbach e Douglas K. Smith. HarperBusiness press 1994, página 149.)

</div>

### 8. Evite gírias e jargões

Gírias e jargões podem ser úteis às pessoas que os entendem, porém podem ser confusos para aquelas que 
não entendem.

<div class="example" markdown="1">
<div class="title">Exemplo</div>

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Bad example:" width="20" height="20" /></span>
**Jargão computacional:**
Algumas empresas de software emitem demos de crippleware.
Outras emitem shareware ou nagware. Outras ainda não emitem nada, a não ser vaporware.

As palavras "crippleware," "demos," "shareware," "nagware," and "vaporware,"
são familiares a muitas pessoas na indústria computacional,
mas significam pouco ou nada para pessoas que não são familiarizadas com os termos.

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Good example:" width="20" height="20" /></span>
**Jargão de teoria social:**
A teoria crítica procura problematizar a reificação hegemônica de constructos sociais estratificados opressivos.

A frase acima descreve com precisão um aspecto do movimento social conhecido como teoria crítica,
mas utiliza termos que são de certa forma menos comuns fora da teoria crítica,
e os quais tem significados específicos dentro da perspectiva teórica.
A frase utilizada como exemplo pode confundir as pessoas que não tem familiaridade com a teoria crítica.

</div>

### 9. Utilize palavras comuns e combinações de palavras

Escritores devem empenhar-se em se comunicar com seus leitores,
e não em impressioná-los utilizando palavras incomuns ou chamativas.

<div class="example" markdown="1">
<div class="title">Example</div>

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Bad example:" width="20" height="20" /></span>
**Palavras que não são comuns (a muitas pessoas):**
A legião populosa dos andarilhos impecuniosos congregou-se nas proximidades da basílica.

<span class="inlinemediaobject"><img src="media/smiley.png" alt="Good example:" width="20" height="20" /></span>
**Palavras mais comuns:**
A grande multidão de pessoas pobres e desabrigadas se juntou nas proximidades da velha igreja.

</div>

### 10. Utilize a voz ativa

A voz passiva enfraquece a ação de uma frase por distanciar a ação dos sujeitos que a estão realizando.
A voz ativa liga o sujeito diretamente à ação.

<div class="example" markdown="1">
<div class="title">Exemplo</div>

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Bad example:" width="20" height="20" /></span>
**Passive:**

-   A refeição foi comida na festa pelos convidados.
-   Um bom momento foi tido por todos.
-   O resultado da construção de uma estrada através do terreno agrícola foi a busca no aumento de lucro por alguns donos de propriedades e a eventual perda de terras adjacentes à estrada para os projetos de construção residencial e comercial dos contratantes.

<span class="inlinemediaobject"><img src="media/smiley.png" alt="Good example:" width="20" height="20" /></span>
**Active:**

-   Os convidados comeram a refeição na festa.
-   Nós tivemos um bom momento. OU Nós nos divertimos.
-   Construir uma estrada através do terreno agrícola foi a causa de alguns donos de propriedades buscarem lucro através da venda de suas terras a contratantes que eventualmente construíram projetos residenciais e comerciais em terras adjacentes à estrada. 

</div>

### 11. Evite verbos fracos

Escritores com frequência utilizam o verbo “ser/estar” (é, são, eram, foram) quando, na verdade, verbos ativos
podem ser mais apropriados.
O uso excessivo do verbo “ser/estar” muitas vezes força os escritores a utilizarem a voz passiva mais do que
o necessário.
O verbo “ser/estar” sugere passividade porque ele conecta duas entidades que são essencialmente iguais.
A frase “A é B” essencialmente significa que “A é igual a B”.
A relação entre A e B é estática.
Em contrapartida, outros verbos – tais como “melhorar”, “esclarecer”, “modificar” ou “destruir” – implicam em um maior relacionamento dinâmico entre A e B.

<div class="example" markdown="1">
<div class="title">Exemplo</div>

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Bad example:" width="20" height="20" /></span>
**Verbo fraco ("ser"):**
Um modo de melhorar sua escrita é utilizar verbos fortes.
(A = B)
(Um modo de melhorar sua escrita = utilizar verbos fortes)
A igual relação entre as duas partes da frase implica em nenhuma ação.

<span class="inlinemediaobject"><img src="media/smiley.png" alt="Good example:" width="20" height="20" /></span>
**Verbo forte ("melhorar"):**
Utilizar verbos fortes pode *melhorar* sua escrita.
(A melhora B)
O sujeito da frase ("utilizar verbos fortes") realiza a ação de *melhorar* o objeto da frase ("sua escrita").

</div>

### 12. Utilize-se da construção de frases paralelas

Tenha certeza de que a construção da frase é consistente consigo mesma.

<div class="example" markdown="1">
<div class="title">Exemplo</div>

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Bad example:" width="20" height="20" /></span>
**Construção não-paralela:**
A nova máquina de seleção dele economiza tempo, aumenta o lucro e a satisfação do trabalhador.

<span class="inlinemediaobject"><img src="media/smiley.png" alt="Good example:" width="20" height="20" /></span>
**Construção paralela:**
A nova máquina de seleção dele economiza tempo, aumenta o lucro e aumenta a satisfação do trabalhador.

<div class="note" markdown="1">
<div class="title">Nota</div>

Um modo de descobrir se a frase contém uma construção paralela é listar cada um dos itens, um de cada vez, em uma
frase completa:

1.  A nova máquina de seleção dele economiza tempo.
2.  A nova máquina de seleção dele aumenta o lucro.
3.  A nova máquina de seleção dele a satisfação do trabalhador.

A terceira frase neste exemplo obviamente necessita de um verbo para tornar a frase completa e paralela às frases 
anteriores.

</div>
</div>

### 13. Utilize termos positivos

Enfatize como as coisas são, foram, serão ou seriam.
Até o máximo possível, evite o uso de *não são, não foram,* e outras palavras que estruturem uma frase a partir da
perspectiva como as coisas não são, não foram, não serão ou não seriam.

<div class="example" markdown="1">
<div class="title">Exemplo</div>

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Bad example:" width="20" height="20" /></span>
**Termos negativos:**

-   Não se suje.
-   Não se esqueça de regar as flores.
-   Eu não lembrei onde estive na noite passada..
-   Membros do coral não deveriam cantar de formas que não se misturem ao restante do coral.

<span class="inlinemediaobject"><img src="media/smiley.png" alt="Good example:" width="20" height="20" /></span>
**Termos positivos:**

-   Mantenha-se limpo.
-   Lembre-se de regar as flores.
-   Eu esqueci onde estive na noite passada.
-   Membros do coral deveriam cantar de formas que se misturem ao restante do coral.

</div>

### 14. Dê instruções diretas

Instruções diretas podem aumentar a compreensão e colocar um senso de responsabilidade maior no leitor.

<div class="example" markdown="1">
<div class="title">Exemplo</div>

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Bad example:" width="20" height="20" /></span>
**Instruções indiretas:**

-   Estudantes devem ler o capítulo cinco.
-   É melhor tomar um café-da-manhã saudável antes de deixar a sua casa pela manhã.
-   Pode ser perigoso tentar andar na corda bamba esticada sobre um fosso de crocodilos famintos, então esta prática é altamente desestimulada.

<span class="inlinemediaobject"><img src="media/smiley.png" alt="Good example:" width="20" height="20" /></span>
**Instruções diretas:**

-   Leiam o capítulo cinco.
-   Tome um café-da-manhã saudável antes de deixar sua casa pela manhã.
-   Não ande na corda bamba sobre um fosso de crocodilos famintos.

</div>

### 15. Evite múltiplas negações

A maioria dos leitores considera negações duplas,
ou múltiplas negações, um pouco estranhas, o que pode levar a confusão ou, no mínimo, reduzir a compreensão.

<div class="example" markdown="1">
<div class="title">Exemplo</div>

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Bad example:" width="20" height="20" /></span>
**Dupla negação:**

-   Não se esqueça de não abrir sua boca quando você cair em uma poça de lama.
-   Eu não os deixo não ajudar com os afazeres.

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Good example:" width="20" height="20" /></span>
**Negação única ou frase somente positiva:**

-   Não abra sua boca quando você cair em uma poça de lama. <br>
    **OU** <br>
    Mantenha sua boca fechada quando você cair em uma poça de lama.
-   Eu não os deixo evitar os afazeres. <br>
    **OU** <br>
    Eu me certifico de que eles ajudem com os afazeres.

</div>

### 16. Evite acrônimos e abreviações, se possível; forneça uma explicação a todos os acrônimos e abreviações

Acrônimos incomuns e abreviações não têm significado para os leitores.
Expandir os acrônimos e as abreviações permite que os leitores aprendam seus significados.
Isso é particularmente verdade na primeira vez, ou nas primeiras vezes, em que um acrônimo ou abreviação são
utilizados.

<div class="example" markdown="1">
<div class="title">Exemplo</div>

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Bad example:" width="20" height="20" /></span>
**Acrônimos e abreviações sem explicação:**
A professora teve de preparar um PEI para as crianças com DA e teve de cumprir com as regs. do NCDT de forma 
a atingir os reqs. do PAA.

<!--
  N.T.: As abreviações acima foram feitas através de tradução livre, pois não consegui encontrar nenhuma delas 
  em sites oficiais e confiáveis em português. As abreviações e acrônimos em inglês são, respectivamente: 
  Individualized Education Plan (IEP), learning disabilities (LD), No Child Left Behind (NCLB) e Annual Yearly
  Progress (AYP).
        (@icoffani, 2016-10-20 15:08)
-->

<span class="inlinemediaobject"><img src="media/smiley.png" alt="Good example:" width="20" height="20" /></span>
**Explicações dos acrônimos, com as abreviações eliminadas**
A professora teve de preparar um Programa de Educação Individualizado (PEI) para as crianças com distúrbios no 
aprendizado (DA) e teve de cumprir com as regulamentações do ato Nenhuma Criança Deixada para Trás (NCDT), de 
forma a atingir os requerimentos do Progresso Anual do Anuário (PAA).

</div>

### 17. Confira a ortografia

Utilize um corretor ortográfico automático, mas também revise o documento para palavras com ortografia correta,
porém utilizadas de forma incorreta no texto.

<div class="example" markdown="1">
<div class="title">Exemplo</div>

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Bad example:" width="20" height="20" /></span>
**Ortografia incorreta:**
Eu queria vre o pôr-do-sol por minha conta.

<!--
  N.T.: o autor do texto usou como exemplo de "ortografia incorreta" o hte = the, mas para nós esse artigo possui somente uma letra na frase em questão ("o/a"), por isso foi escolhida outra palavra da frase para dar o sentido correto ao exemplo acima.
        (@icoffani, 2016-10-20 00:16)
-->

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Another bad example:" width="20" height="20" /></span>
**Palavras incorretas escritas corretamente:**
Nossas produtos e serviços são os melhores pelo preço.

</div>

<!--
  N.T.: o autor do texto usou como exemplo de "palavras incorretas escritas corretamente" o fore = for, mas no Português não teria um exemplo válido com a norma da língua portuguesa atual. Por isso, para dar coesão à sentença, o exemplo foi substituido pela palavra nossa = nosso
        (@icoffani, 2016-10-20 00:18)
-->

### 18. Write short sentences

Readers tend to lose the main point of long, run-on sentences.
Help readers stay focused by creating shorter sentences.

> "Good things, when short, are twice as good." <br>
> —Gracián

<div class="example" markdown="1">
<div class="title">Example</div>

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Bad example:" width="20" height="20" /></span>
**Long, run-on sentence:**
We all agreed that we ought to eat at the new Greek restaurant in town,
then see a movie, and, before going home, we should stop at the grocery store to buy milk for breakfast,
because we ran out of milk earlier in the day and cold cereal doesn't taste good without milk,
especially not with orange juice, which gives cereal a tart,
citrus flavor which is fine for drinking from a glass, but not so fine for eating with flakes of cereal.

<span class="inlinemediaobject"><img src="media/smiley.png" alt="Good example:" width="20" height="20" /></span>
**Multiple shorter sentences:** <br>
**Sentence 1:** We all agreed that we ought to eat at the new Greek restaurant in town, then see a movie. <br>
**Sentence 2:** Before going home, we should stop at the grocery store to buy milk for breakfast because we ran out of milk earlier in the day. <br>
**Sentence 3:** Cold cereal doesn't taste good without milk, especially not with orange juice. <br>
**Sentence 4:** Orange juice gives cereal a tart, citrus flavor which is fine for drinking from a glass, but not so fine for eating with flakes of cereal.

</div>

### 19. Ensure that every word and paragraph is necessary

> "Omit needless words. Vigorous writing is concise.
> A sentence should contain no unnecessary words, a paragraph no unnecessary sentences,
> for the same reason that a drawing should have no unnecessary lines and a machine no unnecessary parts."
> —William Strunk, Jr.

<div class="example" markdown="1">
<div class="title">Example</div>

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Bad example:" width="20" height="20" /></span>
**Too wordy:**
It is my opinion that the explanation that was given by the teacher was delivered in a way that was not brief enough to be interesting,
and was not understood by the class.

<span class="inlinemediaobject"><img src="media/smiley.png" alt="Good example:" width="20" height="20" /></span>
**Better:**
I think that the class misunderstood the teacher's long, uninteresting explanation. <br>
**OR** <br>
The class misunderstood the teacher's long, uninteresting explanation.

</div>

### 20. When you're finished, stop

Say only what you need to say.

Additional Considerations for Users with Reading Disorders and Cognitive Disabilities
-------------------------------------------------------------------------------------

All of the writing guidelines discussed above will improve the chances that users with reading disorders or cognitive disabilities will understand the text.
Nevertheless, these guidelines will be insufficient for some users,
especially for those who read poorly, or who cannot read at all.
Text content will always pose problems for these users.
Some of the recommendations most relevant to people with cognitive disabilities are the following:

1.  **Supplement the text with illustrations.**
    The most drastic—and perhaps the most useful—solution for these audiences is to provide illustrations as alternatives to the text,
    or at least as enhancements of the textual content.
    In other words, do everything possible to clarify and simplify the text,
    then go one step further by supplementing the text with illustrations.
2.  **Reduce text to a bare minimum.**
    Pages with a large amount of text can intimidate users with reading difficulties.
    For this audience, the less you say, the better.
3.  **Be as literal as possible.**
    Some people with cognitive disabilities have a hard time distinguishing between the literal meaning of ideas and implied meaning.
    Sarcasm and parody can be especially confusing for some people.

How Can Writers Know if They Have Achieved Clarity and Simplicity?
------------------------------------------------------------------

Strictly speaking, writers cannot know for sure whether their writing is truly "clear and simple."
No matter how well writers think they have explained a concept,
some of the readers will almost always misunderstand.

### Readability tests

Algorithms, such as the Gunning Fog Index, Flesch Reading Ease Index,
and Flesch-Kincaid Index attempt to evaluate the readability or reading level of text content.
Such algorithms appeal to some experts because they are based on clear-cut mathematical formulas.
The tests produce measurable results.
Unfortunately, the tests' emphasis on quantitative (numerical) accuracy can mislead writers into thinking that achieving clear and simple writing is a well-defined,
formulaic process, when it is not.
The algorithms themselves are somewhat questionable too,
since they use such superficial criteria as the number of syllables,
the number of words, the length of sentences, etc, all of which are indirect measures of readability, at best.

Users of Microsoft Word can evaluate written content against the Flesch Reading Ease scale and the Flesch-Kincaid Grade Level scale within the word processor itself.
Word also provides a percentage count of passive sentences (the lower the percentage the better).

To activate this feature in Word,
go to the **Tools** menu, click **Options**, then click on the **Spelling & Grammar** tab.
Select the **Check grammar with spelling** check box and the **Show readability statistics** check box,
and then click OK.
To use the feature, go to **Tools &gt; Spelling & Grammar** and let Word run through the document for spelling and grammar errors.
At the end of this process,
a dialogue box will pop up showing the readability score.

<img src="media/readability.jpg" alt="The MS Word dialogue box showing readability scores of a document (in this case, there are 4% passive sentences, Flesch reading ease score of 54.7, and a Flesch-Kincaid Grade Level score of 9.1" width="321" height="312" />

Other sources of software-based readability evaluators include:

-   [Readability Calculations](http://www.micropowerandlight.com/rd.html) by [Micro Power and Light Co](http://www.micropowerandlight.com/).
-   GrammarExpert Plus, by [Wintertree software](http://www.wintertree-software.com/)

Also, an [online readability test](http://www.juicystudio.com/fog/) using the Fog index is available from Juicy Studios.

<img src="media/juicystudio.jpg" class="border" width="418" height="669" />

Although readability tests are only a superficial measure of true readability,
they can at least provide some basic feedback and give authors a general idea of how readable their documents are.

Summary
-------

It is not easy to write clearly and simply, but it is important to try.
Users are more likely to understand your writing if you take the time to organize your thoughts and write them in the clearest,
simplest form possible, taking into account your audience.
To maximize understandability for people with cognitive disabilities,
limit the text, add appropriate illustrations,
and avoid indirect or implied meanings (such as sarcasm or parody).
In the end, nearly everyone benefits from clarity and simplicity.
