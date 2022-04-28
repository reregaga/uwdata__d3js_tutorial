# Technology fundamentals for D3.js - HTML, CSS, SVG, Javascript

A tutorial by [Kanit "Ham" Wongsuphasawat](http://kanitw.yellowpigz.com/) (@kanitw), [Jane Hoffswell](https://homes.cs.washington.edu/~jhoffs/#CurriculumVitae), and [Dominik Moritz](http://homes.cs.washington.edu/~domoritz/) (@domoritz)
[Interactive Data Lab, University of Washington](http://idl.cs.washington.edu/)

## Notes
- HTML, CSS and SVG examples are all codepens, which you can click edit to play with.
- You can also use inspector (DevTools in Firefox or Chrome) to inspect examples.
- Also use Javascript console to try Javascript code examples.

## HTML
Hypertext Markup Language

HTML is designed for marking up text by adding tags such as `<p>` to create HTML elements. HTML tags begin with `<` and end with `>`. Tags often occur in pairs of opening and closing tags. Some tags such as `<img>` always occur alone. Those tags usually (but not required to) have trailing slash.

Tags can have **attributes**. For example, `<a>` tag has `href` attribute for defining link target. Similarly, `<img>` tag has `src` attribute for defining image source.

```html
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <p>Hello World!</p>
</body>
</html>
```

A `<div>` is a generic **block-level container**. A div block breaks line.
A `<span>` is a generic **inline container**. Therefore, a span blocks do not break line.

### More tags
- See [w3school](http://www.w3schools.com/html/html_quick.asp)s's quick list of the most commonly used HTML tags.
- Or learn more at [Mozilla Develop Network](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML)'s HTML tutorial.

## DOM
- A convention for representing and interacting with objects in HTML, XHTML and XML documents.
- Nodes of every document are organized in a tree structure, called the DOM tree
    - For example, use inspector to see this file's source.
- Provides API to modify its content using language such as Javascript.

## CSS
Cascading Style Sheets

Query the DOM tree:
```css
/* ID: tag#id */
/* multiple selectors can be separated by comma */
#first-div, #first-span {
  font-weight: bold;
}
/* Classes: tag.class */
span.classy{
  font-family: Helvetica;
}
/* attribute -- in this case similar to span.classy */
span[class=classy]{
  color: #364dc2;
}
/* Pseudo-classes: a:hover, div:first-child */
a:hover{
  color: red;
}
span:first-child{
  background-color: #EEE;
}
/* Descendant: A D */
div a{
  color: blue;
}
/* Child: A > C */
div > a{
  text-transform: uppercase;
  font-style: italic;
}
/* Next Sibling: A + C */
span#first-span + span {
  text-decoration: underline;
}
```
See also: CSS Properties – [Webmonkey](http://www.webmonkey.com/2010/02/css-properties/) and CSS Selectors on [NetTuts](http://net.tutsplus.com/tutorials/html-css-techniques/the-30-css-selectors-you-must-memorize/)

### CSS: Box Model, Position
![box-model](./img/box-model.gif)
The default position is `position: static;`

`position: relative` adjust the element's position, without changing layout.

`position: absolute` taken out of the flow and thus takes up no space when placing other elements. The absolutely positioned element is positioned relative to nearest positioned ancestor. If a positioned ancestor doesn't exist, the initial container is used.

### CSS: short form
```css
background-color: #000; background-image: url(images/bg.gif); background-repeat: no-repeat; background-position: top right;
```
Can be shortened to:
```css
background: #000 url(images/bg.gif) no-repeat top right;
```

### CSS: Include
Inline:
```css
<style>
/* put css here */
</style>
```
```html           
<div style="/* put css in style attribute of any tag */"></div>
```         
Include:
```html           
<link rel="stylesheet" href="style.css">
```

### [SASS](http://sass-lang.com/)
Variable, Nesting, Partials, Import, Mixins, Inheritance, Operators
```scss
/* variable, operator */
$font-stack:    Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 0.8*100% $font-stack;
  color: $primary-color;
}

/* nesting */
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li { display: inline-block; }

  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}

/* mixin */
@mixin border-radius($radius) {
  -webkit-border-radius: $radius;
     -moz-border-radius: $radius;
      -ms-border-radius: $radius;
       -o-border-radius: $radius;
          border-radius: $radius;
}

.box { @include border-radius(10px); }
```           
[Compass](http://compass-style.org/) is a collection of reusable mixins for Sass.  
[Less](http://lesscss.org/) is a another option.

### Advanced CSS
- CSS [flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) and [grid](https://css-tricks.com/snippets/css/complete-guide-grid/) can be very useful for creating page layout.
- To make advanced CSS work with older browser, you can easily add [autoprefixer](https://github.com/postcss/autoprefixer) if you use a build system such as [Webpack](https://github.com/postcss/autoprefixer#webpack).

### CSS Grid
Grid is one of the most commonly used graphic design concept.
![grid](./img/grid-crop.png)
For instance, see [bootstrap grid's examples](http://getbootstrap.com/examples/grid/).

### CSS: Learn more!
- [Learn CSS](https://developer.mozilla.org/en-US/learn/css), [CSS Portal](https://developer.mozilla.org/en-US/docs/Web/CSS) – Mozilla Developer Network
- [CSS Zen Garden](http://www.csszengarden.com/) – huge collection of examples
- Use browser inspector to learn from others.

## SVG
Scalable Vector Graphics

### SVG: Shapes
Also check out http://bost.ocks.org/mike/d3/workshop/#109
```html
<svg>
  <line x1="5" x2="5" y1="100" y2="30" stroke="black"/>

  <line x1="100" x2="150" y1="220" y2="40" stroke="black"/>

  <circle cx="250" cy="25" r="7"/>
  
  <rect x="150" y="150" width="15" height="15"/>
  <rect x="220" y="90" width="15" height="15"/>

  <circle cx="150" cy="75" r="7"/>
  <circle cx="80" cy="85" r="7"/>
  
  <ellipse cx="180" cy="30" rx="15" ry="25"/>
  
  <text x="160" y="120">Hello!</text>
</svg>
```

### SVG + CSS
```css
rect{
  fill: green;
}
circle{
  stroke: orange;
  stroke-width: 3;
}
```
```html
<svg>
  <line x1="5" x2="5" y1="5" y2="200" stroke="black"/>
  <circle cx="250" cy="25" r="7"/>
  <rect x="150" y="150" width="15" height="15"/>
  <!--<ellipse cx="150" cy="25" rx="15" ry="25"/>-->
  <text x="100" y="225">Manually Drawn Chart</text>
</svg>
```

### SVG: Polygon, Polyline
Use coordinates to specify path.
```html
<svg>
  <polygon style="fill-rule: nonzero; fill: purple; stroke: black;"
    points="48,16  16,96  96,48  0,48  80,96" />
  <polygon style="fill-rule: evenodd;  fill: yellow; stroke: black;"
    points="148,16  116,96  196,48  100,48  180,96" />
  <polyline fill="none" stroke="blue" stroke-width="2"
     points="05,130
             15,130
             15,120
             25,120
             25,110
             35,110" />
</svg>
<!-- applied from http://oreilly.com/catalog/svgess/chapter/ch03.html#t5 -->
```

### SVG: Path
- `M x y` – Move to (x,y)
- `m dx dy` – Move by (dx,dy)
- `L x y` – Line to (x,y) (or `l dx dy`)
- `H x`, `V y` – draw horizontal and vertical lines
- `Z`, `z` - close path
- See also: [Curves Commands](https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial/Paths#curve_commands)
```html
<svg> <!--small multiples -->
  <path d="M 10 50 h 20 l 10 -20 l 20 10 l 30 10 l 5 -30 l 25 30" fill="none" stroke="black"/>
  <path d="M 10 100 h 20 l 15 -20 l 10 -15 l 10 35  l 10 -20 l 20 10 l 30 10" fill="none" stroke="black"/>
  <path d="M 10 150 l 15 -10 l 10 -15 h 20 l 10 20 l 10 -25 l 20 10 l 30 10" fill="none" stroke="black"/>
</svg>
```

### SVG: Group, Title & Transform
- Transform example: `translate`, `rotate`, `scale`, `skewX`, `skewY`
- Use `title` for tooltip
```css
.logo-i{  fill: #808284;}
.logo-d{  fill: #51187D;}
.logo-l{  fill: #CA9A1E;}
```
```html
<svg width="99" height="85">
  <g transform="translate(50,39)">
    <g transform="rotate(25)">
      <rect class="logo-i" x="-24" y="-14" width="6" height="6"></rect>
      <rect class="logo-i" x="-24" y="0" width="6" height="6"></rect>
      <rect class="logo-i" x="-24" y="7" width="6" height="6"></rect>
      <rect class="logo-i" x="-24" y="14" width="6" height="6"></rect>
    </g>
    <g transform="scale(0.8)">
      <rect class="logo-d" x="0" y="0" width="6" height="6"></rect>
      <rect class="logo-d" x="-7" y="0" width="6" height="6"></rect>
      <rect class="logo-d" x="-14" y="0" width="6" height="6"></rect>
      <rect class="logo-d" x="0" y="-7" width="6" height="6"></rect>
      <rect class="logo-d" x="0" y="-14" width="6" height="6"></rect>
      <rect class="logo-d" x="0" y="7" width="6" height="6"></rect>
      <rect class="logo-d" x="0" y="14" width="6" height="6"></rect>
      <rect class="logo-d" x="-14" y="7" width="6" height="6"></rect>
      <rect class="logo-d" x="-14" y="14" width="6" height="6"></rect>
      <rect class="logo-d" x="-7" y="14" width="6" height="6"></rect>
    </g>
    <g transform="skewX(5)">
      <rect class="logo-l" x="11" y="-14" width="6" height="6"></rect>
      <rect class="logo-l" x="11" y="-7" width="6" height="6"></rect>
      <rect class="logo-l" x="11" y="0" width="6" height="6"></rect>
      <rect class="logo-l" x="11" y="7" width="6" height="6"></rect>
      <rect class="logo-l" x="11" y="14" width="6" height="6"></rect>
      <rect class="logo-l" x="18" y="14" width="6" height="6"></rect>
    </g>
  </g>
</svg>
```

### SVG: No-Layer
Painter's Algorithm: any pixel-paint applied later obscure any earlier paint and therefore appear to be "in front".
```html
<!-- an example from http://alignedleft.com/tutorials/d3/an-svg-primer-->
<svg>
<rect x="0" y="0" width="30" height="30" fill="purple"/>
<rect x="20" y="5" width="30" height="30" fill="blue"/>
<rect x="40" y="10" width="30" height="30" fill="green"/>
</svg>
```

### SVG: Transparency
`rgba` or `opacity`
```html
<!-- modified from http://alignedleft.com/tutorials/d3/an-svg-primer--> 
<svg>
  <g transform="translate(10,10)">
    <circle cx="25" cy="25" r="20" fill="rgba(128, 0, 128, 1.0)" />
    <circle cx="50" cy="25" r="20" fill="rgba(0, 0, 255, 0.75)" />
    <circle cx="75" cy="25" r="20" fill="rgb(0, 255, 0)" opacity="0.5"/> 
  </g>
  <g transform="translate(10,70)">
    <circle cx="25" cy="25" r="20" fill="rgba(128, 0, 128, 0.75)" stroke="rgba(0, 255, 0, 0.25)" stroke-width="10" />
    <circle cx="75" cy="25" r="20" fill="rgba(0, 255, 0, 0.75)" stroke="rgba(0, 0, 255, 0.25)" stroke-width="10" />
    <circle cx="125" cy="25" r="20" fill="rgba(255, 255, 0, 0.75)" stroke="rgba(255, 0, 0, 0.25)" stroke-width="10" />
  </g>
  <g transform="translate(10,140)">
    <circle cx="25" cy="25" r="20" fill="purple" stroke="green" stroke-width="10" opacity="0.9" />
    <circle cx="65" cy="25" r="20" fill="green" stroke="blue" stroke-width="10" opacity="0.5" />
    <circle cx="105" cy="25" r="20" fill="yellow" stroke="red" stroke-width="10" opacity="0.1" />
  </g>
</svg>
```

### SVG: Learn more!
-   [Text](https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial/Texts), [Gradient](https://developer.mozilla.org/en-US/SVG/Tutorial/Gradients), [Patterns](https://developer.mozilla.org/en-US/SVG/Tutorial/Patterns), [Clip Mask](https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial/Clipping_and_masking), [Image](https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial/Other_content_in_SVG)
-   [SVG Tutorial](https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial) – Mozilla Developer Network

## JavaScript
- Created in 10 days in May 1995 by Brendan Eich
- Originally developed as a prototype language for web browser (Client-side).
- Now used in server-side (Node.js) as well.
- Not related to Java, just named similarly for marketing purpose.
- C-style syntax but got inspiration from Functional programming
    - `for`, `while`, `continue`, `break`, `if`/`else`, `switch` are similar to C
    - operators (`+`,`-`,`*`,`/`,`%`) are also similar (except `==`,`!=`,`||`)
    - include function operations such as `map`, `reduce`, `forEach`.

### Note
- Javascript world is [moving extremely fast](https://medium.com/@ericclemmons/javascript-fatigue-48d4011b6fc4) with new standards and tools introduced all the time.
    - Javascript Next include versions of new syntax release annually (ES2015, ES2016, and ES2017). To use these new syntax, take a look at [Babel](https://babeljs.io/).
    - [Typescript](https://www.typescriptlang.org/) is a version of Javascript with static typing, built by Microsoft.
- For this tutorial, we will only cover classic Javascript (ES5).
    - See our [wiki](https://github.com/uwdata/d3-tutorials/wiki) for more resources.

### Client-side Javascript: Inline/Include
Inline:
```html
<script>
//Put Javascript code here
</script>
```
Include:
```html
<script src="main.js"></script>
```

### Data Types
-   _Numbers_ - 42, 3.14159
-   _Logical_ - true, false
-   _Strings_ - "Hello", 'Hello'
-   `null`
-   `undefined`* - Yes. `undefined` is not `null`!
-   Objects
-   functions

See also [Values, Variable, Literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Values,_variables,_and_literals) – MDN.

### Variables
```js
var a;
console.log("The value of a is " + a); // logs "The value of a is undefined"
console.log("The value of b is " + b); // throws ReferenceError exception
b = 5; // declare global variable  ... equivalent to window.b = 5
console.log(b, window.b); // 5, 5
```
Javascript uses dynamic typing.
```js         
x = "The answer is " + 42; // "The answer is 42"
"37" - 7; // 30
"37" + 7; // "377"
"1.1" + "1.1"; //= "1.11.1"
(+"1.1") + (+"1.1"); // 2.2
+"1.1" // 1.1 "+" operator converts string to number
```       
Tips: operator can return Object too.
```js
y = null || "String"
y // "String"
```

### Control Flow
C-Style `for`, `while`, `continue`, `break`, `if`/`else`, `switch/case`.
```js
for (i=0; i<10; i++) {
  if (condition) {
      statement_1_runs_if_condition_is_true();
      break;
  } else {
      statement_2_runs_if_condition_is_false();
      continue;
  }
}
```
>(I'm not showing while, switch/case here for brevity.)

### Object
- An object in javascript is an **associative array** of **property names** (Strings) and **values** (Objects).
- Everything except `null` and `undefined` can be treated as objects.
- Object can be used as **hashmaps**.
- Object can be created using (a) literals, (b) `new`.
```js
//create object using an object literal
var apple = {
  // quotes not required for a property name
  state: "CA",
  // unless the name contains space(s) or precedes with number or the name is reserved word
  "famous founder": "Steve Jobs",
  // property value can be any type including function
  getCity: function(){return "Cupertino";},
  // nested object
  boards: { "CEO": "Tim Cook"}
};
apple.state; // "CA"
apple["state"]; // "CA"
apple.getCity(); // "Cupertino"
apple['getCity'](); // "Cupertino"
apple.boards.CEO // "Tim Cook"

//create object using new instead
var microsoft = new Object();
microsoft.state = "WA";
microsoft['famous founder'] = "Bill Gates";
microsoft.getCity = function(){ return "Redmond";};
```

#### for .. in
Careful: use `hasOwnProperty` to check.
```js
var obj = {a:1, b:2, c:3},
    key;
Object.prototype.crazy = 4;
for (key in obj) {
  if(obj.hasOwnProperty(key)){ //avoid the inherited obj.crazy=4
    console.log(key, obj[key]); // "a, 1" "b, 2", "c, 3"
  }
}
```

### Arrays
```js
var numbers = [ 5, 10, 15, 20, 25];
numbers[1] // 10
numbers[2] // 15
numbers.length = 5
2 in numbers // true
5 in numbers // false
numbers.a = 5 // Array is an object
numbers.a // 5
'a' in numbers // true

var numbers = [ 5, 10, , 20, 25, , ];
numbers[1] // 10
numbers[2] // undefined
numbers.length //6, last empty comma is automatically ignored
          
// array with multiple types of values
var mashup = [ 1,3, 4.5, 5.6, "string", null, undefined, true ];
```

### Function
First class object...
```js
function foo(a1, a2){
  // code
  console.log(a1+a2);
}
```
same as
```js
var foo = function(a1, a2){
  // code
  console.log(a1+a2);
};
```
Call:
```js
foo(a1,a2); // call
```
Callback:
```
function g(f){ f(1,2); }
g(foo) // 3
```
See also: [Arguments Objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions#Using_the_arguments_object)

### Scope
Javascript has **function level scope**, not block level scope*.
The inner function full access to all the variables and functions defined inside the outer function. But the converse is not true.
```js
var name = "Andy"
var pet = function(name) {      // The outer function defines a variable called "name"
  var getName = function() {
    return name;            // The inner function has access to the "name" variable of the outer function, which is "Vivie" in this case.
  }
  return getName;           // Return the inner function, thereby exposing it to outer scopes
};
var myPet = pet("Vivie");
myPet();                        // Returns "Vivie"
console.log(name);              // "Andy"
```
*ES2016 and TypeScript include block-level scoping `let` and `const`.

```js
var x = 1;
{
  var x = 2;
}
alert(x); // outputs 2
```

#### Hoisting
```js
console.log(x === undefined); // logs "true"
var x = 3;
```
is equivalent to
```js
var x;
console.log(x === undefined); // logs "true"
x = 3;
```

### IIFE
Immediately Invoked Function Expression

```js
var elems = document.getElementsByTagName( 'a' );
for ( var i = 0; i < elems.length; i++ ) {
  elems[ i ].addEventListener( 'click', function(e){
    e.preventDefault();
    alert( 'I am link #' + i );
  }, 'false' );
}
```
>The value of `i` never gets locked in and all `i` references to one `i`. Thus, every link, when clicked (well after the loop has finished executing), alerts the total number of elements.

```js
var elems = document.getElementsByTagName( 'a' );
for ( var i = 0; i < elems.length; i++ ) {
  (function( lockedInIndex ){
    elems[ i ].addEventListener( 'click', function(e){
      e.preventDefault();
      alert( 'I am link #' + lockedInIndex );
    }, 'false' );
  })( i );
}
```
>This works, because inside the IIFE, the value of `i` is locked in as new variable `lockedInIndex`, because passed by value.

See also: [Ben Alman's Post](http://benalman.com/news/2010/11/immediately-invoked-function-expression/)

#### IIFE: Anonymous Namespaces
Use IIFE to avoid namespace clashing!
```js
(function() {
    // a self contained "namespace"

    // PUT YOUR NONE PUBLIC SCRIPT HERE

    window.foo = function() {
        // an exposed closure
    };
})(); // execute the function immediately
```

### "this"

```js
var test = {};
this; // this = global object aka window
foo(); // this = global object again
test.foo(); // this = test
new foo(); // this = newly created object
```

Explicity Setting of `this`:
```js
function foo(a, b, c) {
  // this = bar, here when foo is called from apply and call below
}
var bar = {};
foo.apply(bar, [1, 2, 3]); // array will expand to the below
foo.call(bar, 1, 2, 3); // results in a = 1, b = 2, c = 3
```
Source: [Javascript Garden](http://bonsaiden.github.io/JavaScript-Garden/#function.this)

### "that"
```js
Foo = {a:1};
Foo.method = function() {
    var that = this;
    function test() {
        // Use `that` instead of `this` here (closure it)
        // because here `this` is set to the global object
        console.log(this, that); // Window, {a:1, method: function}
    }
    test();
}
```

### OOP in Javascript: using Constructor
```js
function Person(gender) {
  this.gender = gender;
}
Person.prototype.sayHello = function(){
  alert ('hello');
};

var person1 = new Person('Male'), person2 = new Person('Female');
// call the Person sayHello method.
person1.sayHello(); // hello
```
Source: [Mozilla](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Introduction_to_Object-Oriented_JavaScript)

#### Inheritance
Extend `Person`
```js
function Person(gender) {
  this.gender = gender;
}
Person.prototype.sayHello = function(){
  console.log('hello');
};

function Student(){}
// inherit Person
Student.prototype = new Person();
// correct the constructor pointer because it points to Person
Student.prototype.constructor = Student;
// replace the sayHello method
Student.prototype.sayHello = function(){
  console.log('hi, I am a student');
}

Person.prototype.sayBye = function(){
  console.log('bye');
};

function Teacher(){}
Teacher.prototype = new Person();
Teacher.prototype.constructor = Teacher;
Teacher.prototype.sayHello = function(){
  console.log('hi, I am a teacher');
}

var student1 = new Student();
student1.sayHello();
console.log(student1 instanceof Person); // true
console.log(student1 instanceof Student); // true

var teacher1 = new Teacher();
teacher1.sayHello();

student1.sayBye();

/*output:
hi, I am a student
true
true
hi, I am a teacher
bye
*/
```

#### Prototypal Inheritance
```js
var o = {a: 1};

// The newly created object `o` has `Object.prototype` as its [[Prototype]]
// `o` has no own property named 'hasOwnProperty'
// `hasOwnProperty` is an own property of Object.prototype. So `o` inherits hasOwnProperty from Object.prototype
// Object.prototype has null as its prototype.
// o ---> Object.prototype ---> null

var a = ["yo", "whadup", "?"];

// Arrays inherit from Array.prototype (which has methods like indexOf, forEach, etc.)
// The prototype chain looks like:
// a ---> Array.prototype ---> Object.prototype ---> null

function f(){ return 2 }

// Functions inherit from Function.prototype (which has methods like call, bind, etc.)
// f ---> Function.prototype ---> Object.prototype ---> null
```
Source & see also: [prototype chain](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Inheritance_and_the_prototype_chain)

### Module Pattern & Private Variable
Module Pattern use scope to make a private variable:
```js
function Counter(start) {
    var count = start;
    return {
        increment: function() {
            count++;
        },

        get: function() {
            return count;
        }
    }
}
var foo = Counter(4);
foo.increment();
foo.get(); // 5
foo.count // undefined ... outsider can't access count directly
```
[Using `Object.create`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects#Using_the_Object.create_method)

### === and ==
- The `==` operator will compare for equality after doing any necessary type conversions (with very weird conversion rules).
- The `===` operator will not do the conversion, so if two values are not the same type `===` will simply return false.
```js
'' == '0'           // false
0 == ''             // true
0 == '0'            // true

false == 'false'    // false
false == '0'        // true

false == undefined  // false
false == null       // false
null == undefined   // true

' \t\r\n ' == 0     // true
```        
Never use the evil twins. Instead, always use `===` and `!==`. See also: http://stackoverflow.com/questions/359494/does-it-matter-which-equals-operator-vs-i-use-in-javascript-comparisons

### Javascript: [DOM](https://uwdata.github.io/d3-tutorials/fundamental.html)
As mentioned earlier, DOM provided javascript API. You should at least know about:
-   [`Document`](https://developer.mozilla.org/en-US/docs/Web/API/document) and [`Window`](https://developer.mozilla.org/en-US/docs/Web/API/window) Objects
-   [`document.getElementById`](https://developer.mozilla.org/en-US/docs/Web/API/Document.getElementById)
-   [`document.createElement`](https://developer.mozilla.org/en-US/docs/Web/API/Document.createElement)
-   [`document.createNode`](https://developer.mozilla.org/en-US/docs/Web/API/Document.createNode)
-   [`document.querySelector`](https://developer.mozilla.org/en-US/docs/Web/API/Document.querySelector), [`document.querySelectorAll`](https://developer.mozilla.org/en-US/docs/Web/API/Document.querySelectorAll)

### JSON
Javascript Object Notation. Derived from Javascript as an XML alternative for storing data.
```json
[{
    "yield": 27,
    "variety": "Manchuria",
    "year": 1931,
    "site": "University Farm"
}, {
    "yield": 48.86667,
    "variety": "Manchuria",
    "year": 1931,
    "site": "Waseca"
}]
```
- JSON requires double quote (`"`) around keys
- JSON doesn't support `undefined`, expressions, functions, and comments
```js
JSON.parse('{"a":null}'); // {a:null}
JSON.parse('{"a":undefined}'); // SyntaxError: Unexpected token u
JSON.parse('{"a":function(){return 'a';}}'); // SyntaxError: Unexpected identifier
```

### Syntax Alternatives
Some people like syntax alternative that compile into javascript such as [Coffeescript](http://coffeescript.org/), [MS TypeScript](http://www.typescriptlang.org/).

### Libraries
-   _[Lo-Dash](http://lodash.com/)_ – Utility library (arguably a better fork of [Underscore](http://underscorejs.org/)) – See a [tutorial](http://tech.pro/tutorial/1611/functional-javascript)
-   _[jQuery](http://jquery.com/)_ – easy DOM element selections, traversal and manipulation.
    -   However, less useful for visualization since d3 offers similar features
-   Frameworks: [React.js](https://facebook.github.io/react/), [Angular.js](http://angularjs.org/) are useful for developing applications (but maybe an overkill for projects in this class.)

### Javascript: Learn More
-   Basics: **[Javascript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)** – Mozilla Developer Network
-   Refresher: **[Javascript Garden](http://bonsaiden.github.io/JavaScript-Garden/)**
-   More in [cse512 resources](http://courses.cs.washington.edu/courses/cse512/15sp/resources.html#javascript)

## Workflow & Tools
- Learn to use the [Firefox developer tools](https://developer.mozilla.org/en-US/docs/Tools) or [the Webkit Inspector](http://jtaby.com/blog/2012/04/23/modern-web-development-part-1)
- Good Text Editor GUI? – [Visual Studio Code](https://code.visualstudio.com/) or [Sublime Text](http://sublimetext.com/)
    - Also use [Emmet](http://emmet.io/) for faster HTML authoring
- Use a Linter (e.g. [ESLint](https://eslint.org/), TSLint)
- Reduce the gulf of execution and evaluation with [LiveReload](http://livereload.com/) or other similar tools.
- Like IDE and willing to pay (unless you are a student)? [Webstorm](http://www.jetbrains.com/webstorm/) is a good option.

## Feedback
Please fill out the survey https://goo.gl/forms/BOF7jNuucPHyEn2M2