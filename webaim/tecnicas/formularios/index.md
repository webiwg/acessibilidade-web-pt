---
layout: translation
date: 2014-12-19 # Data de ultima atualização do original
title: "Criando Formulários Acessíveis" # Titulo traduzido
description: "Formulários são usados para muitos tipos de interações na web. Quando falamos sobre a acessibilidade de formulários, estamos normalmente referindo-se a sua acessibilidade às pessoas que utilizam leitores de tela ou navegação por teclados."

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
reviewers: [{
    name: "Daniel Oliveira",
    link: "https://twitter.com/ddtaoli"
}]
discussion: https://github.com/webiwg/acessibilidade-web-pt/issues/12
original: {
    title: "Creating Accessible Forms", # Titulo original, no idioma origial
    link: "http://webaim.org/techniques/forms/", # Link para documento original
    dateOfTranslation: "2016-09-25" # Data em que a tradução foi finalizada
}
isDraft: false
isReleaseCandidate: true
---

<!-- Geração automática de índice, inicio -->
<nav markdown="1">

## Índice de tópicos
{:.no_toc}

1. Índice de Tópicos. Esta linha será substituída
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

<!--
  Pagina 1 http://webaim.org/techniques/forms/
-->

<!--
  N.T.:
  Não há tradução em português para "radio button", porém em espanhol foi
  traduzido como "botón de opción", que para o português ficaria "botão de opção".
  Sugiro no entanto manter o nome em inglês, já que o público alvo terá maior
  facilidade em compreender a nomenclatura original do que uma possível tradução.
  (@ddtaoli, 2016-09-30 23:05)

  Sugiro traduzir "labels" como "etiquetas" ao invés de "rótulos".
  (@ddtaoli, 2016-10-01 01:02)
-->

## Visão geral de acessibilidade em formulários

### Introdução

Formulários são usados para muitos tipos de interações na web.
Quando falamos sobre a acessibilidade de formulários,
estamos normalmente nos referindo a sua acessibilidade às pessoas que utilizam leitores de tela ou navegação por teclados.
Pessoas com outros tipos de deficiência são geralmente menos afetadas por formulários com defeito.
Deve-se notar, no entanto, que todos se beneficiam de um formulário bem organizado,
com grande usabilidade, especialmente aquelas pessoas com deficiências cognitivas.

### Certifique-se de que os formulários sejam lógicos e fáceis de usar

Os formulários devem ser claros e intuitivos. Eles devem ser organizados de uma maneira lógica.
Instruções, sugestões, campos de formulário obrigatórios, requisitos de formatação de campo,
etc, devem ser claramente identificados para os usuários.
Dê instruções claras sobre as informações desejadas.
Se quaisquer elementos de formulário são obrigatórios, não se esqueça de indica-los.
Certifique-se de que a ordem em que os elementos de formulário são acessados seja lógica e fácil.
Isto as vezes pode ser problemático se tabelas são usadas para controlar o layout de itens do formulário.

Para verificar a ordem linear de itens na página,
use [a ferramenta de acessibilidade WAVE](http://wave.webaim.org/).

### Certifique-se de que os formulários são acessíveis por teclado

Muitos usuários só podem navegar e usar a web através do teclado.
Você deve garantir que os formulários em seu web site possam ser concluídos usando apenas o teclado.
Existem algumas coisas que podem tornar os formulários totalmente inutilizáveis com o teclado,
das quais a mais comum é o JavaScript.
Tenha cuidado no uso do JavaScript para manipular os dados de formulário,
definir o foco, alterar elementos de formulário ou submeter formulários.
Cada um destes itens pode tornar o formulário difícil ou impossível, para completar ou entender, usando apenas o teclado.
Sempre teste a acessibilidade através do teclado para os formulários do seu site.

### Associe etiquetas de formulários com campos de entrada

Etiquetas de texto geralmente devem descrever a função de cada campo de formulário.
Posicione a etiqueta junto ao seu respectivo campo de formulário (ou seja, caixa de texto, caixa de seleção, "radio button", menu, etc.).

As etiquetas são normalmente posicionadas acima ou à esquerda do campo de formulário, no entanto,
as etiquetas de caixas de seleção e "radio buttons" estão geralmente à direita do campo de formulário.
Usuários com visão devem ser capazes de visualmente associar uma etiqueta de texto ao seu campo correspondente.
No entanto, os usuários com deficiência visual não podem fazer essa associação visual.
As etiquetas podem, contudo, ser associadas programaticamente com campos de formulário utilizando marcação HTML.
O elemento `<label>` é utilizado para associar uma etiqueta de texto a um campo de formulário.
Isso permite que um leitor de tela leia o texto da etiqueta associada quando o usuário navegar pelo campo de formulário.

<div class="important">

<div class="title">Importante</div>
Os usuários de leitores de tela geralmente navegam através de um formulário usando a tecla <kbd> Tab</kbd> para saltar de campo de formulário para outro campo.
Etiquetas de texto associadas são lidas em cada campo de formulário quando o usuário navega por eles.
Qualquer conteúdo de texto que não seja uma etiqueta e estiver entre os campos de formulário são normalmente pulados.
Tenha certeza de incluir sugestões ou instruções importantes em etiquetas associadas ou no início do formulário.
</div>

Algumas vezes agrupamentos de campos de formulário, normalmente grupos de caixas de seleção e "radio buttons",
necessitam de uma descrição de nível superior (como "Método de envio" para um grupo com oções de envio de "radio buttons").
Este texto descritivo pode ser associado com o grupo de campos de formulário usando `<fieldset>` e `<legend>`.
O `<fieldset>` identifica todo o agrupamento e `<legend>` identifica o texto descritivo do agrupamento.
Usando `<fieldset>` e `<legend>` garante-se que a descrição do texto seja lida para os usuários de leitores de tela quando o agrupamento é navegado.

<!--
  Página 2: http://webaim.org/techniques/forms/controls
            Last updated: Aug 9, 2013
-->

## Controles de formulários acessíveis

<form method="post" action=""  markdown="1">

### Entradas de texto

<label for="nome">Nome:</label>
<input id="nome" type="text" name="camponome">

Aqui está a marcação HTML:

<div class="programlisting">
  <code>&lt;label <strong>for="nome"</strong>&gt;Nome:&lt;/label&gt;<br>
  &lt;input <strong>id="nome"</strong> type="text" name="camponome"&gt;
  </code>
</div>
Coloque o mesmo valor para `for` e `id` para associar a etiqueta com o respectivo campo de formulário.
Como `id` deve ser único para cada página,
apenas uma etiqueta pode ser associado para cada elemento de formulário.
Isto significa que você não pode ter uma etiqueta associada a múltiplos elementos.
Além disso, leitores de tela não suportam associação de múltiplas etiquetas ao mesmo elemento de formulário.


<div class="note">
  <div class="title">Nota</div>
  <p>Outra vantagem de usar etiquetas é que o usuário pode clicar na própria etiqueta para definir o foco para o elemento de formulário.
  Isso é útil para algumas pessoas com deficiências motoras, particularmente quando selecionando pequenas caixas de seleção e "radio buttons".
  Você pode tentar isso clicando sobre a palavra "Nome:" acima para ver o foco definido para a caixa de texto.
  Clicar em etiquetas adjacentes proporciona uma maneira fácil de verificar se a etiquetagem de formulário é adequada.
  </p>
</div>

### Áreas de texto (do inglês <em lang="en">Textareas</em>)

<p><label for="endereco">Insira seu endereço</label><br>
  <textarea name="textodoendereco" cols="25" rows="5" id="endereco"></textarea>
</p>
<p>Aqui está a marcação HTML:</p>
<div class="programlisting">
  <code>&lt;label for="endereco"&gt;Insira seu endereço:&lt;/label&gt;&lt;br&gt;<br>
  &lt;textarea id="endereco" name="textodoendereco"&gt;&lt;/textarea&gt;
  </code>
</div>

### Quadro de seleção (do inglês <em lang="en">Checkboxes</em>)

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

O <code>&lt;fieldset&gt;</code> rodeia todo o agrupamento de "radio buttons".
O <code>&lt;legend&gt;</code> provê uma descrição para o agrupamento
Em leitores de tela, o texto da legenda é geralmente lido para cada campo no conjunto de campos,
então a legenda deve ser curta e descritiva.


### Radio Buttons

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
  <p>Conjunto de campos `fieldset` e legenda só devem ser utilizados para associar grupos de campos quando uma descrição de nível superior (ou seja a legenda) é necessária.
  Quadro de seleção (do inglês <em lang="en">checkbox</em> individuais ou "radio buttons" básicos (como masculino / feminino para sexo) que fazem sentido a partir de suas etiquetas sozinhas não exigem conjunto de campos `fieldset` e legenda. Conjunto de campos `fieldset` aninhados devem ser evitados.</p>
</div>

### Menus de seleção

<p>
  <label for="cidadefavorita">Qual sua cidade favorita?</label>
  <select id="cidadefavorita" name="select">
    <option value="1">Amsterdã</option>
    <option value="2">Buenos Aires</option>
    <option value="3">Nova Déli</option>
    <option value="4">Hong Kong</option>
    <option value="5">Londres</option>
    <option value="6">Los Angeles</option>
    <option value="7">Moscou</option>
    <option value="8">Mumbai</option>
    <option value="9">Nova York</option>
    <option value="10">São Paulo</option>
    <option value="11">Tóquio</option>
  </select>
</p>

Aqui está a marcação HTML:

<div class="programlisting"><code>&lt;label for="cidadefavorita"&gt;Qual a sua cidade favorita?&lt;/label&gt;<br>
  &lt;select id="cidadefavorita" name="select"&gt;<br>
  &lt;option value="1"&gt;Amsterdã&lt;/option&gt;<br>
  &lt;option value="2"&gt;Buenos Aires&lt;/option&gt;<br>
  &lt;option value="3"&gt;Nova Déli&lt;/option&gt;<br>
  &lt;option value="4"&gt;Hong Kong&lt;/option&gt;<br>
  &lt;option value="5"&gt;Londres&lt;/option&gt;<br>
  &lt;option value="6"&gt;Los Angeles&lt;/option&gt;<br>
  &lt;option value="7"&gt;Moscou&lt;/option&gt;<br>
  &lt;option value="8"&gt;Mumbai&lt;/option&gt;<br>
  &lt;option value="9"&gt;Nova York&lt;/option&gt;<br>
  &lt;option value="10"&gt;São Paulo&lt;/option&gt;<br>
  &lt;option value="11"&gt;Tóquio&lt;/option&gt;<br>
  &lt;/select&gt;</code>
</div>

Para melhorar a acessibilidade desta lista ainda mais, poderíamos acrescentar `optgroup`, para agrupar as opções.

<p>
  <label for="cidadefavorita2">Qual a sua cidade favorita?</label>
  <select id="cidadefavorita2" name="cidadefavorita2">
    <optgroup label="Asia">
      <option value="3">Nova Déli</option>
      <option value="4">Hong Kong</option>
      <option value="8">Mumbai</option>
      <option value="11">Tóquio</option>
    </optgroup>
    <optgroup label="Europa">
      <option value="1">Amsterdã</option>
      <option value="5">Londres</option>
      <option value="7">Moscou</option>
    </optgroup>
    <optgroup label="América do Norte">
      <option value="6">Los Angeles</option>
      <option value="9">Nova York</option>
    </optgroup>
    <optgroup label="América do Sul">
      <option value="2">Buenos Aires</option>
      <option value="10">São Paulo</option>
    </optgroup>
  </select>
</p>
<p>Aqui está a marcação HTML:</p>
<div class="programlisting"><code>&lt;label for="cidadefavorita2"&gt;Qual a sua cidade favorita?&lt;/label&gt;<br>
  &lt;select id="cidadefavorita2" name="cidadefavorita2"&gt;<br>
  &lt;optgroup label="Asia"&gt;<br>
  &nbsp;&nbsp;&lt;option value="3"&gt;Nova Déli&lt;/option&gt;<br>
  &nbsp;&nbsp;&lt;option value="4"&gt;Hong Kong&lt;/option&gt;<br>
  &nbsp;&nbsp;&lt;option value="8"&gt;Mumbai&lt;/option&gt;<br>
  &nbsp;&nbsp;&lt;option value="11"&gt;Tóquio&lt;/option&gt;<br>
  &lt;/optgroup&gt;<br>
  &lt;optgroup label="Europa"&gt;<br>
  &nbsp;&nbsp;&lt;option value="1"&gt;Amsterdã&lt;/option&gt;<br>
  &nbsp;&nbsp;&lt;option value="5"&gt;Londres&lt;/option&gt;<br>
  &nbsp;&nbsp;&lt;option value="7"&gt;Moscou&lt;/option&gt;<br>
  &lt;/optgroup&gt;<br>
  &lt;optgroup label="América do Norte"&gt;<br>
  &nbsp;&nbsp;&lt;option value="6"&gt;Los Angeles&lt;/option&gt;<br>
  &nbsp;&nbsp;&lt;option value="9"&gt;Nova York&lt;/option&gt;<br>
  &lt;/optgroup&gt;<br>
  &lt;optgroup label="América do Sul"&gt;<br>
  &nbsp;&nbsp;&lt;option value="2"&gt;Buenos Aires&lt;/option&gt;<br>
  &nbsp;&nbsp;&lt;option value="10"&gt;São Paulo&lt;/option&gt;<br>
  &lt;/optgroup&gt;<br>
  &lt;/select&gt;</code>
</div>

Note que o `optgroup` não é totalmente suportado por alguns agentes de usuário e leitores de tela,
por isso não deve ser utilizado para apresentar informações de categorização vitais.
Nos casos onde `optgroup` não é suportado, é simplesmente ignorado.
Não confunda o atributo `label` do elemento `optgroup` com o elemento de etiqueta `label`.
Eles são coisas bem diferentes.

Menus de seleção múltipla permitem ao usuário escolher mais de uma opção na lista ao mesmo tempo.

<p>
  <label for="cidadesfavoritasmultiplo">Quais as suas três cidades favoritas?</label>
  <select id="cidadesfavoritasmultiplo" name="select" multiple="multiple">
    <option value="1">Amsterdã</option>
    <option value="2">Buenos Aires</option>
    <option value="3">Nova Déli</option>
    <option value="4">Hong Kong</option>
    <option value="5">Londres</option>
    <option value="6">Los Angeles</option>
    <option value="7">Moscou</option>
    <option value="8">Mumbai</option>
    <option value="9">Nova York</option>
    <option value="10">São Paulo</option>
    <option value="11">Tóquio</option>
  </select>
</p>
<div class="note">
  <div class="title">Nota</div>
  <strong>É recomendável que menus de seleção múltipla sejam evitados</strong>
  Nem todos os navegadores provêm navegação intuitiva para navegação de menus de seleção múltipla.
  Muitos usuários não sabem usar <kbd>CTRL</kbd>/<kbd>Command</kbd> ou <kbd>Shift</kbd> + <kbd>click</kbd> para selecionar múltiplos itens.

  Geralmente um conjunto de quadro de seleção (do inglês <em lang="en">Checkboxes</em>) podea prover funcionamento similar,
  porém com funcionalidade mais acessível.
</div>

### Botões

Para botões de formulário (elementos envio `submit` e de limpar dados `reset` , além de elementos botões `button`),
não é obritatório fornecer informação adicional sobre acessibilidade.
O atributo de valor `value` para botões de entrada `input` e o texto dentro do elemento `<button>` serão lidos por leitores de tela quando o botão for acessado.
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

Como botões de limpar dados podem ser acidentalmente pressionados,
são poucos os casos em que deveriam ser usados.

### Botões de imagem

Se você usar um botão de imagem (`<input type="image">` em vez de um botão padrão,
o campo de entrada deve ter o texto alternativo do atributo `alt`.

<input type="image" name="botãodeenviar" src="media/search.png" alt="Pesquisar">


Aqui está a marcação HTML:

<div class="programlisting">
  <code>&lt;input type="image" name="botãodeenviar" <strong>alt="Pesquisar"</strong> src="submit.png"&gt;</code>
</div>

### Menus de salto com JavaScript

Porquê estes tipos de menus são ativados quando o item de menu muda, estes menus podem causar problemas de acessibilidade do teclado porque você não pode percorrer a lista sem selecionar uma das opções.

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

Fornecer um botão de envio separado dos menus de salto que ativa o item atualmente selecionado irá permitir acessibilidade completa do teclado.

</form>

<!--
  Pagina 3: http://webaim.org/techniques/forms/advanced
            Last updated: Dec 19, 2014
-->

## Etiquetagem avançada de formulários

### Introdução

Há momentos em que o elemento de etiquetagem `<label>` deixa a desejar -- não pode ser usado para fornecer várias etiquetas para um só campo de formulário,
ou não se pode associar apenas uma etiqueta com múltiplos campos de formulário
Há também momentos quando não há uma etiqueta de texto visível para ser associada a um campo de formulário.
A maioria destas limitações de etiquetagem podem ser superadas com três propriedades ARIA
(`aria-labelledby`, `aria-describedby`, e `aria-label`)
e um par de outras técnicas descritas nesta página.

### `aria-labelledby`

<!--
  @fititnt Nota de tradução/revisão: este tópico não faz sentido. Posso estar cansado e sem
           ritalina agora, mas o código proposto aqui não faz o que o texto diz que faz
           (fititnt, 2016-09-25 08:35)
  @fititnt Eu estava errado. Faz sentido sim. (fititnt, 2016-09-25 09:17)
-->

Um elemento de etiquetagem `<label>` indica de qual campo de formulário etiquetar referenciando o `id` do elemento:

<div class="programlisting">
  <code>&lt;label for="fname"&gt;</code>
</div>
Ele declara "Eu sou a etiqueta para este campo".

Com `aria-labelledby`, o campo de formulário indica qual elemento o nomeia ao referenciar o atributo `id`:

<div class="programlisting">
  <code>&lt;input aria-labelledby="fnamelabel"&gt;</code>
</div>

O campo de formulário declara, "Eu sou um campo nomeado por esta etiqueta".

### Manipulação de múltiplas etiquetas

Como os elementos em uma página devem todos ter valor exclusivo do atributo `id`,
uma `<label>` pode apenas apontar para o `id` de um único campo -
no máximo uma relação um-para-um entre campo e etiqueta
`aria-labelledby`, por outro lado, permite que um elemento seja referência de etiqueta para vários campos,
e permite que múltiplos elementos sejam referência como etiqueta para um campo apenas.
Resumindo, `aria-labelledby` remove a limitação de um-para-um de `<label>`.

Na sequência há um exemplo simplificado de uma tabela que pode ser usada para a entrada de dados.
Cada cabeçalho de tabela funciona como etiqueta visual nas colunas abaixo dela.
Há apenas uma etiqueta visual para vários campos de formulário.
O elemento `<label>` não pode ser usado para associar seu texto com as múltiplas caixas de texto.

<!--
  @fititnt O código original PARECE ter um erro nos atributos name repetidos na tabela.
           O grupo 2 e três ambos terminam no iriginal com 2 (i.e. age2, weigth2)
           (fititnt, 2016-09-25 09:19)
-->

<table>
  <tbody>
    <tr>
      <th id="rotulonome" scope="col">Nome</th>
      <th id="rotuloidade" scope="col">Idade</th>
      <th id="rotulopeso" scope="col">Peso</th>
    </tr>
    <tr>
      <td><input type="text" name="nome1" aria-labelledby="rotulonome"></td>
      <td><input type="text" size="3" name="idade1" aria-labelledby="rotuloidade"></td>
      <td><input type="text" size="4" name="peso1" aria-labelledby="rotulopeso"></td>
    </tr>
    <tr>
      <td><input type="text" name="nome2" aria-labelledby="rotulonome"></td>
      <td><input type="text" size="3" name="idade2" aria-labelledby="rotuloidade"></td>
      <td><input type="text" size="4" name="peso2" aria-labelledby="rotulopeso"></td>
    </tr>
    <tr>
      <td><input type="text" name="nome2" aria-labelledby="rotulonome"></td>
      <td><input type="text" size="3" name="idade2" aria-labelledby="rotuloidade"></td>
      <td><input type="text" size="4" name="peso2" aria-labelledby="rotulopeso"></td>
    </tr>
  </tbody>
</table>

O HTML para o primeiro cabeçalho ("Nome") é:

<div class="programlisting">
  <code>
  &lt;th <strong>id="rotulonome"</strong> scope="col"&gt;Nome&lt;/th&gt;
  </code>
</div>

O HTML para o primeiro campo de texto da tabela é:


<div class="programlisting">
  <code>&lt;input type="text" name="nome1" <strong>aria-labelledby="rotulonome"</strong>&gt;</code>
</div>

Isso etiquetará a caixa de texto com o texto "Nome" no cabeçalho da tabela.
Este atributo `aria-labelledby` pode ser adicionado a todos os três campos "Nome",
assim adequadamente etiquetando todos eles com apenas um item de texto.

Com base neste exemplo, o quadro que se segue tem etiquetas visuais ao longo do topo e do lado - várias 
etiquetas visuais para cada campo de formulário.



<table>
  <tbody>
    <tr>
      <th scope="col">Nome</th>
      <th id="numeroescritorio" scope="col">Número do Escritório</th>
      <th id="etiquetatelefone" scope="col">Telefone</th>
    </tr>
    <tr>
      <th id="cyndi" scope="col">Cyndi</th>
      <td><input type="text" size="4" name="escritorio1" aria-labelledby="cyndi numeroescritorio"></td>
      <td><input type="text" size="12" name="telefone1" aria-labelledby="cyndi etiquetatelefone"></td>
    </tr>
    <tr>
      <th id="jared" scope="col">Jared</th>
      <td><input type="text" size="4" name="escritorio2" aria-labelledby="jared numeroescritorio"></td>
      <td><input type="text" size="12" name="telefone2" aria-labelledby="jared etiquetatelefone"></td>
    </tr>
    <tr>
      <th id="jon" scope="col">Jonathan</th>
      <td><input type="text" size="4" name="escritorio3" aria-labelledby="jon numeroescritorio"></td>
      <td><input type="text" size="12" name="telefone3" aria-labelledby="jon etiquetatelefone"></td>
    </tr>
  </tbody>
</table>

O HTML para o primeiro campo desta tabela é:

<div class="programlisting">
  <code>&lt;input type="text" name="escritorio1" <strong>aria-labelledby="cyndi numeroescritorio"</strong>&gt;</code>
</div>

Os valores `cyndi` e `numeroescritorio` referenciam os `id`s das células de tabela  "Cyndi" e "Número do Escritório".
Um leitor de tela irá ler "Cyndi Número do Escritório" ao navegar nesse campo.
A ordem de leitura das várias etiqeutas baseia-se na ordem em que estes valores são especificados.

<div class="note">
  <div class="title">Nota</div>
  <p>Como regra geral, se uma única etiqueta está presente para um único campo de formulário, 
  o elemento <code>&lt;label&gt;</code> deve ser usado para fazer a referência. 
  Essas etiquetas fornecem funcionalidade adicional - clicando sobre elas define-se o foco ou ativa o controle.
  Isto não ocorre com o uso de <code>aria-labelledby</code>.</p>

</div>
<div class="important">
  <div class="title">Importante!</div>
  <p>Se um campo de formulário tiver ao mesmo tempo <code>&lt;label&gt;</code> <strong>e</strong> <code>aria-labelledby</code>
  a referencia definida por <code>aria-labelledby</code> irá sobrescrever e ser lida <em>em vez de</em> do elemento <code>&lt;label&gt;</code> associado.</p>
</div>

### `aria-describedby`

Há momentos em que um formulário inclui informações que não é exatamente uma etiqeuta,
mas é importante o suficiente para ser lida por um leitor de tela quando estiver navegando pelos campos de formulário.
Esta informação adicional pode ser associada ao campo de formulário com o atributo `aria-describedby`.
Por exemplo:


<label for="resetarsenha">Resetar Senha:</label>
<input type="password" name="resetarsenha" id="resetarsenha" aria-describedby="novasenha">
<br>
<span id="novasenha">Nova senha deve ter 8-15 caracteres e conter letras e números</span>

Aqui o HTML:

<div class="programlisting">
  <code>
  &lt;label for="resetarsenha"&gt;Resetar Senha:&lt;/label&gt;<br>
  &lt;input type="password" name="resetarsenha" id="resetarsenha" <strong>aria-describedby="novasenha"</strong>&gt; <br>
  &lt;br&gt;<br>
  &lt;span <strong>id="novasenha"</strong>&gt;Nova senha deve ter 8-15 caracteres e conter letras e números&lt;/span&gt;	</code>
</div>

Como há uma uma etiqueta, `<label>` é lido em vez de `aria-labelledby`.
Como ocorre com `aria-labelledby`, o atributo `aria-describedby` aponta para o `id` do elemento que contém os requisitos da senha.
Um leitor de tela iria ler tantoambos, a etiqueta associada e as descrições associadas.
As descrições às vezes são lidas após de uma breve pausa.
`aria-describedby`  também pode fazer referência a vários elementos - basta referênciar os valores de `id` separados por espaço.


<div class="note">
  <div class="title">Nota</div>
  <ul>
    <li>Enquanto <code>aria-labelledby</code> sobrescreve o <code>&lt;label&gt;</code>, <code>aria-describedby</code> não faz isso.
    Isto significa que <code>aria-describedby</code> deve apenas ser usado <em>como complemento a uma eitqueta</em>
    (i.e., <code>&lt;label&gt;</code> ou &lt;input <code>aria-labelledby</code>&gt;), não como subistituto de um destes.</li>
    <li>O atributo <code>aria-describedby</code> também pode ser usada como referência em descrições que aparecem como "dica de ferramenta".
    Dica de ferramenta devem se tornar visíveis para usuários que enxergam e usam teclado quando o campo está com foco,
    não apenas quando o usuário passa o mouse por cima, ou clica no elemento com o mouse.</li>
  </ul>
</div>

### Etiquetas invisíveis

Há momentos em que uma etiqueta de texto para um campo de formulário não faz sentido ser exibida visualmente.
O exemplo mais comum é o campo de "Pesquisar". Sua localização na página,
junto ao botão de busca, deixa seu propósito claro para usuários que enxergam.
Adicionar um ródulo visual seria exagero e impactaria negativamente no design do site.

Uma das três técnicas seguintes deveria ser usada quando uma etiqueta exibida visualmente não está disponível:

#### `label` oculta
Esconda o elemento `<label>` movendo-o para fora da tela usando CSS. A etiqueta não vai aparecer visualmente,
porém será lida por um leitor de tela.

<label class="hidden" for="s">Termos de busca</label>
<input id="s" type="text" name="busca">
<button>Buscar</button>

Aqui o HTML para a etiqueta e o campo de formulário:

<div class="programlisting">
  <code>
  &lt;label <strong>class="hidden"</strong> for="s"&gt;Termos de busca&lt;/label&gt;<br>
  &lt;input type="text" id="s" name="s"&gt;</code>
</div>

O CSS que é usado para esconder o rótulo,
e informações adicionais sobre esta técnica, pode ser vista no nosso artigo sobre
[conteúdo invisível para leitores de tela](http://webaim.org/techniques/css/invisiblecontent/).


#### Atributo `title`

Se um campo de formulário tem um atributo `title`, mas nenhum `<label>`, o leitor de tela irá ler o `title` como se fosse uma etiqueta.


<input id="s-2" type="text" name="s-2" title="Termos de busca">
<button>Buscar</button>

Aqui o HTML para a etiqueta e o campo de formulário:

<div class="programlisting">
  <code>
  &lt;input id="s" type="text" name="s" <strong>title="Termos de busca"</strong>&gt;
  </code>
</div>


Esta técnica também fará com que uma dica de ferramenta apareça quando o usuário passar o mouse sobre o campo,
o que poderia ser uma distração para alguns usuários.

#### `aria-label`

O atributo `aria-label` também pode ser usado quando não há uma etiqueta de texto na página.

<input id="s-3" type="text" name="s-3" aria-label="Termos de busca">
<button>Buscar</button>

<div class="programlisting">
  <code>
  &lt;input id="s" type="text" name="s" <strong>aria-label="Termos de busca"</strong>&gt;
  </code>
</div>

Ao contrário de `aria-labelledby` que deve fazer referência a um outro elemento,
`aria-label` contém o texto da etiqueta diretamente. Como ocorre com `aria-labelledby`,
`aria-label` irá sobrescrever qualquer elemento `<label>`.

<div class="important">
  <div class="title">Importante</div>
  <ul>
    <li>Apenas uma destas recomendações deve ser implementada.
    Usar duas ou mais juntas (e.e., <code>&lt;label&gt;</code> oculta e duplicar com o atributo <code>title</code>)
    pode causar repetição da informação por um leitor de tela.</li>
    <li>Texto de espaço reservado (do inglês <em lang="en">placeholder</em>) (e.e., <code>&lt;input type="text" <strong>placeholder="Pesquisar no WebAIM"</strong>&gt;</code>)
    não é uma etiqueta adequada e nunca deve ser usada em lugar das técnicas acima.</li>
  </ul>
</div>

### Recaptulação

*   Use elemento `<label>` quando puder. Ele tem excelente suporte ao navegador e leitor de tela,
 e os usuários podem clicar na etiqeuta para selecionar o campo de formulário associado.
*   Use `aria-labelledby` para contornar as limitações de 1:1 de rótulos `<label>`.
*   Use `aria-describedby` **como complemento a uma etiqueta** quando você precisa relacionar um
 texto descritivo a um campo de formulário.
*   Use `<label>` oculta **ou** atributo `title` **ou** `aria-label` quando texto de uma etiqeuta visível não está disponível.
