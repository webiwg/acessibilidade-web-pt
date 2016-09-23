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

<!-- Geração automática de índice, inicio -->
<nav  markdown="1">

## Índice de tópicos
{:.no_toc}

1. Indice de Tópicos. Esta linha será substituída
{:toc}

</nav>
<!-- Geração automática de índice, fim -->

<!--
  Pagina 1 http://webaim.org/techniques/forms/
-->

# General Form Accessibility

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



<!--
  Página 2: http://webaim.org/techniques/forms/controls
-->

<form method="post" action="">
  <div class="section" id="input">
    <h2>Text inputs</h2>
    <p><label for="name">Name:</label>
      <input id="name" type="text" name="textfield">
    </p>
    <p>Here's the HTML markup:</p>
    <div class="programlisting">
      <code>&lt;label <strong>for="name"</strong>&gt;Name:&lt;/label&gt;<br>
      &lt;input <strong>id="name"</strong> type="text" name="textfield"&gt;
      </code>
    </div>
    <p>Matching <code>for</code> and <code>id</code> values associate the label with the appropriate form control. Because <code>id</code> must be unique on each page, only one label can be associated to each unique form element. This means you cannot have one label for multiple form elements. Additionally, screen readers do not support multiple labels that are associated to the same form element.</p>
    <div class="note">
      <div class="title">Note</div>
      <p>Another benefit of using labels is that the user can click on the label itself to set focus to the form element. This is useful to some with motor disabilities, particularly when selecting small checkboxes and radio buttons. You can try this by clicking on the word "Name:" above to see focus set to the text box. Clicking adjacent labels provides an easy way to check for proper form labeling.</p>
    </div>
  </div>
  <div class="section" id="textarea">
    <h2>Textareas</h2>
    <p><label for="address">Enter your address:</label><br>
      <textarea name="addresstext" cols="25" rows="5" id="address"></textarea>
    </p>
    <p>Here's the HTML markup:</p>
    <div class="programlisting">
      <code>&lt;label for="address"&gt;Enter your address:&lt;/label&gt;&lt;br&gt;<br>
      &lt;textarea id="address" name="addresstext"&gt;&lt;/textarea&gt;
      </code>
    </div>
  </div>
  <div class="section" id="checkbox">
    <h2>Checkboxes</h2>
    <fieldset>
      <legend>Select your pizza toppings:</legend>
      <input id="ham" type="checkbox" name="toppings" value="ham">
      <label for="ham">Ham</label>
      <br>
      <input id="pepperoni" type="checkbox" name="toppings" value="pepperoni">
      <label for="pepperoni">Pepperoni</label>
      <br>
      <input id="mushrooms" type="checkbox" name="toppings" value="mushrooms">
      <label for="mushrooms">Mushrooms</label>
      <br>
      <input id="olives" type="checkbox" name="toppings" value="olives">
      <label for="olives">Olives</label>
    </fieldset>
    <p>Here's the HTML markup:</p>
    <div class="programlisting">
      <code>
      &lt;fieldset&gt;<br>
      &lt;legend&gt;Select your pizza toppings:&lt;/legend&gt;<br>
      &lt;input id="ham" type="checkbox" name="toppings" value="ham"&gt;<br>
      &lt;label for="ham"&gt;Ham&lt;/label&gt;&lt;br&gt;<br>
      &lt;input id="pepperoni" type="checkbox" name="toppings" value="pepperoni"&gt;<br>
      &lt;label for="pepperoni"&gt;Pepperoni&lt;/label&gt;&lt;br&gt;<br>
      &lt;input id="mushrooms" type="checkbox" name="toppings" value="mushrooms"&gt;<br>
      &lt;label for="mushrooms"&gt;Mushrooms&lt;/label&gt;&lt;br&gt;<br>
      &lt;input id="olives" type="checkbox" name="toppings" value="olives"&gt;<br>
      &lt;label for="olives"&gt;Olives&lt;/label&gt;<br>
      &lt;/fieldset&gt;</code>
    </div>
    <p>The <code>&lt;fieldset&gt;</code> surrounds the entire grouping of radio buttons. The <code>&lt;legend&gt;</code> provides a description for the grouping. In screen readers, the legend text is generally read for each control in the fieldset, so the legend text should be brief and descriptive.</p>
  </div>
  <div class="section" id="radio">
    <h2>Radio buttons</h2>
    <fieldset>
      <legend>Choose a shipping method:</legend>
      <input id="overnight" type="radio" name="shipping" value="overnight">
      <label for="overnight">Overnight</label><br>
      <input id="twoday" type="radio" name="shipping" value="twoday">
      <label for="twoday">Two day</label><br>
      <input id="ground" type="radio" name="shipping" value="ground">
      <label for="ground">Ground</label>
    </fieldset>
    <p>Here's the HTML markup:</p>
    <div class="programlisting">
      <code>&lt;fieldset&gt;<br>
      &lt;legend&gt;Choose a shipping method:&lt;/legend&gt;<br>
      &lt;input id="overnight" type="radio" name="shipping" value="overnight"&gt;<br>
      &lt;label for="overnight"&gt;Overnight&lt;/label&gt;&lt;br&gt;<br>
      &lt;input id="twoday" type="radio" name="shipping" value="twoday"&gt;<br>
      &lt;label for="twoday"&gt;Two day&lt;/label&gt;&lt;br&gt;<br>
      &lt;input id="ground" type="radio" name="shipping" value="ground"&gt;<br>
      &lt;label for="ground"&gt;Ground&lt;/label&gt;<br>
      &lt;/fieldset&gt;</code>
    </div>
    <div class="note">
      <div class="title">Note</div>
      <p>Fieldset and legend should only be used to associate groups of controls when a higher level description (i.e., the legend) is necessary. Single checkboxes or basic radio buttons (such as male/female for gender) that make sense from their labels alone do not require fieldset and legend. Nested fieldsets should generally be avoided.</p>
    </div>
  </div>
  <div class="section" id="select">
    <h2>Select menus</h2>
    <p>
      <label for="favcity">Choose your favorite city?</label>
      <select id="favcity" name="select">
        <option value="1">Amsterdam</option>
        <option value="2">Buenos Aires</option>
        <option value="3">Delhi</option>
        <option value="4">Hong Kong</option>
        <option value="5">London</option>
        <option value="6">Los Angeles</option>
        <option value="7">Moscow</option>
        <option value="8">Mumbai</option>
        <option value="9">New York</option>
        <option value="10">Sao Paulo</option>
        <option value="11">Tokyo</option>
      </select>
    </p>
    <p>Here's the HTML markup:</p>
    <div class="programlisting"><code>&lt;label for="favcity"&gt;Choose your favorite city?&lt;/label&gt;<br>
      &lt;select id="favcity" name="select"&gt;<br>
      &lt;option value="1"&gt;Amsterdam&lt;/option&gt;<br>
      &lt;option value="2"&gt;Buenos Aires&lt;/option&gt;<br>
      &lt;option value="3"&gt;Delhi&lt;/option&gt;<br>
      &lt;option value="4"&gt;Hong Kong&lt;/option&gt;<br>
      &lt;option value="5"&gt;London&lt;/option&gt;<br>
      &lt;option value="6"&gt;Los Angeles&lt;/option&gt;<br>
      &lt;option value="7"&gt;Moscow&lt;/option&gt;<br>
      &lt;option value="8"&gt;Mumbai&lt;/option&gt;<br>
      &lt;option value="9"&gt;New York&lt;/option&gt;<br>
      &lt;option value="10"&gt;Sao Paulo&lt;/option&gt;<br>
      &lt;option value="11"&gt;Tokyo&lt;/option&gt;<br>
      &lt;/select&gt;</code>
    </div>
    <p>To improve the accessibility of this list even further, we could add <code>optgroup</code>, to group the options.</p>
    <p>
      <label for="favcity2">Choose your favorite city?</label>
      <select id="favcity2" name="favcity2">
        <optgroup label="Asia">
          <option value="3">Delhi</option>
          <option value="4">Hong Kong</option>
          <option value="8">Mumbai</option>
          <option value="11">Tokyo</option>
        </optgroup>
        <optgroup label="Europe">
          <option value="1">Amsterdam</option>
          <option value="5">London</option>
          <option value="7">Moscow</option>
        </optgroup>
        <optgroup label="North America">
          <option value="6">Los Angeles</option>
          <option value="9">New York</option>
        </optgroup>
        <optgroup label="South America">
          <option value="2">Buenos Aires</option>
          <option value="10">Sao Paulo</option>
        </optgroup>
      </select>
    </p>
    <p>Here's the HTML markup:</p>
    <div class="programlisting"><code>&lt;label for="favcity2"&gt;Choose your favorite city?&lt;/label&gt;<br>
      &lt;select id="favcity2" name="favcity2"&gt;<br>
      &lt;optgroup label="Asia"&gt;<br>
      &nbsp;&nbsp;&lt;option value="3"&gt;Delhi&lt;/option&gt;<br>
      &nbsp;&nbsp;&lt;option value="4"&gt;Hong Kong&lt;/option&gt;<br>
      &nbsp;&nbsp;&lt;option value="8"&gt;Mumbai&lt;/option&gt;<br>
      &nbsp;&nbsp;&lt;option value="11"&gt;Tokyo&lt;/option&gt;<br>
      &lt;/optgroup&gt;<br>
      &lt;optgroup label="Europe"&gt;<br>
      &nbsp;&nbsp;&lt;option value="1"&gt;Amsterdam&lt;/option&gt;<br>
      &nbsp;&nbsp;&lt;option value="5"&gt;London&lt;/option&gt;<br>
      &nbsp;&nbsp;&lt;option value="7"&gt;Moscow&lt;/option&gt;<br>
      &lt;/optgroup&gt;<br>
      &lt;optgroup label="North America"&gt;<br>
      &nbsp;&nbsp;&lt;option value="6"&gt;Los Angeles&lt;/option&gt;<br>
      &nbsp;&nbsp;&lt;option value="9"&gt;New York&lt;/option&gt;<br>
      &lt;/optgroup&gt;<br>
      &lt;optgroup label="South America"&gt;<br>
      &nbsp;&nbsp;&lt;option value="2"&gt;Buenos Aires&lt;/option&gt;<br>
      &nbsp;&nbsp;&lt;option value="10"&gt;Sao Paulo&lt;/option&gt;<br>
      &lt;/optgroup&gt;<br>
      &lt;/select&gt;</code>
    </div>
    <p>Note that <code>optgroup</code> is not fully supported by some user agents and screen readers, so it should not be relied on to present vital category information. In cases where <code>optgroup</code> is not supported, it is simply ignored. Do not confuse the <code>label</code> attribute of the <code>optgroup</code> element with the <code>label</code> element. They are very different things.</p>
    <p>Multiple select menus allow the user to choose more than one option from the list.</p>
    <p>
      <label for="favcities">Choose your three favorite cities?</label>
      <select id="favcities" name="select" multiple="multiple">
        <option value="1">Amsterdam</option>
        <option value="2">Buenos Aires</option>
        <option value="3">Delhi</option>
        <option value="4">Hong Kong</option>
        <option value="5">London</option>
        <option value="6">Los Angeles</option>
        <option value="7">Moscow</option>
        <option value="8">Mumbai</option>
        <option value="9">New York</option>
        <option value="10">Sao Paulo</option>
        <option value="11">Tokyo</option>
      </select>
    </p>
    <div class="note">
      <div class="title">Note</div>
      <p><strong>It is recommended that multiple select menus be avoided.</strong> Not all browsers provide intuitive keyboard navigation for multiple select menus. Many users do not know to use CTRL/Command or Shift + click to select multiple items. Typically, a set of check box options can provide similar, yet more accessible functionality.</p>
    </div>
  </div>
  <div class="section" id="button">
    <h2>Buttons</h2>
    <p>For form buttons (submit and reset input elements and button elements), no additional accessibility information is required. The value attribute for input buttons and the nested text for <code>&lt;button&gt;</code> elements will be read by screen readers when the button is accessed. These must <em>never</em> be left empty.</p>
    <p>
      <input type="submit" name="submit" value="Submit Search">
      <input type="reset" name="reset" value="Reset">
      <button>Activate</button>
    </p>
    <p>Here's the HTML markup:</p>
    <div class="programlisting">
      <code>&lt;input type="submit" name="submit" value="Submit Search"&gt;<br>
      &lt;input type="reset" name="reset" value="Reset"&gt;<br>
      &lt;button&gt;Activate&lt;/button&gt;
      </code>
    </div>
    <p>Because reset buttons can be inadvertently selected, there are few cases when they should be provided.</p>
  </div>
  <div class="section" id="image_button">
    <h2>Image buttons</h2>
    <p>If you use an image button (<code>&lt;input type="image"&gt;</code> rather than a standard button, the input must have appropriate <code>alt</code> text.</p>
    <p><input type="image" name="submitbutton" src="media/search.png" alt="Search"></p>
    <p>Here's the HTML markup:</p>
    <div class="programlisting">
      <code>&lt;input type="image" name="submitbutton" <strong>alt="search"</strong> src="submit.png"&gt;</code>
    </div>
  </div>
  <div class="section" id="javascript">
    <h2>JavaScript jump menus</h2>
    <p>Because these types of menus are activated when the menu item changes, these menus can cause keyboard accessibility issues because you cannot scroll through the list without selecting one of the options.</p>
    <div class="note">
      <div class="title">Note</div>
      <p>Some browsers (including Firefox) override these jump menus so they are not activated on keyboard change, but only after you either select an item using a mouse or press Enter if using the keyboard.</p>
    </div>
    <script type="text/javascript">
      <!--
        function MM_jumpMenu(targ,selObj,restore){ //v3.0
        eval(targ+".location='"+selObj.options[selObj.selectedIndex].value+"'");
        if (restore) selObj.selectedIndex=0;
        }
        //-->
    </script>
    <p>
      <label for="selectweb">Go to a web site:</label>
      <select id="selectweb" name="menu1" onchange="MM_jumpMenu('parent',this,1)">
        <option selected="selected">Select a web site</option>
        <option value="http://www.webaim.org">WebAIM</option>
        <option value="http://google.com">Google</option>
        <option value="http://www.yahoo.com">Yahoo</option>
        <option value="http://www.microsoft.com">Microsoft</option>
      </select>
    </p>
    <p>Providing a submit button separate from the list of choices that activates the currently selected item will allow full keyboard accessibility</p>
  </div>
</form>

<!--
  Pagina 3: http://webaim.org/techniques/forms/advanced
-->

<h1>Creating Accessible Forms<br><span class="subtitle">Advanced Form Labeling</span></h1>
<div class="section" id="intro">
  <h2>Introduction</h2>
  <p>There are times when the <code>&lt;label&gt;</code> element falls short—it cannot be used to provide multiple labels for a single form control, or to associate a single label with multiple form controls. There are also times when there is not a visible text label to be associated to a form control. The majority of these labeling limitations can be overcome with three ARIA properties (<code>aria-labelledby</code>, <code>aria-describedby</code>, and <code>aria-label</code>) and a couple other techniques outlined on this page.</p>
</div>
<div class="section" id="labelledby">
  <h2><code>aria-labelledby</code></h2>
  <p>A <code>&lt;label&gt;</code> element indicates which form field it labels by referencing its <code>id</code> attribute value:</p>
  <div class="programlisting">
    <code>&lt;label for="fname"&gt;</code>
  </div>
  <p>It declares, "I am a label for this control".</p>
  <p>With <code>aria-labelledby</code>, the form field indicates which element labels it by referencing its <code>id</code> attribute:</p>
  <div class="programlisting">
    <code>&lt;input aria-labelledby="fnamelabel"&gt;</code>
  </div>
  <p>The form control declares, "I am a control labeled by this element").</p>
</div>
<div class="section" id="multiple">
  <h2>Handling Multiple Labels</h2>
  <p>Because elements in a page must all have unique <code>id</code> attribute values, a <code>&lt;label&gt;</code> can only point to the <code>id</code> of a single control - at most a one-to-one relationship between label and control. <code>aria-labelledby</code>, however, allows an element to be referenced as a label for multiple controls, and allows multiple elements to be referenced as labels for a single control. In short, <code>aria-labelledby</code> overcomes the 1 to 1 limitation of <code>&lt;label&gt;</code>.</p>
  <p>The following is a simplified example of a table that might be used for data entry. Each table header functions as a visual label for the form controls in the column below it. There is only one visual label for multiple form controls. The <code>&lt;label&gt;</code> element cannot be used to associate this text to the multiple text boxes.</p>
  <table>
    <tbody>
      <tr>
        <th id="namelabel" scope="col">Name</th>
        <th id="agelabel" scope="col">Age</th>
        <th id="weightlabel" scope="col">Weight</th>
      </tr>
      <tr>
        <td><input type="text" name="name1" aria-labelledby="namelabel"></td>
        <td><input type="text" size="3" name="age1" aria-labelledby="agelabel"></td>
        <td><input type="text" size="4" name="weight1" aria-labelledby="weightlabel"></td>
      </tr>
      <tr>
        <td><input type="text" name="name2" aria-labelledby="namelabel"></td>
        <td><input type="text" size="3" name="age2" aria-labelledby="agelabel"></td>
        <td><input type="text" size="4" name="weight2" aria-labelledby="weightlabel"></td>
      </tr>
      <tr>
        <td><input type="text" name="name2" aria-labelledby="namelabel"></td>
        <td><input type="text" size="3" name="age2" aria-labelledby="agelabel"></td>
        <td><input type="text" size="4" name="weight2" aria-labelledby="weightlabel"></td>
      </tr>
    </tbody>
  </table>
  <p>The HTML for the first header ("Name") is:</p>
  <div class="programlisting">
    <code>
    &lt;th <strong>id="namelabel"</strong> scope="col"&gt;Name&lt;/th&gt;
    </code>
  </div>
  <p>The HTML for the first text field within the table is:</p>
  <div class="programlisting">
    <code>&lt;input type="text" name="name1" <strong>aria-labelledby="namelabel"</strong>&gt;</code>
  </div>
  <p>This labels the text box with the "Name" text in the table header. This <code>aria-labelledby</code> attribute could be added to all three Name fields, thus properly labeling all of them with one text item.</p>
  <p>Building on this example, the table below has visual labels along the top and side - multiple visual labels for each control.</p>
  <table>
    <tbody>
      <tr>
        <th scope="col">Name</th>
        <th id="officenum" scope="col">Office Number</th>
        <th id="phonelabel" scope="col">Phone</th>
      </tr>
      <tr>
        <th id="cyndi" scope="col">Cyndi</th>
        <td><input type="text" size="4" name="office1" aria-labelledby="cyndi officenum"></td>
        <td><input type="text" size="12" name="phone1" aria-labelledby="cyndi phonelabel"></td>
      </tr>
      <tr>
        <th id="jared" scope="col">Jared</th>
        <td><input type="text" size="4" name="office2" aria-labelledby="jared officenum"></td>
        <td><input type="text" size="12" name="phone2" aria-labelledby="jared phonelabel"></td>
      </tr>
      <tr>
        <th id="jon" scope="col">Jonathan</th>
        <td><input type="text" size="4" name="office3" aria-labelledby="jon officenum"></td>
        <td><input type="text" size="12" name="phone3" aria-labelledby="jon phonelabel"></td>
      </tr>
    </tbody>
  </table>
  <p>The HTML for the first field in this table is:</p>
  <div class="programlisting">
    <code>&lt;input type="text" name="office1" <strong>aria-labelledby="cyndi officenum"</strong>&gt;</code>
  </div>
  <p>The <code>cyndi</code> and <code>officenum</code> values reference the <code>id</code>s of the "Cyndi" and "Office Number" table cells. A screen reader will read "Cyndi Office Number" when navigating into this field. The reading order of multiple labels is based on the order in which these values are specified.</p>
  <div class="note">
    <div class="title">Note</div>
    <p>As a general rule, if a single label is present for a single control, the <code>&lt;label&gt;</code> element should be used to reference it. These labels provide additional functionality - clicking on them sets focus to or activates the control. This is not available when using <code>aria-labelledby</code>.</p>
  </div>
  <div class="important">
    <div class="title">Important!</div>
    <p>If a control has both an associated <code>&lt;label&gt;</code> <strong>and</strong> <code>aria-labelledby</code>, the referenced <code>aria-labelledby</code> text will override and be read of <em>instead of</em> the associated <code>&lt;label&gt;</code>.</p>
  </div>
</div>
<div class="section" id="describedby">
  <h2><code>aria-describedby</code></h2>
  <p>There are times when a form includes information that isn't exactly a label but is important enough to be read by a screen reader when navigating to the form control. This additional information can be associated to the form field with the <code>aria-describedby</code> attribute. For example:</p>
  <p>
    <label for="resetpass">Reset Password:</label>
    <input type="password" name="resetpass" id="resetpass" aria-describedby="newpass">
    <br>
    <span id="newpass">New password must be 8-15 characters and include letters and numbers</span>
  </p>
  <p>Here is the HTML:</p>
  <div class="programlisting">
    <code>
    &lt;label for="resetpass"&gt;Reset Password:&lt;/label&gt;<br>
    &lt;input type="password" name="resetpass" id="resetpass" <strong>aria-describedby="newpass"</strong>&gt; <br>
    &lt;br&gt;<br>
    &lt;span <strong>id="newpass"</strong>&gt;New password must be 8-15 characters and include letters and numbers&lt;/span&gt;	</code>
  </div>
  <p>Because there is a single label, <code>&lt;label&gt;</code> is used rather than <code>aria-labelledby</code>. As with <code>aria-labelledby</code>, the <code>aria-describedby</code> attribute points to the <code>id</code> of the element that contains the password requirements. A screen reader would read both the associated label(s) and then the associated description(s). Descriptions are sometimes read after a short pause. <code>aria-describedby</code> can also reference multiple elements - just separate the referenced <code>id</code> values with spaces.</p>
  <div class="note">
    <div class="title">Note</div>
    <ul>
      <li>While the <code>aria-labelledby</code> overrides the <code>&lt;label&gt;</code>, <code>aria-describedby</code> does not. This means that <code>aria-describedby</code> should only be used <em>in addition to a label</em> (e.g., <code>&lt;label&gt;</code> or &lt;input <code>aria-labelledby</code>&gt;), not in place of one.</li>
      <li>The <code>aria-describedby</code> attribute can also be used to reference descriptions that appear as 'tooltips'. Tooltips should become visible to sighted keyboard users when the control has keyboard focus, not just when the user hovers or clicks with a mouse.</li>
    </ul>
  </div>
</div>
<div class="section" id="invisible">
  <h2>Invisible Labels</h2>
  <p>There are times when a text label for a form control does not make sense visually. The most common example is the "Search" field. Its location within the page, in conjunction with the Search button, makes its purpose clear to sighted users. Adding a visual text label would be overkill and could negatively impact the site design. </p>
  <p> One of the following three techniques should be used when a visible label is not available:</p>
  <div class="section" id="hiddenlabel">
    <h3>Hidden <code>&lt;label&gt;</code></h3>
    <p>Hide the <code>&lt;label&gt;</code> element off-screen using CSS. The label will not appear visually, but will still be read by a screen reader.</p>
    <p>
      <label class="hidden" for="s">Search Terms</label>
      <input id="s" type="text" name="search">
      <button>Search</button>
    </p>
    <p> Here is the HTML for the label and form control:</p>
    <div class="programlisting">
      <code>
      &lt;label <strong>class="hidden"</strong> for="s"&gt;Search Terms&lt;/label&gt;<br>
      &lt;input type="text" id="s" name="s"&gt;</code>
    </div>
    <p>The CSS that is used to hide the label, and additional information about this technique, is outlined in our article on <a href="http://webaim.org/techniques/css/invisiblecontent/">invisible content for screen readers</a>.</p>
  </div>
  <div class="section" id="title">
    <h3><code>title</code> attribute</h3>
    <p>If a form field has a <code>title</code> attribute, but no <code>&lt;label&gt;</code>, the screen reader will read the <code>title</code> as if it were a label.</p>
    <p>
      <input id="s-2" type="text" name="s-2" title="Search Terms">
      <button>Search</button>
    </p>
    <p> Here is the HTML for the form control:</p>
    <div class="programlisting">
      <code>
      &lt;input id="s" type="text" name="s" <strong>title="Search Terms"</strong>&gt;
      </code>
    </div>
    <p>This technique will also cause a tooltip to appear when the user hovers over the field with a mouse, which could be distracting for some users. </p>
  </div>
  <div class="section" id="arialabel">
    <h3><code>aria-label</code></h3>
    <p>The <code>aria-label</code> attribute can also be used when there is no text label on the page.</p>
    <p>
      <input id="s-3" type="text" name="s-3" aria-label="Search Terms">
      <button>Search</button>
    </p>
    <div class="programlisting">
      <code>
      &lt;input id="s" type="text" name="s" <strong>aria-label="Search Terms"</strong>&gt;
      </code>
    </div>
    <p>Unlike <code>aria-labelledby</code> which must reference another element, <code>aria-label</code> contains the label text directly. As with <code>aria-labelledby</code>, <code>aria-label</code> will override any associated <code>&lt;label&gt;</code> elements.</p>
    <div class="important">
      <div class="title">Important</div>
      <ul>
        <li>Only one of these recommendations should be implemented. Using two or more together (e.g., a hidden <code>&lt;label&gt;</code> and a duplicate <code>title</code> attribute) can cause information to be repeated by a screen reader. </li>
        <li>Placeholder text (e.g., <code>&lt;input type="text" <strong>placeholder="Search WebAIM"</strong>&gt;</code>) is not a suitable label and should never be used in place of the above techniques.</li>
      </ul>
    </div>
  </div>
</div>
<div class="section" id="recap">
  <h2>Recap</h2>
  <ul>
    <li>Use <code>&lt;label&gt;</code> element when you can. It has excellent browser and screen reader support, and users can click on the label to select the associated form control.</li>
    <li>Use <code>aria-labelledby</code> to overcome the 1:1 limitations of <code>&lt;label&gt;</code>.</li>
    <li>Use <code>aria-describedby</code> <strong>in addition to a label</strong> when you need to associate descriptive text to the form control.</li>
    <li>Use a hidden <code>&lt;label&gt;</code> <strong>or</strong> <code>title</code> <strong>or</strong> <code>aria-label</code> when a visible text label is not available.</li>
  </ul>
</div>