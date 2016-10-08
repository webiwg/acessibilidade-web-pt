"Skip Navigation" Links
=======================

<span class="hidden">You are here: </span>[Home](/) &gt; [Articles](/articles/)
&gt; "Skip Navigation" Links

Article Contents
----------------

1.  [Overview](#overview)
2.  [Creating "Skip Navigation" Links](#creating)
3.  [Browser Quirks](#quirks)
4.  [Multiple "Skip" Links](#multiple)
5.  [Alternatives to "Skip Navigation" Links](#alternatives)

Overview
--------

The main content is not usually the first thing on a web page. Keyboard and
screen reader users generally must navigate a long list of navigation links,
sub-lists of links, corporate icons, site searches, and other elements before
ever arriving at the main content. This is particularly difficult for users with
some forms of motor disabilities.

Without some sort of system for bypassing the long list of links, some users are
at a huge disadvantage. Consider users with no arm movement, who use computers
by tapping their heads on a switch or that use a stick in their mouth to press
keyboard keys. Requiring users to perform any action perhaps 100s of times
before reaching the main content is simply unacceptable.

Of course, sighted people who use their mouse do not have any trouble with pages
such as this. They can almost immediately scan over the page and identify where
the main content is. In effect, sighted users have a built-in "skip navigation"
mechanism: their eyes. They can also bypass the many links before the main
content and click directly on the link they want with the mouse. The "skip
navigation" idea was invented to give screen reader and keyboard users the same
capability of going directly to the main content that sighted mouse users take
for granted.

Creating "Skip Navigation" Links
--------------------------------

The idea is simple enough: provide a link at the top of the page which jumps the
user down to an anchor or target at the beginning of the main content. For the
most part, it really is this easy, though there is more than one way to
accomplish the goal. Some techniques are better than others. The techniques
discussed here are:

1.  Providing visible links at the top of the page
2.  Providing visible links elsewhere on the page
3.  Making the link invisible
4.  Making the link invisible until it receives keyboard focus

### Visible links at the top of the page

The easiest method of creating a "skip navigation" link is to put it at the top
of the page in regular text. Put the corresponding anchor (link destination) at
the beginning of the main content.

The horizontal location of the link doesn't matter much. The link can be on the
left side, the middle, the right, or in some location in between. The key is to
**make sure the link is one of the first items** that screen readers hear and
that keyboard users tab to. Otherwise, users may not realize there is a "skip
navigation" link there at all, and may waste time trying to muddle through the
extraneous links. Screen reader users especially may get impatient if they don't
hear the "skip navigation" link very early in the page.

To be optimally usable, the link must also be visually apparent. A very small or
hidden link does not benefit the audience that most needs "skip" links - sighted
keyboard users.

**The verdict:** This method works and is highly accessible. A disadvantage of
this approach is that the link may be intrusive to visual design - it must be
visible and at the very beginning of the page. Also, the link is presented to
all users, even sighted mouse users who may not use it, or that could
potentially be confused by it.

Example

The link is the first item in the page. The anchor or target for the link (where
the link will jump the user to) is placed at the beginning of the main content.

`                 <body>                 <a href="#maincontent">Skip to main content</a>                                  ...                  <main id="maincontent>                 <h1>Heading</h1>                 <p>This is the first paragraph</p>`

The target is identified by its `id` attribute value matching the `href` value
(minus the "\#") of the "skip" link.

Alternatively, you can use a named anchor to identify the target for the link,
though named anchors are no longer conforming in HTML5.

`                 <h1><a name="maincontent" id="maincontent"></a> Heading</h1>                 <p>This is the first paragraph</p>`

### Invisible links

Many developers worry about the aesthetic impact of "skip navigation" links.
They may think these links don't look particularly attractive, they "ruin" the
layout, or that they get in the way of artistic expression. It's easy to argue
that the links may be confusing for users that do not need them. While a visible
"skip" link declares a type of distinct commitment to accessibility, to address
these concerns, the link can be visually hidden.

There are a few methods for doing this, but it's vital that the link still be
usable by all keyboard users, particularly sighted keyboard users. This means
that the link should be hidden visually by default, but that it should become
visible when it receives keyboard focus. Some techniques, such as hiding the
content permanently with CSS, making the link the same color as the background,
sizing the link to 0 pixels, or placing it on a one pixel transparent image do
not meet these important requirements.

Probably the most accessible method for visually hiding skip links is to hide
them off screen, then cause them to be positioned on screen when they receive
keyboard focus.

Important

Review the article on [Invisible Content Just for Screen Reader
Users](/techniques/css/invisiblecontent/) for details on using CSS to hide
"skip" links off-screen.

One potential issue with this approach is that if the user navigates very
quickly using the <span class="keycap">Tab</span> key, the link may be visible
on the page for only a fraction of a second and may be overlooked. This can be
partially addressed by ensuring that the "skip" link is visually distinctive at
the top of the page. Additionally, one could use scripting of (optimally) CSS3
transitions to cause the link to animate so it remains visible on screen for a
period of time.

Note

You can see an example of a hidden skip link that becomes visible on keyboard
focus, that also has CSS3 animation to make it visually distinctive and always
visible on screen momentarily on this very page. Simply navigate through the
links at the beginning of this page using the <span class="keycap">Tab</span>
key and watch for the "skip" link at the top left screen.

**The verdict:** This method works well for nearly all users. Sighted mouse
users (who do not benefit from the link) do not see it, screen reader users will
hear the link, and sighted keyboard users will see the link when they navigate
to it.

### Which wording is best?

There is more than one "best" way to word the link. Here are some fairly common
examples:

-   Skip navigation
-   Skip main navigation
-   Skip navigation links
-   Skip to main content
-   Skip to content

None of these is inherently better than the others. In general, we prefer "Skip
to main content" as it explains where they are navigating to versus what they
are navigating past. Minor variations on these are probably acceptable, such as
"skip top navigation." Don't get too creative here, or else users may not
realize what the purpose of the link is.

Browser Quirks
--------------

"Skip navigation" links are such a simple concept that it's hard to believe
there would be any browser quirks in implementing it, but there are. Some
browsers do not fully support in-page links. While they may visually shift focus
to the location of the target or named anchor for the "skip" link, they do not
actually set keyboard focus to this location. These bugs can potentially be
addressed by using JavaScript to set focus (using JavaScript `focus()`) to the
target element.

Multiple "Skip" Links
---------------------

What if a page has multiple sections and/or multiple layers of navigational
links? Should developers provide a "skip navigation" to each of these sections
or over each layer or navigational links? In most cases, this is not necessary.
Remember, the purpose of "skip navigation" links is to reduce the clutter of
lists of links. Adding more links increases link-clutter.

A popular U.S. government site recently had a total of nine different "skip
navigation" links (the links are hidden using CSS):

1.  Skip to content
2.  Skip to government search
3.  Skip to bottom nav
4.  Skip to top nav bar-right aligned
5.  Skip to By organization
6.  Skip to contact your government
7.  Skip to reference center
8.  Skip to information by topic
9.  Skip to citizens: get it done online!

This brings of the question of whether they need a "Skip the skip links" link!
By providing a proper document outline, perhaps using HTML5 section elements and
ARIA landmarks, and simplifying page structure and navigation, typically one or
two "skip" links is sufficient.

Skip links or other in-page links can also be used to allow users to jump to or
jump over page content. For example, the Table of Contents at the top of this
page includes in-page links to facilitate navigation to page areas. A "skip"
link could also be used to allow the user to quickly bypass confusing or
potentially inaccessible content, such as ASCII art, complex tables, etc.

Alternatives to "Skip Navigation" Links
---------------------------------------

The truth is that "skip navigation" links are a rather clumsy and obtrusive
solution to a real world problem. They work. They're useful, but they're a bit
of a hack. They will continue to be useful until a more standardized method of
designating the difference between navigation and main content evolves and is
fully supported. With ARIA landmarks and the HTML5 `<main>` element, this is
closer to becoming a reality. Unfortunately, no browsers yet fully support
keyboard navigation via these elements. Despite these limitations, there are
other ways one can facilitate page navigation in addition to "skip" links.

### Navigating by headings

The most useful alternative method is to create documents with proper headings
so that users can skip from heading to heading. Most screen readers allow users
to listen to a list of headings or to listen to each heading in sequence,
skipping past the paragraphs, images, links, and other extraneous information.
If documents are created properly, they can often form an outline of headings,
which serves not only as a way to skip past the navigation but also lets screen
reader users "scan" the main ideas of a document without having to read the
whole thing. Defining your primary document heading at the beginning of your
main content as an `<h1>` can provide very quick access to the beginning of the
main content.

The one downside to this approach is that only screen reader users have access
to this functionality. Browsers do not come with this feature. This means that
sighted keyboard users cannot skip from link to link in the same way that screen
reader users can.

**Verdict:** This method is very effective for screen reader users, but sighted
keyboard users generally cannot take advantage of it. Even so, there are many
reasons to use headings, so this method is highly recommended.

### Alternate reading orders

Some developers place the main content first in the reading order and the
navigation last - generally using CSS to maintain the navigation first in the
page visually. This method makes "skip navigation" links unnecessary, but it
raises another question. Should such sites provide "skip *to* navigation" links?
This is a tricky question. Links taking users to the navigation are unexpected,
and can lead to some confusion. With or without "skip to navigation" links,
screen reader users who want to access the navigation may get lost in the page,
wondering if there is any navigation.

This approach also causes a reading and navigation order that is very atypical -
and that can be very confusing, particularly for sighted users who are visually
tracking the navigation focus that seemingly jumps around the page rather than
starting at the beginning.

**Verdict:** The concept can be useful, but users can becomes disoriented with
an atypical reading and navigation order.


