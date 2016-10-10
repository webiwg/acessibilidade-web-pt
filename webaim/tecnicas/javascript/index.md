---
layout: translation
date: 2013-10-24 # Data de ultima atualização do original
title: "Accessible Javascript" # Titulo traduzido
description: "JavaScript allows developers to add increased interaction, information processing, and control in web-based content. However, JavaScript can also introduce accessibility issues."

copyright: 'Copyright WebAIM' # Quem tem direitos de cópia
license: null # Caso seja uma licença padrão (MIT, GPL...) por aqui
license-custom: null # Caso a licença não seja uma padrão, por uma descrição curta dela aqui
authors: [{
    name: "WebAIM",
    link: "http://webaim.org/"
}]
translators: [{
    name: "Roberta Schmitz Mayer",
    link: "http://webiwg.org"
}]
reviewers: []
discussion: https://github.com/webiwg/acessibilidade-web-pt/issues/22
original: {
    title: "Accessible Javascript", # Titulo original, no idioma origial
    link: "http://webaim.org/techniques/javascript/", # Link para documento original
    dateOfTranslation: "2016-10-04" # Data em que a tradução foi finalizada
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
.important, .tip, .note, .example {
    padding: 4px 1.5em 0px 1.5em;
    margin: 1em auto 1em auto;
    width: 85%;
    border-radius: 4px;
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

## Problemas de Acessibilidade com JavasScript

Javascript permite que os desenvolvedores disponibilizem mais interação, processamento de informações e controle num contexto web.
Entretanto, Javascript pode introduzir alguns problemas de acessibilidade.
Esses problemas incluem:

<!--Comentários do item: Problemas de Acessibilidade com JavasScript

  N.T.:  Não tenho certeza da tradução de "user agent" (@robsmayer, 2016-10-06 22:18)
  N.T.:  Deixar esse comentário como exemplo para eu me lembrar por enquanto.
-->

-   **Navegação.** Incapacidade ou dificuldade ao navegar utilizando um teclado ou tecnologia assistiva.
-   **Conteúdo Oculto.** Apresentação de conteúdo ou funcionalidade que não é acessível ao utilizar tecnologia assistiva.
-   **Controle do Usuário.** Falta controle do usuário sobre mudanças automáticas de conteúdo.
-   **Confusão/Desorientamento.** Alterando ou desligando o uso normal do usuário ou ativando eventos que podem ser desconhecidos pelo usuário.

Geralmente, uma página web contendo Javascript será totalmente acessível se o script da página funcionar independente de qual dispositivo for utilizado.
Ou seja, que não requere somente o uso do mouse ou somente o uso do teclado para ser utilizada e que as informações(conteúdo) for disponível para tecnologias assistivas.
Infelizmente, não há um meio simples que possa ser aplicado para resolver todos problemas de acessibilidade associados ao Javascript.
O único modo de garantir a acessibilidade do JavaScript é análisar cada página que utiliza scripts e inventar uma solução única para cada problema encontrado. 

### JavaScript que não altera a acessibilidade

<!--Comentários do item: JavaScript que não altera a acessibilidade

    N.T.1: Não tenho certeza de qual é o melhor termo para "JavaScript prompts" (@robsmayer, 2016-10-07 22:33) 
    N.T.2: Não sei se devo manter o texto original(@robsmayer, 2016-10-07 22:34)
    N.T.3: Obter termos melhores para: (@robsmayer, 2016-10-07 hora indefinida)
        JavaScript prompts
        Navigation items
    N.T.4: Achar mais sinônimos de "por exemplo" (@robsmayer, 2016-10-04 2)
-->

Usar JavaScript numa página não significa que ela não é acessível.
Em muitos casos, JavaScript pode ser usado para aumentar a acessibilidade.
Por meio dos <em lang="en">prompts JavaScript</em> informações adicionais, avisos ou instruções podem ser dadas ao usuário.
Por exemplo, segundo a  <em lang="en">[Section 508 guidelines of United States law](http://webaim.org//standards/508/checklist) and the
[Web Content Accessibility Guidelines](http://webaim.org//standards/wcag/checklist),)</em>,
caso seja necessário uma resposta do usuário num tempo dado, deve-se notificar o mesmo desse tempo de resposta e dar a ele tempo suficiente para que ele possa
indicar que será necessário um período maior.
Implementar tal função seria dificíl usando somente HTML. 

Às vezes, JavaScript é utilizado para criar elementos de interfaces visuais que não afetam a acessibilidade.
Geralmente, JavaScript é usado para rolagem de imagens ou outras modificações apenas visuais,
onde uma imagem é trocada por outra quando o mouse é movido acima dela;
por exemplo, um <em lang="en">navigation item<\em> que muda para exibir uma sombra, brilho, sublinhado quando o cursor fica acima dele.

Para tais usos não são necessários recursos adicionais de acessibilidade, pois tal script não introduz ferramentas ou não exibe conteúdos importantes.

### Credibilidade do JavaScript

<!--Comentários do item: Credibilidade do JavaScript

    N.T.: Acho que exite uma tradução melhor para "don't have or 'do' JavaScript".
    N.T,: Desconheço uma tradução correta de scripted interfaces (supus interfaces script) e scripted content (coloquei conteúdo script).
-->

É um erro comum supor que pessoas com deficiência não precisam do JavaScript ou 'utilizem'  <em lang="en">don't have or 'do' JavaScript</en> o mesmo
e portanto, é aceitável que exista interfaces script inacessíveias, contanto que sejam acessíveis com o JavaScript desativado.
Uma pesquisa feita pela WebAIM de usuários leitores descobriu que [98.6% dos correspondentes tinham JavaScript ativado](http://webaim.org//projects/screenreadersurvey4/#javascript).
Os números são ainda maiores para usuários que possuem um nível maior de [deficiência visual](http://webaim.org/projects/lowvisionsurvey/#javascript)
ou [disfunções motoras](http://webaim.org/projects/motordisabilitysurvey/#javascript).
Resumindo, pessoas com deficiência vão utilizar scripts e por isso o conteúdo dos scripts devem ser naturalmente acessíveis. (criados originalmente de maneira acessível).


As orientações(diretrizes) de acessibilidade devem também exigir que <em lang="en">scripted interfaces</em> sejam acessíveis.
Enquanto, WCAG 1.0 de 1999 exigia que as páginas deveriam ser funcionais e acessíveis com scripts desativados,
WCAG 2.0 e todas outras orientações modernas permitem que você solicite JavaScript,
mas o <em lang="en">scripted content</em> ou interações devem seguir as diretrizes de acessibilidade.

Contudo,é importante ter em mente que alguns usuários com deficiência podem estar usando tecnlogias acessíveis que não ofereçam
suporte ou total suporte aos scripts.
Se sua página web ou aplicação requere o uso de scripts, garanta que ela funcione para usuários que não utilizem JavaScript.
Entretanto, isso não significa que todas funcionalidades devem funcionar sem scripts (embora isso seria ótimo),
se ela não funcionar sem scripts, você deve evitar apresentar algo confuso ou falso que pareça funcionar, mas não 
funcione sem o uso de suporte para JavaScript.

## <em lang="en">JavaScript Event Handlers</em>

<!--Comentários do item: JavaScript Event Handlers

    N.T: Desculpem, não sei a tradução correta de "JavaScript Event Handlres" 
    N.T: Termo mais bonito para dynamically generated content seria legal saber
    N.T: Deixando claro, não é que eu não saiba as coisas, é só que eu ache que tenha algo melhor do que a minha tradução
    N.T: Há muitos termos técnicos nesse item.(@robsmayer 2016-10-09 - 23:50)
    N.T: Esqueci de colocar o horário em basicamente todas notas de tradução (@robsmayer 2016-10-09 - 23:51)
-->

<!--Ideia Geral/Panorama Geral-->
### Visão Geral 

<em lang="en">Event handlers</em> acompanham código HTML existente ou conteúdo gerado dinâmicamente 
são ativados pelo navegador ou pelo usuário -
por exemplo quando uma página carrega, quando um usuário clica o mouse, ou quando são 20h.
Alguns <em lang="en">event handlers</em> dependem do uso do mouse ou do teclado.
Estes são chamados de <em lang="en">**device dependent**event handlers</em>.
Outros <em lang="en">event handlers are **device independent**</em> e são ativados por ambos, mouse e teclado. ou por outros meios.

<div class="important" markdown="1">
<div class="title">Importante</div>

Com objetivo de assegurar a acessibilidade, use tanto um <em lang="en">device independent event handler</em> (Um que funcione com o mouse e com o teclado)
ou utilize ambos <em lang="en">mouse dependente *and* keyboard dependent event handlers</em>.
</div>

### `onMouseOver` and `onMouseOut`

O `onMouseOver` <em> event handler</em> é ativado quando o cursor do mouse é colocado sobre um item.
Como seu nome implica, `onMouseOver` necessita do uso de um mouse, portanto ele é <em>device dependent event handler</em> e pode causar problemas de acessibilidade.
`onMouseOver`, e seu companheiro, `onMouseOut`, podem ser usados, contanto que algum conteúdo ou funcionalidade importante também estiver disponível sem a utilização do mouse.
may be used, as long as any important content or functionality is also available without using the mouse.
// Se a interação do mouse é apenas para aparência (como a adição de um brilho ou uma sombra Aka: deixar bonitinho),
provavelmente não há problemas de acessibilidade, desde que essa mudança não indique alguma função(como deixar indicado que um elemento é clicável).

Se tal interação indica informações ou conteúdos adicionais
tal como um <em>tooltip</em>, um menu de navegação, etc, então esse conteúdo não vai ser acessível para pessoas que não estiverem utilizando um mouse.
Considerações adicionais são necessárias para acessibilidade.

Para usuários que não possuem deficiência visual, o conteúdo adicional pode ser fornecido diretamente de um modo acessível,
como texto alternativo, por <em> ARIA label </em> ou descrição, ou até um meio fora da tela.
Entretanto, para usuários que navegam conhecendo somente o conteúdo do teclado, deve haver algum mecanismo para que eles 
possam acessar e ver o novo conteúdo ou a nova funcionalidade reveladas. 

Em adicição a `onMouseOver`e `onMouseOut`, use `onFocus` e `onBlur`.
Essas ações são ativadas quando o teclado é utilizado para navegar de ou para um elemento.
É claro que estes só podem ser ativados por <em>keyboard-navigable elements</em> -
links e controle de formulários (ou até talvez elementos com [tabindex](http://webaim.org/techniques/keyboard/tabindex)).
Simplesmente, ativando a mudança com um link comum e usando <em> mouse and keyboard event handlers </em> garantirá a acessibilidade.

Ocasionalmente, scripting é usado para exibir interações complexas, como drop-down ou fly-out menu.
Apesar de ser possível fazer com que essas funcionalidades sejam acessíveis,
as vezes, uma alternativa acessível pode ser mais amigável.
Por exemplo, ao invés de forçar usuários a navegar por um longo e complexo menu de navegação, 
você pode garantir que esse sistema de menu não (NOT) é diretamente acessível pelo teclado (nem lido por um <em>screen reader</em>)
mas prover um link padrão de funcionalidade no nível superior de um menu. (e.g., "Produtos").
Esse link levaria o usuário a uma página secundária que forneceria links padrões para páginas incluidas no menu complexo.
(e.g., uma <em>Products landing page</em> que contém links para várias categorias de produtos).
Ainda que não seja exatamente a mesma interação que <em>mouse users</em> poderiam escolher,
tais alternativas são em geral mais intuitivas e amigáveis para todos usuários.

### `onFocus` e `onBlur`

Estes <em>event handlers</em> são tipicamente utilizados junto de elementos de formulários,
tais como caixas de text fields, radio buttons e submit buttons, mas também podem ser usados com links.<!--Aqui preferi utilizar os termos originais-->
`onFocus` é ativado quando o cursor é colocado em cima ou dentro de um item de formulário especifico,
ou quando o usuário aperta 'tab' para ir de um item a outro.
`onBlur` é ativado quando o cursor sai de um elemento de formulário ou aperta 'tab' para sair dele.

Ambos desses <em>event handlers are device independent</em>,
ou seja, eles podem ser ativados com o mouse, o teclado, ou qualquer tecnologia assistiva.
As ações que são provenientes da execução desses <em>event handlers</em> devem ser analisadas para determinar se elas causam algum problema de acessibilidade.
Geralmente, esses eventos não causam problema algum a não ser que eles estejam modificando o comportamento padrão do navegador 
ou estão interferindo com o navegador de teclado dentro da página.
Exemplos de tais problemas podem estar automaticamente colocando o foco em outras áreas da página com `onFocus` e `onBlur`,
prendendo o usuário dentro do formulário, <em>dynamically revealing form controls immediately upon a user leaving (blurring) a form control, etc.
Keyboard and screen reader testing will be necessary to ensure these interactions are built in an accessible manner.</em>

### `onClick` and `onDblClick`

The `onClick` event handler is triggered when the mouse is pressed when over an HTML element.
`onClick` is intended to be a mouse dependent event handler.
However, if the `onClick` event handler is used with keyboard-navigable links or form controls,
then most major browsers and assistive technologies trigger `onClick` if the <kbd>Enter</kbd> key is pressed when the link or control has focus.
In these cases, `onClick` is a device independent event handler.

Nevertheless, the <kbd>Enter</kbd> key will not always trigger the `onClick` event if it is used with non-link and non-control elements,
such as plain text, table cells, or `<div>` elements,
even if they made keyboard navigable using tabindex or are focused using scripting.
In these cases, it will be necessary to detect the <kbd>Enter</kbd> and <kbd>Space</kbd> key presses while focus is placed on them.

The `onDblClick` event handler is associated with the double click of a mouse on a selected HTML element.
There is no device independent or keyboard equivalent to `onDblClick`, so it must be avoided.

### `onChange` and `onSelect`

The `onChange` event handler is triggered when a form element is selected and changed,
for example, when a radio button is initially selected, when the text changes within a text box or text area,
or when the active item in a select menu changes.
Although these event handlers are device independent and can be activated using the mouse, keyboard, or other device,
the actions that are performed as a result of these event handlers must be analyzed to determine if they cause accessibility problems.

A common use of `onChange` is on select menus to trigger navigation when the active option within the menu is changed.
These menus can cause keyboard accessibility issues because you cannot scroll through the list using a keyboard without selecting one of the options,
and thus triggering the `onChange` event.
Some browsers (including Firefox) override these jump menus so they are not activated on keyboard change,
but only after you either select an item using a mouse or press Enter if using the keyboard.
However, these types of JavaScript 'jump' menus can be made keyboard accessible by removing `onChange` and
providing a submit button separate from the list of choices that activates the currently selected item.

### Using Device Independent Event Handlers

Several event handlers are device independent,
including `onFocus`, `onBlur`, `onSelect`, `onChange`, and `onClick`
(when `onClick` is used with link or form elements).
When possible, use device independent event handlers.
Other event handlers are device dependent, meaning that they rely wholly upon a certain type of input.
For instance, `onMouseOver`, `onMouseOut`, and `onDblClick` rely upon the use of a mouse.
There are also some event handlers that are dependent upon use of the keyboard (`onKeyDown`, `onKeyUp`, etc.).
Multiple device dependent event handlers can be used together to allow both mouse and keyboard activation of JavaScript,
but this requires testing across different browsers and assistive technologies to ensure that accessibility is not limited in any way.

## Other Issues

### Dynamic Content and Accessibility

CSS and JavaScript are sometimes used to display, hide, or move information based upon input from the user or pre-programmed commands.
This is sometimes called Dynamic HTML (DHTML).
Most drop-down or fly-out menus or other types of rich interactions involve scripting. Because most of these elements are modified based upon mouse input,
they are typically inaccessible to users who do not use a mouse.
When dynamic content and interactions is used, two items must be evaluated to determine its impact on accessibility:

1.  Is the event used to trigger a change device independent? If the mouse is required, then it is not fully accessible.
2.  Is the dynamic content or functionality itself accessible?
    If assistive technologies cannot adequately access dynamically triggered content or functionality,
    then it is not fully accessible.

### JavaScript Generated Content

Content generated by JavaScript, such as through `document.write` or other functions is generally accessible to assistive technologies.
In some cases, however, if the dynamic content is constantly changing or if it changes while the user is reading it or has set focus to it,
this can interfere with navigation or browser functionality and cause accessibility problems.
For example, if an element that has keyboard focus is significantly changed, hidden,s
or removed from the page, keyboard focus may revert to the very beginning of the page.

When using dynamic information, you must first ask yourself if it is necessary and vital to the function or content of the page.
If so, there is often a way to provide the content without using inaccessible JavaScript.
For instance, ensuring that the dynamic content is generated via user command or interaction,
rather than automatically or randomly,
can ensure that the content does not change when it is focused or being read.

Additionally, sometimes dynamic content needs to receive keyboard focus.
For example, a dialog box that appears will likely need to be given focus
(using JavaScript `focus()`) after it appears to ensure it is navigated or read immediately.
Additional techniques may be necessary to ensure accessibility for such dynamic elements -
a modal dialog, for example, may need to be programmed to maintain keyboard focus
(rather than allowing focus into other parts of the page that are not available).

### Pop-up Windows

Pop-up windows provide a unique accessibility concern.
First of all, most usability experts would argue against the use of pop-up windows except in extreme cases.
For a visual user, it may be difficult to notice and navigate to the new window or tab.
For someone who is using assistive technologies,
the new window may be annoying and confusing because the default behavior for the link has been modified.
JavaScript implementation may make the new window difficult or impossible to resize or scale for someone using a screen enlarger.
For someone who is blind, there is typically an indication that a new window has opened,
but it may be burdensome to then return back to the original page.
When the screen reader user attempts to return to the previous page by selecting the back button,
it may be confusing to find that this does not work.

When using JavaScript to open new windows,
you can modify the size and position of the new window.
You can also add or remove functionality of the window, such as the ability to resize, display scroll bars, show tool bars, etc.
Be very careful when changing the default behavior of the browser window.
If a user has low vision and must enlarge the content,
a small window that cannot be enlarged and does not display scroll bars would be very inaccessible.
Someone with a motor disability may rely upon large tool bars to accurately control the web browser,
so removing or modifying them may introduce difficulties for this user.

As you can see, there are many difficulties in both usability and accessibility that arise through the use of pop-up windows.
Care must be taken in making the decision to use them.
If they are used, thorough user testing of your implementation is vital to ensure accessibility.
It is generally best to alert the user to the fact that a pop-up window will be opened.

### Redirecting and Refreshing Browser Windows

When the page the browser is viewing suddenly changes or refreshes,
the person viewing that page may become disoriented or confused,
especially if that person is using an assistive technology.
This is commonly done with page redirects when page content has been moved or updated,
or with scripting or `<meta>` tags to refresh pages automatically.
Accessibility guidelines requires that users be given control over time sensitive content changes.
Do not automatically change or refresh the browser window without first alerting the user that the change will occur and giving him/her the ability to disable or postpone the change,
or even better, give the user full control over the page change or redirect.

### Using Pure CSS as a JavaScript Alternative

As mentioned previously, Cascading Style Sheet (CSS) parameters are often modified using JavaScript to create dynamically changing content.
However, much of the dynamic functionality often controlled with JavaScript is now available directly within the specifications for CSS itself.
This allows the construction of interactive and dynamic navigation and layout elements without the need for JavaScript events.
You can create drop-down menus, interactive images, animation,
and other exciting features in web sites without worrying about device dependent event handlers.

It's important to note that CSS is intended for visual styling.
As such, screen readers largely ignore CSS.
It should not generally be used to present content or functionality,
at least not without ensuring the content or functionality is fully accessible.
Using CSS alone to produce dynamic content should only employed with much testing in a variety of browsers and screen readers.

## JavaScript Alternatives

### Introduction

Whenever JavaScript cannot be made directly accessible, an accessible alternative must be provided.
Also, some user agents, such as web-enabled cell phones, tablets, and other mobile devices, do not yet fully utilize JavaScript.
There are several ways you can provide accessible alternatives when the scripting cannot be made accessible or when the end user does not have JavaScript enabled.

### Server-side Processing

In many cases, the functionality provided by JavaScript can or should be duplicated by server-side scripting.
For example, JavaScript is often used to validate form elements before a form is posted.
Instead of implementing such JavaScript programming and its accompanying accessibility techniques,
you could use a server-side script to validate the form elements.
Because scripting can always be disabled or modified by the end user,
it should never be relied on for critical form validation or other functions.
JavaScript is often used to write dynamic information to a web page, such as the current date and/or time.
Again, using a server script or include negates the need for additional accessibility implementation.

### Progressive Enhancement

Progressive enhancement is the technique of using scripting to enhance the functionality or behavior of content and functionality that is already sufficient without scripting.
An example might be adding client-side [form validation and error recovery](http://webaim.org/techniques/formvalidation/)
to a form that already has server-side validation.
The form still functions fine without scripting,
ut the scripting progressively enhances the form to make it more usable and accessible.
This is an excellent approach to developing accessible scripted interfaces -
first start with accessible markup and core HTML (and perhaps server-side) functionality,
then add accessible scripting to make it more efficient, friendly, and accessible.

### `<noscript>`

Making JavaScript natively accessible is very important.
However, in some cases, the end user may not have JavaScript enabled or may be using technologies that do not support JavaScript.
In such cases, you can provide non-JavaScript alternatives to user's who cannot or choose not to view JavaScript content.

When JavaScript is used within a Web page, the most straightforward way to provide an alternative for the JavaScript-generated content is to provide
content within the `<noscript>` element.
The `<noscript>` element can be used within your page to display content in browsers that do not support or have disabled JavaScript.
However, if JavaScript IS enabled the `<noscript>` element is ignored.

<div class="important" markdown="1">
<div class="title">Importante</div>
Providing an accessible alternative within the `<noscript>` element for an inaccessible script will not make the page accessible.
The `<noscript>` content will only display if JavaScript is disabled.
Most screen reader users have JavaScript enabled, and will thus encounter your inaccessible script and not the `<noscript>` content.
**In other words, `<noscript>` is an alternative to scripting, NOT an alternative for inaccessibility.**
</div>

Optimally, the `<noscript>` element would contain equivalent or alternative content or functionality to the scripted content or functionality.
You may, for example, provide a link to an accessible HTML alternative or to a page that utilizes server-side scripting instead.
However, this is often not possible, especially for highly complex applications that cannot be duplicated without scripting.
In these cases you may choose to simply indicate "Your browser does not support JavaScript." or similar.
This does nothing to make the content accessible or usable,
but at least conveys why it is not accessible or usable.

Progressive enhancement can also be used to provide JavaScript alternatives or,
at a minimum, failure messages for when scripting is not available.
For example, an error message or link to an alternative version may be provided in HTML at the beginning of the page,
but if scripting is enabled, it is used to hide this message from view using CSS `display:none;`.
Users without scripting enabled will see the message,but users with scripting will not.