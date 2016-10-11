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

### `onClick` e `onDblClick`

O manipulador de evento `onClick` é disparado quando o mouse é pressionado sobre um elemento HTML.
`onClick` destina-se a ser um manipulador de evento dependente do dispositivo mouse.
No entanto, se o manipulador de eventos `onClick` é usado com links navegáveis via teclado ou controles de formulário,
a maioria dos principais navegadores e tecnologias assistivas irão disparar `onClick` se a tecla <kbd>Enter</kbd> é pressionada quando o link ou o controle tem foco.
Nesses casos, o `onClick` é um manipulador de eventos independente de dispositivo.

No entanto, o <kbd>Enter</kbd> não disparará sempre o evento `onClick` se este for usado em algo que não é um link ou controle de formulário,
como texto puro, cécula de tabela, ou elementos `<div>`,
mesmo se eles forem navegaveis com teclado usando tabindex ou focados com uso de <em lang="en">scription</em>
Nestes casos, será necessário detectar o se teclas <kbd>Enter</kbd> e <kbd>Space</kbd> são pressionadas enquanto há foco neles

O manipulador de eventos onDblClick` está associado ao clique do mouse no elemento HTML selecionado.
Não existe um manipulador de eventos independente de dispositivo ou equivalente com teclado ao `onDblClick`, por isso deve ser evitado

### `onChange` e `onSelect`

O manipulador de eventos `onChange` é acionado quando um elemento do formulário é selecionado e alterado,
por exemplo, quando um <em lang="en">radio button</em> é inicialmente selecionado, quando o texto é alterado dentro de uma caixa de texto ou a área de texto,
ou quando um item ativo em um menu de seleção é alterado.
Embora esses manipuladores de eventos são independentes do dispositivo e podem ser ativados usando o mouse, teclado ou outro dispositivo,
as ações que são executadas como resultado desses manipuladores de evento devem ser analisadas para determinar se eles causam problemas de acessibilidade.

Um uso comum de `onChange` é selecionar menus que disparam navegação quando a opção ativa dentro do menu é alterada.
Estes menus podem causar problemas de acessibilidade de teclado, porque você não pode rolar pela lista usando um teclado sem selecionar uma das opções,
e, assim, provocando o evento `onChange`.
Alguns navegadores (incluindo o Firefox) subistituem estes menus de salto para que eles não sejam ativados na mudança do teclado,
Mas só depois que você seleciona um item usando um mouse ou pressione <kbd>Enter</kbd> se usando o teclado.
No entanto, esses tipos de menus JavaScript "de salto" podem ser feitos acessíveis para teclado removendo `onChange` e
fornecendo um botão enviar separado da lista de escolhas que ativa o item atualmente selecionado.

### Usando manipuladores de eventos independentes do dispositivo

Vários manipuladores de eventos são independente de dispositivo,
incluindo o `onFocus`, `onBlur`, `onSelect`, `onChange`, and `onClick`
(quando o `onClick` é usado com elementos link ou de formulário).
Quando possível, use manipuladores de eventos independentes do dispositivo.
Outros manipuladores de eventos são dependentes do dispositivo, significando que eles dependem inteiramente de um determinado tipo de entrada.
Por exemplo, `onMouseOver`, `onMouseOut` e `onDblClick` dependem do uso de um mouse.
Há também algum evento manipuladores que dependem do usam do teclado (`onKeyDown`, `onKeyUp`, etc.).
Vários manipuladores de eventos dependentes do dispositivo podem ser usados juntos para permitir a ativação do mouse e o teclado de JavaScript,
Mas isso requer testes em diferentes navegadores e tecnologias assistivas para garantir que a acessibilidade não é limitada de qualquer forma.

## Outros Problemas

### Conteúdo dinâmico e acessibilidade

CSS e JavaScript são às vezes usados para exibir, ocultar ou mover as informações com base em entrada do usuário ou comandos pré-programados.
Isso às vezes é chamado de HTML dinâmico (DHTML).
A maioria dos menus suspensos ou <em lang="en">fly-out</em> ou outros tipos de interações ricas envolvem criação de scripts. Como a maioria destes elementos é modificada com base na entrada do mouse,
eles são normalmente inacessíveis aos usuários que não usar um mouse.
Quando o conteúdo dinâmico e interações é usado, dois itens devem ser avaliados para determinar o seu impacto na acessibilidade:

1.  O evento usado para disparar a mudança depende do dispositivo? Se mouse é requerido, então não é totalmente acessível.
2.  O conteúdo criado dinamicamente ou a funcionalidade propriamente dita é acessível?
    Se tecnologia assistiva não consegue acessar o conteúdo criado dinamicamente ou sua funcionalidade,
    então não é completamente acessível.

### Conteúdo gerado com JavaScript


Conteúdo gerado por JavaScript, como através de `document.write` ou outras funções é geralmente acessível para tecnologias assistivas.
Em alguns casos, no entanto, se o conteúdo dinâmico está constantemente mudando ou se muda enquanto o usuário está lendo ou tiver definido o foco,
isso pode interferir com a funcionalidade de navegação ou browser e causar problemas de acessibilidade.
Por exemplo, se um elemento que tenha o foco do teclado é significativamente alterado, ocultado,
ou removido da página, o foco do teclado pode reverter para o início da página.

Ao usar informações dinâmicas, você primeiro deve perguntar-se se é necessário e vital para a função ou o conteúdo da página.
Em caso afirmativo, há muitas vezes uma forma de fornecer o conteúdo sem usar JavaScript inacessível.
Por exemplo, garantindo que o conteúdo dinâmico é gerado através do comando do usuário ou interação,
em vez de automaticamente ou aleatoriamente,
pode garantir que o conteúdo não muda quando é focado ou sendo lido.

Além disso, o conteúdo dinâmico às vezes precisa receber o foco do teclado.
Por exemplo, uma caixa de diálogo que aparece provavelmente precisará ser dado foco
(usando JavaScript `focus()`) depois dela aparece para garantir que é navegada ou lida imediatamente.
Técnicas adicionais podem ser necessárias para assegurar a acessibilidade de tais elementos dinâmicos -
uma caixa de diálogo modal, por exemplo, pode precisar de ser programada para manter o foco do teclado
(ao invés de permitir o foco em outras partes da página que não estão disponíveis).

### Janelas pop-up

Janelas pop-up fornecem uma preocupação única de acessibilidade.
Em primeiro lugar, a maioria dos especialistas em usabilidade argumentam contra o uso de janelas pop-up, exceto em casos extremos.
Para um usuário visual, pode ser difícil de notar e de navegar para a nova janela ou aba.
Para alguém que está usando tecnologias assistivas,
a nova janela pode ser chata e confusa porque o comportamento padrão para o link foi modificado.
Implementação de JavaScript pode fazer nova janela difícil ou impossível para redimensionar ou escalar para alguém usando um ampliador de tela.
Para alguém que é cego, normalmente há uma indicação de que uma nova janela se abriu,
Mas pode ser onerosa para em seguida voltar para a página original.
Quando o usuário de leitor de tela tenta retornar à página anterior, selecionando o botão de voltar,
pode ser confuso para achar que isso não funciona.

Ao usar JavaScript para abrir novas janelas,
Você pode modificar o tamanho e a posição da nova janela.
Você também pode adicionar ou remover a funcionalidade da janela, como a capacidade de redimensionar, Exibir barras de rolagem, mostrar barras de ferramentas, etc.
Tenha muito cuidado ao alterar o comportamento padrão da janela do navegador.
Se um usuário tem baixa visão e deve ampliar o conteúdo,
uma pequena janela que não pode ser ampliada e não exibe barras de rolagem seria muito inacessível.
Alguém com deficiência motora pode confiar em barras de ferramenta grande para controlar com precisão o navegador da web,
Então, removendo ou modificando-os pode apresentar dificuldades para este usuário.

Como você pode ver, existem muitas dificuldades em usabilidade e acessibilidade que surgem com o uso de janelas pop-up.
Deve-se tomar cuidado em tomar a decisão de usá-las.
Se elas são usadas, teste de usuário completo da sua implementação é vital para garantir a acessibilidade.
É geralmente melhor alertar o usuário para o fato de que uma janela pop-up será aberta.

### Redirecionando e Atualizando Janelas do Navegador

Quando a página do navegador está sendo vista e de repente muda ou atualiza,
a pessoa que está exibindo essa página pode tornar-se desorientada ou confusa,
especialmente se essa pessoa está usando uma tecnologia assistiva.
Isto é comumente feito com redirecionamentos de página quando o conteúdo da página foi movido ou atualizado,
ou com scripts ou tags de `<meta>` para atualizar páginas automaticamente.
As diretrizes de acessibilidade exige que aos usuários deve ser dado controle sobre conteúdo que é sensível a passagem de tempo.
Não alterar ou atualiza automaticamente a janela do navegador sem primeiro alertar o usuário que a mudança irá ocorrer e dando-lhe a capacidade de desabilitar ou adiar a mudança,
ou melhor ainda, dar ao usuário controle completo sobre a mudança de página ou redirecionamento.

### Uso de CSS Puro Como Alternativa ao JavasScript

Como mencionado anteriormente, folhas de estilo em cascada, do inglês <em lang="en">Cascading Style Sheet</em> (CSS), são muitas vezes modificadas usando JavaScript para criar dinamicamente conteúdo.
No entanto, grande parte da funcionalidade dinâmica muitas vezes controlada com JavaScript está disponível diretamente dentro das especificações para CSS em si.
Isto permite a construção de elementos de navegação e layout interativos e dinâmicos sem a necessidade de eventos de JavaScript.
Você pode criar menus suspensos, imagens interativas, animação,
e outros recursos interessantes em sites da web sem se preocupar com manipuladores de eventos dependentes do dispositivo.

É importante notar que CSS destina-se para o estilo visual.
Como tal, os leitores de tela ignoram a maioria do CSS.
Ele geralmente não deve ser usado para apresentar conteúdo ou funcionalidade,
pelo menos não sem garantir que o conteúdo ou a funcionalidade é completamente acessível.
Usando CSS sozinho para produzir conteúdo dinâmico deve somente empregados com quantidade de testes em uma variedade de navegadores e leitores de tela.

## Alternativas ao JavaScript

<!--
   N.T.: O @suissa vai ficar p da vida ao revisar essa parte do texto original,
         só tem que levar em conta que o artigo é de 2013. Outro ponto é que
         em estatisticas recentes, quem usa tecnologia assistiva USA javascript
         ativado sim. Se ele realmente fizer questão, podemos adicionar uma
         notação SEPARADA e clara de nota de tradução, mas não podemos
         alterar o texto original sem avisar a WebAIM (@fititnt, 2016-10-11 02:34)
-->

### Introdução

Sempre que o JavaScript não pode ser feito acessível diretamente, deve ser fornecida uma alternativa acessível.
Além disso, alguns agentes de usuário, tais como celulares habilitados para web, tablets e outros dispositivos móveis, não ainda utilizam JavaScript completamente.
Existem várias maneiras que você pode fornecer alternativas acessíveis quando o script não pode ser feito acessível ou quando o usuário final não tem JavaScript habilitado.

### Processamento do lado do servidor

Em muitos casos, a funcionalidade fornecida pelo JavaScript pode ou deve ser repetida por script do lado do servidor.
Por exemplo, JavaScript é muitas vezes usado para validar elementos de formulário antes que um formulário é enviado.
Em vez de implementar tal programação JavaScript e suas respectivas técnicas de acessibilidade,
Você pode usar um programação do lado do servidor para validar os elementos de formulário.
Porque o script pode sempre ser desativado ou modificado pelo usuário final,
isso nunca deve ser invocado para validação de forma crítica ou outras funções.
JavaScript é usado frequentemente para gravar informações dinâmicas em uma página da web, tais como a data atual e/ou tempo.
Novamente, usando processamento do lado do servidor nega a necessidade de implementação de acessibilidade adicionais.

### Aprimoramento Progressivo

Aprimoramento Progressivo, do inglês <em lang="en">Progressive enhancement</em>, é a técnica de usar scripts para melhorar a funcionalidade ou comportamento de conteúdos e funcionalidades que já é suficiente sem uso de JavasScript.
Um exemplo poderia ser a adição do lado do cliente de [validação de formulários e mensagens de erro](http://webaim.org/techniques/formvalidation/)
de uma forma que já tem a validação do lado do servidor.
O formulário ainda funciona muito bem sem scripts,
porém uso de Javascript melhora progressivamente o formulário de modo a torná-lo mais útil e acessível.
Esta é uma excelente abordagem para desenvolver interfaces de script acessíveis -
Primeiro comece com marcação acessível e HTML básico que funcione (ainda que com ajuda do lado do servidor),
em seguida, adicione scripts acessível para torná-lo mais eficiente, amigável e acessível.

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