# Responsive Web Design

**Responsive web design (RWD) is the practice of building a website that is suitable for all users, such that it works on all devices with any screen size, for both mobile and desktop, changing layout and content along the way.**

## Responsive vs Adaptive vs Mobile

- Responsive generally means to react quickly and positively to any change
  -  continually and fluidly change based on different factors, such as viewport width
- Adaptive means to be easily modified for a new purpose or situation, such as change
  - respond to preset factors
- Mobile means  to build a separate website only for mobile users

## components of RWD:
1. flexible layouts
1. media queries
1. flexible media

### Flexible Layout
**Flexible layouts are used to make the website dynamically resize to any width**

- building the website layout with a flexible grid, using **relative length units** (percentages or em units) instead of fixed measurement units (pixels or inches)
- relative lengths are then used to declare common grid property values such as width, margin, or padding

 ___
#### Relative Viewport Lengths:  
relative length units, specifically related to the viewport size of the browser or device

| `vw`            | `vh`             | `vmin`                              | `vmax`                              |
| --------------- | ---------------- | ----------------------------------- | ----------------------------------- |
| Viewports width | Viewports height | viewport’s minimum height and width | viewport’s maximum height and width |

___
#### Proportions of a Flexible Layout Formula (using relative values):

- taking the target property value of an element
- dividing it by the width of it’s parent element
- the result is the relative property value of the target element

      target ÷ context = result

___

### Media Queries
**Media queries are used when the width of a browser viewport is so small that even scaling the the layout proportionally doesn't work properly**

 - apply targeted styles - specify different styles for individual browser and device circumstances
 (i.e. width of the viewport, device orientation)

___
#### The Mobile First Approach
using styles targeted at smaller viewports as the default styles for a website, then use media queries to add styles as the viewport grows
___

### Flexible Media
**Flexible media is used for images, videos, and other media types that need to be scalable, changing their size as the size of the viewport changes** 

- using the max-width property with a value of 100%

------------------------------------------------------------------------

# CSS Flaots

- `float` is a CSS positioning property used for elements to remain a part of the flow of the web page (other elements wrap around floated elements)
- `float` property takes 4 values:
  1. left
  1. right
  1. none
  1. inherent
- floats can be used to wrap text around images, or create entire web layouts or small instances layout

 ## Clearing Floats
 
- `clear` is a CSS property used usually with `float` 
- cleared elements will not wrap around floated elements, but will move down past the floated elements
- `clear` property takes 4 values:
  1. both (clears floats coming from left and right)
  1. left
  1. right
  1. none
  
## The Great Collapse
- floated elements can  affect the parent element that contains them
- if a parent element contains only floats, the height of it would collapse to nothing 
- collapsing effects problems are fixed by clearing the float **after the floated elements** in the container but **before the close of the container**

## Techniques for Clearing Floats:

1. The Empty Div Method
  `<div style="clear: both;"></div>`
1. The Overflow Method
  setting the overflow CSS property on a parent element to `auto` or `hidden`, which clears succeeding elements and the parent will expand to contain the floats
1. The Easy Clearing Method
  using the CSS pseudo selector `:after` to clear floats

## Problems with Floats:

1. Pushdown
1. Double Margin Bug
1. Bottom Margin Bug