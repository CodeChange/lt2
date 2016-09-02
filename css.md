# [HTML Introductory Course](https://github.com/ScriptSmith/lt2/blob/master/html.md)

[DOWNLOAD](https://github.com/ScriptSmith/lt2/archive/master.zip)
## CSS

CSS Stands for Cascading Style Sheet. The term 'Cascading' refers to the priority of the styles being applied.

Here is an example of the contents of a typical CSS file
```css

body {
    font: 100% Lucida Sans, Verdana;
    margin: 20px;
    line-height: 26px;
}

.container {
    xmin-width: 900px;
}
```

CSS files are made up of CSS rules. CSS rules are made up of selectors, properties and values.

```css
p {
    font-size: 16pt;
}
```

`p` is the selector

`font-size` is the property

`16pt` is the value

Have a look at the CSS of a website you often visit

### Block and inline elements
Block elements like `<h1>` , `<p>` , `<ul>` , and `<li>` always appear on the page as a new line.

Inline elements like `<a>` , `<b>` , `<em>` , and `<img>` always appear on the page on the same line.

### DIVs and SPANs

You can group elements of HTML that you want to apply the same style to by closing them in `<div>` or `<span>` tags depending on whether you want to group as a block or inline respectively.

```html
<div>
    <h1>Title</h1>
    <p>Paragraph 1</p>
    <p>Paragraph 2</p>
</div>
```

### Applying CSS
You can apply CSS to specific sections of the document by defining classes and IDs. Classes apply CSS to many elements of an html document, and IDs apply CSS to just one:

```css
.news {
    font-weight: bold;
    font-family: serif;
}

#headline {
    font-size: 25pt;
}
```

```html
<h1 id="headline">BIG NEWS</h1>
<p class="news">Details, details, details, details, details, details, details, details.</p>
<p class="news">Details, details, details, details, details, details, details, details.</p>
<p class="news">Details, details, details, details, details, details, details, details.</p>
<p class="news">Details, details, details, details, details, details, details, details.</p>
```

[DEMO](https://jsfiddle.net/ff9tL9xk/)

Inside your html document, you can apply CSS internally

```html
<style>
    body: {
        background-color: red;
    }
</style>
```

Or externally

```html
<link href="css/styles.css" type="text/css" rel="stylesheet" />
```

### [Demonstration](http://www.w3schools.com/css/demo_default.htm)
The following page exhibits the power that CSS has to change the look and feel of a website.
<hr>
<iframe style="width:90%;height:600px;background:#ffffff;border:none;" src="http://www.w3schools.com/css/demo_default.htm"></iframe>
<hr>

### Selectors
There are many types of selectors in CSS, w3schools provides a good reference

[Selector Reference](http://www.w3schools.com/cssref/css_selectors.asp)

### Cascading
Always remember that if there are two rules for a particular selector, the one that appears last in the document will take precedence.

If you need to override that rule, you can add `!important` after any property value

```css
p {
    background-color: blue !important;
}
```

### Colours in CSS

In this demonstration, we've already been changing the color of elements using names like `red` and `blue`, but how can you be more specific about your colour choices?

Lets have a look at a 'colour picker' to see what options are availabile to us.

[LINK](http://www.colorpicker.com/)

#### RGB
RGB stands for Red-Green-Blue. `rgb(x,y,z)` tells the browser to render a colour with `X` Red, `Y` Green, and `Z` Blue

#### Hex
Hex codes do the same in a shorter format.

```css
body {
    background-color: rgb(46, 145, 179);
}
```

Is the same as

```css
body {
    background-color: #2E91B3;
}
```

#### Names
And of course, you can specify colours using their names.

[LINK](http://www.w3schools.com/colors/colors_names.asp)

#### Opacity
You can make html elements more opaque on screen by changing a colour's opacity.

```css
p {
    background-color: rgb(46, 145, 179);
    opacity: 0.5;
}
```

```css
p {
    background-color: rgb(46, 145, 179, 0.5);
}
```

### Text
There are a number of properties of text that you can change with css

#### Font family

```css
.demonstration {
    font-family: Georgia, Times, serif;
}
```

```html
<p class="demonstration">
    Hello there
</p>
```

<style>
.demonstration {
    font-family: Georgia, Times, serif;
}
</style>

<hr>
<p class="demonstration">
Hello there
</p>
<hr>

#### Font size
##### Pixels

```css
.demonstration {
    font-size: 14px;
}
```
This is exactly 14 pixels tall
#### Percentage

```css
.demonstration {
    font-size: 50%;
}
```
This is half the normal size
#### EM
Relative to the current element's size

```css
.demonstration {
    font-size: 3em;
}
```

That is three times the normal size

#### Font weight
To make text bold, use `font-weight`

```css
.demonstration {
    font-weight: bold;
}
```

#### Font style
To make text italic, use `font-style`

```css
.demonstration {
    font-style: italic;
}
```

#### Text alignment
`text-align` changes the alignment of text on the horizontal axis.
```css
.demonstration {
    text-align: center;
}
.demonstration {
    text-align: left;
}
.demonstration {
    text-align: right;
}
```

#### Text Decoration
Text decoration controls the additional styling of text like adding underlines.

Removing underlines from links
```css
a {
    text-decoration: none;
}
```

```css
a {
    text-decoration: line-through;
}
a {
    text-decoration: overline;
}
a {
    text-decoration: underline;
}
```
#### Misc
w3schools covers the rest of the text-styling options [here](http://www.w3schools.com/css/css_text.asp)

### Boxes
Here's a box demonstration:

```html
<div>
	 <p>The Moog company pioneered the commercial
		 manufacture of modular voltage-controlled
		 analog synthesizer systems in the early
		 1950s.</p>
</div>
```

```css
.box {
    margin: 0;
    padding: 0;
    height: 300px;
    width: 300px;
    background-color: #bbbbaa;
}
.box p {
    margin: 0;
    padding: 0;
    height: 75%;
    width: 75%;
    background-color: #0088dd;
}
```

```html
<style>
.box {
    margin: 0;
    padding: 0;
    height: 250px;
    width: 250px;
    background-color: yellow;
}
.box p {
    margin: 0;
    padding: 0;
    height: 75%;
    width: 75%;
    background-color: blue;
}
</style>     

<div class="box">
	 <p>
        This is some dummy text...
     </p>
</div>
```

w3schools explains how the box model works visually [here](http://www.w3schools.com/css/css_boxmodel.asp)

You can override box sizes with `height` and `width`, and by default a box is just large enough for its contents.

#### Min and Max width
When designing for interfaces that change in size (like a web browser), we can use `min` and `max`

Here is a demonstration:

```html
<style>
div.norm {
    width:600px;
    border: 3px solid red;
}

div.max {
    max-600px:350px;
    border: 3px solid red;
}
</style>
</head>
<body>

<div class="norm">Normal width</div>
<br>

<div class="max">Max width</div>
```

#### Overflow
When we have lots of text in  a fixed space, we can make the content fit using Overflow
```html
<style>
div.norm {
    width:600px;
    height:100px;
    border: 3px solid red;
    overflow: scroll; /*or hidden*/
}

div.max {
    max-600px:350px;
    border: 3px solid red;
}
</style>
</head>
<body>

<div class="norm">Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width Normal width </div>
<br>

<div class="max">Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width Max width </div>
```

#### Borders
There are lots of styles that can apply to borders, w3schools lists them briefly [here](http://www.w3schools.com/css/css_border.asp)

#### Centering
To center a box, set the margins to auto.
```css
p{
    margin: 5px auto 5px auto;
}
```
For a full reference of center-styling, see css-tricks's guide [here](https://css-tricks.com/centering-css-complete-guide/)

### Positioning
There are four types of positions:
* [Static](http://www.w3schools.com/css/tryit.asp?filename=trycss_position_static)
* [Fixed](http://www.w3schools.com/css/tryit.asp?filename=trycss_position_fixed)
* [Relative](http://www.w3schools.com/css/tryit.asp?filename=trycss_position_relative)
* [Absolute](http://www.w3schools.com/css/tryit.asp?filename=trycss_position_absolute)

When elements are overlapping, you can layer them by adjusting the `z-index` property.


## Additional Functionality
### Embedding youtube videos
```html
<iframe width="560" height="315" src="https://www.youtube.com/embed/s86-Z-CbaHA" frameborder="0" allowfullscreen></iframe>
```
<hr>
<iframe width="560" height="315" src="https://www.youtube.com/embed/s86-Z-CbaHA" frameborder="0" allowfullscreen></iframe>
<hr>

### Google maps
```html
<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3539.935879355097!2d153.01582491527873!3d-27.471255523346525!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x6b915a07b67caa5f%3A0xfc22e8caf1f501ae!2sState+Library+of+Queensland!5e0!3m2!1sen!2sau!4v1469337465617" width="600" height="450" frameborder="0" style="border:0" allowfullscreen></iframe>
```
<hr>
<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3539.935879355097!2d153.01582491527873!3d-27.471255523346525!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x6b915a07b67caa5f%3A0xfc22e8caf1f501ae!2sState+Library+of+Queensland!5e0!3m2!1sen!2sau!4v1469337465617" width="600" height="450" frameborder="0" style="border:0" allowfullscreen></iframe>
<hr>


## Projects
### Project 2 - From scratch
Now try to make the same personal site using your own stying. You can refer to the [CSS reference](css.pdf) or [w3Schools](http://www.w3schools.com/css/) if you need help or ideas.

Start with this structure:

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title></title>
    </head>
    <body>

    </body>
</html>
```

## Further reading
[Code Changers](codechangers.slack.com)

* [w3Schools HTML](http://w3schools.com/html)
* [w3Schools CSS](http://www.w3schools.com/css/)
* [w3Schools Bootstrap](http://www.w3schools.com/bootstrap)
* [w3schools Javascript](http://www.w3schools.com/js/default.asp)
