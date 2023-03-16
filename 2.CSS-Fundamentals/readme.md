# Adding CSS to the basic HTML page

Modified the basic layout of an HTML page using some basic CSS concept.

## Key learnings:

CSS stands for Cascading Style Sheet and is used to add styles or to design an HTML page.

CSS can be added to an HTML page in mainly 3 ways:

1. Inline CSS - In this method we add CSS using a style attribute to the element that needs to be styled. <br></br>

2. Internal CS - In this method, we write CSS in the Head tag of the HTML page. We write CSS between Style tags on the HTML page that needs styling. <br></br>

3. External CSS - Just like we create an HTML page, we can create a page for adding design also. This page ends with an extension, '.css' -- Usually 'style.css'. We then link this page to our HTML page using the link element in the head of an HTML page.

---

Learnt about the various properties to add style to text, like - font-size, font-weight, text-transform,font-style, line-height, letter-spacing etc.

---

Learnt about the structure of writing a CSS declaration block. A declaration block is a collection of key/ property - value pair arranged in sequence inside curly braces - '{}'.

Eg: {font-size: 14px;}

Learnt about different types of selectors:-

1. Element Selectors - We can use elements like p, h1, h2, div etc. to style these respective elements. In such cases, the selector is called an element selector.

   - When more than 2 elements are seperated by commas (,), it implies that all the elements selected are being targeted.<br></br>

2. Descendant Selectors - As the name suggests we can combine selectors in a way such as to target the descendant(s) of an element. When 2 elements are written with a space in between, it implies that the second element is being targetted and it is the descendant of the first.

   - Nested Descendant Selectors - When we use three (or more) elements seperated by space, it means that the third (or the last) element is being targeted and is the grandchild of the first. i.e, it is a nested descendant. <br></br>

3. ID and Class Selectors: We can use ids and classes to target and style particular sections of an HTML page. Ids and Classes are nothing but attributes that can give certain characteristics to the elements. Ids are unique to an element, whereas classes are common attributes that can be shared by multiple elements. The most common practice is to however use Class selectors in most of the cases. <br></br>

> 💡 When a Selector and a Declaration block combine together, this is called a CSS Rule-Set. This is how every CSS is written. <br></br>Eg of a CSS Rule-set: p {font-size: 14px;}

---

Learnt about RGB and Hexadecimal Notations - In CSS, colors is of utmost importance. We can assign a color property to almost any element. There are many ways to assign a particular color to an element and hence it is important to understand some of the basic principles:

1. RGB and RGBA - Stands for Red, Green, Blue and Alpha. The values for each component can vary from 0 to 255.

   For Eg: - rgb(0,0,0); denotes the color black since it denotes the absence of any value in either three colors.

   rgb(255,255,255); denotes white as it denotes the presense of all the maximum possible values for all the three colors.

   The permutations and combinations of values between 0 to 255 creates a plethora of possible colors.

   A or Alpha denotes transperancy.

   All these values can be adjusted by hovering on top of the rgb values and by using a color picker that most of the code editors provide by default.
   <br></br>

2. Hexadecimal Notations - Instead of using a scale from 0 to 255, we use a scale from 0 to f. It is 6 letters followed by a # symbol. Yet to learn in detail about this.

   In short colors can be denoted as a bunch of numbers.
   <br></br>

> 💡If the values one each channel (R, G and B) are a same number, we get some shade of gray. It is a continuum from black to white, from rgb(0,0,0) to rgb(255, 255, 255)

---

Learnt about Inheritance. This is a CSS concept using which some of the property of the a parent element is inherited by their child elements.

Mostly, it is observed that the properties related to text are inherited. Eg: font-size, font-family, color etc.

> 💡It is key to note that even if some properties of th parent elements are inherited by their child elements, we can change their behaviour and style them uniquely by specifically targetting the elements.

---

Learnt about Universal Selector. A Universal Selector is denoted by an asterisk (\*) and denotes everything in the HTML page. It selects all the elements.

We commonly use the Universal selector to reset the margin and padding of all the elements to 0 and then provide custom values based on our design needs.

> 💡It is important to note the key difference between a Universal Selector and a Body selector. A universal Selector targets/ selects each and every element, whereas by using a 'body' selector, we treat the whole body as a single element. <br></br> Whatever property-value we apply using the 'body' selector is applied to the body and NOT to all the individula elemets. Some properties set to the 'body' can be inherited by its children. However, this can always be changed by writing specific CSS for the child elements.

---

Learnt about CSS box-model. This is one of the core concepts of CSS. Every element in CSS is considered to be a box. The box can be surrounded by border, padding and margin. These are the concepts that are crucial in calculating dimensions like the height and width of each element.

The outer boundary of the element is its border. We can customise the thickness, style and colour of this border.

The area from the border towards the content of an element is called its padding. This can also be customised as per our style requirements.

The area from the border towards outside of the element is called its margin. The dimensions can be customised. Usually, margins are used to allocate spaces between two elements.

> 💡Final Element Width = left border + left padding + content width + right padding + right border <br> <br> Final Element Height = top border + top padding + content height + bottom padding +bottom border

There are 3 different 'types' of boxes/ elements:-

1. Block Level Elements (Block Level Boxes): They take up the entire row (100%) of the screen. This is their default width. The width, margin, and padding can be adjusted. They can be visualised as being stacked up one over the other. The box-model applies.
   Eg: h1, p, div, section, etc.

2. Inline elements - The default width of these elements is only as much as its content. <em>The height and width property doesn't apply to these elements. Padings and Margins can be applied horizontally.</em> <br>

> 💡An inline element can be converted into a block level element by setting display: block; All the box properties like margin, padding, height and width will then work fine.

3. Inline-block elements - These elements have a mix of both inline and block level elements. They appear inline, but carries the functionalities of a block level element, i.e, the box model applies like in the block-level elements.

---

<br>
Margin Collapse - When two adjacent elements share a margin,  the margin value that is greater of the both is the effective margin between the two elements. This is called Margin collapse.

---

Learnt about Absolute Position: The normal document flow of an HTML page is based on the display type of the element. They are either stacked as blocks or arranged side by side other elements (in case of inline elements).

When we set the CSS property of an element to, position: absolute; , this removes the element from the regular 'flow' of the document. We can then set their positions using properties like 'top', 'bottom', 'left' and 'right'.

Using these, the position of an element can be adjusted in relation to the closest parent element whose position is relative.

---

Learnt about pseudo-elements. Pseudo elements are elements that are not really present in the HTML but can be inserted in the DOM using CSS.

Eg-

::after - used to add content after an element.

:: before - used to add content before an element

::first-letter - modifies the first letter of an element

::last-letter - modifies last letter of an element

::first-line - modifies first line of an element

::last-line - modifies last line of an element

Learnt about pseudo-classes. Pseudo-classes are classes that are added using CSS to manipulate some of the behaviour of the HTML elements.

Eg:-

:hover - can be used to customize the hover state

:first-child - can be used to target the first child of an element

:nth child() - can be used to target various elements based on a given formula inside the paranthesis

---
