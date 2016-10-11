---
layout: translation
date: 2010-01-01 # Data de ultima atualização do original
title: "Writing Clearly and Simply" # Titulo traduzido
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


Is it *Possible* to Write "Clearly and Simply"?
-----------------------------------------------

The task of writing clearly and simply has never been either clear or simple.
In fact, it can be one of the most difficult of all writing tasks.
Clear and simple writing is an art to which many aspire and few achieve.
Even so, the understandability of web content depends upon clear and simple writing.
Unclear or confusing writing is an accessibility barrier to all readers,
but can be especially difficult for people with reading disorders or cognitive disabilities.

> "My aim is to put down on paper what I see and what I feel in the best and simplest way." <br>
> —Ernest Hemingway

> "Unless one is a genius, it is best to aim at being intelligible." <br>
> —Anthony Hope Hawkins

**Language and cultural differences matter.**
To complicate matters, the "rules" of clear and simple writing in English may not apply at all in other languages,
or even between cultures that speak the same language.
Many English-speaking countries value directness and explicitness in written communication.
Other cultures feel that this style is too blunt, and perhaps even insulting to readers.

Despite the difficulties in defining the meaning of "clear and simple" writing,
the suggestions in this section may still benefit writers of web content.
The suggestions serve as general guidelines for writing clear and simple English,
primarily from an American English perspective.
Those who write in other languages should seek resources that apply specifically to those languages.

**Cognitive abilities matter.**
Not everyone reads at the same level or has the ability to understand text content,
even when presented clearly and simply.
Reading disorders, memory disorders, attention deficit disorders,
and other conditions which affect the brain's cognitive processes can compromise a person's ability to benefit from text.
The guidelines presented below will improve readability for many people, but not for all.

General Guidelines
------------------

The guidelines presented here are not a complete list,
nor do they apply to every situation, but they are a good starting point.
Writers who take these guidelines seriously are more likely to write clearly and simply.

### 1. Organize your ideas into a logical outline—before and during the writing process

This may be the most important guideline of all.
You have to think clearly about a topic in order to communicate it clearly.
The organization process is ongoing,
starting before any words are written and continuing throughout the entire process.
There is nothing wrong with reorganizing a paper as you write it.
When you think you're finished,
take the opportunity to analyze it one more time to see if the organization still makes sense to you.
If it does, great! If not, try again!

Here are some thoughts by accomplished writers about the need to organize ideas:

> "If any man wishes to write in a clear style, let him first be clear in his thoughts." <br>
> —Johann Wolfgang von Goethe

> "Writing comes more easily if you have something to say." <br>
> —Sholem Asch

### 2. Tell the readers what you're going to tell them; tell them; then tell them what you told them

The formula to follow is to begin with an introduction, or overview of the paper's ideas,
explain the ideas in the main body of the text, then summarize or review the ideas at the end.

<div class="example" markdown="1">
<div class="title">Example</div>

In a simplified format, here is a structural analysis of ideas for a paper about baldness:

<div style="border:gray solid 1px;padding:20px;margin:20px;" markdown="1">
**Introduction (Tell them what you're going to tell them)**

Not everyone appreciates baldness as they should.
There are advantages to being bald.

**Body (Tell them)**

**Main idea 1:**
Bald people don't have to worry about the cost of haircuts.
They can cut their own hair (what remains of it) with a razor or clippers.

**Main idea 2:**
Bald people don't have to style their hair.
They only have to dry their head with a towel after showering,
and are then free to move on to other more relevant activities,
like reading the comics, practicing yoga, or climbing trees.

**Main idea 3:**
Even on windy days, bald people never get hair in their eyes or mouth,at least not their own hair,
which makes windy days more bearable for the vast majority of people who don't particularly like the taste of hair.

**Review and Conclusion (Tell them what you told them)**

Baldness allows for some under-appreciated conveniences in life,
in terms of haircuts, styling, and windy days. You ought to consider being bald.

</div>
</div>

### 3. Stick to the point

The more you stray from your main point, the less likely people will be to remember it.

### 4. Make it interesting

Capture the attention of your readers by including relevant details that motivate them to continue reading.

Here are some thoughts by famous individuals about the importance of making things interesting:

> "If you would not be forgotten as soon as you are dead, either write things worth reading or do things worth writing." <br>
> —Benjamin Franklin

> "Imagination is more important than knowledge."
> —Albert Einstein

> "What we want is a story that starts with an earthquake and builds to a climax." <br>
> —Samuel Goldwyn

### 5. Write for your target audience

You should write differently for a classroom of first-graders than you would for a committee of post-graduate scholars.
In addition, you should take into account people's areas of expertise,
even if they have the same level of education or intelligence.
Cultural and gender differences can also play a role in defining a target audience.
As you write, keep your audience's characteristics in mind and write accordingly.

### 6. Assume that your readers are intelligent, but do not assume that they know the subject matter as well as you

The amount of explaining you need to do depends upon how familiar your audience is with the topic.
Explaining concepts is not insulting; it is helpful,
as long as the explanations show that you respect the reader.
Some people with cognitive disabilities may need more explanation than others,
but when you write for general audiences, assume a general level of intelligence.

Some experts say writers should aim for "eighth grade level" writing.
It is difficult to determine for sure what this means. Many popular magazines,
such as Readers Digest and Ladies' Home Journal are written at about this level.
News sources such as Newsweek are written at a slightly higher level, approximately 10th grade.

### 7. Write cohesive paragraphs constructed around a single major idea

All of the ideas in a paragraph should relate back to the main point.
If possible, put the main idea of the paragraph in the first sentence.

<div class="example" markdown="1">
<div class="title">Example</div>

The following paragraph presents an idea about teams.
The first sentence clearly states the main idea of the paragraph ("Obstacles are a continual fact of life for teams").
As you read this paragraph,
notice how the other sentences in the paragraph support the main idea in the first sentence.

> **Obstacles are a continual fact of life for teams.**
They occur from the moment a potential team gathers until the team comes to an end.
Obstacles also differ as much as the teams, performance challenges, organizational settings,
and business contexts that produce them.
The Burlington Northern Intermodal Team, for example, encountered weak support from management,
policies against advertising, distrust of truckers, and mediocre talent in the intermodal department.
It also faced bad weather, intense competition, and a poor economy when it had to prove its strategy with the two new hubs.
Any of these obstacles could have derailed the team's progress and performance.
None of them did. Indeed, working through the obstacles made the team stronger.

(From "The Wisdom of Teams" by Jon R. Katzenbach and Douglas K. Smith, HarperBusiness press 1994, page 149.)

</div>

### 8. Avoid slang and jargon

Slang and jargon can be useful to people who understand it, but confusing to people who don't.

<div class="example" markdown="1">
<div class="title">Example</div>

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Bad example:" width="20" height="20" /></span>
**Computer jargon:**
Some software companies issue crippleware demos.
Others issue shareware or nagware. Still others issue nothing but vaporware.

The words "crippleware," "demos," "shareware," "nagware," and "vaporware,"
are familiar to many people in the computer industry,
but mean little or nothing to people unfamiliar with the terms.

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Good example:" width="20" height="20" /></span>
**Social theory jargon:**
Critical theory seeks to problematize the hegemonic reification of oppressive stratified social constructs.

The above sentence accurately describes one aspect of the social movement known as critical theory,
but it uses terms that are somewhat less common outside of critical theory,
and which have specific meanings within the theoretical perspective.
The example sentence may confuse people who are unfamiliar with critical theory.

</div>

### 9. Use familiar words and combinations of words

Writers should strive to communicate with their readers,
not impress readers by using uncommon or showy words.

<div class="example" markdown="1">
<div class="title">Example</div>

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Bad example:" width="20" height="20" /></span>
**Unfamiliar words (to many people):**
The populous legion of impecunious vagrants congregated near the basilica.

<span class="inlinemediaobject"><img src="media/smiley.png" alt="Good example:" width="20" height="20" /></span>
**More familiar words:**
The large crowd of poor homeless people gathered near the old church.

</div>

### 10. Use active voice

Passive voice weakens the action of a sentence by distancing the action from the subjects performing the action.
Active voice links the subjects directly with the action.

<div class="example" markdown="1">
<div class="title">Example</div>

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Bad example:" width="20" height="20" /></span>
**Passive:**

-   The food was eaten at the party by the guests.
-   A good time was had by all.
-   The result of building a highway through the farmland was increased profit-seeking by some property owners and the eventual loss of land adjacent to the highway to contractors' commercial and residential construction projects.

<span class="inlinemediaobject"><img src="media/smiley.png" alt="Good example:" width="20" height="20" /></span>
**Active:**

-   The guests ate the food at the party.
-   We all had a good time. OR We all enjoyed ourselves.
-   Building a highway through the farmland caused some property owners to seek profits by selling their land to contractors who eventually constructed commercial and residential projects on the land adjacent to the highway.

</div>

### 11. Avoid weak verbs

Writers often use the verb "to be" (is, are, was, were) when more active verbs may be more appropriate.
Over-use of the verb "to be" often forces writers to use the passive voice more than necessary.
The verb "to be" suggests passivity because it connects two entities that are essentially equal.
The phrase "A is B" essentially means "A equals B."
The relationship between A and B is static.
In contrast, other verbs—such as "to improve," "to clarify," "to modify," or "to destroy"—imply more of a dynamic relationship between A and B.

<div class="example" markdown="1">
<div class="title">Example</div>

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Bad example:" width="20" height="20" /></span>
**Weak verb ("is"):**
One way to improve your writing *is* to use strong verbs.
(A = B)
(One way to improve your writing = to use strong verbs)
The equal relationship between the two parts of the sentence implies no action.

<span class="inlinemediaobject"><img src="media/smiley.png" alt="Good example:" width="20" height="20" /></span>
**Strong verb ("improve"):**
Using stronger verbs can *improve* your writing.
(A improves B)
The subject of the sentence ("using stronger verbs") performs the action of *improving* the object of the sentence ("your writing").

</div>

### 12. Use parallel sentence construction

Make sure that the sentence construction is consistent within itself.

<div class="example" markdown="1">
<div class="title">Example</div>

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Bad example:" width="20" height="20" /></span>
**Non-parallel construction:**
His new sorting machine saves time, increases profitability, and worker satisfaction.

<span class="inlinemediaobject"><img src="media/smiley.png" alt="Good example:" width="20" height="20" /></span>
**Parallel Construction:**
His new sorting machine saves time, increases profitability, and increases worker satisfaction.

<div class="note" markdown="1">
<div class="title">Note</div>

One way to find out if the sentence contains parallel construction is to list each of the items one at a time in a complete sentence:

1.  His new sorting machine saves time.
2.  His new sorting machine increases profitability.
3.  His new sorting machine worker satisfaction.

The third sentence in this example obviously needs a verb to make the sentence complete and parallel with the previous sentences.

</div>
</div>

### 13. Use positive terms

Emphasize the way things are, were, will be, or would be.
To the extent possible, avoid the use of *don't, didn't,* and other words that structure a sentence from the perspective of the way things are not, were not, will not be, or would not be.

<div class="example" markdown="1">
<div class="title">Example</div>

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Bad example:" width="20" height="20" /></span>
**Negative terms:**

-   Do not get dirty.
-   Don't forget to water the flowers.
-   I didn't remember where I was last night.
-   Choir members are not supposed to sing in ways that don't blend with the rest of the choir.

<span class="inlinemediaobject"><img src="media/smiley.png" alt="Good example:" width="20" height="20" /></span>
**Positive terms:**

-   Stay clean.
-   Remember to water the flowers.
-   I forgot where I was last night.
-   Choir members are supposed to sing in ways that blend with the rest of the choir.

</div>

### 14. Give direct instructions

Direct instructions can increase comprehension and place more of a sense of responsibility on the reader.

<div class="example" markdown="1">
<div class="title">Example</div>

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Bad example:" width="20" height="20" /></span>
**Indirect instructions:**

-   Students should read chapter five.
-   It is best to eat a healthy breakfast before leaving the house in the morning.
-   It can be dangerous to attempt to walk on a tightrope stretched over a pit of hungry crocodiles, so this practice is highly discouraged.

<span class="inlinemediaobject"><img src="media/smiley.png" alt="Good example:" width="20" height="20" /></span>
**Direct instructions:**

-   Read chapter five.
-   Eat a healthy breakfast before leaving the house in the morning.
-   Don't walk on a tightrope over a pit of hungry crocodiles .

</div>

### 15. Avoid multiple negatives

Most readers find double negatives,
or multiple negatives, a bit awkward, which can lead to confusion, or at least to slower comprehension.

<div class="example" markdown="1">
<div class="title">Example</div>

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Bad example:" width="20" height="20" /></span>
**Double negative:**

-   Don't forget to not open your mouth when you fall in a muddy puddle.
-   I don't let them not help with the chores.

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Good example:" width="20" height="20" /></span>
**Single negative, or only positive phrase:**

-   Don't open your mouth when you fall in a muddy puddle. <br>
    **OR** <br>
    Keep your mouth closed when you fall in a muddy puddle.
-   I don't let them avoid the chores. <br>
    **OR** <br>
    I make sure they help with the chores.

</div>

### 16. Avoid acronyms and abbreviations if possible; explain all acronyms and abbreviations

Unfamiliar acronyms and abbreviations mean nothing to readers.
Expanding acronyms and abbreviations allows readers to learn their meaning.
This is especially true the first time, or the first few times, an acronym or abbreviation is used.

<div class="example" markdown="1">
<div class="title">Example</div>

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Bad example:" width="20" height="20" /></span>
**Unexplained acronyms and abbreviations:**
The teacher had to prepare an IEP for the children with LD and had to comply with the NCLB regs in order to meet AYP reqs.

<span class="inlinemediaobject"><img src="media/smiley.png" alt="Good example:" width="20" height="20" /></span>
**Explanations for acronyms, with abbreviations eliminated:**
The teacher had to prepare an Individualized Education Plan (IEP) for the children with learning disabilities (LD),
and had to comply with the regulations of the No Child Left Behind (NCLB) Act in order to meet the Annual Yearly Progress (AYP) requirements.

</div>

### 17. Check the spelling

Use an automated spell checker, but also proof-read the document for correctly spelled words that are used incorrectly.

<div class="example" markdown="1">
<div class="title">Example</div>

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Bad example:" width="20" height="20" /></span>
**Incorrect spelling:**
I wanted to see hte sunset for myself.

<span class="inlinemediaobject"><img src="media/frowny.png" alt="Another bad example:" width="20" height="20" /></span>
**Incorrect words spelled correctly:**
Our products an services are the best ones fore the price.

</div>

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
