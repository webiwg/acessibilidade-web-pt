CSS in Action  
<span class="subtitle">Invisible Content Just for Screen Reader Users</span>
============================================================================

Introduction
------------

<span
class="floatright"><img src="media/peekaboo.jpg" alt="A woman hides behind her hands." width="130" height="110" /></span>There
are occasional instances where content should be made available to screen reader
users, but hidden from sighted users. In most cases, if content (particularly
content that provides functionality or interactivity) is important enough to
provide to screen reader users, it should probably be made available to all
users. Cases where verbose cues or instructions are provided only for screen
reader users are most likely a reflection of poor design and accessibility.
However, there are a few cases where information is apparent visually, but may
not be apparent to screen reader users. In these cases, it may be appropriate to
mark-up content in a way that it is read by a screen reader, but invisible to
sighted users.

Techniques for hiding text
--------------------------

There are several mechanisms that can be used for hiding content. It's important
that a technique be implemented that results in the desired outcome and
accessibility.

### `visibility: hidden;` and/or `display:none;`

These styles will hide text from all users. The text is removed from the visual
flow of the page and is ignored by screen readers. **Do not use this CSS if you
want the content to be read by a screen reader. But DO use it for content you
don't want read by screen readers.**

### `width:0px`, `height:0px` or other 0 pixel sizing techniques

As above, because an element with no height or width is removed from the flow of
the page, most screen readers will ignore this content. HTML width and height
may give the same result. **Do not size content to 0 pixels if you want the
content to be read by a screen reader.** Content styled with `font-size:0px` or
`line-height:0` may work, though the elements would still take horizontal space
on the screen. All of these techniques may result in search engine penalties as
they may interpreted to be malicious.

### `text-indent: -10000px;`

This approach moves the content to the left 10000 pixels - thus off the visible
screen. The actual value matters little, so long as it is positioned off-screen.
Screen readers will still read text with this style. However, if a link or form
element is given this style, it may result in a focus indicator (the dotted
lines or 'marching ants' that surround a focused link) that extends from where
the element should be located in the page to the place it is actually located
(way to the left). This is not very pretty. This approach also causes issues in
right-to-left languages. As such, this approach *may* be a viable option if the
element does not contain navigable elements, though better techniques are
available.

### CSS clip

`position: absolute !important; clip: rect(1px 1px 1px 1px); /* IE6, IE7 */ clip: rect(1px, 1px, 1px, 1px);`

A fairly modern technique of using CSS to hide or clip content that does not fit
into a 1 pixel visible area will essentially hide the content visibly, but still
allow it to be read by modern screen readers.

### Absolutely positioning content off-screen

Using CSS to move hidden elements to a position off-screen is generally accepted
as the most useful and accessible method of hiding content visually.

Positioning content off-screen
------------------------------

The following are the recommended styles for visually hiding content that will
be read by a screen reader.

` .hidden          {position:absolute;     left:-10000px;     top:auto;     width:1px;     height:1px;     overflow:hidden;}`

The .hidden CSS class should then be referenced from within the tag of the
element being hidden, as shown:

`<div class="hidden">This text is hidden.</div>`

Sighted users will not see the hidden content at all. It will be out of their
viewing range - hidden well to the left of the visible browser window. Screen
reader users will have access to the content as if it were not hidden at all.
Screen readers read the content normally, completely ignoring the styles used in
this technique.

Let's analyze the styles in detail.

`position:absolute;` tells the browser to remove the element from the page flow
and to begin positioning it. `left:-10000px;` moves the content 10000 pixels to
the left. `top:auto;` tells the browser to position the content vertically at
the same location it was originally. Omitting `top` may result in the `left`
style being ignored in some instances and browsers. In short, this part of the
code moves the element 10000 pixels straight to the left.

`width:1px; height:1px; overflow:hidden;` tells the browser to make the element
1px by 1px in size and to visually hide everything that does not fit into these
dimensions. While this is a likely a little overkill and can probably be omitted
in most circumstances, there are a few instances where positioning may be
disabled, but all other styles remain enabled. In this case, the element will
remain in its original position, but will only take 1 pixel of space.

Note

It is sometimes recommended to position content using `left:0px; top:-500px` (or
similar). While this works by positioning the content above the top of the page,
if the hidden element contains a link or form element, upon receiving keyboard
focus, the browser attempts to scroll to the element - thus scrolling the
browser to the top of the page. This could result in confusion for sighted
keyboard users. By positioning directly to the left, the browser will not scroll
to the top of the page. **It should be noted that because links and form
elements provide functionality, they should rarely be hidden from sighted users.
Sighted users will not be able to see which element currently has focus because
it is hidden off-screen.**

Examples
--------

Important!

In general, content should only be hidden from sighted users and made available
to screen reader users when content is apparent visually, but not apparent to
screen reader users.

### Instructional cues and indicators

This technique can be used to provide instructional cues and indicators to
screen reader users. This should be implemented with discretion and only where
necessary. This page demonstrates proper use of this technique in two places.

First, the search text box at the top of the page has a hidden label immediately
before it. It is apparent visually that the text box is for searching due to the
presentation and the search button, but a screen reader requires a label for the
text field. As such, we provided a label, but have hidden it visually.

Second, the breadcrumbs at the top of the page are a common design convention.
Most web users understand the convention and can identify breadcrumbs visually.
Because a screen reader accesses the breadcrumb links and content linearly, it
may not be apparent to them that it is breadcrumbs until they have read a
portion of it. As such, we have added hidden text of "You are here:" just prior
to the breadcrumbs.

You can see all of this hidden text by disabling styles for this page.
**Remember, all content hidden visually with CSS will become visible if styles
are disabled.**

### "Skip to main content" links

["Skip to main content" links](/techniques/skipnav/) are one of the few places
where accessibility has a direct and distinct impact on visual design. In order
to be useful, the "skip" link should be one of the first on the page. Designers
may balk at the idea of providing a link as the first thing on the page -
particularly when that link is unlikely to be utilized by the majority of the
site visitors. However, hiding the link makes them unusable to sighted keyboard
users - a user group that can greatly benefit from this link.

One way to reconcile the impact that "skip" links have on visual design with the
needs of screen reader users and users with mobility impairments is to use a
technique that hides the "skip to main content" link until the user tabs to it.
When the link receives focus, the link becomes visible to sighted users. This
would allow both blind and sighted keyboard users to take advantage of the
link's functionality

In order to accomplish this, two styles are created - one for the `<a>` element
and one for the `a:focus` pseudo-class. The style for the `a:focus` pseudo-class
will only be active when the user tabs to the link (i.e., it has focus), and the
link will revert back to its default style (i.e., it will be hidden off-screen
again) when the user tabs away from the link.

`         #skip a         {          position:absolute;          left:-10000px;          top:auto;          width:1px;          height:1px;          overflow:hidden;         }                    #skip a:focus          {          position:static;          width:auto;          height:auto;          }      `

The styles should then be applied to the "skip" link.

`<div id="skip"><a href="#content">Skip to Main Content</a></div>`

The one drawback to this approach, on a conceptual level, is that the sudden
appearance of a link that was previously invisible will be unexpected, and could
confuse the sighted keyboard user. The link should also be clearly styled so it
is apparent. These will not be problems for screen reader or mouse users because
they never see the link.

### Other implementations

Form controls are sometimes presented visually so that text is visually
associated as the label for multiple controls. Consider data entry where one
"First name" text might describe the function of multiple text boxes that appear
below it. Sometimes tables are used for these presentations. Alternatively,
sometimes one control may be labeled by multiple items of text, such as a
password field that is preceded by the word "Password:" and followed by the word
"Required". Using standard [form labelling](/techniques/forms/controls), there
is no way to associate one text item to multiple controls or multiple texts to
one form control. In these case, the appropriate labels could be provided in the
markup adjacent to their respective form elements, but hidden using the CSS
above.

A common example of this is when two or more text input elements are used for
phone numbers.

<img src="media/phone1.jpg" alt="The words &#39;phone number&#39; are followed by 4 text input boxes, intended to be used for area code, first three digits, last four digits, and then extension" class="border" width="389" height="42" />

Most visual users in North America will understand that the individual text
input areas correspond to the different sections of standard phone numbers.
Screen reader users, however, may attempt to enter the entire phone number in
the first box. Confusion is likely when they discover that the box limits them
to only 3 characters or that there are additional unlabeled text boxes that
follow.

The most obvious workaround for this particular problem would be to combine all
of the text input boxes into a single text input box, and then provide the
appropriate label. However, off-screen labels for each distinct text box will
also ensure accessibility.

`         Phone number:          (         <label for="area" class="hidden">Area code</label>         <input name="area" id="area" type="text" size="3" maxlength="3">         )         …`

The off-screen labels would, in this case, provide an adequate description for
screen reader users.

Note

In the example above, the `title` attribute could also be used to provide this
information. Information in the `title` attribute will be read by screen readers
when a label is not present. Additionally, `aria-labelledby` could be used to
provide multiple labels per input or multiple inputs per label.

Conclusion
----------

When the CSS techniques presented here are used to hide content, sighted users
will never know that the content is there at all (unless they disable styles).
Screen reader users, on the other hand, will never realize that this content is
invisible to sighted users. Both kinds of users will be able to use the content
intuitively, without having to adjust for either too much or too little
information in the markup. This can provide important contextual cues that are
otherwise impossible for screen reader users to grasp because of the visual
nature of these cues. When used judiciously, this technique can resolve some of
the tension between the demands of accessibility and the demands of visual
design. It is not the only technique or method of solving this problem, but it
is one that web developers can add to their list of possible solutions when the
need arises.


