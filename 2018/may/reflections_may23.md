# May 23 Reflections

## Responsive Website Optimization

* Fonts

Text in websites should atleast be 60 characters per line to build a thought easily and not to be awkward to read when too short or too long for readers

Font should be 14-small 16-normal 18-large
and an em size of 1.5

* Padding and Margin Difference

refer to the box model to understand more clearly and visually
the Padding is the space between the content and the border
while Margin is the space between the border and the next element
in otherwords Margin is the space between outside the border and the next element

* Minor Breakpoints

Consider having minor breakpoints when a major breakpoints is met ex.
increasing the content size a specific example is belows
increasing fonts when the 550px <- major breakpoint is met let say make it 20px

* Responsive Images

use max-width: to consider larger images
use calc when adding padding on images ex. calc((100% - 10px) / 2)
last of type selector to ensure there's only margin between the images you are adding space

Viewport Size will not always stay the same

making the image 100% in height is to use vh for viewport height
width:100vmax/100vmin;
height:100vmax/100vmin;
 It'll compress your images to squares, so be careful if you want to maintain a different aspect ratio!

 How to check if images are optimized
 use google's Pagespeed insights
 use Page insights from dev tools
 pagespeed insight api
 grunt-page speed
