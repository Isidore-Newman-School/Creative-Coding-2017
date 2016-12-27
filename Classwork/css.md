# CSS Cheat Sheet

Cascading Style Sheet (CSS) is a way to easily add style to HTML elements. For example, to add padding to the body and set the style for all header elements and paragraphs in our index.html:

```css
body {
  padding: 10px;
}
h1 {
  color: blue;
  font-family: verdana;
  font-size: 300%;
}
p  {
  color: red;
  font-family: courier;
  font-size: 160%;
}
```


## Where to include it?
#### Embed in ```<head>```
```html
<head>
  <style type="text/css">
    h1 {
      color: #36CFFF;
    }
  </style>
</head>
```

#### Link to external
```html
<head>
  <link rel="stylesheet" type="text/css" href="PATH TO CSS FILE HERE" />
</head>
```

#### Inline
```html
<p  style="color: #36C">my paragraph</p>
```

## Text Styles
* **text-align:** left;	Horizontal Alignment - left | center | right
* **text-decoration:** underline;	Text Decorations - eg. none | underline | line-through
* **font-family:** fontname;	Font Face (Typeface) - eg. Verdana, Arial, Helvetica
* **font-size:** 16pt;	Font Size or Height - eg. 12pt | 15px
* **font-weight:** bold;	Font Weight (Boldness) - eg. bold | normal | 200

## Size and Layout
* **width:** 400px;	Width of HTML element - eg. 100px | 50%
* **height:** 100%;	Height of HTML element - eg. 20px | 100%
* **margin:** 5px;	Margin - space around an element, or distance between two elements
  * margin-top: 1px;	Top Margin.
  * margin-bottom: 1px;
  * margin-left: 1px;
  * margin-right: 1px;
* **padding:** 5px;	Padding - distance between an elements contents and its border
  * padding-top: 1px;	Top Padding. Also try -bottom: -left: or -right:

## Colors & Borders
* **color:** red;	Element Colour - eg. red | #FF0000
* **background-color:** white;	Background Colour of element
* **background-image:** url(image.gif);	Background Colour of element
* **border-color:** yellow;	Border Colour of element
* **border:** 1px solid blue;	Width, style and colour of border defined together

## CSS Lists
* **list-style:** none;	Clear existing bullet types set by html list tags
