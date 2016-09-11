---
layout: translation
date: 2016-03-02 # Data de ultima atualização do original
title: "Switching From JAWS To NVDA" # Titulo traduzido
description: Switching From JAWS To NVDA # Descrição traduzida
copyright: 'Copyright NVDA Community Wiki' # Quem tem direitos de cópia
license: null # Caso seja uma licença padrão (MIT, GPL...) por aqui
license-custom: null # Caso a licença não seja uma padrão, por uma descrição curta dela aqui
authors: ["kara-louise"] # Array com lista do autor
translators: [{
    name: "Vilmar Neto",
    link: "http://www.webiwg.org"
}]
reviewers: [{
    name: "Emerson Rocha Luiz",
    link: "http://twitter.com/fititnt"
}]
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

O propósito deste guia é auxiliar usuários de JAWS (<em lang="en">Job Acess With Speech</em>, em português "Acesso ao Trabalho com Fala"), um leitor de tela comercial da <em lang="en">Freedom Scientific</em> a troca para o leitor de tela de código aberto NVDA (_NonVisual Desktop Access_, em português "Acesso à Desktop Não-Visual") com facilidade. Se assume conhecimento prévio prévio de JAWS e que você é proficiente em seu uso.

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


Suporte para recursos avançados do pacote <em lang="en">Microsoft® Office</em> é uma adição relativamente recente, então você pode não achar uma experiência tão polida quanto JAWS. De qualquer forma, tem sido significativamente melhorado em versões recentes, e está sendo constantemente melhorado.

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

  @fititnt Mudei de ideia. Vou usar apenas Notebook (fititnt, 2016-09-11 05:41)

  @fititnt layout = leiaute. Muita mão ficar adicionado <em lang="en">layoyt</em> (fititnt, 2016-09-11 05:44)
-->
## Uma nota rápida sobre o NVDA com leiaute do teclado de notebook

Selecionando o layout do teclado de notebook, não ativa automaticamente a tecla <kbd>CapsLock</kbd> para agir como tecla modificadora do NVDA. Entretanto, uma quadro de seleção estará sendo providenciado próximo ao combo box que define o layout de teclado para alterar esta configuração.

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

## <em lang="en">Eloquence</em>

Uma das perguntas mais pedidas preocupa-se no uso do sintetizador de texto para voz <em lang="en">Eloquence</em> com NVDA. Até recentemente, isto era ilegal, como explicado pelo desenvolvedor no link http://community.nvda-project.org/blog/NVDAAndEloquenceSituation.

De qualquer forma, a <em lang="en">Code Factory</em> liberou uma versão de oratória como um add-on do NVDA que pode ser comprada no endereço http://codefactoryglobal.com/app-store/voices-for-nvda/.

A licença para o uso do sintetizador <em lang="en">Nuance's Vocalizer</em> está também incluída no valor.

Veja a seção intitulada "Scripts" para informações sobre add-ons do NVDA.

eSpeak não é o único sintetizador suportado. No seguinte endereço está uma página detalhando onde conseguir vozes extras: http://community.nvda-project.org/wiki/ExtraVoices.


## Terminologia

Na maioria do tempo, ambos NVDA e JAWS compartilham da mesma terminologia para descrever controles, isto é, botões de radio, combo boxes, quadros de seleções, etc.

Uma das mais notáveis diferenças é que NVDA se diferencia entre campos de edição de linhas singulares e múltiplas, e isso também irá te dizer se um campo está "protegido" (qualquer coisa que você digitar será substituído por asteriscos). Irá também te alertar se o texto está selecionado no campo ao pressionar tab. Caso sim, ao digitar o texto destacado será substituído.

NVDA se referencia a diferentes linguagens como um sintetizador de fala que pode falar como vozes, e diferentes vozes suportadas pelo sintetizador como variantes.

## Cursores

NVDA tem diversos cursores para auxiliar na navegação do Windows e suas aplicações, similiar ao JAWS. A terminologia é ligeiramente diferente como descrita abaixo.

O cursor do PC na documentação do NVDA está referenciada como um sistema de foco e um sistema de cursor.

O equivalente para o cursor de JAWS é uma combinação de navegação de objetos, um cursor de revisão e um <em lang="en">Screen Review</em>. A função de <em lang="en">Screen Review<em> é um, senão o mais similiar cursor para JAWS, de qualquer forma é o mais vantajoso para ser tornar familiar com todos os 3. Você irá achar minucioso, fácil de entender instruções para estas no guia do usuário.

Diferente de JAWS, você não irá ter que mudar entre o cursores equivalentes do PC e do JAWS, assim como o teclado numérico está reservado exclusivamente para o trabalhar com o cursor de JAWS como funções.

<!--
Vilmar: Foi deixado tree-like como estrutura de árvore na sua semântica
        touchscreens, object mode, browse mode , object navigation e outros termos permanecem em inglês.

@fititnt Vilmar, cuidado ao colar HTML, como esses comentários, em tags de markdown, porque daí o
         jekyll não converte corretamente (fititnt, 2016-09-11 06:07)
-->

### Cursor de Toque

No JAWS 15 ou superior, você pode usar as teclas do teclado numérico para navegar entre aplicativos usando uma estrutura em forma de árvore, similiar a como usuários de leitores de tela de <em lang="en">smartphone</em>, como VoiceOver, iriam navegar em <em lang="en">touchscreens</em>. No NVDA, comando de toque do <em lang="en">object mode</em> e do <em lang="en">object navigation</em> podem ser usados para este próposito.

##Cursor Virtual

O cursor virtual no NVDA é conhecido como <em lang="en">browse mode</em>. Funciona da mesma maneira do JAWS, proporcionando acesso a teclas rápidas de navegação, ou no NVDA speak , navegação por letra única.

A seguir estão alguns problemas que você pode encontrar enquanto estiver navegando na rede com NVDA pela primeira vez, e como resolvê-los.

<!--
Vilmar: Default foi mantido com mesmo significado.
@fititnt Mudei "default" para padrão"

-->

### Por que tudo numa só linha?

Caso esteja desavisado, JAWS tem dois modos para exibir páginas web ou outros documentos usando o cursor virtual, leiaute simples e leiaute de tela. O leiaute simples é o padrão, que exibe conteúdo numa forma linear - colocando cada link ou controle em sua própria linha. Leiaute de tela formata o conteúdo de forma similiar a como é exibido na tela.

O padrão em NVDA é o leiaute de tela, mas você pode facilimente trocar para a versão de leiaute simples pressionando <kbd>NVDA</kbd> + <kbd>V</kbd> enquanto no <em lang="en">browse mode</em>. Isso irá deixar o leiaute de tela desligado. Tenha certeza de salvar a configuração após fazer a mudança com <kbd>NVDA<kbd> + <kbd>CTRL</kbd> + </kbd>c</kbd>.

<!--
Vilmar: control foi traduzido para controle, necessito que verifiquem se é o adequado.
        Acabei mudando para inglês, as configurações que devem ser clicadas.
-->
### Continua dizendo Clicável, Clicável, Clicável !

Enquanto estiver lendo páginas web, você pode perceber que às vezes que NVDA diz "clicável", até múltiplas vezes numa mesma linha ou controle.

De qualquer forma, é consertado facilmente com a versão 2014.1 ou mais recente. Vá em dialógo "Document Formatting", desmarque a caixa "Reporte if clickable" e aperte OK. Lembre-se de salvar sua configuração.

### Procurar(CTRL+F) não funciona na web.

Enquanto o JAWS está carregado, pressionando <kbd>CTRL</kbd> + <kbd>f</kbd> no Internet Explorer ou no Firefox mostra uma caixa de procurar do JAWS, ao invés de ativar o comando interno do browser. Isto permite procurar texto usando o cursor virtual. O comando de procurar regular irá procurar pela próxima ocorrência do texto digitado, mas não irá mover o cursor virtual para a devida localização. Isto é por conta de como os leitores de tela interagem com páginas web.

NVDA tem seu próprio comando de busca no <em lang="en">browse mode</em>, mas não está ligado a <kbd>CTRL</kbd> + <kbd>f</kbd>, então pressionar este atalho irá chamar o comando de busca do próprio navegador, consequentemente não funcionando como esperado.

Para mostrar o comando de Procurar do NVDA, pressione <kbd>CTRL</kbd> + <kbd>NVDA</kbd> + <kbd>f</kbd>. Digite o que você quiser pesquisar, enão pressione <kbd>Enter</kbd> .

<!--
Vilmar: headings foi mantido da mesma forma.
@fititnt headings = cabecalhos; formas (forms) = formulários
-->

### Sem comando para visualizar formulários e cabeçalhos?

No JAWS, você pode pressionar <kbd>JAWS</kbd> + <kbd>F5</kbd> para listar formulários, <kbd>JAWS</kbd> + <kbd>F6</kbd> para listar cabecalhos e <kbd>JAWS</kbd> + <kbd>F7</kbd> para listar link. No NVDA, as duas últimas se combinaram em elementos de diálogos de lista, e você pode acessar pressionando <kbd>NVDA</kbd> + <kbd>F7</kbd>.

## Modo de formulários

O equivalente ao modo de formulários no NVDA é o <em lang="en">focus mode</em>, e se comporta muito similiar ao JAWS, até mesmo mudando de modos automaticamente quando navegando por uma página web. Isso irá tocar um som alertando que vocẽ para qual modo você está.

Detalhes sobre o <em lang="en">focus mode</em> podem ser achados no guia do usuário.

<!--
Vilmar: list views foi mantido da mesma forma.

@fititnt "NVDA fala pra caramba." para "NVDA fala demais". Isso deve ser mais fácil para
         pessoas que falam português mas não são nativos do Brasil (fititnt, 2016-09-11 06:24)
-->

## NVDA fala demais

Às vezes, você pode achar que NVDA pode ser muito verboso, particularmente em algumas <em lang="en">list views</em>. Isso é porque na questão do NVDA, <em lang="en">list views</em> são tabelas.  NVDA está configurado por padrão para anunciar cada cabeçalho de coluna ou cabeçalho de linha.

Para desligar esta opção, desmarque <em lang="en">"Report table row/columns headers"</em> no dialógo <em lang="en">"Document Formatting"</em>.

<!--
Vilmar: check box foi mantido como original por estar junto com case sensitive que ficaria dificil de traduzir junto.
        Recomendo que para palavras mantidas em inglês haja uma pequena explicação sobre, em forma de itens.
-->

## Resolvendo comportamento inesperado do Dicionário de Fala.

NVDA sempre incluiu uma função para editar <em lang="en">"Speech Dictionaries"</em>, Dicionários de Fala, em português, que são similiares ao gerenciador de arquivos de dicionários do JAWS. De qualquer forma, até recentemente, o resultado de adicionar uma palavra para eles pode não sair como o esperado.
Se você adicionou uma palavra que queria mudar a pronunciação de uma dicionário, como "mono", qualquer outra palavra que iniciasse com a palavra mono seria afetada. Enquanto em JAWS, somente o texto digitado no campo da "palavra atual" seria afetado, a menos que você concatene com um asterisco (*). Então como neste exemplo, mono só seria visto como palavra de rota.

Houve um trabalho sobre, mas como isso envolvia expressões regulares, que não são tão óbvias para usuário regular. De qualquer forma , como a versão 2014.4 ou mais recente, você ira achar um grupo de botões de rádio no dicionário de adição/edição do tipo rótulo de entrada, que determina como texto no padrão, (<em lang="en">NVDA speak</em> para ser exato), será tratado na caixa.

 *  Em qualquer lugar, como é o comportamento padrão.
 *  Toda a palavra, que é como o JAWS manipula entradas de dicionário.
 *  Expresão Regular, que no caso é complicado.

Você irá achar uma caixa de seleção para marcar diferenciar maiúsculas de minúsculas.

Se você anteriormente achou os dicionários de fala do NVDA frustantes, tenha certeza de dar uma nova olhada.

## Scripts

Como JAWS, scripts podem ser adicionados ao NVDA para promover suporte para outras aplicações ou adicionar recursos que podem ser acessados de qualquer lugar. Esses pacotes de scripts são chamados de NVDA <em lang="en">Add-ons</em>. Você pode achar vários <em lang="en">add-ons</em> em http://addons.nvda-project.org/.

Isso inclui alguns que emulam os recursos de JAWS que não estão atualmente presentes no NVDA como <em lang="en">system tray list</em>, <em lang="en">virtualise window function</em> e a habilidade de concatenar texto na área de transferência. Scripts são aplicações populares como <em lang="en">GoldWare</em> estão disponíveis. O guia do usuário tem vários detalhes na instalação de <em lang="en">add-ons</em>, e você pode ajudar a documentação que vem com cada <em lang="en">add-ons</em> para aprender mais sobre como usar o <em lang="en">add-ons</em>.


O seguinte link é para o guia de desenvolvedor com informação sobre como criar <em lang="en">add-ons</em>: http://community.nvda-project.org/documentation/developerGuide.html

## Acesso Remoto

Em 2015, Christopher Toth e Tyler Spivey lançaram um <em lang="en">add-ons</em> gratuito que permite usuários de NVDA promoverem suporte remoto, similiar ao <em lang="en"JAWS Tandem</em>. Para aprender mais sobre este <em lang="en">add-ons</em>, vá para http://www.nvdaremote.com.

## Configurações de Aplicação específica

Até recentemente, as configurações do NVDA eram globais (aplicadas em qualquer lugar). A partir do NVDA 2013.3, é possível configurar certas configurações  para serem aplicadas quando estive usando um programa. Isso pode ser feito criando uma configuração de perfil de aplicativo específico. Para criar um perfil de aplicativo específico, abra a caixa de dialógo <em lang="en">Configuration Profiles</em> enquanto estiver usando o aplicativo em questão. Quando a caixa de dialógo abrir (NVDA menu/<em lang="en">Configuration Profiles</em>), selecione <em lang="en">"New"</em> e então <em lang="en">"current application"</em> quando perguntado para usar tal perfil.

<!--
Vilmar: Aqui também deixei say all com o mesma palavra.
-->

### Alternativo diz tudo
Nas versões recentes de JAWS, você pode configurar um sintetizador de voz diferente para ser usado quando <em lang="en">say all</em> está ativo. Você pode fazer isso no NVDA criando um perfil <em lang="en">say all</em> e configurando o sintetizador enquanto o perfil <em lang="en">say all</em> está ativo.

