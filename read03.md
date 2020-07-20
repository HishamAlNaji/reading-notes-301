# Javascript Templating

- **JS Templating:  
 a technique used to render client-side view templates (which are HTML markup, with added templating tags) with JS by using a JSON data source**

- **Template Engine:  
replaces variables and instances declared in a template file with actual values at runtime, and convert the template into an HTML file sent to the client**

- **Mustache:**
  - **a template syntax that can be used for anything (HTML, config files, source code ...)**
  - **works by expanding tags in a template using values provided in a hash or object**
  -  **often referred to as “logic-less” because it doesn't use if statements, else clauses, or for loops**

- **mustache.js:**
  - **an implementation of the mustache template system in JavaScript, and it is the base for JS templating**
  - **syntax: `{{placeholder}}`**

- **mustache-express:**
  - **to use mustache with Node and Express**
  - **syntax: `res.render(template-file-name, JSON-data)`**

----------------------

# Flexbox

## Flexbox Layout

- **Flexbox Layout provides a way to lay out, align and distribute space among items in a container efficiently, even when their sizes are dynamic**

- **It gives the container the ability to alter its items’ width/height (and order) to best fill the available space**

- **Flexbox layout is more flexible that other layouts because it's independent of direction (vertical-base and horizontal-base)**

- **Flexbox layout is most appropriate for small-scale layouts, while Grid layout is for large-scale layouts**

## Flexbox Basics

- **Flexbox is a CSS module including a set of properties**

- **_flex container_ is a parent element, which the flebox properties are set on**

- **_flex items_ are children elements which flexbox properties are set on**

- **flex layout is based on _flex-flow directions_, rather than on block and inline flow directions as regular layout**

![flexbox-layout](https://css-tricks.com/wp-content/uploads/2018/11/00-basic-terminology.svg)


 ### Properties used with the flex container:
 
- display
- flex-direction
- flex-wrap
- flex-flow
- align-content
- align-items

### Properties used with the flex items:

- order
- flex-grow
- flex-shrink
- flex-basis
- flex
- align-self and information about each one
