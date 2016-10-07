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

<!--
  N.T.:  Não tenho certeza da tradução de "user agent" (@robsmayer, 2016-10-06 22:18)
-->

-   **Navigation.** Inability or difficulty navigating using a keyboard or assistive technology.
-   **Hidden content.** Presentation of content or functionality that is not accessible to assistive technologies.
-   **User control.** Lack of user control over automated content changes.
-   **Confusion/Disorientation.** Altering or disabling the normal functionality of the <em lang="en">user agent</em> (navegador) or triggering events that the user may not be aware of.

A web page containing JavaScript will typically be fully accessible if the functionality of the script is device independent
(does not require only a mouse or only a keyboard) and the information (content) is available to assistive technologies.
Unfortunately, there is no easy fix that can be applied to solve all accessibility problems associated with JavaScript.
The only way to ensure JavaScript accessibility is by evaluating each pages that utilizes scripting and devising a unique solution to any accessibility problem found.

### JavaScript that does not impact accessibility

Just because JavaScript is utilized on a page does not mean that the page is inaccessible.
In many cases, JavaScript can be used to increase accessibility.
Additional information, warnings, or instructions can be given to users through JavaScript prompts.
For instance, under the [Section 508 guidelines of United States law](http://webaim.org//standards/508/checklist) and the
[Web Content Accessibility Guidelines](http://webaim.org//standards/wcag/checklist),
a user must be notified when a timed response is required and given sufficient time to indicate more time is required.
Such functionality would be difficult with HTML alone.

JavaScript is sometimes used to create visual interface elements that do not affect accessibility.
JavaScript is commonly used for image rollovers or other visual-only modifications,
where one image is replaced with another when the mouse is placed above it;
for example, when a navigation item changes to display a shadow, glow, or highlight when the user mouses over it.

Such uses of JavaScript do not need additional accessibility features incorporated because important content is not displayed or functionality introduced by such scripting.

### JavaScript Reliance

It is a common misconception that people with disabilities don't have or 'do' JavaScript,
and thus, that it's acceptable to have inaccessible scripted interfaces, so long as it is accessible with JavaScript disabled.
A 2012 survey by WebAIM of screen reader users found that [98.6% of respondents had JavaScript enabled](http://webaim.org//projects/screenreadersurvey4/#javascript).
The numbers are even higher for users with [low vision](http://webaim.org/projects/lowvisionsurvey/#javascript) or
[motor disabilities](http://webaim.org/projects/motordisabilitysurvey/#javascript).
In short, people with disabilities will experience scripting, so scripted content must be made natively accessible.

Accessibility guidelines also require scripted interfaces to be accessible.
While WCAG 1.0 from 1999 required that pages be functional and accessible with scripting disabled,
WCAG 2.0 and all other modern guidelines allow you to require JavaScript,
but the scripted content or interactions must be compliant with the guidelines.

It is important to keep in mind, however, that some users do disable JavaScript or may be using technologies that don't support or fully support scripting.
If your web page or application requires scripting, ensure that you account for users without JavaScript.
While this does not necessarily mean that all functionality must work without scripting (though this would clearly be optimal),
if it does not work without scripting, you must avoid a confusing or non-functional presentation that may appear to function,
but does not because of lack of JavaScript support.

## JavaScript Event Handlers

### Overview

Event handlers accompany existing HTML code or dynamically generated content and are triggered by a browser or user event -
such as when the page loads, when the user clicks the mouse, or when the time is 8 p.m.
Some event handlers are dependent upon use of a mouse or keyboard.
These are called **device dependent** event handlers.
Other event handlers are **device independent** and are triggered by both the mouse and keyboard or by other means.

<div class="important" markdown="1">
<div class="title">Importante</div>
To ensure accessibility, use either a device independent event handler (one that works with both the mouse and the keyboard)
or use both mouse dependent *and* keyboard dependent event handlers.
</div>

### `onMouseOver` and `onMouseOut`

The `onMouseOver` event handler is triggered when the mouse cursor is placed over an item.
As its name implies, `onMouseOver` requires the use of a mouse, thus it is a device dependent event handler and may cause accessibility issues.
`onMouseOver`, and its companion, `onMouseOut`, may be used, as long as any important content or functionality is also available without using the mouse.
If the mouse interaction is purely cosmetic (such as the addition of a glow or drop shadow),
there are likely no accessibility issues, so long as the style change does not indicate some function (such as to indicate that an element is clickable).

If the mouse interaction presents additional information or content,
such as a tooltip, a navigation menu, etc., then this content will not be accessible to anyone not using a mouse.
Additional considerations are necessary for accessibility.

For screen reader users, the additional content might be provided directly in an accessible way,
such as through alternative text, through an ARIA label or description, or perhaps through off-screen text.
However, for sighted keyboard-only users, there must be a mechanism for them to access and view the newly revealed content or functionality.

In addition to `onMouseOver` and `onMouseOut`, use `onFocus` and `onBlur`.
These actions are triggered when the keyboard is used to navigate to and from an element.
Of course these can only be triggered on keyboard-navigable elements -
links and form controls (or perhaps elements with [tabindex](http://webaim.org/techniques/keyboard/tabindex)).
Simply triggering the change with a standard link and using both mouse and keyboard dependent event handlers will help ensure accessibility.

Sometimes scripting is used to present complex interactions, such as a drop-down or fly-out menu.
While these can be made technically accessible,
sometimes an accessible alternative approach may be more friendly.
For example, instead of forcing users to navigate through a complex and lengthy navigation menu,
you could instead ensure that the menu system is NOT directly keyboard accessible (nor read by a screen reader),
but provide standard link functionality on the top-level menu item (e.g., "Products").
This link would take the user to a secondary page that provides standard links to the pages provided through the complex menu
(e.g., a Products landing page that has links to the various product categories).
While not exactly the same interaction that mouse users may choose,
such alternatives are often more intuitive and friendly for all users.

### `onFocus` and `onBlur`

These event handlers are typically used with form elements,
such as text fields, radio buttons, and submit buttons, but can also be used with links.
`onFocus` is triggered when the cursor is placed on or within a specific form element,
or when a user 'tabs' to the element using the keyboard.
`onBlur` is triggered when the cursor leaves a form element or the user 'tabs' away from it.

Both of these event handlers are device independent,
meaning that they can be performed with the mouse, keyboard, or other assistive technology.
The actions that are performed as a result of these event handlers must be analyzed to determine if they cause accessibility problems.
Typically, these events do not cause accessibility issues unless they are modifying the default behavior of the web browser or are interfering with keyboard navigation within the web page.
Examples of such issues might be automatically setting focus to other page areas with `onFocus` and `onBlur`,
trapping the user inside a form control, dynamically revealing form controls immediately upon a user leaving (blurring) a form control, etc.
Keyboard and screen reader testing will be necessary to ensure these interactions are built in an accessible manner.

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