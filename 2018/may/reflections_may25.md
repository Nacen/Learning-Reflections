# Reflections for May 25

## Lessening your HTTP REQUEST

* First

Use CSS Techniques to reduce the http request. HOW?
There are various ways to do it fonts, using different type of the image, optimizing the image.
Providing more Performant Options

* Second

Lessen Images in your websites if possible. Ask yourself if your website really need images
sometimes the best image is no image at all. Use Fonts instead

* Third

SVG and data URLS

SVG is so lightweight by using INLINE we can further more optimize it
There is also img source using DATA URLS
data URLS have more browser support up to 97%
and both can also be inlined with our CSS

### Full Responsiveness

* Using the srcset attribute

by using the srcset attribute we are letting the browser handle which image to present
we have this _1x and _2x to present the DPR(Density Pixel Ratio) different devices have different DPR
usually mobile phones with smaller screen only have 1DPR while laptops or larger screens have 2DPR
We also have the almighty w property which refers to the width of the image where we will tell the browser what is the width of the image

example below

* Reacting to Image Width

img src="image_200.jpg" srcset="image_200.jpg 200w, image_100.jpg 100w" alt="a cool image"

* Reacting to DPR(Device Pixel Ratio)

img src="image_2x.jpg" srcset="image_2x.jpg 2x, image_1x.jpg 1x" alt="a cool image"

* Image Width with sizes

srcset with sizes Syntax
Here's an example:

img src="images/great_pic_800.jpg"
        sizes="(max-width: 400px) 100vw, (min-width: 401px) 50vw"
        srcset="images/great_pic_400.jpg 400w, images/great_pic_800.jpg 800w"
        alt="great picture"

sizes consists of comma separated mediaQuery width pairs. sizes tells the browser early in the load process that the image will be displayed at some width when the mediaQuery is hit.

if sizes is missing, the browser defaults sizes to 100vw

sizes gives the browser one more piece of information to ensure that it downloads the right image file based on the eventual display width of the image. Just to be clear, it does not actually resize the image - that's what CSS does.

Art-Direction
Pixel-Display

* Picture Element

using picture tag as a scaffold for an image
example: picture

{picture
source
media="(min-width: 1024px)"
srcset="opera-fullshot.webp"
type="image/webp"

source
media="(min-width: 1024px)"
srcset="opera-fullshot.jpg">

source
srcset="opera-closeup.webp"
type="image/webp"
img src="opera-closeup.jpg" alt="The Oslo Opera House"
/picture}

* Tips

Crop Before Compressing an Image if you are considering the image responsiveness.
Use picturefill for browser that doesn't support picture
if a dpr is 2x then you should double the image width if 800px 1x then 1600px 2x