# [HTML Introductory Course](https://github.com/ScriptSmith/codein180minutes/blob/master/html.md)
[DOWNLOAD](https://github.com/ScriptSmith/codein180minutes/archive/master.zip)
### Topics
1. Using a text editor
2. How websites work
3. What HTML is
4. An example HTML page
5. Structure of an HTML document
6. HTML Elements
   * Text
   * Lists
   * Links
   * Images
   * Tables
   * Forms
   * Applying CSS
   * Additional functionality
      * Youtube videos
      * Google maps
      * Javascript
7. Simple exercises to take home


## Using a Text Editor
The text editor we will be using is named `atom`. `atom` is an open-source program developed by [GitHub](https://github.com) that is used to edit text documents and source code. This document was written in `atom`.

You can download `atom` for your operating system by following the instructions at [atom.io](https://atom.io/).

http://flight-manual.atom.io/ is `atom`'s reference.

If you have questions, check [flight manual](http://flight-manual.atom.io/) for instructions on manipulating files, editing text, and features of the `atom` program.

Make sure that you are familiar with the following:
* Opening and saving files
* Selecting text
* Making new lines
* Indenting text
* Copying and pasting text
* Enabling code highlighting

## How websites work
When you go to `google.com`. Your browser sends a request to another computer which sends files back to you. These files are usually `HTML`, `CSS` and `JavaScript`.

* `HTML` tells your browser how the website is structured
* `CSS` tells your browser what the website will look like
* `JavasScript` tells your browser what the website will do

## What is HTML
[W3Schools](http://www.w3schools.com/hTml/html_intro.asp):

> **HTML is a markup language for describing web documents (web pages).**

> * HTML stands for Hyper Text Markup Language
> * A markup language is a set of markup tags
> * HTML documents are described by HTML tags
> * Each HTML tag describes different document content

## Example HTML page

HTML pages look something like this:

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>This is a webpage</title>
    </head>
    <body>
        <p>
        	Hello
        </p>
    </body>
</html>
```
[DEMO](https://jsfiddle.net/3xdzgjt6/) <-- Click here to see what the above code does

Try and copy this code into atom.

![](https://i.imgur.com/f6EJR1u.png)

Try editing the text and opening the file in your web browser.

When you make changes to your webpage, ensure that you save the file (`Ctrl+S`) in atom and refresh the page (`F5` or `Ctrl+R`) in your web browser.

## Structure of an HTML document

`<!DOCTYPE html>` tells your browser that the file it is about to read is an HTML file. This line is not required for a webpage to be viewed in a browser. However, it is good practice because it can be used to convey more complex information. In this case, `<!DOCTYPE html>` tells your browser that this file is written according to the most recent HTML **5** specification.

`<p>` is an example of a tag.

Tags are keywords that are used to define sections of an HTML document. Most tags have an opening tag `<p>` and a closing tag `</p>`.

Tags have attributes like `width` or `src` that describe some property of the tag.

```html
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/85/Smiley.svg/2000px-Smiley.svg.png">
```

Inside the `<html>` tag is the `<head>` tag.

```html
<html>
	<head>
    	<title>My Webpage</title>
    </head>
</html>

```
The head tag contains information about the webpage that doesn't appear within the webpage like the title, meta-information and links to code that will run inside the page.

The title tag contains the text that will appear in the title of the window of the browser.

![](https://i.imgur.com/7Drnj6b.png)

The `<body>` tag contains all the things that will appear on the webpage.

```html
<html>
	<body>
    	<p>This is a paragraph of text</p>
    </body>
</html>
```

Here is an example of a very simple webpage:
```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>My Webpage</title>
        <style>
            img {
                width: 200px;
            }
        </style>
    </head>
    <body>
        <h1>My Name</h1>
        <div id="about">
            <h2>About me</h2>
            <p>
                Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
            </p>
        </div>
        <div id="photos">
            <h2>Photos</h2>
            <table>
                <tr>
                    <td>
                        <img src="https://upload.wikimedia.org/wikipedia/commons/b/bf/Bucephala-albeola-010.jpg">
                    </td>
                    <td>
                        <img src="https://upload.wikimedia.org/wikipedia/commons/f/f2/Mallard_drake_and_blue_mood.jpg">
                    </td>
                </tr>
                <tr>
                    <td>
                        <img src="https://upload.wikimedia.org/wikipedia/commons/5/51/Mandarin.duck.arp.jpg">
                    </td>
                    <td>
                        <img src="https://upload.wikimedia.org/wikipedia/commons/a/a6/Parrulo_-Muscovy_duckling.jpg">
                    </td>
                </tr>
            </table>
        </div>
    </body>
</html>
```
[DEMO](https://jsfiddle.net/06Lzsx77/)

Copy the code into Atom, save it as a new file named `mypage.html` and try customising it.
## HTML Elements
Now that you've seen some of the things that HTML can do, lets learn about how they work.
### Text
#### Headings
HTML has 6 heading levels in descending size.
```html
<h1>Heading Size 1</h1>
<h2>Heading Size 2</h2>
<h3>Heading Size 3</h3>
<h4>Heading Size 4</h4>
<h5>Heading Size 5</h5>
<h6>Heading Size 6</h6>
```
[DEMO](https://jsfiddle.net/art8p1w5/)
#### Paragraphs
Paragraphs are sections of text that exist on new lines.
```html
<p>This is a paragraph of information</p>
<p>This is another, it exists on its own line</p>
```
[DEMO](https://jsfiddle.net/r3tgdq40/)
#### Links
The web is navigated using links, which 'link' different pages to eachother. You can link to pages inside the current website.
```html
<a href="contact.html">Contact Us</a>
```
Or to external websites.

```html
<a href="http://www.google.com">Google</a>
```

Links wrap around sections of html that we can click to go to new pages.

```html
<a href="https://en.wikipedia.org/wiki/Crocodile">
	<h1>Crocodile</h1>
    <img src="https://upload.wikimedia.org/wikipedia/commons/b/bd/Nile_crocodile_head.jpg" width="200px">
</a>
```
[DEMO](https://jsfiddle.net/ha922usq/)

#### Bold
```html
<b>This text is bold</b>
```
<b>This text is bold</b>
#### Italic
```html
<i>This text is italicised</i>
```
<i>This text is italicised</i>
#### Superscript
```html
4<sup>2</sup> = 16
```
4<sup>2</sup> = 16
#### Subscript
```html
Our planet is 71% H<sub>2</sub>O
```
Our planet is 71% H<sub>2</sub>O
#### Line break
```html
<p>
	You can have line breaks in the middle of a <br /> paragraph, using the 'br' tag
</p>
```
[DEMO](https://jsfiddle.net/rhLn2583/)
#### Horizontal Rule
```html
This text
<hr />
is seperated
<hr />
by horizontal lines
```
[DEMO](https://jsfiddle.net/yr64wggh/)

### Images
Images are the most used HTML tags that don't have a closing tag.
```html
<img src="https://i.imgur.com/tpXqSrj.jpg">
```

You can specify an image's dimensions using the `width` and `height` attributes.

```html
<img src="https://i.imgur.com/tpXqSrj.jpg" width="100px">
```
<img src="https://i.imgur.com/tpXqSrj.jpg" width="100px">

*The *`px`* denotes the number of pixels.*

You can also specify the width as a percentage of the size of the containing tag.
```html
<img src="https://i.imgur.com/tpXqSrj.jpg" width="50%">
```
<img src="https://i.imgur.com/tpXqSrj.jpg" width="50%">

### Tables
Tables allow you to represent things in a grid format
```html
<table>
	<tr>
    	<th>Heading 1</th>
    	<th>Heading 2</th>
    </tr>
	<tr>
    	<td>Row 1, Column 1</td>
        <td>Row 1, Column 2</td>
    </tr>
    <tr>
    	<td>Row 2, Column 1</td>
        <td>Row 2, Column 2</td>
    </tr>
</table>
```
Produces:
<table>
	<tr>
    	<th>Heading 1</th>
    	<th>Heading 2</th>
    </tr>
	<tr>
    	<td>Row 1, Column 1</td>
        <td>Row 1, Column 2</td>
    </tr>
    <tr>
    	<td>Row 2, Column 1</td>
        <td>Row 2, Column 2</td>
    </tr>
</table>

[DEMO](https://jsfiddle.net/3yq087xo/1)

`<tr>` represents a row

`<td>` represents a cell -- *it stands for 'table data'*

`<th>` represents a heading

Here is an example of a more complicated table:

```html
<table>
    <thead>
        <tr>
            <th></th>
            <th scope="col">Vanilla Ice cream</th>
            <th scope="col">Chocolate Ice cream</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th scope="row">Sugar</th>
            <td>10g</td>
            <td>13g</td>
        </tr>
        <tr>
            <th scope="row">Fat</th>
            <td>2g</td>
            <td>6g</td>
        </tr>
    </tbody>
        <tfoot>
            <tr>
            <td>Price</td>
            <td colspan="2">&#36;5</td>
        </tr>
    </tfoot>
</table>
```

<table>
    <thead>
        <tr>
            <th></th>
            <th scope="col">Vanilla Ice cream</th>
            <th scope="col">Chocolate Ice cream</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th scope="row">Sugar</th>
            <td>10g</td>
            <td>13g</td>
        </tr>
        <tr>
            <th scope="row">Fat</th>
            <td>2g</td>
            <td>6g</td>
        </tr>
    </tbody>
        <tfoot>
            <tr>
            <td>Price</td>
            <td colspan="2">&#36;5</td>
        </tr>
    </tfoot>
</table>
[DEMO](https://jsfiddle.net/9q47aj4v/)

### Lists
HTML lists come in three styles; ordered, unordered, and definitions.

Ordered lists look like
```html
<ol>
	<li>First</li>
	<li>Second</li>
	<li>Third</li>
</ol>
```
<hr>
<ol>
	<li>First</li>
	<li>Second</li>
	<li>Third</li>
</ol>
<hr>

Unordered lists look like

```html
<ul>
	<li>Eggs</li>
	<li>Bacon</li>
	<li>Sausages</li>
</ul>
```
<hr>
<ul>
	<li>Eggs</li>
	<li>Bacon</li>
	<li>Sausages</li>
</ul>
<hr>

Definition lists look like
```html
<dl>
	<dt>HTML</dt>
    <dd>Hypertext Markup Language, a standardized system for tagging text files to achieve font, colour, graphic, and hyperlink effects on World Wide Web pages.</dd>
	<dt>CSS</dt>
    <dd>Cascading Style Sheets (CSS) is a style sheet language used for describing the presentation of a document written in a markup language.</dd>
    <dt>Javascript</dt>
    <dd>an object-oriented computer programming language commonly used to create interactive effects within web browsers.</dt>
</dl>
```
<hr>
<dl>
	<dt>HTML</dt>
    <dd>Hypertext Markup Language, a standardized system for tagging text files to achieve font, colour, graphic, and hyperlink effects on World Wide Web pages.</dd>
	<dt>CSS</dt>
    <dd>Cascading Style Sheets (CSS) is a style sheet language used for describing the presentation of a document written in a markup language.</dd>
    <dt>Javascript</dt>
    <dd>an object-oriented computer programming language commonly used to create interactive effects within web browsers.</dt>
</dl>
<hr>

You can nest lists by placing another list inside a `<li>` element

```html
<ol>
	<li>
    	First
    	<ol>
        	<li>a</li>
        	<li>b</li>
        	<li>c</li>
        </ol>
    </li>
	<li>Second</li>
	<li>Third</li>
</ol>
```
<hr>
<ol>
	<li>
    	First
    	<ol>
        	<li>a</li>
        	<li>b</li>
        	<li>c</li>
        </ol>
    </li>
	<li>Second</li>
	<li>Third</li>
</ol>
<hr>



### Forms

Forms allow you to obtain information from people that visit your website.
<hr>
Name: <input type="text">
<button>Submit</button>
<hr>
When submitting a form, data is sent back to a server that is able to deal with this information. This is not something that is handled by HTML.

Here is an example of a form:
```html
<form action="http://www.example.com/submit">
	 <p>
     	Username:
		 <input type="text" name="username" />
	 </p>
</form>
```
<hr>
<form action="http://www.example.com/submit">
	 <p>
     	Username:
		 <input type="text" name="username" />
	 </p>
</form>
<hr>

The `action` attribute is the url that the form data will be given to.

Inside the form, the input is a textbox which has the name `username`. When the data is handed back to the server, the server will look for the value associated with the name `username`.

Here are all the HTML form elements:

#### Textbox

```html
<input type="text" name="username" value="qwertyuiop"/>
```
<hr>
<input type="text" name="username" value="qwertyuiop"/>
<hr>

#### Password

```html
<input type="password" name="username" value="password1"/>
```
<hr>
<input type="password" name="username" value="password1"/>
<hr>

#### Textarea

```html
<textarea name="details"> Bla bla bla </textarea>
```
<hr>
<textarea name="details"> Bla bla bla </textarea>
<hr>

#### Radio button

```html
<input type="radio" name="flavour"> Vanilla
<input type="radio" name="flavour"> Strawberry
<input type="radio" name="flavour" checked="checked"> Chocolate
<input type="radio" name="other"> Extra
```
<hr>
<input type="radio" name="flavour"> Vanilla
<input type="radio" name="flavour"> Strawberry
<input type="radio" name="flavour" checked="checked"> Chocolate
<input type="radio" name="other"> Extra
<hr>

When you give radio buttons the same name, you can only choose one at a time.

#### Checkbox

```html
<input type="checkbox" name="features"> Air Conditioning
<input type="checkbox" name="features"> Radio
<input type="checkbox" name="features"> Rear-view camera
<input type="checkbox" name="features"> Cruise control
<input type="checkbox" name="features"> Power steering
```
<hr>
<input type="checkbox" name="features"> Air Conditioning
<input type="checkbox" name="features"> Radio
<input type="checkbox" name="features"> Rear-view camera
<input type="checkbox" name="features"> Cruise control
<input type="checkbox" name="features"> Power steering
<hr>

#### Dropdown

```html
<p>How old are you?</p>
<select name="ages">
	<option value="0-18">0-18</option>
    <option value="19-35">19-35</option>
    <option value="36-55" selected="selected">36-55</option>
    <option value="56-70">56-70</option>
    <option value="70+">70+</option>
</select>
```
<hr>
<p>How old are you?</p>
<select name="ages">
	<option value="0-18">0-18</option>
    <option value="19-35">19-35</option>
    <option value="36-55" selected="selected">36-55</option>
    <option value="56-70">56-70</option>
    <option value="70+">70+</option>
</select>
<hr>

#### File upload

```html
<input type="file" />
```

<hr>
<input type="file" />
<hr>

#### Date
```html
<input type="date">
```
<hr>
<input type="date">
<hr>

#### Button

```html
<button onclick="alert('You clicked me!')">Click me!</button>
```
<hr>
<form>
<button onclick="alert('You clicked me!')">
Click me!
</button>
</form>
<hr>


#### Submit button

```html
<form action="submit.php">
<input type="submit" />
</form>
```

<hr>
<form action="submit.php">
<input type="submit" />
</form>
<hr>

Submit buttons will send the entered data to the location described in the action attribute.
