---
layout: translation
date: 2016-03-02 # Data de ultima atualização do original
title: "Switching From JAWS To NVDA" # Titulo traduzido
description: Switching From JAWS To NVDA # Descrição traduzida
copyright: 'Copyright NVDA Community Wiki' # Quem tem direitos de cópia
license: null # Caso seja uma licença padrão (MIT, GPL...) por aqui
license-custom: null # Caso a licença não seja uma padrão, por uma descrição curta dela aqui
authors: ["kara-louise"] # Array com lista do autor
translators: null # Tradutores
reviewers: null # Quem revisou a tradução
issue: https://github.com/webiwg/acessibilidade-web-pt/issues/6
original: {
    title: "Switching From JAWS To NVDA", # Titulo original, no idioma origial
    link: "https://github.com/nvaccess/nvda-community/wiki/SwitchingFromJawsToNVDA", # Link para documento original
    dateOfTranslation: "2016-09-02", # Data em que a tradução foi finalizada
    backup: "_switching-from-jaws-to-nvda.md" # arquivo que contém documento original, sem alteracoes.
}
---

# Mudando do JAWS para o NVDA

<!--
Vilmar: JAWS e NVDA são termos em inglês. A tradução pode não ter ficado de forma definitiva.
Quem for ajudar na revisão, pode alterar tais detalhes ou colocar outro comentário abaixo.
Seguindo o padrão deste aqui em cima.
-->

## Introdução

O propósito deste guia é auxiliar usuários de JAWS ( Job Acess With Speech / Acesso ao Trabalho com Fala), leitor de tela comercial da Freedom Scientific a troca para o leitor de tela open source NVDA (NonVisual Desktop Access/Acesso Desktop Não-Visual) com facilidade. Se assume conhecimento prévio de JAWS e que você é proficiente em seu uso.

Não é a intenção ser uma substituição do guia de uso incluso, muito menos uma forma de fazer NVDA menos intimidador.

## Prós e Contras

A intenção deste guia não é ser uma comparação entre JAWS e NVDA, mas é necessário mencionar algumas coisas que NVDA não suporta atualmente ou precisa aprimoramento para que você possa fazer a escolha informada.

Suporte para recursos avançados do Microsoft office suite é uma adição relativamente recente, então você pode não achar uma experiência tão polida quanto JAWS. De qualquer forma, tem sido significativamente melhorado em versões recentes, e está sendo constantemente trabalhada.

Com isto dito, você achar que - na maioria das situações diárias, NVDA funciona tão bem quanto JAWS, se não melhor em alguns casos.
<!--
Vilmar: deixei a tradução de Laptop por laptop mesmo e também coloquei entre parenteses na primeira aparição do texto principal notebook, termo usado no Brasil
Por isso foi feita esta breve explicação no texto.
Além disso combo box foi deixada em inglês por não ter tradução para portuguÊs
-->
## Uma nota rápida sobre o Layout NVDA para teclado de Laptop 

Selecionando o layout para teclado de Laptop, ou Notebook em português, não ativa automaticamente a tecla CapsLock para agir como tecla modificador do NVDA. De qualquer forma, uma quadro de seleção estará sendo providenciado junto ao combo box do  Layout de teclado para alterar esta configuração.

## Nota sobre a Tecla Insert

Como você deve estar informado, ambos JAWS e NVDA podem utilizar a tecla insert como tecla modificadora. Ambos leitores de tela tratam o levemente diferente, o que pode levar a alguma confusão se você está acostumado com um ou com outro.

Com JAWS carregado, a tecla insert é somente para este uso. Isso significa que, em  ordem para usar a função original designada (assim como mudar entre insert e sobreescrever modos no editor de textor ou no processador de texto), primeiro você tem que ativar o a pass key do JAWS através de comando.

Por outro lado, NVDA permite que você realize a função original do insert, através do toque duplo. Tenha isso em mente na próxima vez que você estiver editando um texto pelo NVDA e perceber que está apagando o que você acabou de escrever.

## Oratória

Uma das perguntas mais pedidas preocupa-se no uso do sintetizador de oratória com NVDA. Até recentemente, isto era ilegal, como explicado pelo desenvolvedor:http://community.nvda-project.org/blog/NVDAAndEloquenceSituation.

De qualquer forma, Code Factory liberou uma versão de oratória como um add-on do NVDA que pode ser comprada no endereço: http://codefactoryglobal.com/app-store/voices-for-nvda/.

A licença para o uso do sintetazidor Nuance's Vocalizer está também incluída no valor.

Veja a seção intitulada "Scripts" para informações sobre add-ons do NVDA.

eSpeak não é o único sintetizador suportado. No seguinte endereço está uma página detalhando onde conseguir vozes extras.
http://community.nvda-project.org/wiki/ExtraVoices.


## Terminologia

Na maioria do tempo, ambos NVDA e JAWS compartilham da mesma terminologia para descrever controles, isto é, botões de radio, combo boxes, quadros de seleções, etc.

Uma das mais notáveis diferenças é que NVDA se diferencia entre campos de linhas singulares e múltiplas, e isso também irá te dizer se um campo está "protegido" (qualquer coisa que você digitar será substituído por asteriscos). Irá também te alertar se o texto está selecionado no campo ao pressionar tab. Caso sim, ao digitar o texto destacado será substituído.

NVDA se referencia a diferentes linguagens como um sintetizador de fala que pode falar como vozes, e diferentes vozes suportadas pelo sintetizador como variantes.


## Cursors

NVDA has various cursors to aid in navigating Windows and applications, similar to JAWS.  The terminology is slightly different as described below.

The PC cursor in NVDA's documentation is referred to as the system focus and system caret.

The equivalent to the JAWS cursor is a combination of object navigation, the review cursor and Screen Review.  The Screen Review function is the one perhaps most similar to the JAWS cursor, however it is beneficial to become familiar with all 3.  You will find thorough, easy to understand instructions for these in the user guide.

Unlike JAWS, you don't have to switch between the PC and JAWS cursor equivalents as the numpad is reserved exclusively for working with the JAWS cursor like functions.

### Touch cursor

In JAWS 15 or later, you can use numpad keys to navigate apps using a tree-like structure, similar to how users of smartphone screen readers such as VoiceOver would navigate touchscreens. in NVDA, object navigation and object mode touch commands can be used for this purpose

## Virtual Cursor

The virtual cursor in NVDA is known as browse mode. It functions in much the same way as JAWS, giving you access to navigation quick keys, or in NVDA speak, single letter navigation.

Following are some common issues you may encounter when browsing the web with NVDA for the first time, and how to address them.

### Why Is Everything On One Line?

In case you are unaware, JAWS has two modes for displaying webpages or other documents using the virtual cursor, simple layout and screen layout.  Simple layout is the default, which displays content in a linear fashion - putting each link or control on its own line.  Screen layout formats the content similar to how it's displayed on screen.

The default in NVDA is screen layout, but you can easily switch to its version of simple layout by pressing NVDA+V while in browse mode. This will turn Screen layout off. Be sure to save your configuration after making this change with NVDA+CTRL+c.

### It Keeps Saying Clickable Clickable Clickable.

While  reading webpages, you might notice sometimes that NVDA says "clickable", even multiple times on the same link or control.

However, this is easily fixable as of version 2014.1 or later. Go to the Document Formatting dialogue, uncheck the "Report if clickable" check box and press OK. Remember to save your configuration.

### Find doesn't work on the web.

While JAWS is loaded, pressing ctrl+f in Internet Explorer or Firefox brings up the JAWS Find dialogue rather than activating the browser's built-in find command.  This is to allow you to search for text using the virtual cursor.  The regular find command will search for the next occurrence of the entered text, but will not move the virtual cursor to that location.  This is due to how screen readers interact with web pages.

NVDA has its own find command to search in browse mode, but it has not been tied to CTRL+F, so pressing that shortcut key calls up the browser's find command, hence find not working as expected.

To bring up NVDA's find dialogue, press ctrl+NVDA+F.  Type in what you wish to find then press enter.

### No commands to view forms and headings?

In JAWS, you can press JAWS+F5 to list forms, JAWS+F6 to list headings and JAWS+F7 to list links. In NVDA, the latter two have been combined into an elements list dialog, and you can access it by pressing NVDA+F7.

## Forms Mode

The equivalent of forms mode in NVDA is focus mode, and it behaves very similar to JAWS, Even switching modes automatically when navigating through a webpage. It will play a sound alerting you to which mode you are in.

Details about Focus Mode can be found in the user guide.

## NVDA talks too much.

Sometimes you may find that NVDA can seem overly verbose, particularly in some list views. This is because as far as NVDA is concerned, list views are tables.   NVDA is configured by default to announce each column or row header.

To turn that option off, uncheck "Report table row/column headers" in the "Document Formatting" dialogue.

## Solving unexpected Speech Dictionary behavior.

NVDA has always included a function to edit "Speech Dictionaries", which are similar to JAWS' dictionary manager files.  However, until recently, the result of adding a word to them might not be what you had expected.
If you added a word you wanted to change the pronunciation of to a dictionary , such as "mono", any word that started with or included the word mono would be affected.  Whereas in JAWS, only the text entered into the "actual word" field would be affected, unless you appended an asterisk (*). So as in this example, mono would be seen as a route word.

There was a work around, but this involved regular expressions, which aren't at all obvious to the average user.  However, as of 2014.4 or later, you will now find a group of radio buttons in the Add/edit dictionary entry labelled type, which determines how the text in the pattern, (NVDA speak for actual word), box will be treated.
 * anywhere, which is the default behavior.
 * Whole word, which is how JAWS handles dictionary entries.
 * Regular Expression, which is complicated.
You will also find a case sensitive check box.

If you previously found NVDA's speech dictionaries frustrating, be sure to take another look.

## Scripts

Like JAWS, scripts can be added to NVDA to provide support  for other applications or to add new features that can be accessed from anywhere.  These script packages are called NVDA Add-ons.  You can find several add-ons here:
http://addons.nvda-project.org/.

These include a few that emulate JAWS features not currently present in NVDA such as a system tray list, virtualise window function and ability to append text to clipboard. Scripts for popular applications such as GoldWave are also available. The user guide has details on installing add-ons, and you can read help documentation that comes with each add-on to learn more about how to use the add-on.

The following link is to the developer guide with information on how to create ad-ons. http://community.nvda-project.org/documentation/developerGuide.html

## Remote access

In 2015, Christopher Toth and Tyler Spivey released a free add-on to allow NVDA users to provide remote support, similar to JAWS Tandem. To learn more about this add-on, go to http://www.nvdaremote.com.

## Application-specific settings

Until recently, NVDA's settings were global (applied everywhere). Starting with NVDA 2013.3, it is possible to configure certain settings to be applied when using a program. This is done by creating an app-specific configuration profile. To create an app-specific profile, open the Configuration Profiles dialogue while using the app in question. When the dialogue opens (NVDA menu/Configuration Profiles), select New, and select "current application" when asked when to use this profile.

### Alternate say all

In recent versions of JAWS, you can configure a different speech synthesizer to be used when say all is active. You can do this in NVDA by creating a say all profile and configuring the synthesizer while say all profile is active.
