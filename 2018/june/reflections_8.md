# Reflections

## Web Development

### Responsive Web Design Principles

#### Media Query
- are new techniques introduced in CSS3 that change the presentation of content based on different viewport sizes.
- The viewport is a user's visible area of a web page, and is different depending on the device used to access the site.
- Media Queries consist of a media type, and if that media type matches the type of device the document is displayed on, the styles are applied. You can have as many selectors and styles inside your media query as you want.

```
Media Query Example that returns the content when device width
is less than or equal to 100px

@media (max-width: 100px) {/* CSS Rules */}

and the following media query returns the content when the device's height is more than or equal to 350px:

@media (min-height: 350px) { /* CSS Rules */ }
```

#### Making an Image Responsive
- Making Images responsive with CSS is actually very simple.

```
img {
    max-width: 100%;
    display: block;
    height: auto;
    margin: 0 auto;
}
```
The max-width property of 100% scales the image to fit the width of its container, but the image won't stretch wider than its original width. Setting the display property to block changes the image from an inline element (its default), to a block element on its own line. The height property of auto keeps the original aspect ratio of the image.

#### Use a Retina Image for Higher Resolution Display
- The simplest way to make your images appear "retina"(and optimize them for retina display) is to define their width and height values as only half of what the original size is.

``` 
Example: 
<style>
img { height: 250px; width: 250px; }
</style>
<img src="coolPic500x500" alt="A most excellent picture">
```

#### Make Typography Responsive
-Instead of using em or px to size text, you can use viewport units for responsive typography. Viewport units, like percentages are relative units, but they are based off different items. Viewport units are relative to the viewport dimensions(width or height) of a device, and percentages are relative to the size of the parent container element.

The four different viewport units are:
* vw: 10vw would be 10% of the viewport's width
* vh: 3vh would be 3% of the viewport's height
* vmin: 70vmin would be 70% of the viewport's smaller dimension(height vs. width).
* vmax: 100vmax would be 100% of the viewport's bigger dimension(height vs. width)

### CSS Flexbox

#### Display Flex
- Placing the CSS property ``` display: flex ``` on an element allows you to use other flex properties to build a responsive page

#### Flex-Direction
By adding display: flex to an element turns it into a flex container. This makes it possible to align any children of that element into rows or columns.

To do this by adding the ```flex-direction``` property to the parent item and setting it to row or column.

Creating a row will align the children horizontally, and creating a column will align the children vertically.

