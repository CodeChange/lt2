# [HTML Introductory Course](https://github.com/ScriptSmith/lt2/blob/master/html.md)

[DOWNLOAD](https://github.com/ScriptSmith/lt2/archive/master.zip)
## JavaScript
### Purpose
* JavaScript is used to define the behaviour of webpages.
* It makes your site interactive.
* You send and receive information without refreshing the page.

### Embedding it
```HTML
<script>
    //stuff
</script>

<!-- or -->

<script src="script.js"></script>
```

### Syntax and Style Guide
[REFERENCE](http://www.w3schools.com/js/js_syntax.asp)
**Literals:**
`1000`
`0.1`
**Strings:**
`"John Citizen"`
`'a'`
Strings are just pieces of text
**Variables:**
`x = 5`
`name = "Kate"`
Variables store values to be accessed later
**Operators and Expressions:**
`+ - * /`
`5 * 2 = 10`
`"Dog" + " " + "Cat"`
Expressions manipulate values
**Comments:**
Comments exist after `//` or between `/*` and `*/`
Comments aren't run by your browser

### Statements, operators, arithmetic and variables example
Write a program that asks for a user's age, and tell them how old they were in a given year

```JavaScript
var age = parseInt(prompt("What is your age?"))
var date = new Date().getFullYear();
var difference = parseInt(prompt("What year do you want to know how old you were on this date?"))
alert(difference - date + age)

```
### Booleans
In programming, we like to check whether things are `true` or `false`
```JavaScript
1 == 1
true

1 != "1"
true

"hello" == 'hello'
true

1 == 2
false
```

### Arrays
We also often have to store multiple variables in succession
```JavaScript
var names = ["Jack","Jill","Mary","Sue"]
```
Which we can access later
```JavaScript
names[0]
"Jack"

names[3]
"Sue"

names.length
4

names[names.length]
```
### Control Statements
We often only want to perform actions if certain conditions are met
#### If
```JavaScript
var password = prompt("Password:")

if(password == "qwertyuiop"){
    alert("Welcome")
} else if(password == "poiuytrewq"){
    alert("You are denied access")
} else {
    alert("Incorrect Password")
}

```
#### While
```JavaScript
var guessedPassword = false

while (!guessedPassword) {
    var guess = prompt("Password:")
    guessedPassword = (guess == "franklin")
}
alert("Welcome")
```
#### For
We can use for loops to iterate over arrays
```JavaScript
var names = ["Jack","Jill","Mary","Sue"]
var ages = [22, 31, 43, 65]

for(var i = 0; i<names.length; i++){
    alert(names[i] + ": " + ages[i].toString())
}
```
### Functions
Functions define code that we want to use more than once

```JavaScript
function guessedPassword() {
    var guessedPassword = false

    while (!guessedPassword) {
        var guess = prompt("Password:")
        guessedPassword = (guess == "franklin")
    }
    alert("Welcome")
}

guessedPassword()
```

### Events
When certain things happen in HTML, we can call JavaScript functions
[DEMO](http://www.w3schools.com/js/tryit.asp?filename=tryjs_event_onclick1)
