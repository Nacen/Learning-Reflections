# Reflections

## Web Development

CSS will be practiced for atleast 2 weeks

### Things i learned with CSS

#### CSS Box Model

consists of three parts

* Margin
* Border
* Padding

Margin - the spacing between elements
Border - the spacing between the Margin and Padding
Padding - the spacing between the element and border

#### CSS Colors

* RGB
* RGBA
* HSL
* Hex Colors

example:

* RGB(255, 0, 0 )
* RGBA(255,0, 0, 0.2 )
* HSL(180, 100%, 50% )
* '#FFF' '#FF00FF'

RGBA - red green blue \
RGBA - red green blue alpha(dictates the opacity) \
HSL - Hue, Saturation, Light

* Hue is the color known by the people
* Saturation Dictates how many gray is in the color
* Light is how much dark or light a color is 0% is dark 50% normal color 100% is light

Hexadecimal is either '#fff' or '#00ffff'

All of the colors above are flat colors
we can also have transitional colors using Gradient

Gradient - transitional colors
using two types

* linear gradient
* repeating linear gradient

#### Texture

Texture of a background can be changed using a texture of an image

background: url(image)

#### Scaling

Scaling using Transform

transform:scale(1.5) = makes the element 1.5x larger
transform: skewX(24deg);
transform: skewY(24deg);

Opacity: is how transparent an object is \
0 full transparency
0.5 half transparency
1 no transparency

#### Graphic

before and after pseudoclass \
before adds something before the element \
after adds something after the element

Using keyframe and animation we can animate graphics in css

animation-name: colorful
animation-duration: 3s
animation-fill-mode:
animation-iteration-count:
key frames need to refer to the animation name

@keyframes colorful { \
        0% { <-- Opening Scene\
        bg blue; \
    } \
    100% { <-- Ending Scene \
    }
}



