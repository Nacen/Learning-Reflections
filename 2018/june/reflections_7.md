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

syntax example 
```
<audio id="meowClip" controls>
<source src="audio/meow.mp3" type="audio/mpeg" />
<source src="audio/meow.ogg" type="audio/ogg" />
</audio>
```

#### figure 
- wrap visual representation(image, diagram, chart) along with its caption

syntax example
```
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

syntax example
```
<form>
<label for="name">Name:</label>
<input type="text" id="name" name="name">
</form>
```

#### fieldset 
- surrounds the entire group of radio buttons 
- which is better than using label for each one of them
- used a legend tag to provide a description for the grouping

syntax example
```
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

