---
layout: translation
date: 2016-08-28 # Data de ultima atualização do original
title: "How to make your wireframes more accessible in five easy steps" # Titulo traduzido
description: "Most websites in North America and Europe now need to meet accessibility requirements.
These include requirements described by Section 508 of the American Disabilities Act (ADA)."

copyright: 'Copyright http://accessib.li/' # Quem tem direitos de cópia
license: null # Caso seja uma licença padrão (MIT, GPL...) por aqui
license-custom: null # Caso a licença não seja uma padrão, por uma descrição curta dela aqui
authors: [{
    name: "Alison Walden",
    link: "http://accessib.li/about-alison-walden/"
}]
translators: [{
    name: "Nome Do Tradutor Aqui",
    link: "http://twitter.com/webiwg"
}]
reviewers: []
discussion: https://github.com/webiwg/acessibilidade-web-pt/issues/11
original: {
    title: "How to make your wireframes more accessible in five easy steps", # Titulo original, no idioma origial
    link: "http://accessib.li/2016/08/28/how-to-make-your-wireframes-more-accessible-in-five-easy-steps/", # Link para documento original
    dateOfTranslation: "2016-10-04" # Data em que a tradução foi finalizada
}
isDraft: true
isReleaseCandidate: false
---

Most websites in North America and Europe now need to meet accessibility
requirements. These include requirements described by Section 508 of the
American Disabilities Act (ADA). They also refer to the Web Content
Accessibility Guidelines (WCAG 2.0).

Follow these five easy steps to make your wireframes more accessible:

-   One: Document the heading structure.
-   Two: Document hidden way-finding cues.
-   Three: Document focus order information and specify the visible focus state.
-   Four: Provide clear link labels.
-   Five: Design simple, usable forms.

<span id="more-279"></span>

One: Document the heading structure
-----------------------------------

Remember the last time you wrote an essay? You probably had a series of sections
in your essay that each had a heading. Most likely you had a table of contents
that listed all your headings. If someone read your table of contents, they
would have had a good idea of what your essay was about.

This is what headings are for on a website. They should describe the page they
are on. Assistive devices like screen readers allow users to navigate web pages
by headings. This is one way that a non-sighted person can "scan" a webpage, by
choosing to hear all the headings on the page. Listening to the headings allows
them to assess if the page is useful for them. If the headings are not developed
and written in a clear and proper way, they will not be helpful to this
audience.

<img src="http://i0.wp.com/accessib.li/wp-content/uploads/2016/08/headings.jpg?resize=550%2C217" alt="A primary heading that asks the question, Should I be a primary heading?" class="size-full wp-image-282" sizes="(max-width: 550px) 100vw, 550px" srcset="http://i0.wp.com/accessib.li/wp-content/uploads/2016/08/headings.jpg?w=550 550w, http://i0.wp.com/accessib.li/wp-content/uploads/2016/08/headings.jpg?resize=300%2C118 300w" width="550" height="217" />

The experience designer or copywriter should decide the heading structure. The
wireframe or content matrix should include an annotation that describes the
heading structure. A developer should not decide the heading structure by
herself (in absence of documentation).

Two: Document hidden way-finding cues
-------------------------------------

Screen reader users benefit from additional way-finding cues to help them
navigate a webpage. These include:

-   "Bypass block links": These allow screen reader users to skip over repeated
    blocks of content.  Without them, screen reader users would have to tab
    through repetitive blocks of content from page to page. They are most often
    used to skip over navigation menus. Other candidates for bypassing include
    filter menus or carousels with many panels.
-   Bypass block links can be hidden by default, but should appear on
    keyboard focus. They should allow the user to skip past the content block to
    the content immediately after. It's important to test these with your
    keyboard once they are implemented. Make sure that you can tab once into the
    content area, and tab again into the next interactive element in the
    content area.

Three: Document focus order information and specify the visible focus state
---------------------------------------------------------------------------

### Focus order

Focus order is an important concept for keyboard accessibility. It refers to the
order that elements on the page receive keyboard focus. The usual focus order
for the Western world is from top to bottom, left to right, the same way we
read.

For keyboard users, a common way to access a website is to move through the
content by pressing the tab key. The tab key moves the focus state to links or
form elements. Screen reader users can have their device begin reading the page
at any point.

Usually experiences benefit from implementing a default focus order. There are
instances where the focus order should be changed. This is best determined by an
experience designer.

The following flow illustrates a situation where the default tabbing order
should be overridden:

-   User clicks on a link to log in to a website, and the log in link leads to a
    different page.
-   By default, the first focused area on the page would probably be in the top
    left-most link or form field. But in this instance, the user is definitely
    there to log in. It makes sense here to put the focus state on the first
    field in the sign in form.

Again, this cannot be decided by a developer in absence of documentation. It
must be annotated in the wireframe.

### Visible focus state

The visible focus state is the visual indicator that an element has focus. It is
common for designers to create a hover state for mouse users. Usually the focus
state should match the hover state.

For developers to handle this state in their implementations, it must be defined
in the wireframe. Additionally, the design of each element's focus state must be
described in the style guide. Each browser has its own default focus state.
Either allow this to be used, or have the designer create a new one that matches
your client's branding.

Many clients do not understand the value of the visible focus state. When it is
described in the style guide, the client has an opportunity to see it up front
and ask questions about it.

> What is a visible focus state?
>
> Try it out on my website: Press your tab key now and try to see what the
> current focused element is on the site. You will see that my navigation links
> along the top of the site get underlines, and other links change color and
> have an outline. This is so keyboard users can see where the focus is.

Four: Provide clear link labels
-------------------------------

For users who navigate with a screen reader, many of them will only hear link
labels. They will not have any context on surrounding information. That's why it
is important to make sure the link itself (or the form field label) is
meaningful.

Do this: Learn more about our services

Don't do this: Learn more

Do this: Edit my account settings

Don't do this: Edit

Sometimes the context is clear to a sighted user based on surrounding content.
In this case, indicate in the wireframe that the developer should hide the
additional content from sighted users. This way, a sighted user who can gain
context from the surrounding content will see "Learn more". A non-sighted user
will hear, "Learn more about our services".

Five: Design simple, usable forms
---------------------------------

### Usable form design

I often ask designers if they plan to enter their form design into the coveted
Form Design Awards. Usually they stare back at me blankly. Sometimes they perk
up and ask for more information about these awards.

There are no Form Design Awards. Isn't it great? We can put our aesthetic goals
aside and focus on making the form usable. Trust me: forms are meant to be
filled out. They don't need to be flashy. It's okay if they aren't ultra clean
and sleek.

Here are some form design best practices that also make the form more
accessible:

-   Place the label above the form field, not beside it.
-   Put a "required field" indicator inside the field's label. It's also helpful
    to put "(optional)" within optional field's labels.
-   Do not replace proper form fields with placeholder text. Users of all ages
    and abilities complain about this. Placeholder text disappears when a user
    clicks into the field and begins to type. It can be hard to remember what
    content the field needed (e.g. Email address vs. username).
-   If fields do not have a visible label (e.g. search fields), provide the
    annotation for a hidden label. Indicate the label text. All form fields must
    have labels.

<img src="http://i2.wp.com/accessib.li/wp-content/uploads/2016/08/label-top-of-field.jpg?resize=550%2C170" alt="Form field labels should be placed above the field, not beside it." class="size-full wp-image-280" sizes="(max-width: 550px) 100vw, 550px" srcset="http://i2.wp.com/accessib.li/wp-content/uploads/2016/08/label-top-of-field.jpg?w=550 550w, http://i2.wp.com/accessib.li/wp-content/uploads/2016/08/label-top-of-field.jpg?resize=300%2C93 300w" width="550" height="170" />

*See this article:* *[The definitive guide to form label
positioning](http://www.sitepoint.com/definitive-guide-form-label-positioning/)[/](http://www.sitepoint.com/definitive-guide-form-label-positioning/)*

<img src="http://i0.wp.com/accessib.li/wp-content/uploads/2016/08/no-placeholders.jpg?resize=550%2C153" alt="Do not replace labels with placeholder text." class="size-full wp-image-281" sizes="(max-width: 550px) 100vw, 550px" srcset="http://i0.wp.com/accessib.li/wp-content/uploads/2016/08/no-placeholders.jpg?w=550 550w, http://i0.wp.com/accessib.li/wp-content/uploads/2016/08/no-placeholders.jpg?resize=300%2C83 300w" width="550" height="153" />

*From the Nielsen Norman Group article:*
*[https](https://www.nngroup.com/articles/form-design-placeholders/)[Form design
placeholders](https://www.nngroup.com/articles/form-design-placeholders/)[/](https://www.nngroup.com/articles/form-design-placeholders/)*

### Accessible form error messaging

Screen readers automatically read out form field labels when the field has
focus. The form error messaging flow should work like this:

-   User fills out a field the wrong way.
-   User attempts to submit form.
-   The first form field that has an error message should automatically gain
    keyboard focus.
-   The form field error message should be programmatically appended to the
    field's label.

In this way, the screen reader will read out the form field followed by the
error message text. Example: "Email address. Email address is a required field."
The user can then fix this issue, then tab through the rest of the form and hear
any other error messages along the way.

[WebAIM has a great article about accessible form development<span
class="icon-webfont fa-external-link" aria-hidden="true"></span><span
class="screen-reader-text">Opens in a new
window</span>](http://webaim.org/techniques/forms/) that I encourage everyone to
read.

You might be interested in these other articles related to accessible user experience:
--------------------------------------------------------------------------------------

-   [Creating accessible experiences starts with experience
    design](http://accessib.li/2016/05/14/creating-accessible-experiences-starts-with-experience-design/)
-   [Why accessibility compliance should be a criteria in web design
    awards](http://accessib.li/2016/04/22/why-accessibility-compliance-should-be-a-criteria-in-web-design-awards/)
-   [Usability should include
    accessibility](http://accessib.li/2016/03/18/usability-should-include-accessibility/)

Let me know in the comments section what accessibility features you add to your
wireframes.
