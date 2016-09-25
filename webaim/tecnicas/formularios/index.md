---
layout: translation
date: 2013-08-09 # Data de ultima atualização do original
title: "Como criar formulários acessíveis" # Titulo traduzido
description: "Forms are used for many types of interactions on the web. When we talk about the accessibility of forms, we are usually referring to their accessibility to people who use screen readers or keyboards. People with other types of disabilities are generally less affected by faulty forms. It should be noted, however, that everyone benefits from a well-organized, highly usable form, especially those with cognitive disabilities."

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
issue: https://github.com/webiwg/acessibilidade-web-pt/issues/12
original: {
    title: "Creating Accessible Forms", # Titulo original, no idioma origial
    link: "http://webaim.org/techniques/forms/", # Link para documento original
    dateOfTranslation: "2016-09-17" # Data em que a tradução foi finalizada
}
isDraft: true
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

</style>

<!--
  Pagina 1 http://webaim.org/techniques/forms/
-->

# Visão geral de acessibilidade em formulários

## Introdução

Formulários são usados para muitos tipos de interações na web.
Quando falamos sobre a acessibilidade de formulários,
estamos normalmente referindo-se a sua acessibilidade às pessoas que utilizam leitores de tela ou navegação por teclados.
Pessoas com outros tipos de deficiência são geralmente menos afetada por formulários com defeito.
Deve notar-se, no entanto, que todas as pessoas se beneficiam de um formulário bem organizado,
com grande usabilidade, especialmente aquelas com deficiências cognitivas.

## Certifique-se de que formulários sejam lógicos e fácil de usar

Os formulários devem ser claros e intuitivos. Eles devem ser organizados de uma maneira lógica.
Instruções, sugestões, campos de formulário obrigatórios, requisitos de formatação de campo,
etc, devem ser claramente identificados para os usuários.
De instruções claras sobre as informações desejadas.
Se quaisquer elementos de formulário são obrigatórios, não se esqueça de indicar-lo.
Certifique-se de que a ordem em que os elementos de formulário são acessados é lógica e fácil.
Isto às vezes pode ser problemático se as tabelas são usadas para controlar o layout de itens do formulário.

Para verificar a ordem linear de itens na página,
use [a ferramenta de acessibilidade WAVE](http://wave.webaim.org/).

## Certifique-se de que formulários são acessíveis por teclado

Muitos usuários só podem usar um teclado para navegar e usar a web.
Você deve garantir que os formulários em seu web site podem ser concluídos usando apenas o teclado.
Existem algumas coisas que podem fazer formulários totalmente inutilizáveis com o teclado,
o mais comum dos quais é JavaScript.
Tenha cuidado no seu uso do JavaScript para manipular os dados do formulário,
definir o foco, alterar elementos de formulário ou submeter formulários.
Cada um destes pode tornar o formulário difícil ou impossível para completar ou entender usando apenas teclado.
Sempre teste os formulários do site para acessibilidade através do teclado.

## Associe rótulos de formulários com campos de entrada

Rótulos de texto geralmente deve descrever a função de cada controle de formulário.
Posicione o rótulo junto ao seu respectivo controle de formulário (ou seja, caixa de texto, caixa de seleção, botão de opção, menu, etc.).

Os rótulos são normalmente posicionado acima ou para a esquerda do campo de controle, no entanto,
os rótulos de caixas de seleção e _radio buttons_ são geralmente à direita do controle.
Usuários com visão devem ser capazes de visualmente associar um rótulo de texto com seu controle de formulário correspondente.
Os usuários com deficiência visual, no entanto, não pode fazer essa associação visual.
Os rótulos podem, no entanto, ser associado programaticamente com controles de formulário utilizando marcação HTML.
O elemento `<label>` é utilizado para associar um rótulo de texto a um controle de formulário.
Isso permite que um leitor de tela ler o texto do rótulo associado quando o usuário navega para o controle de formulário.

<div class="important">

<div class="title">Importante</div>
Os usuários de leitores de tela geralmente navegam através de um formulário usando a tecla <kbd> Tab</kbd> para saltar de controle de formulário para formulário de controle.
Rótulos de formulários associados são lidos para cada controle de formulário quando o usuário navega para eles.
Qualquer conteúdo de texto que não for rótulo e estiver entre os controles de formulário são normalmente são pulado.
Tenha certeza de incluir sugestões ou instruções importantes em etiquetas associadas ou no início do formulário.
</div>

Agrupamentos de controles de formulário, normalmente grupos de caixas de seleção e _radio buttons_,
algumas vezes necessitam uma descrição de nível superior (como "Método de envio" para um grupo com oções de envio de _radio buttons_).
Este texto descritivo pode ser associado com o grupo de controlos de formulário usando `<fieldset>` e `<legend>`.
O `<fieldset>` identifica todo o agrupamento e `<legend>` identifica o texto descritivo de agrupamento.
Usando `<fieldset>` e `<legend>` garante que a descrição do texto é lido para os usuários de leitores de tela quando o agrupamento é navegado.

<!--
  Página 2: http://webaim.org/techniques/forms/controls
-->

# Controles de de formulário acessíveis

<form method="post" action=""  markdown="1">

## Entradas de texto

<label for="nome">Nome:</label>
<input id="nome" type="text" name="camponome">

Aqui está a marcação HTML:

<div class="programlisting">
  <code>&lt;label <strong>for="nome"</strong>&gt;Nome:&lt;/label&gt;<br>
  &lt;input <strong>id="nome"</strong> type="text" name="camponome"&gt;
  </code>
</div>
Coloque o mesmo valor para  `for` e `id` para assoriar o rótulo com o respectivo controle de formulário.
Como `id` devem ser únicos para cada página,
apenas um rótulo pode ser associado para cada elemento de formulário
Isto significa que você não pode ter um rótulo associado a multiplos elementos.
Além disso, leitores de tela não suportam associação de multiplos rótilos ao mesmo elemento de formulário.


<div class="note">
  <div class="title">Nota</div>
  <p>Outra vantagem de usar rótulos é que o usuário pode clicar no próprio rótulo para definir o foco para o elemento de formulário.
  Isso é útil para algumas pessoas com deficiências motoras, particularmente quando selecionando pequenas caixas de seleção e _radio buttons_.
  Você pode tentar isso clicando sobre a palavra "Nome:" acima para ver o foco definido para a caixa de texto.
  Ao clicar em rótulos adjacentes proporciona uma maneira fácil de verificar se a rotulagem de formulário é adequada.
  </p>
</div>

## Áreas de texto (do inglês <em lang="en">Textareas</em>)

<p><label for="endereco">Insira seu endereço</label><br>
  <textarea name="textodoendereco" cols="25" rows="5" id="endereco"></textarea>
</p>
<p>Aqui está a marcação HTML:</p>
<div class="programlisting">
  <code>&lt;label for="endereco"&gt;Insira seu endereço:&lt;/label&gt;&lt;br&gt;<br>
  &lt;textarea id="endereco" name="textodoendereco"&gt;&lt;/textarea&gt;
  </code>
</div>

## Quadro de seleção (do inglês <em lang="en">Checkboxes</em>)

<fieldset>
  <legend>Escolha as coberturas da sua pizza:</legend>
  <input id="presunto" type="checkbox" name="coberturas" value="presunto">
  <label for="presunto">Presunto</label>
  <br>
  <input id="pepperoni" type="checkbox" name="coberturas" value="pepperoni">
  <label for="pepperoni">Pepperoni</label>
  <br>
  <input id="cogumelos" type="checkbox" name="coberturas" value="cogumelos">
  <label for="cogumelos">Cogumelos</label>
  <br>
  <input id="azeitonas" type="checkbox" name="coberturas" value="azeitonas">
  <label for="azeitonas">Azeitonas</label>
</fieldset>

<p>Aqui está a marcação HTML:</p>

<div class="programlisting">
  <code>
  &lt;fieldset&gt;<br>
  &lt;legend&gt;Escolha as coberturas da sua pizza:&lt;/legend&gt;<br>
  &lt;input id="presunto" type="checkbox" name="coberturas" value="presunto"&gt;<br>
  &lt;label for="presunto"&gt;Presunto&lt;/label&gt;&lt;br&gt;<br>
  &lt;input id="pepperoni" type="checkbox" name="coberturas" value="pepperoni"&gt;<br>
  &lt;label for="pepperoni"&gt;Pepperoni&lt;/label&gt;&lt;br&gt;<br>
  &lt;input id="cogumelos" type="checkbox" name="coberturas" value="cogumelos"&gt;<br>
  &lt;label for="cogumelos"&gt;Cogumelos&lt;/label&gt;&lt;br&gt;<br>
  &lt;input id="azeitonas" type="checkbox" name="coberturas" value="azeitonas"&gt;<br>
  &lt;label for="azeitonas"&gt;Azeitonas&lt;/label&gt;<br>
  &lt;/fieldset&gt;</code>
</div>

O <code>&lt;fieldset&gt;</code> rodeia todo o agrupamento de Botões do rádio.
O <code>&lt;legend&gt;</code> provê uma descrição para o agrupamento
Em leitores de tela, o texto da legenda é geralmente lido para cada controle no conjunto de campos,
então a legenda deve ser curta e descritiva.


## Botões do rádio (do inglês <em lang="en">Radio buttons</em>)

<fieldset>
  <legend>Escolha um método de envio:</legend>
  <input id="duranteanoite" type="radio" name="metododeentrega" value="duranteanoite">
  <label for="duranteanoite">Durante a noite</label><br>
  <input id="doisdias" type="radio" name="metododeentrega" value="doisdias">
  <label for="doisdias">Dois dias</label><br>
  <input id="motoboy" type="radio" name="metododeentrega" value="motoboy">
  <label for="motoboy">Motoboy</label>
</fieldset>

<p>Aqui está a marcação HTML:</p>

<div class="programlisting">
  <code>&lt;fieldset&gt;<br>
  &lt;legend&gt;Escolha um método de envio:&lt;/legend&gt;<br>
  &lt;input id="duranteanoite" type="radio" name="metododeentrega" value="duranteanoite"&gt;<br>
  &lt;label for="duranteanoite"&gt;Durante a noite&lt;/label&gt;&lt;br&gt;<br>
  &lt;input id="doisdias" type="radio" name="metododeentrega" value="doisdias"&gt;<br>
  &lt;label for="doisdias"&gt;Dois dias&lt;/label&gt;&lt;br&gt;<br>
  &lt;input id="motoboy" type="radio" name="metododeentrega" value="motoboy"&gt;<br>
  &lt;label for="motoboy"&gt;Motoboy&lt;/label&gt;<br>
  &lt;/fieldset&gt;</code>
</div>
<div class="note">
  <div class="title">Note</div>
  <p>Conjunto de campos `fieldset` e legenda só deve ser utilizado para associar grupos de controles quando uma descrição de nível superior (ou seja a legenda) é necessária.
  Quadro de seleção (do inglês <em lang="en">checkbox</em> individuais ou botões de rádio básicos (como masculino / feminino para sexo) que fazem sentido a partir de seus rótulos sozinho não exigem conjunto de campos `fieldset` e legenda. Conjunto de campos `fieldset` aninhados devem ser evitados.</p>
</div>

## Menus de seleção

<p>
  <label for="cidadefavorita">Qual sua cidade favorita?</label>
  <select id="cidadefavorita" name="select">
    <option value="1">Amsterdam</option>
    <option value="2">Buenos Aires</option>
    <option value="3">Delhi</option>
    <option value="4">Hong Kong</option>
    <option value="5">Londes</option>
    <option value="6">Los Angeles</option>
    <option value="7">Moscou</option>
    <option value="8">Mumbai</option>
    <option value="9">New York</option>
    <option value="10">Sao Paulo</option>
    <option value="11">Tokyo</option>
  </select>
</p>

Aqui está a marcação HTML:

<div class="programlisting"><code>&lt;label for="cidadefavorita"&gt;Qual sua cidade favorita?&lt;/label&gt;<br>
  &lt;select id="cidadefavorita" name="select"&gt;<br>
  &lt;option value="1"&gt;Amsterdam&lt;/option&gt;<br>
  &lt;option value="2"&gt;Buenos Aires&lt;/option&gt;<br>
  &lt;option value="3"&gt;Delhi&lt;/option&gt;<br>
  &lt;option value="4"&gt;Hong Kong&lt;/option&gt;<br>
  &lt;option value="5"&gt;Londes&lt;/option&gt;<br>
  &lt;option value="6"&gt;Los Angeles&lt;/option&gt;<br>
  &lt;option value="7"&gt;Moscou&lt;/option&gt;<br>
  &lt;option value="8"&gt;Mumbai&lt;/option&gt;<br>
  &lt;option value="9"&gt;New York&lt;/option&gt;<br>
  &lt;option value="10"&gt;Sao Paulo&lt;/option&gt;<br>
  &lt;option value="11"&gt;Tokyo&lt;/option&gt;<br>
  &lt;/select&gt;</code>
</div>

Para melhorar a acessibilidade desta lista ainda mais, poderíamos acrescentar `optgroup`, para agrupar as opções.

<p>
  <label for="cidadefavorita2">Qual sua cidade favorita?</label>
  <select id="cidadefavorita2" name="cidadefavorita2">
    <optgroup label="Asia">
      <option value="3">Delhi</option>
      <option value="4">Hong Kong</option>
      <option value="8">Mumbai</option>
      <option value="11">Tokyo</option>
    </optgroup>
    <optgroup label="Europa">
      <option value="1">Amsterdam</option>
      <option value="5">Londres</option>
      <option value="7">Moscow</option>
    </optgroup>
    <optgroup label="América do Norte">
      <option value="6">Los Angeles</option>
      <option value="9">New York</option>
    </optgroup>
    <optgroup label="América do Sul">
      <option value="2">Buenos Aires</option>
      <option value="10">Sao Paulo</option>
    </optgroup>
  </select>
</p>
<p>Aqui está a marcação HTML:</p>
<div class="programlisting"><code>&lt;label for="cidadefavorita2"&gt;Qual sua cidade favorita?&lt;/label&gt;<br>
  &lt;select id="cidadefavorita2" name="cidadefavorita2"&gt;<br>
  &lt;optgroup label="Asia"&gt;<br>
  &nbsp;&nbsp;&lt;option value="3"&gt;Delhi&lt;/option&gt;<br>
  &nbsp;&nbsp;&lt;option value="4"&gt;Hong Kong&lt;/option&gt;<br>
  &nbsp;&nbsp;&lt;option value="8"&gt;Mumbai&lt;/option&gt;<br>
  &nbsp;&nbsp;&lt;option value="11"&gt;Tokyo&lt;/option&gt;<br>
  &lt;/optgroup&gt;<br>
  &lt;optgroup label="Europa"&gt;<br>
  &nbsp;&nbsp;&lt;option value="1"&gt;Amsterdam&lt;/option&gt;<br>
  &nbsp;&nbsp;&lt;option value="5"&gt;Londres&lt;/option&gt;<br>
  &nbsp;&nbsp;&lt;option value="7"&gt;Moscow&lt;/option&gt;<br>
  &lt;/optgroup&gt;<br>
  &lt;optgroup label="América do Norte"&gt;<br>
  &nbsp;&nbsp;&lt;option value="6"&gt;Los Angeles&lt;/option&gt;<br>
  &nbsp;&nbsp;&lt;option value="9"&gt;New York&lt;/option&gt;<br>
  &lt;/optgroup&gt;<br>
  &lt;optgroup label="América do Sul"&gt;<br>
  &nbsp;&nbsp;&lt;option value="2"&gt;Buenos Aires&lt;/option&gt;<br>
  &nbsp;&nbsp;&lt;option value="10"&gt;Sao Paulo&lt;/option&gt;<br>
  &lt;/optgroup&gt;<br>
  &lt;/select&gt;</code>
</div>

Note que o `optgroup` não é totalmente suportado por alguns agentes de usuário e leitores de tela,

por isso não deve ser utilizado para apresentar informações de categorização vitais.
Nos casos onde `optgroup` não é suportado, é simplesmente ignorado.
Não confunda o atributo `label` do elemento `optgroup` com o elemento de rótulo `label`.
Eles são coisas bem diferentes.

Menus de seleção múltipla permitem ao usuário escolher mais de uma opção na lista ao mesmo tempo.

<p>
  <label for="cidadesfavoritasmultiplo">Quais suas três cidades favoritas?</label>
  <select id="cidadesfavoritasmultiplo" name="select" multiple="multiple">
    <option value="1">Amsterdam</option>
    <option value="2">Buenos Aires</option>
    <option value="3">Delhi</option>
    <option value="4">Hong Kong</option>
    <option value="5">Londres</option>
    <option value="6">Los Angeles</option>
    <option value="7">Moscow</option>
    <option value="8">Mumbai</option>
    <option value="9">New York</option>
    <option value="10">Sao Paulo</option>
    <option value="11">Tokyo</option>
  </select>
</p>
<div class="note">
  <div class="title">Nota</div>
  <strong>É recomendável que menus de seleção múltipla devem ser evitados</strong>
  Nem todos os navegadores provêm navegação intuitíva para navegação de menus de seleção múltipla
  Muitos usuários não sabem usar <kbd>CTRL</kbd>/<kbd>Command</kbd> ou <kbd>Shift</kbd> + <kbd>click</kbd> para selecionar múltiplos itens.

  Geralmente um conjunto de quadro de seleção (do inglês <em lang="en">Checkboxes</em>) podem prover funcionamento similar,
  porem com funcionalidade mais acessível.
</div>

## Botões

Para botões de formulário (elementos envio `submit` e de limpar dados `reset` , além de elementos botões `button`),
não é obritatório fornecer informação adicional sobre acessibilidade.
O atributo de valor `value` para botões de entrada `input` e o texto dentro do elemento `<button>` elementos serão lidos por leitores de tela quando o botão for acessado.
Estes <em>jamais</em> devem ser deixados vazios.

<p>
  <input type="submit" name="submit" value="Enviar Busca">
  <input type="reset" name="reset" value="Limpar Dados">
  <button>Ativar</button>
</p>
<p>Aqui está a marcação HTML:</p>
<div class="programlisting">
  <code>&lt;input type="submit" name="submit" value="Enviar Busca"&gt;<br>
  &lt;input type="reset" name="reset" value="Limpar Dados"&gt;<br>
  &lt;button&gt;Ativar&lt;/button&gt;
  </code>
</div>

Como botões de limpar dados pode ser acidentalmente pressionados,
são poucos os casos em que deveriam ser usados.

## Botões de imagem

Se você usar um botão de imagem (`<input type="image">` em vez de um botão padrão,
o campo de entrada deve ter o texto alternativo do atributo `alt`.

<input type="image" name="botãodeenviar" src="media/search.png" alt="Pesquisar">


Aqui está a marcação HTML:

<div class="programlisting">
  <code>&lt;input type="image" name="botãodeenviar" <strong>alt="Pesquisar"</strong> src="submit.png"&gt;</code>
</div>

## Menus de salto com JavaScript

Porque estes tipos de menus são ativados quando o item de menu muda, estes menus pode causar problemas de acessibilidade do teclado porque você não pode percorrer a lista sem selecionar uma das opções.

<div class="note">

<div class="title">Nota</div>

Alguns navegadores (inclusive o Firefox) sobrescrevem o comportamento destes menus de salto, logo eles não são ativados com mudança via teclado,
mas apenas quando você os seleciona usando um mouse ou ao pressionar <kbd>Enter</kbd> usando o teclado.

</div>

<script type="text/javascript">
    function MM_jumpMenu(targ,selObj,restore){ //v3.0
    eval(targ+".location='"+selObj.options[selObj.selectedIndex].value+"'");
    if (restore) selObj.selectedIndex=0;
    }
</script>

<label for="selectweb">Vá para um website:</label>
<select id="selectweb" name="menu1" onchange="MM_jumpMenu('parent',this,1)">
  <option selected="selected">Select a web site</option>
  <option value="http://www.webaim.org">WebAIM</option>
  <option value="http://google.com">Google</option>
  <option value="http://www.yahoo.com">Yahoo</option>
  <option value="http://www.microsoft.com">Microsoft</option>
</select>

Fornecer um botão de envio separado do menus de salto que ativa o item atualmente selecionado irá permitir acessibilidade teclado completa.

</form>

<!--
  Pagina 3: http://webaim.org/techniques/forms/advanced
-->

# Advanced Form Labeling

## Introduction

There are times when the `<label>` element falls short—it cannot be used to provide multiple labels for a single form control,
or to associate a single label with multiple form controls.
There are also times when there is not a visible text label to be associated to a form control.
The majority of these labeling limitations can be overcome with three ARIA properties
(`aria-labelledby`, `aria-describedby`, and `aria-label`)
and a couple other techniques outlined on this page.

## `aria-labelledby`

<p>A <code>&lt;label&gt;</code> element indicates which form field it labels by referencing its <code>id</code> attribute value:</p>
<div class="programlisting">
  <code>&lt;label for="fname"&gt;</code>
</div>
<p>It declares, "I am a label for this control".</p>
<p>With <code>aria-labelledby</code>, the form field indicates which element labels it by referencing its <code>id</code> attribute:</p>
<div class="programlisting">
  <code>&lt;input aria-labelledby="fnamelabel"&gt;</code>
</div>
<p>The form control declares, "I am a control labeled by this element").</p>

## Handling Multiple Labels

Because elements in a page must all have unique `id` attribute values,
a `<label>` can only point to the `id` of a single control -
at most a one-to-one relationship between label and control.
`aria-labelledby`, however, allows an element to be referenced as a label for multiple controls,
and allows multiple elements to be referenced as labels for a single control.
In short, `aria-labelledby` overcomes the 1 to 1 limitation of `<label>`.

The following is a simplified example of a table that might be used for data entry.
Each table header functions as a visual label for the form controls in the column below it.
There is only one visual label for multiple form controls.
The `<label>` element cannot be used to associate this text to the multiple text boxes.

<table>
  <tbody>
    <tr>
      <th id="namelabel" scope="col">Name</th>
      <th id="agelabel" scope="col">Age</th>
      <th id="weightlabel" scope="col">Weight</th>
    </tr>
    <tr>
      <td><input type="text" name="name1" aria-labelledby="namelabel"></td>
      <td><input type="text" size="3" name="age1" aria-labelledby="agelabel"></td>
      <td><input type="text" size="4" name="weight1" aria-labelledby="weightlabel"></td>
    </tr>
    <tr>
      <td><input type="text" name="name2" aria-labelledby="namelabel"></td>
      <td><input type="text" size="3" name="age2" aria-labelledby="agelabel"></td>
      <td><input type="text" size="4" name="weight2" aria-labelledby="weightlabel"></td>
    </tr>
    <tr>
      <td><input type="text" name="name2" aria-labelledby="namelabel"></td>
      <td><input type="text" size="3" name="age2" aria-labelledby="agelabel"></td>
      <td><input type="text" size="4" name="weight2" aria-labelledby="weightlabel"></td>
    </tr>
  </tbody>
</table>

<p>The HTML for the first header ("Name") is:</p>
<div class="programlisting">
  <code>
  &lt;th <strong>id="namelabel"</strong> scope="col"&gt;Name&lt;/th&gt;
  </code>
</div>
<p>The HTML for the first text field within the table is:</p>
<div class="programlisting">
  <code>&lt;input type="text" name="name1" <strong>aria-labelledby="namelabel"</strong>&gt;</code>
</div>
<p>This labels the text box with the "Name" text in the table header.
This <code>aria-labelledby</code> attribute could be added to all three Name fields,
thus properly labeling all of them with one text item.</p>
<p>Building on this example, the table below has visual labels along the top and side -
multiple visual labels for each control.</p>
<table>
  <tbody>
    <tr>
      <th scope="col">Name</th>
      <th id="officenum" scope="col">Office Number</th>
      <th id="phonelabel" scope="col">Phone</th>
    </tr>
    <tr>
      <th id="cyndi" scope="col">Cyndi</th>
      <td><input type="text" size="4" name="office1" aria-labelledby="cyndi officenum"></td>
      <td><input type="text" size="12" name="phone1" aria-labelledby="cyndi phonelabel"></td>
    </tr>
    <tr>
      <th id="jared" scope="col">Jared</th>
      <td><input type="text" size="4" name="office2" aria-labelledby="jared officenum"></td>
      <td><input type="text" size="12" name="phone2" aria-labelledby="jared phonelabel"></td>
    </tr>
    <tr>
      <th id="jon" scope="col">Jonathan</th>
      <td><input type="text" size="4" name="office3" aria-labelledby="jon officenum"></td>
      <td><input type="text" size="12" name="phone3" aria-labelledby="jon phonelabel"></td>
    </tr>
  </tbody>
</table>
<p>The HTML for the first field in this table is:</p>
<div class="programlisting">
  <code>&lt;input type="text" name="office1" <strong>aria-labelledby="cyndi officenum"</strong>&gt;</code>
</div>

The `cyndi` and `officenum` values reference the `id`s of the "Cyndi" and "Office Number" table cells.
A screen reader will read "Cyndi Office Number" when navigating into this field.
The reading order of multiple labels is based on the order in which these values are specified.

<div class="note">
  <div class="title">Note</div>
  <p>As a general rule, if a single label is present for a single control, the <code>&lt;label&gt;</code> element should be used to reference it. These labels provide additional functionality - clicking on them sets focus to or activates the control. This is not available when using <code>aria-labelledby</code>.</p>
</div>
<div class="important">
  <div class="title">Important!</div>
  <p>If a control has both an associated <code>&lt;label&gt;</code> <strong>and</strong> <code>aria-labelledby</code>, the referenced <code>aria-labelledby</code> text will override and be read of <em>instead of</em> the associated <code>&lt;label&gt;</code>.</p>
</div>

## `aria-describedby`

There are times when a form includes information that isn't exactly a label but is important enough to be read by a screen reader when navigating to the form control.
This additional information can be associated to the form field with the `aria-describedby` attribute.
For example:

<p>
  <label for="resetpass">Reset Password:</label>
  <input type="password" name="resetpass" id="resetpass" aria-describedby="newpass">
  <br>
  <span id="newpass">New password must be 8-15 characters and include letters and numbers</span>
</p>
<p>Here is the HTML:</p>
<div class="programlisting">
  <code>
  &lt;label for="resetpass"&gt;Reset Password:&lt;/label&gt;<br>
  &lt;input type="password" name="resetpass" id="resetpass" <strong>aria-describedby="newpass"</strong>&gt; <br>
  &lt;br&gt;<br>
  &lt;span <strong>id="newpass"</strong>&gt;New password must be 8-15 characters and include letters and numbers&lt;/span&gt;	</code>
</div>

Because there is a single label, `<label>` is used rather than `aria-labelledby`.
As with `aria-labelledby`, the `aria-describedby` attribute points to the `id` of the element that contains the password requirements.
A screen reader would read both the associated label(s) and then the associated description(s).
Descriptions are sometimes read after a short pause.
`aria-describedby` can also reference multiple elements - just separate the referenced `id` values with spaces.

<div class="note">
  <div class="title">Note</div>
  <ul>
    <li>While the <code>aria-labelledby</code> overrides the <code>&lt;label&gt;</code>, <code>aria-describedby</code> does not. This means that <code>aria-describedby</code> should only be used <em>in addition to a label</em> (e.g., <code>&lt;label&gt;</code> or &lt;input <code>aria-labelledby</code>&gt;), not in place of one.</li>
    <li>The <code>aria-describedby</code> attribute can also be used to reference descriptions that appear as 'tooltips'. Tooltips should become visible to sighted keyboard users when the control has keyboard focus, not just when the user hovers or clicks with a mouse.</li>
  </ul>
</div>

## Invisible Labels

There are times when a text label for a form control does not make sense visually.
The most common example is the "Search" field. Its location within the page,
in conjunction with the Search button, makes its purpose clear to sighted users.
Adding a visual text label would be overkill and could negatively impact the site design.


One of the following three techniques should be used when a visible label is not available:

### Hidden `label`

<p>Hide the <code>&lt;label&gt;</code> element off-screen using CSS. The label will not appear visually, but will still be read by a screen reader.</p>
<p>
  <label class="hidden" for="s">Search Terms</label>
  <input id="s" type="text" name="search">
  <button>Search</button>
</p>
<p> Here is the HTML for the label and form control:</p>
<div class="programlisting">
  <code>
  &lt;label <strong>class="hidden"</strong> for="s"&gt;Search Terms&lt;/label&gt;<br>
  &lt;input type="text" id="s" name="s"&gt;</code>
</div>
<p>The CSS that is used to hide the label, and additional information about this technique, is outlined in our article on <a href="http://webaim.org/techniques/css/invisiblecontent/">invisible content for screen readers</a>.</p>

## `title` attribute

<p>If a form field has a <code>title</code> attribute, but no <code>&lt;label&gt;</code>, the screen reader will read the <code>title</code> as if it were a label.</p>
<p>
  <input id="s-2" type="text" name="s-2" title="Search Terms">
  <button>Search</button>
</p>
<p> Here is the HTML for the form control:</p>
<div class="programlisting">
  <code>
  &lt;input id="s" type="text" name="s" <strong>title="Search Terms"</strong>&gt;
  </code>
</div>
<p>This technique will also cause a tooltip to appear when the user hovers over the field with a mouse, which could be distracting for some users. </p>

## `aria-label`

<p>The <code>aria-label</code> attribute can also be used when there is no text label on the page.</p>
<p>
  <input id="s-3" type="text" name="s-3" aria-label="Search Terms">
  <button>Search</button>
</p>
<div class="programlisting">
  <code>
  &lt;input id="s" type="text" name="s" <strong>aria-label="Search Terms"</strong>&gt;
  </code>
</div>

Unlike `aria-labelledby` which must reference another element,
`aria-label` contains the label text directly. As with `aria-labelledby`,
`aria-label` will override any associated `<label>` elements.


<div class="important">
  <div class="title">Important</div>
  <ul>
    <li>Only one of these recommendations should be implemented. Using two or more together (e.g., a hidden <code>&lt;label&gt;</code> and a duplicate <code>title</code> attribute) can cause information to be repeated by a screen reader. </li>
    <li>Placeholder text (e.g., <code>&lt;input type="text" <strong>placeholder="Search WebAIM"</strong>&gt;</code>) is not a suitable label and should never be used in place of the above techniques.</li>
  </ul>
</div>

## Recap

*   Use `<label>` element when you can. It has excellent browser and screen reader support, and users can click on the label to select the associated form control.
*   Use `aria-labelledby` to overcome the 1:1 limitations of `<label>`.
*   Use `aria-describedby` **in addition to a label** when you need to associate descriptive text to the form control.
*   Use a hidden `<label>` **or** `title` **or** `aria-label` when a visible text label is not available.