---
layout: translation
date: 2013-08-09 # Data de ultima atualização do original
title: "Deficiências Cognitivas" # Titulo traduzido
description: "The concept of cognitive disabilities is extremely broad,
and not always well-defined. In loose terms,
a person with a cognitive disability has greater difficulty with one or more types of mental tasks than the average person.
There are too many types of cognitive disabilities to list here, but we will cover some of the major categories. "

copyright: 'Copyright WebAIM' # Quem tem direitos de cópia
license: null # Caso seja uma licença padrão (MIT, GPL...) por aqui
license-custom: null # Caso a licença não seja uma padrão, por uma descrição curta dela aqui
authors: [{
    name: "WebAIM",
    link: "http://webaim.org/"
}]
translators: [{
    name: "João Vitor Do Erre",
    link: "https://github.com/joaodoerre"
}]
reviewers: []
discussion: https://github.com/webiwg/acessibilidade-web-pt/issues/28
original: {
    title: "Cognitive Disabilities", # Titulo original, no idioma origial
    link: "http://webaim.org/articles/cognitive/", # Link para documento original
    dateOfTranslation: "2016-10-09" # Data em que a tradução foi finalizada
}
isDraft: true
isReleaseCandidate: false
---

<!-- Geração automática de índice, inicio -->
<nav markdown="1">

## Índice de tópicos
{:.no_toc}

1. Indice de Tópicos. Esta linha será substituída
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


## Intodução

### Algo para se pensar...

<span style="float: right; margin: 8px 0px 1px 10px;"><img src="media/head.jpg" alt="Imagem gerada da cabeça humana por computador" width="156" height="149"></span>
O conceito de deficiência cognitiva é extremamente amplo, e nem sempre bem definido.
De forma simplificada,
uma pessoa com deficiência cognitiva tem mais dificuldade em uma ou mais habilidades mentais que a maioria da população.
Há muitos tipos de deficiências cognitivas para listar aqui, mas nós vamos cobrir a maior parte das categorias.
A maioria das deficiências cognitivas tem algum tipo de base na biologia e fisiologia do induvíduo.
A conecção entre a biologia da pessoa e o processo mental é mais obvia no caso de traumatismo cerebral e desordem genética,
mas mesmo a mais suave das deficiências cerebrais é baseada na estrutura ou na química cerebral.

Uma pessoa com deficiência cogniticas profunda irá precisar de assistência em quase todos os aspectos da vida cotidiana.
Alguém com menor dificuldade de aprendizagem talvéz esteja apto a se adaptar adequadamente apesar da deficiência,
talvez mesmo com a extensão da deficiência ela não seja nunca descoberta ou diagnosticada.
Aditidamente, a grande variância entre as capacidades mentais destes que com deficiências cognitivas severas impacta de alguma maneira.
Na realidade, talvéz um argumento racional seja o fato que o conteúdo da rede pode não ser acessível à indivíduos com profundas deficiência cognitivas,
não importando quanto trabalho no desevolviment haja.
Alguns conteúdos serão sempre complexos demais para certa audiência.
Isto é inevitável.
Mesmo assim, há ainda alguumas coisas que designers podem fazer para aumentar a acessibilidade ao conteúdo da rede para pessoas com deficiência cognitivas menos severas.

### Deficiência Cognitiva Funcional VS Clínica

Há pelo menos duas maneiras de classificar deficiências cognitivas:
pela deficiência funcional ou pela deficiência clínica.
Deficiência clínica ou deficiência cognitiva incluem autismo,
sindrome de down, traumatismo craniâno (TBI), e até mesmo demência.
Condições de deficiência menos severas incluem defict de atenção e desorde (ADD),
dislexia (dificuldade de leitura), discalculia ( dificuldade com matemática),
e defict de aprendizagem em geral.
Diagnóstico clínico pode ser útil para a perspectiva de tratamento,
mas para fin de acessibilidade a web, classificar as deficiências cognitivas pela desabilidade *funcional* é mais útil.
Deficiências funcional ignora causas médicas ou comportamentais da deficiência e concentra-se nas habilidades e desafios resultantes.
Algumas das principais categorias de deficiências cognitivas funcionais incluem defict ou dificuldade com:

1. Memória
2. Resolução de problemas
3. Atenção
4. Leitura, linguistica, e compreensão verbal
5. Compreensão matemática
6. Compreensão visual

As principais razões pelas quais a tese de deficiência funcional são mais úteis quando considerada a acessibilidade a web é por que eles são mais diretamente relacionados com as preocupações de web desenvolvedores.
Dizer a um desenvolvedor que alguém tem autismo não é muito significativo ao menos que o desenvolvedor saiba quais tipos de barreira alguem com autismo talvéz encontre no seu web site.
Por outro lado,
dizer a um desenvolvedor que alguem tem dificuldades de compreensão matemática fornece ao desevolvedor uma estrutura para abordar as necessidades deste tipo de público.

Adicionalmente, diagnóstico clínico não são mutuamente excludentes em termos de que dificuldades as pessoas enfrentam.
Há consideravelmente uma sobreposição de deficiências funcionais com diagnóstico clínico.
Este tipo de sobreposição se encaixa com um modelo médico,
mas não é particularmente útil para desevolvedores web,
os quais simplesmente precisam saber o que a pessoa consegue ou não fazer.

### Memória

Memória se refere a habilidade de se lembrar de algo uma vez aprendido.
Um modelo comum para explicar a memória envolver os conceitos de memória trabalho 
( i.e., imediata), memória de curto e de longo prazos.
Alguns indivíduos com deficiências cognitivas tem dificuldades com uma, duas ou mais de três tipos de memória.
Alguns dos usuário tem dificuldades de memória que prejudicam suas habilidades de se lembrar como eles conseguiram o conteúdo.
Considere uma complexa forma de multiplos displays de mensagem de erro na parte superior do formulário quando enviado.
Talvez isto seja bem difícil para o usuário de se lembrar de vários erros,
Ou talvez mesmo esquecendo as informações de erro antes de eles estarem mesmo válidos para encaminhar este erro..

### Problem-Solving

Some individuals with cognitive disabilities have a difficult time solving problems as they arise.
In many instances,
their resilience can be low and the resulting frustration is such that they choose to leave the site and not persist to solve the problem.
One example of this would be the presence of a 404 error from a bad link,
or a link that does not take them where they thought they were going.

### Attention

<span style="float: right; margin: 8px 0px 1px 10px;">![A distracted student](media/student.jpg)</span>
There are many individuals that have difficulty with focusing their attention to the task at hand.
Distractions such as scrolling text, blinking icons,
and pop-up windows can make the web environment difficult or even impossible.
Even for typical users, such things can be irritating.
Good design principles would limit these instances to only that which is necessary to convey the content.

Some people with Attention Deficit Hyperactivity Disorder (ADHD) have difficulties learning,
but oftentimes this is due to their distractibility,
rather than to any kind of inability to process information.
People with ADHD can be impulsive, easily distracted, and inattentive.
On a positive note,
some people with attention deficits are highly creative and very productive in short bursts,
with an abundance of energy and enthusiasm.
On a less positive note, it can be difficult for people with ADHD to stick to a task for a long period of time.

Avoiding anything that draws a person's attention away from the main content and using good design,
such as color, white space,
and simple presentation can help users focus on important content and functionality.

### Reading, Linguistic, and Verbal Comprehension

<span style="float: right; margin: 8px 0px 1px 10px;"><img src="media/text.jpg" alt="complex words floating through space" width="203" height="203" /></span>
Some individuals have difficulties understanding text.
These difficulties may be mild or severe, ranging from minor challenges to a complete inability to read any text.
It would be unreasonable to expect web developers to accommodate the entire range of reading abilities.
The difference between non-readers and genius readers is simply too vast.
It *is* reasonable, however, to expect developers to
[write as simply and clearly as is feasible](http://webaim.org/techniques/writing/),
taking into account the primary audience and including those who may have difficulty with some of the content.
After all, *an estimated 15-20% of the population,
including many of the brightest minds of recent generations such as Albert Einstein,
Thomas Edison, and Henry Ford,
has some sort of language or text comprehension difficulty*.

<div class="example" markdown="1">
<div class="title">Example</div>

Here is one example of a reading problem.
Note that it may be one of perception or of processing.
See if the associated accessibility fix helps you.

What is being said in this phrase?

**Tob eornot obe**

Now check the power and importance of embedded graphics as a way to enhance the context of the written word by looking at the [phrase with a graphic.](graphic.html)

Another interesting simulation of a reading difficulty and our resilience in the face of reading problems can be found at
<http://www.angmail.fsnet.co.uk/jumbltxt.htm>.

</div>

#### Non-Literal Text

Non-literal text, such as sarcasm, satire, parody, allegory, metaphor, slang, and colloquialisms,
can be a problem for some readers.
In some cases, readers will not realize that the words are not meant to be understood literally.
A writer who says "I just love getting stuck in traffic when I'm already late for work" probably means the opposite of what this sentence actually says.
Sarcasm such as this can be confusing to some readers.
Similarly, someone who reads she must "get her ducks in a row" may not realize that the author is probably not referring to real ducks at all.
The author is suggesting that the reader get organized or disciplined,
using the comparison of a mother duck with her ducklings lined up behind her in order to illustrate the concept.

#### Non-Existent Text

The unstated assumptions and implied meaning of written content may seem obvious to the writer,
but readers may not have the necessary background knowledge.
Some readers may not have the skills to infer meaning from text without additional help.

### Math Comprehension

<!--
  Nota de preparação do documento: no original, o alt da imagem seguinte
    NÃO tem conteúdo (fititnt, 2016-10-09 17:20)
-->

<span style="float: right; margin: 8px 0px 1px 10px;">![](media/formula.gif)</span>
Mathematical expressions are not easy for everybody to understand.
This does not mean that authors should avoid math entirely.
For people who are comfortable reading equations and thinking mathematically,
the best way to explain mathematical concepts is to use equations.
On the other hand, often it is helpful to explain math conceptually, either with or without the formulas.
Conceptual explanations help readers understand the reasoning behind the math.

### Visual Comprehension

Some individuals have difficulties processing visual information.
In many ways, this is the opposite of the problem experienced by people with reading and verbal processing difficulties.
Individuals with visual comprehension difficulties may not recognize objects for what they are.
They may recognize the fact that there are objects on a web page, but may not be able to identify the objects.
For example, they may not realize that a photograph of a person is a representation of a person,
though they can plainly see the photograph itself (as an object) on the web page.

For these people, a moving,
talking person in a video may be easier to identify and mentally process than a static image of a person in a photograph.
Video and multimedia, accompanied with narration, may be the best way to communicate to these individuals.

## Design Considerations

### Overview

Any list of design considerations for users with cognitive disabilities can easily turn into a lengthy list of usability concerns and general "good design principles."
The ideas presented here do not exhaust all avenues of thought on the topic, by any means.
They merely present some of the larger principles which categorize more specific techniques.

### Accommodating Memory Deficits

Any kind of reminder of the overall context of a web site can help people with memory deficits.
Lengthy interactive processes,
such as those required to purchase items online,
should be kept as simple and brief as possible.
To focus the users' attention on specific tasks,
the interaction should probably be broken up into separate pages,
but help users keep track of their progress so they do not get lost in the process.
Simple reminders such as "step 2 of 4" help them keep track of what they have already done and what they have left to do.
Each step can also be named or labeled so instead of saying "previous page" and "next page," a link could say "previous page
(payment and shipping information)" and "next page
(review order)."

### Accommodating Problem-Solving Deficits

Everyone at some point or another accidentally clicks on the wrong link,
misspells a word, or commits some kind of error on the web.
This is normal human behavior.
In some individuals, this tendency is exaggerated, so they make even more mistakes.
Whether people make many or few mistakes, everyone likes to be able to correct their errors.
Error messages should be as explanatory as possible, telling users what they did wrong and how to fix the problem.
Search features should suggest alternate spellings to users if the original spelling seems suspicious or if it returns no results.
Users should be warned when actions can cause potentially serious consequences, such as deleting a file.
In many cases,
providing instructions at the start of a task will eliminate or at least reduce the overall number of user errors.
Also, avoid extreme changes in the context of the web site without first warning users.
All functionality should be as predictable as possible,
and any deviations from predictability should be preceded by warnings and/or explained to users after the changes occur.

### Accommodating Attention Deficits

Focus the attention of users.
Use visual cues to highlight important points or sections of the content.
If possible, eliminate advertisements and sponsored links.
Use headings to draw attention to the important points and outline of the content.
Avoid background noises or images that distract.
Use them instead to focus the users attention.

### Accommodating Reading, Linguistic, and Verbal Comprehension Deficits

#### Supplemental media

Supplemental media such as illustrations, icons,
video and audio have the potential to greatly enhance the accessibility of web content for people with cognitive disabilities.
The problem is that high quality media is often difficult to produce.
Poor quality media may actually decrease the accessibility of web content, by making it more confusing.
But don't use this as an excuse not to try.
Use your judgment.
Incorporate media where it makes sense.
Realize, too, that the vast majority of web content could benefit from some sort of supplemental media,
if only supplemental graphics.

#### Document organization and structure

##### Structural organization

As a general statement, the more structured your document is, the easier it will be to understand.
Structure in documents can be created by adding:

-   headings
-   bulleted lists
-   numbered lists
-   definition lists
-   indented quotes (using the `<blockquote>` element)

All of the above structural elements can be added into the markup of the document.
In other words, there are built in methods in HTML of designating a part of your content as a heading, or a list item, etc.

##### Visual organization

You can also add visual structure to a document that will benefit those who have sight.
For example, you can:

-   indent sub-items in a hierarchical list[\*](#note1)
-   highlight items by changing the font color or background color

<div class="note" markdown="1">
<div class="title">Note:</div>

Developers should not ignore the semantics of the markup language when trying to achieve a visual effect.
For example, despite the fact that the `<blockquote>` element causes the text within it to be visually indented,
this tag should not be used for its visual effect alone.
If the text truly is a quote, then the `<blockquote>` element is appropriate.
If the text is not a quote, then CSS (Cascading Style Sheet) attributes should be used to achieve the effect
(for example, the developer could add the following style attribute to the paragraph: `style="margin-left: 5%"`).

</div>

##### White space

It is usually easier to read text when it is visually separated from the borders of the surrounding design.
People with reading disorders, such as dyslexia,
can benefit from white space in the margins and vertical white space between headings, paragraphs, tables, etc.
Long paragraphs can be more difficult to read than shorter ones,
partly because readers may lose their place within the paragraph.

#### Clear and simple writing

Short, simple, unambiguous phrases are easier to understand than long, complex, ambiguous ones.
People with more profound cognitive disabilities need sentences that are extremely short, simple, and unambiguous.
In some cases, they will not be able to understand sentences at all,
relying completely on graphics, illustrations, and other non-text visual materials.
This does NOT mean that you have to create image-only sites for general audiences,
though adding high-quality supplemental illustrations is certainly a good idea.
If, however, your primary audience is individuals with more severe cognitive disabilities you may need to create an image-only site.

To the extent possible, try to avoid non-literal content such as sarcasm, parody, and metaphors.
Also make sure to give readers all necessary background information about the topic at hand. <span class="ifnotrichmedia">(See also the
article on [writing clearly and simply](http://webaim.org/techniques/writing/).)</span>

### Accommodating Math Comprehension Deficits

Math computations or formulas can be difficult for many people to understand,
whether they have a genuine deficit in math comprehension abilities or just "math phobia," to use the term "phobia" loosely.
In this context, math phobia is not a clinical condition but a simple dislike of math,
influenced largely by cultural factors.
The United States, for some reason, has created a culture in which math is commonly disliked and derided.
By way of comparison, math abilities are highly prized in Asian countries,
and it would be somewhat of an insult to say that an Asian person is not good at math.

No matter what the cause of math comprehension deficits—biologically-based deficits or culturally-based aversions—authors can increase the understandability of their content by either avoiding math altogether,
or by explaining the math conceptually.
Where computations are required—as in e-commerce sites that add the price of the items purchased,
tax, shipping and handling, and other charges—it is usually best to perform these computations automatically,
so the user does not have to.

### Accommodating Visual Comprehension Deficits

Usually, the best advice to help users with cognitive disabilities is to provide information in muliple formats,
with a heavy emphasis on visual formats.
While this remains true for the majority of people with cognitive disabilities,
some types of cognitive disabilities cause difficulties in visual comprehension.
If authors rely entirely on visual communication methods, some users will not understand the message.
Visual communication methods include color, spatial relationships, styles, design elements, photos, images, etc.

Even though most web content suffers for a lack of visually-enhanced communicative methods,
the take-home message is that no one method is sufficient by itself.
Supplement the information with multiple modes and methods of communication.

## Cognitive Disabilities Activity

### Instructions

Here are your instructions:

1.  Find a blank piece of paper.
2.  If it isn't already perfectly square, cut off one edge of the paper until it is perfectly square.
3.  Fold the paper in half diagonally.
4.  Lay the paper down in front of you so that the longest edge is facing you.
5.  Take the bottom left corner and fold it over the main area of the piece of paper so that the corner touches the opposite edge,
    and so that the top of the newly folded edge is parallel with the bottom of the piece of paper.
6.  Do the same thing to the right corner,
    folding it across the main area of the piece of paper until it touches the opposite edge.
    The top edge of this fold should be exactly on top of the top edge of the previous fold.
7.  Take the outer layer of the very top corner and fold it down until the corner touches the spot where the bottom of the other two folds meet.
    You should see a pattern in the shape of an "X."
8.  Do the same thing to the other layer, but in the opposite direction.
9.  Spread apart the two layers on the top and gently push the sides in.
10. You made an origami cup! (Or did you?)

### Questions and Discussion

-   How successful were you at performing the task?
-   Were you able to make anything resembling a cup?
-   Are you sure that you performed the task correctly? Perhaps you made a mistake or two, whether you know it or not.

Here's what your origami cup should look like (although the color of your paper may be different):

<div style="text-align: center;"><img src="media/origami.jpg" alt="photo of an origami cup" width="188" height="188" /></div>

How closely does your origami cup match the one pictured above?
Is it even close? If not, why not?

Although some of you may have been able to complete the task of folding an origami cup by simply reading the instructions,
my guess is that most of you got a little bit confused at some point along the way.
My instructions may have seemed ambiguous to you.
They may have seemed poorly written.
Perhaps you misunderstood my instructions even when you thought that you understood them.

-   Would it have helped to have a picture of the end goal before starting the task?
-   Would it have helped to see someone perform the task, or an illustration of how to perform the task?

<div class="note" markdown="1">
<div class="title">Note:</div>

The following example presents visual content that will not be of use to people who cannot see it,
but we have provided a brief discussion of this material in the [Note About Visual Disabilities](#note) section.

</div>

Compare the written instructions to a visual method of instruction:

-   [Example 1](http://www.origami-instructions.com/origami-cup.html):
    Simple step-by step instructions on how to fold an origami cup,
    which are illustrated with graphical arrows and other visual cues showing you how to fold the piece of paper.

After looking at the above visual methods of giving instructions on the task:

-   Would you say that you are better able to perform the task?
-   Which instructional method did you like best?
-   Can you think of other instructional methods that may be even better?

### How This Relates to Cognitive Disabilities

Those of you who are visually-oriented were at a cognitive disadvantage when trying to fold an origami cup with nothing more than written instructions. Individuals with learning disabilities, reading disorders,
or more profound cognitive disabilities often feel similarly disadvantaged when trying to understand concepts that are difficult for them.
Content needs to be clear and accurate, and sometimes in more than one format,
in order for these individuals to fully understand content.
In the case of folding an origami cup, illustrations and animations are particularly useful.
With other types of information, audio content may be more appropriate.

<div class="important" markdown="1">
<div class="title">Important</div>

In many cases, the techniques for more making web content accessible to people with cognitive disabilities are nothing more than techniques for effective communication.

</div>

Once you understand this principle,
the task of making content accessible to people with cognitive disabilities becomes a little bit less mysterious,
even if it doesn't become less challenging.

Designing for people with cognitive disabilities is much more of an art than a science.
Some people prefer animated instructions, while others prefer static graphical illustrations.
But it is not a simple matter of static versus animated illustrations.
The effectiveness of graphics and animations depends largely on the skills of the artist,
both in the sense of draftsmanship ("being able to draw well") and presentation (being able to communicate well).

### Note About Visual Disabilities

As you can imagine, illustrations, graphics,
and other materials that are visually-oriented are going to be useless to someone who cannot see them.
This does *NOT* mean that there is a direct conflict between the needs of people with visual disabilities and the needs of people with cognitive disabilities.
It simply means that you have to keep the needs of both audiences in mind.
If you provide illustrations for people with cognitive disabilities,
provide `alt` text for those illustrations to benefit those with visual disabilities.
If you provide videos, provide a transcript of the videos that can be accessed by screen readers, and so on.
In the case of the origami cup,
more detailed instructions would probably need to be written for a blind person to be able to perform the task more effectively.
These detailed instructions would be the "text alternative" to the illustration format.
With both illustrations and detailed textual instructions, both audiences would receive what they need.
