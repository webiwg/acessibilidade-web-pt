---
layout: translation
date: 2014-12-11 # Data de ultima atualização do original
title: "CSS in Action: Invisible Content Just for Screen Reader Users"
description: "There are occasional instances where content should be made available to screen reader users, but hidden from sighted users. In most cases, if content (particularly content that provides functionality or interactivity) is important enough to provide to screen reader users, it should probably be made available to all users. "

copyright: 'Copyright WebAIM' # Quem tem direitos de cópia
license: null # Caso seja uma licença padrão (MIT, GPL...) por aqui
license-custom: null # Caso a licença não seja uma padrão, por uma descrição curta dela aqui
authors: [{
    name: "WebAIM",
    link: "http://webaim.org/"
}]
translators: [{
    name: "Emerson Rocha Luiz",
    link: "http://twitter.com/fititnt"
}]
reviewers: []
discussion: https://github.com/webiwg/acessibilidade-web-pt/issues/16
original: {
    title: "CSS in Action: Invisible Content Just for Screen Reader Users", # Titulo original, no idioma origial
    link: "http://webaim.org/techniques/css/invisiblecontent/", # Link para documento original
    dateOfTranslation: "2016-09-25" # Data em que a tradução foi finalizada
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




Introdução
------------

<span style="float: right;margin: 8px 0px 1px 10px;"><img src="media/peekaboo.jpg" alt="A woman hides behind her hands." width="130" height="110" /></span>Existem
casos pontuais em que o conteúdo deve ser disponibilizados para usuários de leitor de tela,
mas escondido de utilizadores normovisuais. Na maioria dos casos, se o conteúdo (principalmente
conteúdo que fornece a funcionalidade e interatividade) é importante o suficiente para
usuários de leitor de tela, ele provavelmente deve ser disponibilizado a todos os
usuários. Casos em que sugestões são verbosas ou instruções são fornecidas apenas por usuários de leitores
de tela são, provavelmente, um reflexo da má concepção e acessibilidade.
No entanto, existem alguns casos onde a informação é evidente visualmente, mas pode
não ser clara para os usuários de leitores de tela. Nestes casos, pode ser conveniente
marcação de conteúdo de uma forma que ele é lido por um leitor de tela, mas invisível para
utilizadores normovisuais.


Técnicas para o ocultar texto
--------------------------

Existem diversos mecanismos que podem ser usados para esconder o conteúdo. É importante
que a técnica a ser implementada resulte em o resultado desejado e a
acessibilidade.

### `visibility: hidden;` e/ou `display:none;`

Esses estilos vão ocultar o texto de todos os usuários. O texto é removido do fluxo visual
da página e é ignorado pelos leitores de tela. **Não use este CSS se
quiser que o conteúdo a ser lido por um leitor de tela. Mas USE isto para o conteúdo
que você não quer que sejam lidos por leitores de tela.**

### `width:0px`, `height:0px` e outras técnicas de tamanho 0 pixel

Tal como referido acima, devido a um elemento sem nenhuma altura ou largura é removido do fluxo da
página, a maioria dos leitores de tela irão ignorar este conteúdo. Largura e altura do HTML
pode dar o mesmo resultado. **Não redimensione o conteúdo a 0 pixels, se você deseja que o
conteúdo seja lido por um leitor de tela.** Conteúdo estilizado com `font-size:0px` ou
`line-height:0` podem funcionar, ainda que os elementos tomariam espaço horizontal
na tela. Todas estas técnicas podem implicar em penalizações de mecanismo de pesquisa já
que podem interpretado como maliciosas.


### `text-indent: -10000px;`


Esta abordagem move o conteúdo para 10000 pixels para esquerda - portanto, fora da tela
visível. O valor real tem pouca importância, desde que ele estiver posicionado fora da tela.
Os leitores de tela ainda vai ler o texto com esse estilo. No entanto, se um link ou elemento de formulário
recebe esse estilo, que pode resultar em um indicador de foco (as linhas pontilhadas
ou "formigas em marcha" que cercam um link focalizado) que se estende a partir de onde
o elemento deve ser localizado na página para o lugar é efectivamente localizado
(para a esquerda). Isto não é muito bonito. Essa abordagem também causa problemas em
idiomas da direita para a esquerda. Como tal, esta abordagem *pode* ser uma opção viável se
o elemento não contém elementos navegáveis, embora melhores técnicas estão
disponíveis.

### CSS clip

```css
position: absolute !important;
clip: rect(1px 1px 1px 1px); /* IE6, IE7 */
clip: rect(1px, 1px, 1px, 1px);
```

A fairly modern technique of using CSS to hide or clip content that does not fit
into a 1 pixel visible area will essentially hide the content visibly, but still
allow it to be read by modern screen readers.

### Absolutely positioning content off-screen

Using CSS to move hidden elements to a position off-screen is generally accepted
as the most useful and accessible method of hiding content visually.

Positioning content off-screen
------------------------------

The following are the recommended styles for visually hiding content that will
be read by a screen reader.

```css
.hidden {
    position:absolute;
    left:-10000px;
    top:auto;
    width:1px;
    height:1px;
    overflow:hidden;
}
```

The .hidden CSS class should then be referenced from within the tag of the
element being hidden, as shown:

```html
<div class="hidden">This text is hidden.</div>
```

Sighted users will not see the hidden content at all. It will be out of their
viewing range - hidden well to the left of the visible browser window. Screen
reader users will have access to the content as if it were not hidden at all.
Screen readers read the content normally, completely ignoring the styles used in
this technique.

Let's analyze the styles in detail.

`position:absolute;` tells the browser to remove the element from the page flow
and to begin positioning it. `left:-10000px;` moves the content 10000 pixels to
the left. `top:auto;` tells the browser to position the content vertically at
the same location it was originally. Omitting `top` may result in the `left`
style being ignored in some instances and browsers. In short, this part of the
code moves the element 10000 pixels straight to the left.

`width:1px; height:1px; overflow:hidden;` tells the browser to make the element
1px by 1px in size and to visually hide everything that does not fit into these
dimensions. While this is a likely a little overkill and can probably be omitted
in most circumstances, there are a few instances where positioning may be
disabled, but all other styles remain enabled. In this case, the element will
remain in its original position, but will only take 1 pixel of space.

Note

It is sometimes recommended to position content using `left:0px; top:-500px` (or
similar). While this works by positioning the content above the top of the page,
if the hidden element contains a link or form element, upon receiving keyboard
focus, the browser attempts to scroll to the element - thus scrolling the
browser to the top of the page. This could result in confusion for sighted
keyboard users. By positioning directly to the left, the browser will not scroll
to the top of the page. **It should be noted that because links and form
elements provide functionality, they should rarely be hidden from sighted users.
Sighted users will not be able to see which element currently has focus because
it is hidden off-screen.**

Examples
--------

Important!

In general, content should only be hidden from sighted users and made available
to screen reader users when content is apparent visually, but not apparent to
screen reader users.

### Instructional cues and indicators

This technique can be used to provide instructional cues and indicators to
screen reader users. This should be implemented with discretion and only where
necessary. This page demonstrates proper use of this technique in two places.

First, the search text box at the top of the page has a hidden label immediately
before it. It is apparent visually that the text box is for searching due to the
presentation and the search button, but a screen reader requires a label for the
text field. As such, we provided a label, but have hidden it visually.

Second, the breadcrumbs at the top of the page are a common design convention.
Most web users understand the convention and can identify breadcrumbs visually.
Because a screen reader accesses the breadcrumb links and content linearly, it
may not be apparent to them that it is breadcrumbs until they have read a
portion of it. As such, we have added hidden text of "You are here:" just prior
to the breadcrumbs.

You can see all of this hidden text by disabling styles for this page.
**Remember, all content hidden visually with CSS will become visible if styles
are disabled.**

### "Skip to main content" links

["Skip to main content" links](/techniques/skipnav/) are one of the few places
where accessibility has a direct and distinct impact on visual design. In order
to be useful, the "skip" link should be one of the first on the page. Designers
may balk at the idea of providing a link as the first thing on the page -
particularly when that link is unlikely to be utilized by the majority of the
site visitors. However, hiding the link makes them unusable to sighted keyboard
users - a user group that can greatly benefit from this link.

One way to reconcile the impact that "skip" links have on visual design with the
needs of screen reader users and users with mobility impairments is to use a
technique that hides the "skip to main content" link until the user tabs to it.
When the link receives focus, the link becomes visible to sighted users. This
would allow both blind and sighted keyboard users to take advantage of the
link's functionality

In order to accomplish this, two styles are created - one for the `<a>` element
and one for the `a:focus` pseudo-class. The style for the `a:focus` pseudo-class
will only be active when the user tabs to the link (i.e., it has focus), and the
link will revert back to its default style (i.e., it will be hidden off-screen
again) when the user tabs away from the link.

```css
#skip a {
    position:absolute;
    left:-10000px;
    top:auto;
    width:1px;
    height:1px;
    overflow:hidden;
}
#skip a:focus {
    position:static;
    width:auto;
    height:auto;
}
```

The styles should then be applied to the "skip" link.

```html
<div id="skip"><a href="#content">Skip to Main Content</a></div>
```

The one drawback to this approach, on a conceptual level, is that the sudden
appearance of a link that was previously invisible will be unexpected, and could
confuse the sighted keyboard user. The link should also be clearly styled so it
is apparent. These will not be problems for screen reader or mouse users because
they never see the link.

### Other implementations

Form controls are sometimes presented visually so that text is visually
associated as the label for multiple controls. Consider data entry where one
"First name" text might describe the function of multiple text boxes that appear
below it. Sometimes tables are used for these presentations. Alternatively,
sometimes one control may be labeled by multiple items of text, such as a
password field that is preceded by the word "Password:" and followed by the word
"Required". Using standard [form labelling](/webaim/tecnicas/formularios/#controles-de-de-formulrio-acessveis), there
is no way to associate one text item to multiple controls or multiple texts to
one form control. In these case, the appropriate labels could be provided in the
markup adjacent to their respective form elements, but hidden using the CSS
above.

A common example of this is when two or more text input elements are used for
phone numbers.

<img src="media/phone1.jpg" alt="The words &#39;phone number&#39; are followed by 4 text input boxes, intended to be used for area code, first three digits, last four digits, and then extension" class="border" width="389" height="42" />

Most visual users in North America will understand that the individual text
input areas correspond to the different sections of standard phone numbers.
Screen reader users, however, may attempt to enter the entire phone number in
the first box. Confusion is likely when they discover that the box limits them
to only 3 characters or that there are additional unlabeled text boxes that
follow.

The most obvious workaround for this particular problem would be to combine all
of the text input boxes into a single text input box, and then provide the
appropriate label. However, off-screen labels for each distinct text box will
also ensure accessibility.

```html
 Phone number: (
   <label for="area" class="hidden">Area code</label>
   <input name="area" id="area" type="text" size="3" maxlength="3">
)…
```

The off-screen labels would, in this case, provide an adequate description for
screen reader users.

Note

In the example above, the `title` attribute could also be used to provide this
information. Information in the `title` attribute will be read by screen readers
when a label is not present. Additionally, `aria-labelledby` could be used to
provide multiple labels per input or multiple inputs per label.

Conclusion
----------

When the CSS techniques presented here are used to hide content, sighted users
will never know that the content is there at all (unless they disable styles).
Screen reader users, on the other hand, will never realize that this content is
invisible to sighted users. Both kinds of users will be able to use the content
intuitively, without having to adjust for either too much or too little
information in the markup. This can provide important contextual cues that are
otherwise impossible for screen reader users to grasp because of the visual
nature of these cues. When used judiciously, this technique can resolve some of
the tension between the demands of accessibility and the demands of visual
design. It is not the only technique or method of solving this problem, but it
is one that web developers can add to their list of possible solutions when the
need arises.


