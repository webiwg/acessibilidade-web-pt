---
layout: translation
date: 2013-08-09 # Data de ultima atualização do original
title: "Creating Accessible Forms" # Titulo traduzido
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

# Creating Accessible Forms

## Introduction

Forms are used for many types of interactions on the web. When we talk about the accessibility of forms, we are usually referring to their accessibility to people who use screen readers or keyboards. People with other types of disabilities are generally less affected by faulty forms. It should be noted, however, that everyone benefits from a well-organized, highly usable form, especially those with cognitive disabilities.

## Ensure Forms are Logical and Easy to Use

Forms should be clear and intuitive. They should be organized in a logical manner. Instructions, cues, required form fields, field formatting requirements, etc. should be clearly identified to users. Provide clear instructions about what information is desired. If any form elements are required, be sure to indicate so. Make sure that the order in which form elements are accessed is logical and easy. This can sometimes by problematic if tables are used to control layout of form items. To check the linearized order of items on the page, use [the WAVE accessibility tool](http://wave.webaim.org/).

## Ensure Forms are Keyboard Accessible

Many users can only use a keyboard to navigate and use the web. You must ensure that the forms on your web site can be completed using only the keyboard. There are a few things that can make forms totally unusable with the keyboard, the most common of which is JavaScript. Be careful in your use of JavaScript to manipulate form data, set focus, change form elements, or submit forms. Each of these can make the form difficult or impossible to complete or understand using the keyboard alone. Always test your web site forms for keyboard accessibility.

## Associate Form Labels with Controls

Text labels should generally describe the function of each form control. Place the label adjacent to its respective form control (i.e., text box, check box, radio button, menu, etc.). Labels are usually positioned above or to the left of controls, however, the labels for checkboxes and radio buttons are usually to the right of the control. Sighted users should be able to visually associate a text label with its corresponding form control. Users with visual disabilities, however, cannot make this visual association. Labels can, however, be associated programmatically with form controls using HTML markup.

The `<label>` element is used to associate a text label to a form control. This allows a screen reader to read the associated label text when the user navigates to the form control.

<div class="important">

<div class="title">Important</div>

Screen reader users generally navigate through a form using the <span class="keycap">Tab</span> key to jump from form control to form control. Associated form labels are read for each form control when the user navigates to them. Any non-label text content between the form controls is usually skipped over. Be sure to include important cues or instructions in associated labels or at the beginning of the form.

</div>

Groupings of form controls, typically groups of related checkboxes and radio buttons, sometimes require a higher level description (such as "Shipping Method" for a group of shipping option radio buttons). This descriptive text can be associated to the group of form controls using `<fieldset>` and `<legend>`. The `<fieldset>` identifies the entire grouping and `<legend>` identifies the grouping's descriptive text. Using `<fieldset>` and `<legend>` ensures that the text description is read to screen reader users when the grouping is navigated to.