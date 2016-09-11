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
<!--
  @fititnt NVDA e JAWS são siglas
  "open source" = código aberto
-->

## Introdução

O propósito deste guia é auxiliar usuários de JAWS ( _Job Acess With Speech_, em português "Acesso ao Trabalho com Fala"), um leitor de tela comercial da Freedom Scientific a troca para o leitor de tela de código aberto NVDA (_NonVisual Desktop Access_, em português "Acesso à Desktop Não-Visual") com facilidade. Se assume conhecimento prévio prévio de JAWS e que você é proficiente em seu uso.

<!--
  @fititnt removi "incluso" do parafrafo abaixo.
-->

Não é a intenção ser uma substituição do guia de usuário, mas sim uma forma de fazer NVDA menos intimidador.

<!--
  @fititnt  de "Strengths And Weaknesses" do original, e "Prós e Contras" do
            tradutor, recomendo "Pontos positivos e negativos"
-->

## Pontos positivos e negativos

A intenção deste guia não é ser uma comparação entre JAWS e NVDA, mas é necessário mencionar algumas coisas que NVDA não suporta atualmente ou precisa aprimoramento para que você possa fazer a escolha informada.

<!--
  @fititnt de "Microsoft office suite" para "pacote Microsoft® Office"
-->


Suporte para recursos avançados do pacote Microsoft® Office é uma adição relativamente recente, então você pode não achar uma experiência tão polida quanto JAWS. De qualquer forma, tem sido significativamente melhorado em versões recentes, e está sendo constantemente melhorado.

Com isto dito, você achar que - na maioria das situações diárias, NVDA funciona tão bem quanto JAWS, se não melhor em alguns casos.
<!--
Vilmar: deixei a tradução de Laptop por laptop mesmo e também coloquei entre parenteses na primeira aparição do texto principal notebook, termo usado no Brasil
Por isso foi feita esta breve explicação no texto.
Além disso combo box foi deixada em inglês por não ter tradução para portuguÊs
-->
<!--
  @fititnt do original "A Quick Note about NVDA's Laptop Keyboard Layout" e
           tradução "Uma nota rápida sobre o Layout NVDA para teclado de Laptop"
           sugiro "Uma nota rápida sobre o NVDA com _layout_ do teclado de _laptop_"
-->
## Uma nota rápida sobre o NVDA com _layout_ do teclado de _laptop_

Selecionando o layout do teclado de _laptop_ (ou _Notebook_ em português), não ativa automaticamente a tecla CapsLock para agir como tecla modificadora do NVDA. Entretanto, uma quadro de seleção estará sendo providenciado próximo ao combo box que define o layout de teclado para alterar esta configuração.

## Nota sobre a Tecla <kbd>Insert</kbd>

Como você deve estar informado, tanto JAWS como NVDA podem utilizar a tecla <kbd>insert</kbd> como tecla modificadora. Ambos leitores de tela tratam o levemente diferente, o que pode levar a alguma confusão se você está acostumado com um ou com outro.

<!--
  @fititnt da tradução "no editor de textor ou no processador de texto" sugiro
           usar apenas "no editor de texto"
           do original "you first have to activate JAWS's pass key through command." e tradução
           "primeiro você tem que ativar o a pass key do JAWS através de comando".  (2016-09-11 04:49)

  @fititnt "Passar Tecla a Aplicação" é usado como tradução de "Pass Through key". (2016-09-11 04:49)
-->

Com JAWS carregado, a tecla <kbd>insert</kbd> é somente para este uso. Isso significa que, para usar a função original designada (assim como mudar entre <kbd>insert</kbd> e sobreescrever modos no editor de texto), primeiro você tem que ativar o comando "Passar Tecla a Aplicação" (N.T.: normalmente <kbd>insert</kbd> + <kbd>3</kbd>.

Por outro lado, NVDA permite que você realize a função original do <kbd>insert</kbd>, através do toque duplo. Tenha isso em mente na próxima vez que você estiver editando um texto pelo NVDA e perceber que está apagando o que você acabou de escrever.

<!--
  @fititnt do inglês "Eloquence" e sugestão "Oratória" do tradutor, eu não tenho certeza
           se esse termo é o melhor, mas não tenho sugestão melhor agora (2016-09-11 05:09)
-->

## Oratória

Uma das perguntas mais pedidas preocupa-se no uso do sintetizador de oratória com NVDA. Até recentemente, isto era ilegal, como explicado pelo desenvolvedor:http://community.nvda-project.org/blog/NVDAAndEloquenceSituation.

De qualquer forma, Code Factory liberou uma versão de oratória como um add-on do NVDA que pode ser comprada no endereço: http://codefactoryglobal.com/app-store/voices-for-nvda/.

A licença para o uso do sintetizador Nuance's Vocalizer está também incluída no valor.

Veja a seção intitulada "Scripts" para informações sobre add-ons do NVDA.

eSpeak não é o único sintetizador suportado. No seguinte endereço está uma página detalhando onde conseguir vozes extras.
http://community.nvda-project.org/wiki/ExtraVoices.


## Terminologia

Na maioria do tempo, ambos NVDA e JAWS compartilham da mesma terminologia para descrever controles, isto é, botões de radio, combo boxes, quadros de seleções, etc.

Uma das mais notáveis diferenças é que NVDA se diferencia entre campos de linhas singulares e múltiplas, e isso também irá te dizer se um campo está "protegido" (qualquer coisa que você digitar será substituído por asteriscos). Irá também te alertar se o texto está selecionado no campo ao pressionar tab. Caso sim, ao digitar o texto destacado será substituído.

NVDA se referencia a diferentes linguagens como um sintetizador de fala que pode falar como vozes, e diferentes vozes suportadas pelo sintetizador como variantes.


## Cursores

NVDA tem diversos cursores para auxiliar na navegação do Windows e suas aplicações, similiar ao JAWS. A terminologia é ligeiramente diferente como descrita abaixo.

O cursor do PC na documentação do NVDA está referenciada como um sistema de foco e um sistema de cursor.

O equivalente para o cursor de JAWS é uma combinação de navegação de objetos, um cursor de revisão e um Screen Review. A função de  Screen Review é um, senão o mais similiar cursor para JAWS, de qualquer forma é o mais vantajoso para ser tornar familiar com todos os 3. Você irá achar minucioso, fácil de entender instruções para estas no guia do usuário.

Diferente de JAWS, você não irá ter que mudar entre o cursores equivalentes do PC e do JAWS, assim como o numpad está reservado exclusivamente para o trabalhar com o cursor de JAWS como funções.
<!--
Vilmar: Foi deixado tree-like como estrutura de árvore na sua semântica
        touchscreens, object mode, browse mode , object navigation e outros termos permanecem em inglês.
-->
### Cursor de Toque

No JAWS 15 ou superior, você pode usar as teclas numpad para navegar entre aplicativos usando uma estrutura em forma de árvore, similiar a como usuários de leitores de tela de smartphone, como VoiceOver, iriam navegar em touchscreens. No NVDA, comando de toque do object mode e do object navigation podem ser usados para este próposito.

##Cursor Virtual

O cursor virtual no NVDA é conhecido como browse mode. Funciona da mesma maneira do JAWS, proporcionando acesso a teclas rápidas de navegação, ou no NVDA speak , navegação por letra única.

A seguir estão alguns problemas que você pode encontrar enquanto estiver navegando na rede com NVDA pela primeira vez, e como resolvê-los.
<!--
Vilmar: Default foi mantido com mesmo significado.
-->
### Por que tudo numa só linha?

Caso esteja desavisado, JAWS tem dois modos para exibir páginas web ou outros documentos usando o cursor virtual, layout simples e layout de tela. O Layout simples é o default, que exibe conteúdo numa forma linear - colocando cada link ou controle em sua própria linha. Layout de tela formata o conteúdo de forma similiar a como é exibido na tela.

O padrão em NVDA é o layout de tela, mas você pode facilimente trocar para a versão de layout simples pressionando NVDA+V enquanto no modo browse. Isso irá deixar o layout de tela desligado. Tenha certeza de salvar a configuração após fazer a mudança com NVDA+CTRL+C.

<!--
Vilmar: control foi traduzido para controle, necessito que verifiquem se é o adequado.
        Acabei mudando para inglês, as configurações que devem ser clicadas.
-->
### Continua dizendo Clicável, Clicável, Clicável !

Enquanto estiver lendo páginas web, você pode perceber que às vezes que NVDA diz "clicável", até múltiplas vezes numa mesma linha ou controle.

De qualquer forma, é consertado facilmente com a versão 2014.1 ou mais recente. Vá em dialógo "Document Formatting", desmarque a caixa "Reporte if clickable" e aperte OK. Lembre-se de salvar sua configuração.

### Procurar(CTRL+F) não funciona na web.

Enquanto o JAWS está carregado, pressionando ctrl+f no Internet Explorer ou no Firefox mostra uma caixa de Procurar do JAWS, ao invés de ativar o comando interno do browser. Isto permite procurar texto usando o cursor virtual. O comando de procurar regular irá procurar pela próxima ocorrência do texto digitado, mas não irá mover o cursor virtual para a devida localização. Isto é por conta de como os leitores de tela interagem com páginas web.

NVDA tem seu próprio comando de busca no modo browse, mas não está ligado a CTRL+F, então pressionar este atalho irá chamar o comando de busca do próprio browser, consequentemente não funcionando como esperado.

Para mostrar o comando de Procurar do NVDA, pressione ctrl+NVDA+F. Digite o que você quiser pesquisar, enão pressione Enter .
<!--
Vilmar: headings foi mantido da mesma forma.
-->
### Sem comando para visualizar formas e headings?

No JAWS, você pode pressionar JAWS+F5 para listar formas, JAWS+F6 para listar headings e JAWS+F& para listar link. No NVDA, as duas últimas se combinaram em elementos de diálogos de lista, e você pode acessar pressionando NVDA+F7.

## Modo de formas

O equivalente ao modo de formas no NVDA é o modo focus, e se comporta muito similiar ao JAWS, até mesmo mudando de modos automaticamente quando navegando por uma página web. Isso irá tocar um som alertando que vocẽ para qual modo você está.

Detalhes sobre o Modo Focus podem ser achados no guia do usuário.
<!--
Vilmar: list views foi mantido da mesma forma.
-->
## NVDA fala pra caramba.
Às vezes, você pode achar que NVDA pode ser muito verboso, particularmente em algumas list views. Isso é porque na questão do NVDA, list views são tabelas.  NVDA está configurado por default para anunciar cada header de coluna ou header de linha.

Para desligar esta opção, desmarque "Report table row/columns headers" no dialógo "Document Formatting".

<!--
Vilmar: check box foi mantido como original por estar junto com case sensitive que ficaria dificil de traduzir junto.
        Recomendo que para palavras mantidas em inglês haja uma pequena explicação sobre, em forma de itens.
-->
## Resolvendo comportamento inesperado do Dicionário de Fala.

NVDA sempre incluiu uma função para editar "Speech Dictionaries", Dicionários de Fala, em português, que são similiares ao manager de arquivos de dicionários do JAWS. De qualquer forma, até recentemente, o resultado de adicionar uma palavra para eles pode não sair como o esperado.
Se você adicionou uma palavra que queria mudar a pronunciação de uma dicionário, como "mono", qualquer outra palavra que iniciasse com a palavra mono seria afetada. Enquanto em JAWS, somente o texto digitado no campo da "palavra atual" seria afetado, a menos que você concatene com um asterisco (*). Então como neste exemplo, mono só seria visto como palavra de rota.

Houve um trabalho sobre, mas como isso envolvia expressões regulares, que não são tão óbvias para usuário regular. De qualquer forma , como a versão 2014.4 ou mais recente, você ira achar um grupo de botões de rádio no dicionário de adição/edição do tipo rótulo de entrada, que determina como texto no padrão, (NVDA trata da palavra atual), será tratado na caixa.
 *  em qualquer lugar, como é o comportamento padrão.
 *  Toda a palavra, que é como o JAWS manipula entradas de dicionário.
 *  Expresão Regular, que no caso é complicado.
Você irá achar um case sensitive check box.

Se você anteriormente achou os dicionários de fala de NVDA frustantes, tenha certeza de dar outra olhada.

## Scripts

Como JAWS, scripts podem ser adicionados ao NVDA para promover suporte para outras aplicações ou adicionar recursos que podem ser acessados de qualquer lugar. Esses pacotes de scripts são chamados de NVDA Add-ons. Você pode achar vários add-ons aqui:
http://addons.nvda-project.org/.

Isso inclui alguns que emulam os recursos de JAWS que não estão atualmente presentes no NVDA como system tray list, virtualise window function e a habilidade de concatenar texto ao clipboard. Scripts são aplicações populares assim como GoldWare estão disponíveis. O guia do usuário tem vários detalhes na instalação de add-ons, e você pode ajudar a documentação que vem com cada add-on para aprender mais sobre como usar o add-on.


O seguinte link é para o guia de desenvolvedor com informação sobre como criar add-ons. http://community.nvda-project.org/documentation/developerGuide.html

## Acesso Remoto

Em 2015, Christopher Toth e Tyler Spivey lançaram um add-on gratuito que permite usuários de NVDA promoverem suporte remoto, similiar ao JAWS Tandem. Para aprender mais sobre este add-on, vá para http://www.nvdaremote.com.

## Configurações de Aplicação específica

Até recentemente, as configurações do NVDA eram globais (aplicadas em qualquer lugar). A partir do NVDA 2013.3, é possível configurar certas configurações  para serem aplicadas quando estive usando um programa. Isso pode ser feito criando uma configuração de perfil de app-específico. Para criar um perfil de app-específico, abra a caixa de dialógo Configuration Profiles enquanto estiver usando o app em questão. Quando a caixa de dialógo abrir (NVDA menu/Configuration Profiles), selecione New e então "current application" quando perguntado para usar tal perfil.

<!--
Vilmar: Aqui também deixei say all com o mesma palavra.
-->
### Alternativo diz tudo
Nas versões recentes de JAWS, você pode configurar um sintetizador de voz diferente para ser usado quando say all está ativo. Você pode fazer isso no NVDA cirando um perfil say all e configurando o sintetizador enquanto o perfil say all está ativo.

