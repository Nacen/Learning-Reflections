# May 22 Reflections

## Full Stack Dev Courses

### Use Dev Tools to Debug/Make Experimental Changes to your website

media queries most used often for min width and max width are the most commonly used for responsive design

Media Queries are your friends for making responsive website

@media screen and (min-width: 300px) and (max-width: 600px)
breakpoints in responsiveness refers to how a website should be seen on devices when the screen size gets larger and larger to make the website more responsive or fit to it

* grid fluid system bootstrap uses this system

* Flexbox for layout great general strategy for responsive design
    display: flex;
    flex-wrap: wrap;
    flex item: changing the order of elements using the css order attrib
 example of a flex item   -> @media screen and (min-width:700px) {
        .dark_blue {order: 4;}
        .light_blue {order: 5;}
        .green {order: 2;}
        .orange {order: 3;}
        .red {order: 1;}
    }

### common responsive patterns

* Column Drop

.container {
    display: flex;
    flex-wrap: wrap;
}

.box {
    width:100%
}

@media screen and (min-width: 450px) {
    .darkblue {
        width:25%;
    }
    .lightblue {
        width:75%
    }
}

@media screen and (min-width: 550px) {
    .darkblue .green {
        width:25%;
    }
    .lightblue {
        width:50%
    }
}

* Mostly Fluid

@media screen and (min-width: 450px) {
    .darkblue .green{
        width:50%;
    }
}

@media screen and (min-width: 550px) {
    .darkblue .green {
        width:50%;
    }
    .lightblue .orange .red{
        width:33%
    }
}

@media screen and (min-width: 550px) {
    .container {
        width: 700px
        margin-left: auto;
        margin-right: auto;
    }
}

* Layout Shifter

uses order to shift the elements on the website

* Off Canvas

off canvas use hamburger for less frequently used content offscreen only showing them if the screen is large enough
hamburger icon for a nav bar

## Learn Fun

* Have Fun while learning is the best possible way to learn it sticks in to your brain easier

* Learn With a smile

* Tell yourself be active not passive

* Be Active enough that it being active is passive for you in the long run

### Responsiveness Optimizations

* Images

With Images almost taking 60% of data in our websites we really need to consider images on how it is represented on the screen as being part of responsiveness

use source-set, art direction

* Responsive Tables

Consider transforming a table into a list when the viewport is too small for the table
or make the table scrollable by putting it into a DIV and setting it to a width:100% and overflow-x: auto

* Fonts