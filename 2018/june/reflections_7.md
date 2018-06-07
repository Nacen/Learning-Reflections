# Reflections

## Web Development

### Applied Accessibility

Semantic HTML

Tags used around content indicates the type of information it contains

e.g a header contains the heading content

#### HTML5
Introduced a number of new elements that gives developer more options while also incorporating accessibility features 

These are main, header, footer, nav, article and section among others

Before we used div to wrap up our elements in place but using the elements mentioned above we can indicate the type of information the content will have

Assistive Technologies can access this info to provide better page summary or navigation options to their users  

tags and their used \

#### main 
- used to wrap the main content and there should only be one per page

#### article 
- sectioning element to wrap independent self contained content

#### section
- for standalone content is for grouping thematically related content

For example, if a book is the article, then each chapter is a section. 

When there's no relationship between groups of content, then use a div.

div - groups content \
section - groups related content \
article - groups independent, self-contained content

#### header
- used to wrap introductory info or navigation links for its parent tag
- header and head are different header is for the body while head contains meta info

#### nav 
- wrap around the main navigation links in the page

#### audio
- gives semantic meaning when it wraps sound or audio stream content
- Also needs text alternative to the deaf or hard of hearing can be done by using a nearby text or a link to a transcript
- also supports controls attribute which shows default play, pause and other controls

 
```
Example

<audio id="meowClip" controls>
<source src="audio/meow.mp3" type="audio/mpeg" />
<source src="audio/meow.ogg" type="audio/ogg" />
</audio>
```

#### figure 
- wrap visual representation(image, diagram, chart) along with its caption

 
```
Example
<figure>
<img src="roundhouseDestruction.jpeg" alt="Photo of Camper Cat executing a roundhouse kick">
<br>
<figcaption>
Master Camper Cat demonstrates proper form of a roundhouse kick.
</figcaption>
</figure>
```

#### label
- wrap text for a specific form control item
- this ties meaning to the item and makes the form more readable
- value of for attribute must be the same as the value of id attribute of the form control


```
Example
<form>
<label for="name">Name:</label>
<input type="text" id="name" name="name">
</form>
```

#### fieldset 
- surrounds the entire group of radio buttons 
- which is better than using label for each one of them
- used a legend tag to provide a description for the grouping


```
Example:

<form>
<fieldset>
<legend>Choose one of these three items:</legend>
<input id="one" type="radio" name="items" value="one">
<label for="one">Choice One</label><br>
<input id="two" type="radio" name="items" value="two">
<label for="two">Choice Two</label><br>
<input id="three" type="radio" name="items" value="three">
<label for="three">Choice Three</label>
</fieldset>
</form>
```

#### Links Navigatable with HTML Access Keys
- HTML offers access keys attribute to specify a shortcut key to activate or bring focus to an element
- HTML5 allows this attribute to be used on any element but it's particularly useful when used with interactive ones. e.g links, button and form controls

```
Example: 
<button accesskey="b">Important Button</button>

```

#### Give Links Meaning by using Descriptive Link Text

instead of having a link text with click here or read more links isn't helpful 

use a brief but descriptive text within the anchor tags
example
```
    Click here for information about batteries
    instead of a click here <a> tag 
```

#### Tab Index to add Keyboard Focus to an element

Has three distinct functions relating to an element's keyboard focus. 

- Tag indicates that element can be focused on
- The value(an integer that's positive, negative or zero) determines the behavior

Certain elements, such as links and form controls, automatically receive keyboard focus when a user tabs through a page. It's in the same order as the elements come in the HTML source markup. This same functionality can be given to other elements, such as div, span, and p, by placing a tabindex="0" attribute on them. Here's an 

```
Example:
<div tabindex="0">I need keyboard focus!</div>

```
Tab index also specifies the exact tab order of elements

This is achieved when the value of the attribute is set to a positive number of 1 or higher

Setting a tabindex="1" will bring keyboard focus to that element first. Then it cycles through the sequence of specified tabindex values (2, 3, etc.), before moving to default and tabindex="0" items

Important Note

when the tab order is set this way, it overrides the default order (which uses the HTML source). This may confuse users who are expecting to start navigation from the top of the page. This technique may be necessary in some circumstances, but in terms of accessibility, take care before applying it.


### CSS

CSS can also improve accessibility on the page
when we want to visually hide content meant for screen readers


```
Example

.sr-only {
position: absolute;
left: -10000px;
width: 1px;
height: 1px;
top: auto;
overflow: hidden;
}
```

The following CSS approaches will NOT do the same thing:


display: none; or visibility: hidden; 
- hides content for everyone, including screen reader users

Zero values for pixel sizes, such as width: 0px; height: 0px; 
- removes that element from the flow of your document, meaning screen readers will ignore it

#### Improve Readability with High Contrast Text
Low contrast between the foreground and background colors can make text difficult to read. Sufficient contrast improves the readability of your content, but what exactly does "sufficient" mean?

The Web Content Accessibility Guidelines (WCAG) recommend at least a 4.5 to 1 contrast ratio for normal text. The ratio is calculated by comparing the relative luminance values of two colors. This ranges from 1:1 for the same color, or no contrast, to 21:1 for white against black, the strongest contrast. There are many contrast checking tools available online that calculate this ratio for you.

#### Avoid Colorblindness Issues by Using Sufficient Contrast

Color is a large part of visual design, but its use introduces two accessibility issues. First, color alone should not be used as the only way to convey important information because screen reader users won't see it. Second, foreground and background colors need sufficient contrast so colorblind users can distinguish them.

The WCAG-recommended contrast ratio of 4.5:1 applies for color use as well as gray-scale combinations.

#### Avoid Colorblidness Issues by Carefully Choosing Colors that Convery Information

There are various forms of colorblindness. These can range from a reduced sensitivity to a certain wavelength of light to the inability to see color at all. The most common form is a reduced sensitivity to detect greens.

For example, if two similar green colors are the foreground and background color of your content, a colorblind user may not be able to distinguish them. Close colors can be thought of as neighbors on the color wheel, and those combinations should be avoided when conveying important information.

##### Note

Some online color picking tools include visual simulations of how colors appear for different types of colorblindness. These are great resources in addition to online contrast checking calculators.
