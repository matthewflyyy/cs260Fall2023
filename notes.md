Cloning a repository from the terminal:
    git clone https://github.com/webprogramming260/startup-example.git


Add, commit and push from the terminal to github:
    git add test.md

➜  git commit -am "update(notes) thoughts about startup applications"

➜  git push

Configure your github account in the terminal:
    git config --global user.email "you@example.com"
    git config --global user.name "Your name"

Check if there are changes to commit:
➜  git fetch
➜  git status

Development and production environments:
     it is critical to separate where you develop your application, from where the production release of your application is made publicly available

     You should never consider your production environment as the place where you develop or experiment with your application

     You run a deployment script from a console window in your development environment with a command like the following:
         ./deployService.sh -k ~/prod.pem -h yourdomain.click -s simon

dig (url) gives you the ip address of a website

The local host ip address is 127.0.0.1 is just to access your own local machine

# Console commands
- chmod: Stands for "change mode." It's used to change the permissions of files and directories in Unix-based systems. You can specify who can read, write, and execute a file or directory.
-  pwd: Stands for "print working directory." It displays the current directory path.
- cd: Stands for "change directory." It's used to navigate between directories. You provide the path of the directory you want to change to.
- ls: Stands for "list." It's used to list the contents of a directory, such as files and subdirectories. When you combine -la, you get a long format listing that includes hidden files and directories. This is a useful way to see a comprehensive view of the contents of a directory, including hidden configuration files and directories that are often important for system configuration and customization.
- vim: A text editor in the console. It's known for its powerful features and is often used for code editing.
- nano: Another text editor for the console, but it's simpler and more user-friendly compared to vim.
- mkdir: Stands for "make directory." It's used to create new directories or folders.
- mv: Stands for "move." It's used to move or rename files and directories.
- rm: Stands for "remove." It's used to delete files and directories. Be careful, as it permanently deletes files.
- man: Stands for "manual." It's used to display the manual or documentation for various commands and programs.
- ssh: Stands for "secure shell." It's used for secure remote access to a server or computer over a network. can be used to create a remote shell session. "ssh user@192.168.1.100"
- ps: Stands for "process status." It's used to list currently running processes on a Unix-based system.
- wget: A command-line utility for downloading files from the internet, typically via HTTP or FTP.
- sudo: Stands for "superuser do." It's used to run a command with elevated privileges, typically as a superuser or administrator.

# Domain names
![Domain name parts](https://github.com/webprogramming260/.github/raw/main/profile/webServers/domainNames/domainNameParts.jpg)
- Top Level Domain (TLD) - .com, .edu, .click
- Root domain - cs260.click, byu.edu
- subdomain - travel (travel.cs260.click), blog (blog.cs260.click)

A web certificate is necessary to use HTTPS.
A DNS A record can point to an IP address, but not directly to another A recor

## Ports
- Port 443: Used for HTTPS (Hypertext Transfer Protocol Secure)
- Port 80: Used for HTTP (unencrypted)
- Port 22: Used for SSH (Secure Shell) protocol



# HTML
## Hyperlink
```html
<a href="https://byu.edu">Go to the Y</a>
```
## Common elements
| element   | meaning                                                                |
| --------- | ---------------------------------------------------------------------- |
| `html`    | The page container                                                     |
| `head`    | Header information                                                     |
| `title`   | Title of the page                                                      |
| `meta`    | Metadata for the page such as character set or viewport settings       |
| `script`  | JavaScript reference. Either a external reference, or inline           |
| `include` | External content reference                                             |
| `body`    | The entire content body of the page                                    |
| `header`  | Header of the main content                                             |
| `footer`  | Footer of the main content                                             |
| `nav`     | Navigational inputs                                                    |
| `main`    | Main content of the page                                               |
| `section` | A section of the main content                                          |
| `aside`   | Aside content from the main content                                    |
| `div`     | A block division of content                                            |
| `span`    | An inline span of content                                              |
| `h<1-9>`  | Text heading. From h1, the highest level, down to h9, the lowest level |
| `p`       | A paragraph of text                                                    |
| `b`       | Bring attention                                                        |
| `table`   | Table                                                                  |
| `tr`      | Table row                                                              |
| `th`      | Table header                                                           |
| `td`      | Table data                                                             |
| `ol,ul`   | Ordered or unordered list                                              |
| `li`      | List item                                                              |
| `a`       | Anchor the text to a hyperlink                                         |
| `img`     | Graphical image reference                                              |
| `dialog`  | Interactive component such as a confirmation                           |
| `form`    | A collection of user input                                             |
| `input`   | User input field                                                       |
| `audio`   | Audio content                                                          |
| `video`   | Video content                                                          |
| `svg`     | Scalable vector graphic content                                        |
| `iframe`  | Inline frame of another HTML page                                      |

HTML defines a header (<!DOCTYPE html>) that tells the browser the type and version of the document.

## Images 
```html
<img alt="mountain landscape" src="https://images.pexels.com/photos/164170/pexels-photo-164170.jpeg" />
```

# CSS
## Intro
CSS - Cascading Style Sheets
- Converts the structe and content of HTML into a vibrant, responsive experience.
- Can animate the page, deploy custom fonts, respond to user actions, and dynamically alter the entire layout of the page based on the size of a device and its orientation.
- Defines rulesets (rules) that are comprised of:
    -  A selector that selects the elements to apply the rule to
    - One or more declarations that represent the property to style with the given property value
![Example code](<https://github.com/webprogramming260/.github/raw/main/profile/css/introduction/cssDefinitions.jpg>)
### Associating CSS with HTML
Style:
- use the style attribute of an HTML element and assign it one or more declarations
```html
<p style="color:green">CSS</p>
```
- use the style element to define CSS rules within HTML document. Style element should be in head element
```html
<head>
  <style>
    p {
      color: green;
    }
  </style>
</head>
<body>
  <p>CSS</p>
</body>
```
Link:
- Create a hyperlink reference to an external file containing CSS rules. Must be within head element
```html
<link rel="stylesheet" href="styles.css" />
```
styles.css
```html
p {
  color: green;
}
```
### Cascading styles
Rules cascade down from the highest nodes in the DOM tree to the lowest level. Delcarations as lower levels will override the higher declaration.
### The box model
CSS defines everything as boxes
![Box Model](<https://github.com/webprogramming260/.github/raw/main/profile/css/introduction/cssBoxModel.jpg>)

You can change the box-sizing CSS property from the default value of content-box to border-box in order to redefine the width and height to also include the padding and the border.

## Selectors
### Element type selector
To change the font of all elements, use an element name selector. Select the body, which will affect the whole document.
```html
body {
  font-family: sans-serif;
}
```
(* also selects all elements instead of using body)

Could do the same with h1 (top level heading).
```html
h1 {
  border-bottom: thin black solid;
}

section {
  background: #eeeeee;
  padding: 0.25em;
  margin-bottom: 0.5em;
}
```

### Combinators
To change only the h2 in a specific section, use a descendant combinator that only affects items that are a descendant of the previous item
```html
section h2 {
  color: #004400;
}
```
Other combinations:

| Combinator       | Meaning                    | Example        | Description                                |
| ---------------- | -------------------------- | -------------- | ------------------------------------------ |
| Descendant       | A list of descendants      | `body section` | Any section that is a descendant of a body |
| Child            | A list of direct children  | `section > p`  | Any p that is a direct child of a section  |
| General sibling  | A list of siblings         | `p ~ div`      | Any p that has a div sibling               |
| Adjacent sibling | A list of adjacent sibling | `p + div`      | Any p that has an adjacent div sibling     |

### Class selector
Any element can have 0 or more classifications applied to it. If you wanted to bold text in a class called "summary":
```html
.summary {
  font-weight: bold;
}
```
Can combine element name and class selectors:
```html
p.summary {
  font-weight: bold;
}
```

### ID selector
All IDs should be unique within an HTML document, so it targets a specific element. Prefix the ID with #:
```
#physics {
  border-left: solid 1em purple;
}
```

### Attribute selector
Select elements based on their attributes. Select any element with a given attribute (a[href]). Can also specify a specific value (a[href="./fish.png"]). Also support attribute values containing a specific text ('p[href*="https://"]).
```html
p[class='summary'] {
  color: red;
}
```

### Pseudo selector
Select based on positional relationships, mouse interactions, hyperlink visitation states, and attributes. Select whenever a section is hovered over:
```html
section:hover {
  border-left: solid 1em purple;
}
```

## CSS Declarations
Specify a property and value to assign when rule selector matches one or more elements.

| Property           | Value                              | Example             | Discussion                                                                     |
| ------------------ | ---------------------------------- | ------------------- | ------------------------------------------------------------------------------ |
| background-color   | color                              | `red`               | Fill the background color                                                      |
| border             | color width style                  | `#fad solid medium` | Sets the border using shorthand where any or all of the values may be provided |
| border-radius      | unit                               | `50%`               | The size of the border radius                                                  |
| box-shadow         | x-offset y-offset blu-radius color | `2px 2px 2px gray`  | Creates a shadow                                                               |
| columns            | number                             | `3`                 | Number of textual columns                                                      |
| column-rule        | color width style                  | `solid thin black`  | Sets the border used between columns using border shorthand                    |
| color              | color                              | `rgb(128, 0, 0)`    | Sets the text color                                                            |
| cursor             | type                               | `grab`              | Sets the cursor to display when hovering over the element                      |
| display            | type                               | `none`              | Defines how to display the element and its children                            |
| filter             | filter-function                    | `grayscale(30%)`    | Applies a visual filter                                                        |
| float              | direction                          | `right`             | Places the element to the left or right in the flow                            |
| flex               |                                    |                     | Flex layout. Used for responsive design                                        |
| font               | family size style                  | `Arial 1.2em bold`  | Defines the text font using shorthand                                          |
| grid               |                                    |                     | Grid layout. Used for responsive design                                        |
| height             | unit                               | `.25em`             | Sets the height of the box                                                     |
| margin             | unit                               | `5px 5px 0 0`       | Sets the margin spacing                                                        |
| max-[width/height] | unit                               | `20%`               | Restricts the width or height to no more than the unit                         |
| min-[width/height] | unit                               | `10vh`              | Restricts the width or height to no less than the unit                         |
| opacity            | number                             | `.9`                | Sets how opaque the element is                                                 |
| overflow           | [visible/hidden/scroll/auto]       | `scroll`            | Defines what happens when the content does not fix in its box                  |
| position           | [static/relative/absolute/sticky]  | `absolute`          | Defines how the element is positioned in the document                          |
| padding            | unit                               | `1em 2em`           | Sets the padding spacing                                                       |
| left               | unit                               | `10rem`             | The horizontal value of a positioned element                                   |
| text-align         | [start/end/center/justify]         | `end`               | Defines how the text is aligned in the element                                 |
| top                | unit                               | `50px`              | The vertical value of a positioned element                                     |
| transform          | transform-function                 | `rotate(0.5turn)`   | Applies a transformation to the element                                        |
| width              | unit                               | `25vmin`            | Sets the width of the box                                                      |
| z-index            | number                             | `100`               | Controls the positioning of the element on the z axis                          |

### Units
```html
p {
  width: 25%;
  height: 30vh;
}
```
List of commonly used units. All are prefixed with a number:

| Unit | Description                                                      |
| ---- | ---------------------------------------------------------------- |
| px   | The number of pixels                                             |
| pt   | The number of points (1/72 of an inch)                           |
| in   | The number of inches                                             |
| cm   | The number of centimeters                                        |
| %    | A percentage of the parent element                               |
| em   | A multiplier of the width of the letter `m` in the parent's font |
| rem  | A multiplier of the width of the letter `m` in the root's font   |
| ex   | A multiplier of the height of the element's font                 |
| vw   | A percentage of the viewport's width                             |
| vh   | A percentage of the viewport's height                            |
| vmin | A percentage of the viewport's smaller dimension                 |
| vmax | A percentage of the viewport's larger dimension                  |

### Color

| Method       | Example                   | Description                                                                                                                                                                                                       |
| ------------ | ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| keyword      | `red`                     | A set of predefined colors (e.g. white, cornflowerblue, darkslateblue)                                                                                                                                            |
| RGB hex      | `#00FFAA22` or `#0FA2`    | Red, green, and blue as a hexadecimal number, with an optional alpha opacity                                                                                                                                      |
| RGB function | `rgb(128, 255, 128, 0.5)` | Red, green, and blue as a percentage or number between 0 and 255, with an optional alpha opacity percentage                                                                                                       |
| HSL          | `hsl(180, 30%, 90%, 0.5)` | Hue, saturation, and light, with an optional opacity percentage. Hue is the position on the 365 degree color wheel (red is 0 and 255). Saturation is how gray the color is, and light is how bright the color is. |


## CSS Fonts
Can make users want to use your application or drive them away.
CSS "font-family" propery defines the fonts used. Is an ordered list of fonts. Always defaults to first available font in list which is important bc some browsers might not have your first choice.

### Font Families
Four major one: serif (strokes at end of character's major strokes), sans-serif (no extra strokes), fixed (all same size), and symbol(non-language characters).

### Importing fonts
Allows your font to always be the same. Use @font-face rule w/ name and source location.
```html
@font-face {
  font-family: 'Quicksand';
  src: url('https://cs260.click/fonts/quicksand.woff2');
}

p {
  font-family: Quicksand;
}
```
If you don't want to host font files on your server, load from font provider (e.g. Google). Use CSS importart statement.
```html
@import url('https://fonts.googleapis.com/css2?family=Rubik Microbe&display=swap');

p {
  font-family: 'Rubik Microbe';
}
```

## CSS Animation
Created using animation properties and defining keyframes for what element should look like at different times in animation.
Centered text, zoom until size is 20% of view height.
```html
p {
  text-align: center;
  font-size: 20vh;
}
```
Add animation-name property. Add animation-duration property.
```html
p {
  text-align: center;
  font-size: 20vh;

  animation-name: demo;
  animation-duration: 3s;
}
```
Now, create keyframes. Start with invisible text and zoom into full final size.
```html
@keyframes demo {
  from {
    font-size: 0vh;
  }

  to {
    font-size: 20vh;
  }
}
```
Make it bounce out to a little bigger first. Happens 95% thru animation.
```html
@keyframes demo {
  from {
    font-size: 0vh;
  }

  95% {
    font-size: 21vh;
  }

  to {
    font-size: 20vh;
  }
}
```


## Responsive Design
Ability to reconfigure the interface to accomadate and take advantage of screen's size and orientation.
### Display
| Value  | Meaning                                                                                                                      |
| ------ | ---------------------------------------------------------------------------------------------------------------------------- |
| none   | Don't display this element. The element still exists, but the browser will not render it.                                    |
| block  | Display this element with a width that fills its parent element. A `p` or `div` element has block display by default.        |
| inline | Display this element with a width that is only as big as its content. A `b` or `span` element has inline display by default. |
| flex   | Display this element's children in a flexible orientation.                                                                   |
| grid   | Display this element's children in a grid orientation.                                                                       |

Demonstration using many div elements, which by default have the display property of "block":
```html
<div class="none">None</div>
<div class="block">Block</div>
<div class="inline">Inline1</div>
<div class="inline">Inline2</div>
<div class="flex">
  <div>FlexA</div>
  <div>FlexB</div>
  <div>FlexC</div>
  <div>FlexD</div>
</div>
<div class="grid">
  <div>GridA</div>
  <div>GridB</div>
  <div>GridC</div>
  <div>GridD</div>
</div>
```
Which would look like this:

![block example](<https://github.com/webprogramming260/.github/raw/main/profile/css/responsive/cssDisplayDefault.jpg>)

Modify the display property of each element, getting a completely different rendering.
```html
.none {
  display: none;
}

.block {
  display: block;
}

.inline {
  display: inline;
}

.flex {
  display: flex;
  flex-direction: row;
}

.grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
}
```
![Another exaple](<https://github.com/webprogramming260/.github/raw/main/profile/css/responsive/cssDisplay.jpg>)

### Viewport meta tag
Include meta tag in head element of html pages so that browser doesn't scale the page:
```html
<meta name="viewport" content="width=device-width,initial-scale=1" />
```

### Float
Moves element to left or right and allows inline elements to wrap around it.
```html
aside {
  float: right;
  padding: 3em;
  margin: 0.5em;
  border: black solid thin;
}
```
![Example](<https://github.com/webprogramming260/.github/raw/main/profile/css/responsive/cssFloat.gif>)

### Media queries
@media selector detects size and orientation of device and aplies rules to accommadate the change
If orientation is portrait:
```html
@media (orientation: portrait) {
  div {
    transform: rotate(270deg);
  }
}
```
Can also make entire pieces disappear or move to different location:
```html
@media (orientation: portrait) {
  aside {
    display: none;
  }
}
```

## CSS Grid
Grid display layout is for displaying child elements in responsive grid.
Use display property with value "grid" on the parent element. "grid-template-columns" property which specifies layout of grid columns. minimum 300 pixels and max "1fr" (equal fractional unit) (fill parent's width). Fractional unitsplits up parent element's width into equal parts for children. 300 pixels high with "grid-auto-rows" property and "grid-gap" property says we want >= 1em gap between itmes.
```html
.container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  grid-auto-rows: 300px;
  grid-gap: 1em;
}
```
![example](<https://github.com/webprogramming260/.github/raw/main/profile/css/grid/cssGrid.gif>)


## CSS Flexbox
"flex" display layout partitions application into areas that move as window resizes or changes orientation.
Include CSS display property w/ value "flex". "flex-directions" property w/ "column" to make column oriented.
```html
body {
  display: flex;
  flex-direction: column;
  margin: 0;
  height: 100vh;
}
```
Ex: flex: 0 80px - 0 means it won't grow and has starting height of 80px. Fixed size box
flex: 1 - gets 1 fractional unit of growth, will get remaining space since it's the only non-zero growth value.
flex-direction: row - children are oriented side by side
```html
header {
  flex: 0 80px;
  background: hsl(223, 57%, 38%);
}

footer {
  flex: 0 30px;
  background: hsl(180, 10%, 10%);
}

main {
  flex: 1;
  display: flex;
  flex-direction: row;
}
```
1st one gets 1 unit (25%) of space and content gets 3 (rest of) space. Will always remain constant no matter how we resize things.
```html
section:nth-child(1) {
  flex: 1;
  background-color: hsl(180, 10%, 80%);
}
section:nth-child(2) {
  flex: 3;
  background-color: white;
}
```

### Media Query
Drops the header and footer if the viewport gets too short, and orient the main sections as rows if it gets too narrow.
Support narrow screen (portrait mode), check if we're in portrait mode and sets "flex-direction" to be column instead of row
Make header and footer disappear: triggers when viewport has max value of 700px. Change "display" for header and footer to "none"
```html
@media (orientation: portrait) {
  main {
    flex-direction: column;
  }
}

@media (max-height: 700px) {
  header {
    display: none;
  }
  footer {
    display: none;
  }
}
```

## CSS Frameworks
Open source repositories that make web development easier. Basically, allows you to do CSS really fast.

### Tailwind
A new contender in CSS framework space. Is different than most bc it uses smaller definitions that are applied specifically to individual HTML elements.
```html
<div class="pt-6 md:p-8 text-center md:text-left space-y-4">
  <img class="w-24 h-24 md:w-48 md:h-auto md:rounded-none rounded-full mx-auto" src="profile.png" />
  <p class="text-lg font-medium">“Tailwind CSS”</p>
</div>
```

### Bootstrap
Getting started with Bootstrap: https://getbootstrap.com/docs/5.2/getting-started/introduction/
1. Include <meta name="viewport"> in html file for proper responsive behavior in mobile devices.
2. Place <link> tag in <head> for Bootstrap CSS, and <script> tag for Bootstrap JavaScript bundle before closing </body>.
3. Now you can start building w/ Bootstrap

Bootstrap is the favorite CSS framework. Bc it's so popular, users recognize the style and how to use a website like it, but it may not grab their attention.

#### Getting bootstrap
This references bootstrap CSS files from their content delivery network(CDN) and adds HTML link elements to head element:
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css"
      rel="stylesheet"
      integrity="sha384-rbsA2VBKQhggwzxH7pPCaAqO46MgnOM80zW1RWuH61DGLwZJEdK2Kadq2F9CUG65"
      crossorigin="anonymous"
    />
  </head>
  <body>
    ...
  </body>
</html>
```
If you use bootstrap components that involve JavaScript, include bootstrap's JavaScript module at the end of your HTML body element.
```html
<body>
  ...
  <script
    src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/js/bootstrap.bundle.min.js"
    integrity="sha384-kenU1KFdBIe4zVF0s0G1M5b4hcpxyD9F7jL+jjXkk+Q2h455rYXK/7HAuoJl+0I4"
    crossorigin="anonymous"
  ></script>
</body>
```
To include bootstrap using NPM in your application (numbers are the specific version):
```html
npm install bootstrap@5.2.3
```
#### Using bootstrap
Simple button: btn gets the button and btn-primary shades the button which defaults to Blue
```html
// Bootstrap styled button
<button type="button" class="btn btn-primary">Bootstrap</button>

// Default browser styled button
<button type="button">Plain</button>
```

# JavaScript
Most used programming language in the world.

## Getting Started
Concatenate a string and output string to debugger console:
```js
console.log('Hello' + ' ' + 'world');
```
Build functions:
```js
function join(a, b) {
  return a + ' ' + b;
}
console.log(join('Hello', 'world'));
```

## Comments
```js
// Line comment

/*
Block comment
*/
```
## Playgrounds
Use codepen or use F12 in Chrome to open debugger and open debugger to code JS.

## JS Console
Provides interaction w/ JS runtime's debugger console.

### Log
Create formatted messages:
```js
console.log('hello %s', 'world');
// OUTPUT: hello world
```
Styled log output:
```js
console.log('%c JavaScript Demo', 'font-size:1.5em; color:green;');
// OUTPUT: JavaScript Demo //in large green text
```

### Timers
Wrap piece of code w/ "time" and "timeEnd" and will output duration between time and timeEnd:
```js
console.time('demo time');
// ... some code that takes a long time.
console.timeEnd('demo time');
// OUTPUT: demo time: 9762.74 ms
```

### Count
See how many times a block of code is called:
```js
console.count('a');
// OUTPUT: a: 1
console.count('a');
// OUTPUT: a: 2
console.count('b');
// OUTPUT: b: 1
```

## Adding JS to HTML
Can add directly to HTML using <script> element or src attribute references outside JS file.
index.js:
```js
function sayHello() {
  console.log('hello');
}
```
index.html:
```js
<head>
  <script src="javascript.js"></script>
</head>
<body>
  <button onclick="sayHello()">Say Hello</button>
  <button onclick="sayGoodbye()">Say Goodbye</button>
  <script>
    function sayGoodbye() {
      alert('Goodbye');
    }
  </script>
</body>
```

## JS Type and Construct
### Declaring variables
Declared using let or const. Let allows the variable to be changed while const will cause an error if you try to change it.
### Type
| Type        | Meaning                                                    |
| ----------- | ---------------------------------------------------------- |
| `Null`      | The type of a variable that has not been assigned a value. |
| `Undefined` | The type of a variable that has not been defined.          |
| `Boolean`   | true or false.                                             |
| `Number`    | A 64 bit signed number.                                    |
| `BigInt`    | A number of arbitrary magnitude.                           |
| `String`    | A textual sequence of characters.                          |
| `Symbol`    | A unique value.                                            |

Object types:
| Type       | Use                                                                                    | Example                  |
| ---------- | -------------------------------------------------------------------------------------- | ------------------------ |
| `Object`   | A collection of properties represented by name value pairs. Values can be of any type. | `{a:3, b:'fish'}`        |
| `Function` | An object that has the ability to be called.                                           | `function a() {}`        |
| `Date`     | Calendar dates and times.                                                              | `new Date('1995-12-17')` |
| `Array`    | An ordered sequence of any type.                                                       | `[3, 'fish']`            |
| `Map`      | A collection of key value pairs that support efficient lookups.                        | `new Map()`              |
| `JSON`     | A lightweight data-interchange format used to share information across programs.       | `{"a":3, "b":"fish"}`    |

### Type Conversions
JS is weakly typed, type of var can change. Automatic, unexpected conversions can occurr:
```js
2 + '3';
// OUTPUT: '23'
2 * '3';
// OUTPUT: 6
[2] + [3];
// OUTPUT: '23'
true + null;
// OUTPUT: 1
true + undefined;
// OUTPUT: NaN
```
Dealing with the equality operator:
```js
1 == '1';
// OUTPUT: true
null == undefined;
// OUTPUT: true
'' == false;
// OUTPUT: true
```
Use === and !== to get correct answers
```js
1 === '1';
// OUTPUT: false
null === undefined;
// OUTPUT: false
'' === false;
// OUTPUT: false
```

### Conditionals
Supports if, else, and if else. Includes compact if else (ternary operator):
```js
a === 1 ? console.log(1) : console.log('not 1');
```
Uses && || and !
if:
```js
if (a === 1) {
  //...
} else if (b === 2) {
  //...
} else {
  //...
}
```

### Loops
Suppors for (let i = 0; i < 2; i++), for in, for of, while, do while and switch:
do while:
```js
let i = 0;
do {
  console.log(i);
  i++;
} while (i < 2);
// OUTPUT: 0 1
```
for in iterates over object's property names. gets the index values for an array:
```js
const obj = { a: 1, b: 'fish' };
for (const name in obj) {
  console.log(name);
}
// OUTPUT: a
// OUTPUT: b
```
for of iteratoes over property values:
```js
const arr = ['a', 'b'];
for (const val of arr) {
  console.log(val);
}
// OUTPUT: 'a'
// OUTPUT: 'b'
```
Able to use "break" and "continue"
switch:
```js
switch (expression) {
  case value1:
    // Code to be executed if expression === value1
    break;
  case value2:
    // Code to be executed if expression === value2
    break;
  // More cases can be added as needed
  default:
    // Code to be executed if expression doesn't match any case
}
```

## JS String
Single and double quotes are equivalent, but ` backticks defines string literal that may contain JS that is evaluated in place and concatenated into the string. literal replacement specifier is declared by ${}.
```js
const l = 'literal';
console.log(`string ${l + (1 + 1)} text`);
// OUTPUT: string literal2 text
```
### Unicode Support
Defines string as 16-bit unsigned integer representing UTF-16 strings. Allows it to represent most languages.
### String functions
| Function      | Meaning                                                      |
| ------------- | ------------------------------------------------------------ |
| length        | The number of characters in the string                       |
| indexOf()     | The starting index of a given substring                      |
| split()       | Split the string into an array on the given delimiter string |
| startsWith()  | True if the string has a given prefix                        |
| endsWith()    | True if the string has a given suffix                        |
| toLowerCase() | Converts all characters to lowercase                         |

## Functions
1st class objects: can be passed as parameter, returned, and referenced from object or array.
Functino begins w/ "function" keyword.
### Parameters
Caller may choose which parameters to provide. If a parameter isn't provided, it is "undefined" when functione executes.
### Anonymous functions
Functions are often assigned to var so they can be passed as parameter to some other function or stored as obj property.
## JS Arrow Function
Used to make code more compact. Basically a lambda with => placed after the parameter declaration. These 2 are equal:
```js
const a = [1, 2, 3, 4];

// standard function syntax
a.sort(function (v1, v2) {
  return v1 - v2;
});

// arrow function syntax
a.sort((v1, v2) => v1 - v2);
```
Can't be used for constructors or iterator generators.
Return values are optional if no curly brackets and only contains a single expression. If there are curly brackets, it behaves as a standard runction.
Debounce function only executes a specified function once within a given time window.

## JS Array
Functions:
| Function | Meaning                                                   | Example                       |
| -------- | --------------------------------------------------------- | ----------------------------- |
| push     | Add an item to the end of the array                       | `a.push(4)`                   |
| pop      | Remove an item from the end of the array                  | `x = a.pop()`                 |
| slice    | Return a sub-array                                        | `a.slice(1,-1)`               |
| sort     | Run a function to sort an array in place                  | `a.sort((a,b) => b-a)`        |
| values   | Creates an iterator for use with a `for of` loop          | `for (i of a.values()) {...}` |
| find     | Find the first item satisfied by a test function          | `a.find(i => i < 2)`          |
| forEach  | Run a function on each array item                         | `a.forEach(console.log)`      |
| reduce   | Run a function to reduce each array item to a single item | `a.reduce((a, c) => a + c)`   |
| map      | Run a function to map an array to a new array             | `a.map(i => i+i)`             |
| filter   | Run a function to remove items                            | `a.filter(i => i%2)`          |
| every    | Run a function to test if all items match                 | `a.every(i => i < 3)`         |
| some     | Run a function to test if any items match                 | `a.some(i => 1 < 1)`          |

## JSON
A simple way to share and store data. Easily convertible to and from JS objects.
### Format
Contains one of the following data types:
| Type    | Example                 |
| ------- | ----------------------- |
| string  | "crockford"             |
| number  | 42                      |
| boolean | true                    |
| array   | [null,42,"crockford"]   |
| object  | {"a":1,"b":"crockford"} |
| null    | null                    |

Most common is an object. Key is a string and value is valid JSON data types. 
Ex JSON document:
```js
{
  "class": {
    "title": "web programming",
    "description": "Amazing"
  },
  "enrollment": ["Marco", "Jana", "فَاطِمَة"],
  "start": "2025-02-01",
  "end": null
}
```
Always encoded w/ UTF-8.
### Converting to JS
Use JSON.parse and JSON.stringify functions.
```js
const obj = { a: 2, b: 'crockford', c: undefined };
const json = JSON.stringify(obj);
const objFromJson = JSON.parse(json);

console.log(obj, json, objFromJson);

// OUTPUT:
// {a: 2, b: 'crockford', c: undefined}
// {"a":2, "b":"crockford"}
// {a: 2, b: 'crockford'}
```
JSON can't represent JS undefined object so it gets dropped in conversion.

## JS Regular Expressions
Textual pattern matchers. Can be using class constructor or regular expression literal:
```js
const objRegex = new RegExp('ab*', 'i');
const literalRegex = /ab*/i;
```
string functions that accept regular expressions: match, replace, search and split. Test function sees if there's a match
```js
const petRegex = /(dog)|(cat)|(bird)/gim;
const text = 'Both cats and dogs are pets, but not rocks.';

text.match(petRegex);
// RETURNS: ['cat', 'dog']

text.replace(petRegex, 'animal');
// RETURNS: Both animals and animals are pets, but not rocks.

petRegex.test(text);
// RETURNS: true
```
## JS rest and spread
### Rest
If we want a function to take unknown # of parameters, we use rest syntax. To turn las parameter of function into "rest" parameter, prefix it w/ 3 periods. Then, any number of parameters are automatically combined into an array:
```js
function hasNumber(test, ...numbers) {
  return numbers.some((i) => i === test);
}

hasNumber(2, 1, 2, 3);
// RETURNS: true
```
### Spread
Spread does opposite of rest. Takes object that is iterable (array, string, etc.) and expands it into function's parameters:
```js
function person(firstName, lastName) {
  return { first: firstName, last: lastName };
}

const p = person(...['Ryan', 'Dahl']);
console.log(p);
// OUTPUT: {first: 'Ryan', last: 'Dahl'}
```
## JS Exceptions
Supports try catch and throw syntax. Can also specify a finally block that is always called wether or not an exception was thrown:
```js
try {
  // normal execution code
} catch (err) {
  // exception handling code
} finally {
  // always called code
}
```
Try to restrict exceptions to truly exceptional situations such as running when a file isn't found that's necessary to run the code.
### Fallbacks
Often implemented using exception handling. Allows you to always return something, even if the desired feature is temporarily unavailable.
```js
function getScores() {
  try {
    const scores = scoringService.getScores();
    // store the scores so that we can use them later if the network is not available
    window.localStorage.setItem('scores', scores);
    return scores;
  } catch {
    return window.localStorage.getItem('scores');
  }
}
```

## JS destructuring
Process of pulling idividual items out of existing one (or removing structure). Example:
```js
const a = [1, 2, 4, 5];

// destructure the first two items from a, into the new variables b and c
const [b, c] = a;

console.log(b, c);
// OUTPUT: 1, 2
```
Can combine multiple items from the original object using rest syntax:
```js
const [b, c, ...others] = a;

console.log(b, c, others);
// OUTPUT: 1, 2, [4,5]
```
When destructuring objects, explicity specify properties you want to pull from source object:
```js
const o = { a: 1, b: 'animals', c: ['fish', 'cats'] };

const { a, c } = o;

console.log(a, c);
// OUTPUT 1, ['fish', 'cats']
```
Can map names to new variables:
```js
const o = { a: 1, b: 'animals', c: ['fish', 'cats'] };

const { a: count, b: type } = o;

console.log(count, type);
// OUTPUT 1, animals
```
Default values can be provided for missing ones:
```js
const { a, b = 22 } = {};
const [c = 44] = [];

console.log(a, b, c);
// OUTPUT: undefined, 22, 44
```
Reassign existing values:
```js
let a = 22;

[a] = [1, 2, 3];

console.log(a);
// OUTPUT: 1
```

## JS Object and classes
JS obj represents collection of name value pairs called properties. Property name must be String/Symbol, value can be anything. Have constructors, "this" pointer, static properties/functions, and inheritance. Properties can be referenced w/ dot (obj.prop) or brackets (obj['prop']). Can add new properties w/ js.
```js
const obj = new Object({a:3});
obj['b'] = 'fish';
obj.c = [1, 2, 3];
obj.hello = function () {
  console.log('hello');
};

console.log(obj);
// OUTPUT: {a: 3, b: 'fish', c: [1,2,3], hello: func}
```
### Object-literals
Can declare variable of obj type w/ object-literal syntax. Allows you to provide initial composition of obj:
```js
const obj = {
  a: 3,
  b: 'fish',
};
```
### Obj Functions
Commonly used ones:
| Function | Meaning                             |
| -------- | ----------------------------------- |
| entries  | Returns an array of key value pairs |
| keys     | Returns an array of keys            |
| values   | Returns an array of values          |
```js
const obj = {
  a: 3,
  b: 'fish',
};

console.log(Object.entries(obj));
// OUTPUT: [['a', 3], ['b', 'fish']]
console.log(Object.keys(obj));
// OUTPUT: ['a', 'b']
console.log(Object.values(obj));
// OUTPUT: [3, 'fish']
```
### Constructor
Invoked w/ "new" operator:
```js
function Person(name) {
  return {
    name: name,
  };
}

const p = new Person('Eich');
console.log(p);
// OUTPUT: {name: 'Eich'}
```
Can create methods on obj as part of its encapsulation:
```js
function Person(name) {
  return {
    name: name,
    log: function () {
      console.log('My name is ' + this.name);
    },
  };
}

const p = new Person('Eich');
p.log();
// OUTPUT: My name is Eich
```
### Classes
Used to define objects. Person obj above would look like this when converted to a class:
```js
class Person {
  constructor(name) {
    this.name = name;
  }

  log() {
    console.log('My name is ' + this.name);
  }
}

const p = new Person('Eich');
p.log();
// OUTPUT: My name is Eich
```
Make properties/functions private by prefixing them with a #.
### Inheritance
Classes can be extended using "extends" keyword to define inheritance. Parameters passed to parent class are delivered using "super" function. Functions w/ same name as parent override the parent function. Parent function used explicity using "super" keyword:
```js
class Person {
  constructor(name) {
    this.name = name;
  }

  print() {
    return 'My name is ' + this.name;
  }
}

class Employee extends Person {
  constructor(name, position) {
    super(name);
    this.position = position;
  }

  print() {
    return super.print() + '. I am a ' + this.position;
  }
}

const e = new Employee('Eich', 'programmer');
console.log(e.print());
// OUTPUT: My name is Eich. I am a programmer
```

## Scope
Scope is defined as the variables that're visible in the current context of exectution. JS has 4 types of scope:
1. Global - Visible to all code
2. Module - Visible to all code running in a module
3. Function - Visible within a function
4. Block - Visible within a block of code delimited by curly braces
### VAR
When var is used to declare a variable, it ignores block scope. Automatically brought to top of the function. 
### This
Represents variable that points to obj. Automatically declared and can be accessed anywhere in JS program. 3 different context this can refer to:
1. Global - When this is referenced outside a func or obj, refers to "globalThis" obj. Represents context for runtime environment.
2. Function - When this is referenced in a cun, refers to obj that owns the func. 
3. Object - When this is referenced in obj refers to the obj.
### Closure
Defined as a function and its surrounding state. That means whatever variables are accessible when a func is created are available inside of that func. 
```js
globalThis.x = 'global';

const obj = {
  x: 'object',
  f: function () {
    console.log(this.x);
  },
};

obj.f();
// OUTPUT: object
```
Arrow functions inherit pointer of their creation context.
```js
globalThis.x = 'global';

const obj = {
  x: 'object',
  f: () => console.log(this.x),
};

obj.f();
// OUTPUT: global
```
But when it is made inside the context of the obj:
```js
globalThis.x = 'global';

const obj = {
  x: 'object',
  make: function () {
    return () => console.log(this.x);
  },
};

const f = obj.make();
f();
// OUTPUT: object
```

## JS Modules
Allow for partitioning and sharing of code. Node.js modules are called CommonJS modules. JS modules are called ES modules. We're focusing only on ES modules.
Must explicitly export obj from one file and import to other. 
alert.js
```js
export function alertDisplay(msg) {
  alert(msg);
}
```
main.js
```js
import { alertDisplay } from './alert.js';

alertDisplay('called from main.js');
```
### ES Modules in the browser
Cannot access JS contained in module from global scope that your non-module JS is executing in.
From HTML, can specify use of ES module by including "type" attribute w/ value of "module" in "script" element. Then can import and use other modules.
index.html
```html
<script type="module">
  import { alertDisplay } from './alert.js';
  alertDisplay('module loaded');
</script>
```
If we want to use module in global scope that HTML or other non-module JS is executing in, must leak it into global scope by attaching it to event handler or explicitly adding it to a function, to global window obj. 
index.html
```js
<html>
  <body>
    <script type="module">
      import { alertDisplay } from './alert.js';
      window.btnClick = alertDisplay;

      document.body.addEventListener('keypress', function (event) {
        alertDisplay('Key pressed');
      });
    </script>
    <button onclick="btnClick('button clicked')">Press me</button>
  </body>
</html>
```
### Modules with web frameworks
Generally don't have to worry abt differentiating between global scope and ES module scope when using web framework bundler

## Document Object Model
DOM is an obj representation of HTML elements that browser uses to render display. Allows you to write programs that dynamically manipulate the HTML.
Browser provides access to DOM thru global variable "document".
### Accessing the DOM
Every element in HTML doc implements the DOM Element interface, derived from DOM Node interface. Provides means for iterating child elements, accessing parent element and manipulating element's attributes. In JS, start w/ "document" var and wakl thru each element in the tree.
```js
function displayElement(el) {
  console.log(el.tagName);
  for (const child of el.children) {
    displayElement(child);
  }
}

displayElement(document);
```
Can procide CSS selector to "querySelectorAll" func in order to select elements from doc. "textContent" property contains all of element's text. Can access text representation of element's HTML content w/ "innerHTML" property.
```js
const listElements = document.querySelectorAll('p');
for (const el of listElements) {
  console.log(el.textContent);
}
```
### Modifying the DOM
Can insert, modify or delete elements in DOM. Add element:
```js
function insertChild(parentSelector, text) {
  const newChild = document.createElement('div');
  newChild.textContent = text;

  const parentElement = document.querySelector(parentSelector);
  parentElement.appendChild(newChild);
}

insertChild('#courses', 'new course');
```
Delete elements w/ "removeChild" func:
```js
function deleteElement(elementSelector) {
  const el = document.querySelector(elementSelector);
  el.parentElement.removeChild(el);
}

deleteElement('#courses div');
```
### Injecting HTML
Can inject entire blocks of HTML into an element. This code finds 1st "div" and replaces it w/ all HTML it contains:
```js
const el = document.querySelector('div');
el.innerHTML = '<div class="injected"><b>Hello</b>!</div>';
```
Make sure injected HTML can't be manipulated by user.
### Event Listeners
Can attach a func that gets called when an event occurs in the element. Called "event listeners". Here's one when the element's clicked:
```js
const submitDataEl = document.querySelector('#submitData');
submitDataEl.addEventListener('click', function (event) {
  console.log(event.type);
});
```
Some commonly used events:
| Event Category | Description           |
| -------------- | --------------------- |
| Clipboard      | Cut, copied, pasted   |
| Focus          | An element gets focus |
| Keyboard       | Keys are pressed      |
| Mouse          | Click events          |
| Text selection | When text is selected |
Can be added directly to HTML:
```html
<button onclick='alert("clicked")'>click me</button>
```

## Local Storage
localStorage api in browser provides ability to store and retrieve data (scores, usernames, etc.) on user's browser across sessions and HTML page renderings. Also cache for when data can't be obtained from server.

### How to use LocalStorage
4 main functions:
| Function             | Meaning                                      |
| -------------------- | -------------------------------------------- |
| setItem(name, value) | Sets a named item's value into local storage |
| getItem(name)        | Gets a named item's value from local storage |
| removeItem(name)     | Removes a named item from local storage      |
| clear()              | Clears all items in local storage            |
Value must be type string, number or boolean.

Ex:
```js
let user = 'Alice';

let myObject = {
  name: 'Bob',
  info: {
    favoriteClass: 'CS 260',
    likesCS: true,
  },
};

let myArray = [1, 'One', true];

localStorage.setItem('user', user);
localStorage.setItem('object', JSON.stringify(myObject));
localStorage.setItem('array', JSON.stringify(myArray));

console.log(localStorage.getItem('user'));
console.log(JSON.parse(localStorage.getItem('object')));
console.log(JSON.parse(localStorage.getItem('array')));
```
## Promises
In JS, only 1 piece of code executes at a time. Can asynchronously execute code w/ use of JS Promise. Promise obj can be in 1 of 3 states:
1. pending - currently running asynchronously
2. fulfilled - completed successfully
3. rejected - failed to complte
Ex:
```js
const delay = (msg, wait) => {
  setTimeout(() => {
    console.log(msg, wait);
  }, 1000 * wait);
};

new Promise((resolve, reject) => {
  // Code executing in the promise
  for (let i = 0; i < 3; i++) {
    delay('In promise', i);
  }
});

// Code executing after the promise
for (let i = 0; i < 3; i++) {
  delay('After promise', i);
}

// OUTPUT:
//   In promise 0
//   After promise 0
//   In promise 1
//   After promise 1
//   In promise 2
//   After promise 2
```
### Resolving and rejecting
Must set state to fulfilled or rejected once done. Promise executor func takes 2 funcs as parameters, resolve and reject. Resolve sets to fulfilled state while reject sets to rejected state.
"coin toss" waits 10 sec then has 50% chance of resolving/rejecting:
```js
const coinToss = new Promise((resolve, reject) => {
  setTimeout(() => {
    if (Math.random() > 0.5) {
      resolve('success');
    } else {
      reject('error');
    }
  }, 10000);
});
```
Logging promise to console right after calling it:
```js
console.log(coinToss);
// OUTPUT: Promise {<pending>}
```
Wait 10 sec will be fulfilled or rejected:
```js
console.log(coinToss);
// OUTPUT: Promise {<fulfilled>}
```
### Then, catch, finally
We must do something w/ result of promise. Promsie has 3 funcs: then, catch and finally. Then is called if promise is fulfilled. Catch called if rejected. Finally called after all processing is completed.
```js
const coinToss = new Promise((resolve, reject) => {
  setTimeout(() => {
    if (Math.random() > 0.1) {
      resolve(Math.random() > 0.5 ? 'heads' : 'tails');
    } else {
      reject('fell off table');
    }
  }, 10000);
});

coinToss
  .then((result) => console.log(`Coin toss result: ${result}`))
  .catch((err) => console.log(`Error: ${err}`))
  .finally(() => console.log('Toss completed'));

// OUTPUT:
//    Coin toss result: tails
//    Toss completed
```
### The observer pattern
"Observer" pattern can run things asynchronously in JS. Observers can be reused, and result of executing an Observable can be saved as history of a particular execution.

## JS Async/await
Makes a more concise representation of prosmises. "await" wraps execution of promise and removed need to chain functions. Will block until promise is fulfilled or throw exception if rejected. Coin toss promise:
```js
const coinToss = () => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (Math.random() > 0.1) {
        resolve(Math.random() > 0.5 ? 'heads' : 'tails');
      } else {
        reject('fell off table');
      }
    }, 1000);
  });
};
```
Can create equivalent execution w/ then/catch or w/ await w/ try/catch block:
then/catch chain version:
```js
coinToss()
  .then((result) => console.log(`Toss result ${result}`))
  .catch((err) => console.error(`Error: ${err}`))
  .finally(() => console.log(`Toss completed`));
```
async, try/catch:
```js
try {
  const result = await coinToss();
  console.log(`Toss result ${result}`);
} catch (err) {
  console.error(`Error: ${err}`);
} finally {
  console.log(`Toss completed`);
}
```
### async
Can't vall await unless it's called at top level of JS, or is in func that's defined w/ async keyword. 
```js
function cow() {
  return 'moo';
}
console.log(cow());
// OUTPUT: moo
```
Now designated as asynchronous:
```js
async function cow() {
  return 'moo';
}
console.log(cow());
// OUTPUT: Promise {<fulfilled>: 'moo'}
```
Explicitly create a promise
```js
async function cow() {
  return new Promise((resolve) => {
    resolve('moo');
  });
}
console.log(cow());
// OUTPUT: Promise {<pending>}
```
### await
Declares that a func returns a promise. Wraps a call to asyn func, blocks execution until resolves and returns reult of promise.
Let's us return result of promise instead of actual promise obj:
```js
console.log(cow());
// OUTPUT: Promise {<pending>}

console.log(await cow());
// OUTPUT: moo
```
Promise:
```js
const httpPromise = fetch('https://simon.cs260.click/api/user/me');
const jsonPromise = httpPromise.then((r) => r.json());
jsonPromise.then((j) => console.log(j));
console.log('done');

// OUTPUT: done
// OUTPUT: {email: 'bud@mail.com', authenticated: true}
```
async/await:
```js
const httpResponse = await fetch('https://simon.cs260.click/api/user/me');
const jsonResponse = await httpResponse.json();
console.log(jsonResponse));
console.log('done');

// OUTPUT: {email: 'bud@mail.com', authenticated: true}
// OUTPUT: done
```

### Changing CSS contents w/ JS
Changing the text color of an element w/ id of "byu" to green:
```js
// Select the element with the id "byu"
var element = document.getElementById("byu");

// Change the text color to green
element.style.color = "green";
```

# Web Services
## Introduction
From our frontend JS we can make requests to a web service by using the fetch function that's built into the browser. Our web service will provde static frontend files w/ functions to handle fetch requests for things like sotring data persistently, providing security, running tasks, executing application logic that you don't want your user to be able to see, and communicating with other users. This is the "backend" of your app.
Functions provided by a web service are called "endpoints" or APIs. Access web service endpoints from frontend JS w/ fetch function. 
Backend web service can use fetch to make requests to other web services.
## URL
Uniform Resource Locator (URL) represents location of a web resource. Could be anything temporary or permanent.
Most parts of the url are optional. The only required ones are the scheme and the domain name:
```html
https://byu.edu:443/cs/260/student?filter=accepted#summary
<scheme>://<domain name>:<port>/<path>?<parameters>#<anchor>
```
| Part        | Example                              | Meaning                                                                                                                                                                                                                                                                             |
| ----------- | ------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Scheme      | https                                | The protocol required to ask for the resource. For web applications, this is usually HTTPS. But it could be any internet protocol such as FTP or MAILTO.                                                                                                                            |
| Domain name | byu.edu                              | The domain name that owns the resource represented by the URL.                                                                                                                                                                                                                      |
| Port        | 3000                                 | The port specifies the numbered network port used to connect to the domain server. Lower number ports are reserved for common internet protocols, higher number ports can be used for any purpose. The default port is 80 if the scheme is HTTP, or 443 if the scheme is HTTPS.     |
| Path        | /school/byu/user/8014                | The path to the resource on the domain. The resource does not have to physically be located on the file system with this path. It can be a logical path representing endpoint parameters, a database table, or an object schema.                                                    |
| Parameters  | filter=names&highlight=intro,summary | The parameters represent a list of key value pairs. Usually it provides additional qualifiers on the resource represented by the path. This might be a filter on the returned resource or how to highlight the resource. The parameters are also sometimes called the query string. |
| Anchor      | summary                              | The anchor usually represents a sub-location in the resource. For HTML pages this represents a request for the browser to automatically scroll to the element with an ID that matches the anchor. The anchor is also sometimes called the hash, or fragment ID.                     |
### URL, URN, URI
Uniform Resource Name (URN) is unique resource name that doesn't specify location info. Uniform Resource Identifier (URI) is a general resource indentifier that could refer to either a URL or URN.

## Ports
To connect to a device on the internet, you need both IP address and a numbered port. Port numbers allow a single device to support multiple protocals (http, https, ftp, SSH, etc.) and different types of services (search, document, authentication, etc.). Ports may be exposed externally or may only be used internally on device. 
Ports from 0 to 1023 represent standard protocols. Ports from 1024 to 49151 represent ports assigned to requesting entities, but common for these to be used by services running internally on a device. Ports from 49152 to 65535 are considered dynamis and are used to create dynamic connections to a device. Common port numbers:
| Port | Protocol                                                                                           |
| ---- | -------------------------------------------------------------------------------------------------- |
| 20   | File Transfer Protocol (FTP) for data transfer                                                     |
| 22   | Secure Shell (SSH) for connecting to remote devices                                                |
| 25   | Simple Mail Transfer Protocol (SMTP) for sending email                                             |
| 53   | Domain Name System (DNS) for looking up IP addresses                                               |
| 80   | Hypertext Transfer Protocol (HTTP) for web requests                                                |
| 110  | Post Office Protocol (POP3) for retrieving email                                                   |
| 123  | Network Time Protocol (NTP) for managing time                                                      |
| 161  | Simple Network Management Protocol (SNMP) for managing network devices such as routers or printers |
| 194  | Internet Relay Chat (IRC) for chatting                                                             |
| 443  | HTTP Secure (HTTPS) for secure web requests                                                        |
### Your ports
When you built your web server, you internally exposed port 22 to use SSH to open a remove console on the server, port 443 for secure HTTP communication and port 80 for unsecure communication.
## HTTP
Hypertext Transfer Protocol (HTTP) is how the web talks. 
When a web client (web browser) and web server talk, they exchange HTTP requests and responses. Can see this exchange by using browser's debugger or console tool like "curl":
```sh
curl -v -s http://info.cern.ch/hypertext/WWW/Helping.html
```
### Request
HTTP request for above commant would like:
```http
GET /hypertext/WWW/Helping.html HTTP/1.1
Host: info.cern.ch
Accept: text/html
```
HTTP request has this general syntax:
```http
<verb> <url path, parameters, anchor> <version>
[<header key: value>]*
[

  <body>
]
```
First line contains "verb" of the request, followed by the path, parameters and anchor of URL, and finally the version of HTTP being used. Following lines are optional headers defined by key value pairs. After hearders there is optional body. Body starts is delimited from the headers w/ 2 new lines.
In ex. above, we askt to GET a resource found at /hypertext/WWW/Helping.html path. Version used is HTTP/1.1. It's followed by 2 headers. First specifies the requested host (domain name). Second specifies type of resources client will accept. Resource type is always MME type. We are asking for HTML.

### Response
Response to above request is this:
```http
HTTP/1.1 200 OK
Date: Tue, 06 Dec 2022 21:54:42 GMT
Server: Apache
Last-Modified: Thu, 29 Oct 1992 11:15:20 GMT
ETag: "5f0-28f29422b8200"
Accept-Ranges: bytes
Content-Length: 1520
Connection: close
Content-Type: text/html

<TITLE>Helping -- /WWW</TITLE>
<NEXTID 7>
<H1>How can I help?</H1>There are lots of ways you can help if you are interested in seeing
the <A NAME=4 HREF=TheProject.html>web</A> grow and be even more useful...
```
Has following syntax:
```http
<version> <status code> <status string>
[<header key: value>]*
[

  <body>
]
```
First line represents the version and status of the response.
### Verbs
| Verb    | Meaning                                                                                                                                                                                                                                                  |
| ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| GET     | Get the requested resource. This can represent a request to get a single resource or a resource representing a list of resources.                                                                                                                        |
| POST    | Create a new resource. The body of the request contains the resource. The response should include a unique ID of the newly created resource.                                                                                                             |
| PUT     | Update a resource. Either the URL path, HTTP header, or body must contain the unique ID of the resource being updated. The body of the request should contain the updated resource. The body of the response may contain the resulting updated resource. |
| DELETE  | Delete a resource. Either the URL path or HTTP header must contain the unique ID of the resource to delete.                                                                                                                                              |
| OPTIONS | Get metadata about a resource. Usually only HTTP headers are returned. The resource itself is not returned.                                                                                                                                              |

### Status Code
It's important to use standard HTTP status codes in HTTP responses so client of request can know how to interpret response. Codes are partitioned into 5 blocks:
- 1xx - informational
- 2xx - Success
- 3xx - Redirect to some other location, or that the previously catched resource is still valid
- 4xx - Client errors. The request is invalid
- 5xx - Server errors. The request cannot be satisfied due to an error on the server.
Common codes:
| Code | Text                                                                                 | Meaning                                                                                                                           |
| ---- | ------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------- |
| 100  | Continue                                                                             | The service is working on the request                                                                                             |
| 200  | Success                                                                              | The requested resource was found and returned as appropriate.                                                                     |
| 201  | Created                                                                              | The request was successful and a new resource was created.                                                                        |
| 204  | No Content                                                                           | The request was successful but no resource is returned.                                                                           |
| 304  | Not Modified                                                                         | The cached version of the resource is still valid.                                                                                |
| 307  | Permanent redirect                                                                   | The resource is no longer at the requested location. The new location is specified in the response location header.               |
| 308  | Temporary redirect                                                                   | The resource is temporarily located at a different location. The temporary location is specified in the response location header. |
| 400  | Bad request                                                                          | The request was malformed or invalid.                                                                                             |
| 401  | Unauthorized                                                                         | The request did not provide a valid authentication token.                                                                         |
| 403  | Forbidden                                                                            | The provided authentication token is not authorized for the resource.                                                             |
| 404  | Not found                                                                            | An unknown resource was requested.                                                                                                |
| 408  | Request timeout                                                                      | The request takes too long.                                                                                                       |
| 409  | Conflict                                                                             | The provided resource represents an out of date version of the resource.                                                          |
| 418  | [I'm a teapot](https://en.wikipedia.org/wiki/Hyper_Text_Coffee_Pot_Control_Protocol) | The service refuses to brew coffee in a teapot.                                                                                   |
| 429  | Too many requests                                                                    | The client is making too many requests in too short of a time period.                                                             |
| 500  | Internal server error                                                                | The server failed to properly process the request.                                                                                |
| 503  | Service unavailable                                                                  | The server is temporarily down. The client should try again with an exponential back off.                                         |

### Headers
Specify metadata about a request or response. Includes things like how to handle security, catching, data formats and cookies. Common headers:
| Header                      | Example                              | Meaning                                                                                                                                                                        |
| --------------------------- | ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Authorization               | Bearer bGciOiJIUzI1NiIsI             | A token that authorized the user making the request.                                                                                                                           |
| Accept                      | image/\*                             | What content format the client accepts. This may include wildcards.                                                                                                            |
| Content-Type                | text/html; charset=utf-8             | The format of the response content. These are described using standard [MIME](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types/Common_types) types. |
| Cookie                      | SessionID=39s8cgj34; csrftoken=9dck2 | Key value pairs that are generated by the server and stored on the client.                                                                                                     |
| Host                        | info.cern.ch                         | The domain name of the server. This is required in all requests.                                                                                                               |
| Origin                      | cs260.click                          | Identifies the origin that caused the request. A host may only allow requests from specific origins.                                                                           |
| Access-Control-Allow-Origin | https://cs260.click                  | Server response of what origins can make a request. This may include a wildcard.                                                                                               |
| Content-Length              | 368                                  | The number of bytes contained in the response.                                                                                                                                 |
| Cache-Control               | public, max-age=604800               | Tells the client how it can cache the response.                                                                                                                                |
| User-Agent                  | Mozilla/5.0 (Macintosh)              | The client application making the request.                                                                                                                                     |

### Body
Format of body of HTTP request/response is defined by Content-Type header. Ex: HTML text (text/html), binary image format (image/png), JSON (application/json), or JS (text/javascript). Client may specify what formats it accepts using the accept header.

### Cookies
HTTP is stateless, one request doesn't know anything about previous or future requests. A common method of tracking state is cookie. Generated by server and passed to clinet as HTTP header:
```http
HTTP/2 200
Set-Cookie: myAppCookie=tasty; SameSite=Strict; Secure; HttpOnly
```
Client caches cookie and returns it as HTTP header back to server on subsequent requests.
```http
HTTP/2 200
Cookie: myAppCookie=tasty
```
Allows server to remember user preferences, authentication credentials, track what user does. 

## SOP and CORS
Cross-origin requests: JS makes request from one domain while displaying a website from a different domain. This is a security hazard. Any website could be requesting your data by impersonating another website.
Same Origin Policy (SOP) was created to combat this. SOP only allows JS to make requests to a domain if it's the same domain that user is currently viewing. Provides significant security but introduces complications b/c other websites can't access services of other sites. Cross Origin Resource Sharing (CORS) was made to address this.
CORS allows client (browser) to specificy origin of request and let server respond w/ what origins are allowed. If the server doesn't specify what origin is allowed, browser assumes it must be the same origin.
W/ CORS, browser is protecting user from accessing course website's authentication endpoint from wrong origin. CORS only alerts user that something bad is being attempted, course website needs to implement its own precautions to stop a hacker form using its services inappropriately.
### Using third party services
Making request to own web services is on same origing so it doesn't violate SOP. If you want to make requests to different domain, then you need to make sure that domain allows requests as defined by "Access-Control-Allow-Origin" header it returns. 
If it doesn't return one, the browser assumes that all requests must be made from same origin.
If returns a value of *, any origin can make requests to this service:
```http
HTTP/2 200
access-control-allow-origin: *

Did you hear about the bread factory burning down? They say the business is toast.
```
Also succeeds if HTTP header explicitly lists your web application domain:
```http
HTTP/2 200
access-control-allow-origin: https://cs260.click

I’ll tell you something about German sausages, they’re the wurst
```
Test services you want to use before you include them in your app to make sure you'll be able to use them.

## Fetch
The fetch functino is built into the browser's JS runtime. Can call it from JS code running in a browser.
Basic usage of fetch takes a URL and returns a promise. The promise "then" function takes a callback func that is asynchronously called when requested URL content is obtained. If return content is of type application/json you can use json func on response obj to conver it to JS obj.
Make a fetch request to get and display an inspirational quote:
```js
fetch('https://api.quotable.io/random')
  .then((response) => response.json())
  .then((jsonResponse) => {
    console.log(jsonResponse);
  });
```
Response:
```jse
{
  content: 'Never put off till tomorrow what you can do today.',
  author: 'Thomas Jefferson',
};
```
To do a POST request, you populate the options parameter w/ HTTP method and headers:
```js
fetch('https://jsonplaceholder.typicode.com/posts', {
  method: 'POST',
  body: JSON.stringify({
    title: 'test title',
    body: 'test body',
    userId: 1,
  }),
  headers: {
    'Content-type': 'application/json; charset=UTF-8',
  },
})
  .then((response) => response.json())
  .then((jsonResponse) => {
    console.log(jsonResponse);
  });
```

## Service design
Web service provide interactive functionality of web app. Authenticate users, track their session state, provide, store and analyze data, connect peers, and aggregate user info. Good design results in increased productivity, satisfied users and lower processing costs.
### Model and sequence diagrams
Helpful to model application's primary obj and interactions of objs. You attempt to stay as close as possible to model that's in user's mind. 
### Leveraging HTTP
HTTP verbs like GET, POST, PUT and DELETE often mirror the designed actions of web service. Ex, web service for managing comments might list comments (GET), create comment (POST), update comment (PUT), and delete comment (DELETE). The goal is to leverage those technologies as much as possible so you don't need to recreate functionality they provide and instead take advantage of significant networking infrastructure built up HTTP. 
### Endpoints
Web service is usually divided up into multiple service endpoints. Each one provide single functional purpose. 
![HTTP](https://github.com/webprogramming260/.github/blob/main/profile/webServices/design/webServicesHTTPEndpoints.jpg)
Things to consider when designing your service's endpoints:
- Grammatical - w/ HTTP everything is a resource (think noun or obj). You act on resource w/ an HTTP ver. Ex, you might have an order resource that is contained in a store resource. You then create, get, update, and delete order resources on the store resource.
- Readable - The resource you are referencing w/ an HTTP request should be clearly readable in URL path. Ex, an order resource might contain the path to both the order and the store where the order resource resides: /store/provo/order/28502. Makes it easier to remember how to use the endpoint b/c it's human readable.
- Discoverable - As you expose resources that contain other resources, you can provide endpoints for the aggregated resources. Makes it so someone using your endpoints only has to remember the top level endpoint and then they can discover everything else. Ex, if you have a store endpoint thatt returns info abt store you can include an endpoint for working w/ a store in the response:
```http
GET /store/provo  HTTP/2
```
```http
{
  "id": "provo",
  "address": "Cougar blvd",
  "orders": "https://cs260.click/store/provo/orders",
  "employees": "https://cs260.click/store/provo/employees"
}
```
- Compatible - When you build your endpoints you want to make it so that you can add new functionality w/out breaking existing clients. Usually means that clients of your service endpoints should ignore anything they don't understand. Consider the 2 following JSON response versions:
Version1
```js
{
  "name": "John Taylor"
}
```
Version 2
```js
{
  "name": "John Taylor",
  "givenName": "John",
  "familyName": "Taylor"
}
```
By adding a new represention of the "name" field, you provide new functionality for clients that know how to use new fields w/out harming older clients that can ignore new ones and only use old representation. You usually want to keep at least 1 previous version of the endpoint to give enough time for all clients to migrate before compatibility is removed.
- Simple - Keeping your endpoints on primary resources of app helps avoid temptation to add endpoints that duplicate or create parallel access to primary resources. Helpful to write some simple class and sequence diagrams that outline primary resources before beginning to code. These resources should focus on the actual resources of the system you're modeling. They shouldn't focus on data structure or devices used to host resources. Only have 1 way to act on a resource. Endpoints should only do 1 thing.
- Documented - The Open API specification is good ex. of tooling that helps create, use, and maintain documentation of service endpoints. Should be used to make client libraries for your endpoints and a sondbox for experimentation.  Creating initial draft of endpoint doc before starting will help mentally clarify design. Provide access to endpoint doc w/ production sys helps w/ client implementations and facilitates easier maintenance of service.
3 models to expose endpoints: RPC, REST, and GraphQL
### RPC
Remote Procedure Calls (RPC) expose service endpoints as simple func calls. Usually just leverages the POST HTTP verb. Actual verb and subject of func call is repr. by func name. The name of func is entire path of URL or parameter in the POST body:
```http
POST /updateOrder HTTP/2

{"id": 2197, "date": "20220505"}
```
or
```http
POST /rpc HTTP/2

{"cmd":"updateOrder", "params":{"id": 2197, "date": "20220505"}}
```
One adv. is that it maps directly to func calls that might exist within server. Could also be disadv. b/c exposer inner working of service, coupling the endpoints and implementation.
### REST
Representational State Transfer (REST) attempts to take adv. of foundational principles of HTTP. REST HTTP verbs always act upon a resource. Operations on resource impact state of resource as it's transferred by a REST endpoint call. Allows for catching functionality of HTTP to work optimally. Ex, GET always returns same resource until PUT is executed on resource. When PUT is used, catched resource is replaced w/ updated resource.
W/ REST, updateOrder endpoint would look like the following:
```http
PUT /order/2197 HTTP/2

{"date": "20220505"}
```
Where proper HTTP verb is used and URL path uniquely identifies resource. Makes it easy for HTTP infrastructure like caching to wrok properly.
### GraphQL
Focuses on manipulation of data instead of func call (RPC) or resource (REST). Heart of GraphQL is query that specifies the desired data and how it should be joined and filtered. GraphQL was developed to address frustration concerning massive # of REST, or RPC calls, that web app client needs to make in order to support even simple UI widget.
Instead of making call for getting a store, and then a bunch for calls for gettings store's orders and employees, GraphQL would send single query that requests all of that info in one big JSON response. Serve examines the query, joins desired data, and filters out anything that wasn't wanted.  Ex:
```js
query {
  getOrder(id: "2197") {
    orders(filter: {date: {allofterms: "20220505"}}) {
      store
      description
      orderedBy
    }
  }
}
```
Helps to remove a lot of logic for parsing endpoints and mapping requests to specific resources. Basically in GraphQL, there's only one endpoint. The query endpoint.
Downside is that client now has significant power to consume resources on the server. Also difficult for server to implement authorization rights to data. However common GraphQL packages provide support for schema implementaions along w/ database adaptors for query support.

## Node.js
First successful application for deploying JS outside of a browser. Means that JS can power your entire technology stack. Often just referred to as Node. 
### Package.json
File contains:
1. Metadata abt your proj such as its name and default entry JS file
2. Commands (scripts) that you can executre to do things like run, test or distribute your code
3. Packages that this proj depends on
package-lock.json tracks the version of the package that you installed.
Main steps
1. Create your proj directory
2. Initialize it for use w/ NPM by running "npm init -y"
3. Make sure .gitignore file contains node_modules (you don't want it in your git, it's a large file)
4. Install any desired packages w/ "npm install <package name here>"
5. Add "require('<package name here>')" to your app's JS
6. Use the code the package provides in your JS
7. Run your code w/ "node index.js"
### Creating a web service
W/ JS we can write code that listens on a network port (e.g. 80, 443, etc.), receives HTTP requests, processes them and thne responds. 

## Express
Express provides support for:
1. Routing requests for service endpoints
2. Manipulating HTTP requests w/ JSON body content
3. Generating HTTP responses
4. Using "middleware" to add functionality
Create an express app by using NPM to install Express package, then calling express constructor to create Express app and listen for HTTP requests on desired port
```
➜ npm install express
```
```js
const express = require('express');
const app = express();

app.listen(8080);
```
W/ app obj you can now add HTTP routing and middleware funcs to app.
### Defining Routes
HTTP endpoints are implements in Express by defining routes that call a func based on HTTP path. Express "app" obj supports all HTTP verbs as funcs on the obj. Ex, if you want to have a route func that handles an HTTP Get request for URL path /store/provo, you would call "get" method on the app:
```js
app.get('/store/provo', (req, res, next) => {
  res.send({name: 'provo'});
});
```
"get" func takes 2 parameters, URL path matching pattern and callback func that's invoked when pattern matches. Path matching parameter is used to match against URL path of incoming HTTP request.
Callback func has 3 parameters representing HTTP request obj (req), HTTP response obj (res), and "next" routing func that Express expects to be called if routing func wants another func to generate a response.
Express app compares routing func patterns in order they are added to Express app obj. So if you have 2 routing funcs w/ patterns that both mathc, the 1st one added will be called and given the next matching func in the "next" parameter
In ex. above, we hard coded the store name to "provo." A real store endpoint would allow any store name to be provided as a parameter in path. Express supporst path parameters by prefixing parameter name w/ :. Creates map of path parameters and populates it w/ matching values found in URL path. Then reference the parameters using "req.params" obj. Using this pattern, can rewrite getStore endpoint as follows:
```js
app.get('/store/:storeName', (req, res, next) => {
  res.send({name: req.params.storeName});
});
```
If run JS using node, we can see resulf when we make HTTP request using curl:
```js
➜ curl localhost:8080/store/orem
{"name":"orem"}
```
If you wanted an endpoint that used the POST or DELETE HTTP verb then just use the post or delete func on Express app obj.
Roue path can also include limited wildcard syntax or even full regular expressions in each pattern. Here's a couple route funcs using different pattern syntax:
```js
// Wildcard - matches /store/x and /star/y
app.put('/st*/:storeName', (req, res) => res.send({update: req.params.storeName}));

// Pure regular expression
app.delete(/\/store\/(.+)/, (req, res) => res.send({delete: req.params[0]}));
```
In these examples, next parameter was omitted since we aren't calling next. If you don't call next, no following middleware funcs will be invoked for request
### Using middleware
Standard mediator/middleware pattern has 2 pieces: a mediator and middleware. Middleware represents componentized pieces of functionality. Loads the middleware components and determines their order of execution. When it receives a request, it passes it to the middleware components. Express is the mediator and middleware funcs are the middleware components.
Middleware func is similar to routing func. That's b/c routing funcs are also middleware funcs. Only difference is that routing funcs are only called if associated pattern matches. Middleware funcs are always called for every HTTP request unless preceding middleware func doesn't call next.  Has following pattern:
```js
function middlewareName(req, res, next)
```
Func parameters repr. HTTP request obj (req), HTTP response obj (res), and next func to pass processing to. Should usually call next func after completing processing so that next func can execute.
### Creating your own middleware
Could create a func that logs out the URL of request, then passes on to next func:
```js
app.use((req, res, next) => {
  console.log(req.originalUrl);
  next();
});
```
The order that you add your middleware to Express app obj control order that funcs are called. Any middleware that doesn't call next func  stops chain from continuing.
### Builtin middleware
Ex of using builtin "static" func:
```js
app.use(express.static('public'));
```
### Third party middleware
Can install middleware funcs w/ NPM and include the package in your JS w/ "require" func. Ex of cookie-parser:
```js
const cookieParser = require('cookie-parser');

app.use(cookieParser());

app.post('/cookie/:name/:value', (req, res, next) => {
  res.cookie(req.params.name, req.params.value);
  res.send({cookie: `${req.params.name}:${req.params.value}`});
});

app.get('/cookie', (req, res, next) => {
  res.send({cookie: req.cookies});
});
```
Common for middleware funcs to add fields and funcs to "req" and "res" objs so other middleware can access their functionality. Is seen when cookie-parser adds the req.cookies obj for reading cookies, and adds res.cookie func to make it easy to add a cookie to response. 
### Error handling middleware
Takes an additional err parameter that contains the error:
```js
function errorMiddlewareName(err, req, res, next)
```
Simple error handler for anything that might go wrong while processing HTTP requests:
```js
app.use(function (err, req, res, next) {
  res.status(500).send({type: err.name, message: err.message});
});
```
Test that error middleware is getting used by adding new endpoint that generates an error:
```js
app.get('/error', (req, res, next) => {
  throw new Error('Trouble in river city');
});
```
➜ curl localhost:8080/error
{"type":"Error","message":"Trouble in river city"}
### Putting it all together
Full ex. web service using Express:
```js
const express = require('express');
const cookieParser = require('cookie-parser');
const app = express();

// Third party middleware - Cookies
app.use(cookieParser());

app.post('/cookie/:name/:value', (req, res, next) => {
  res.cookie(req.params.name, req.params.value);
  res.send({cookie: `${req.params.name}:${req.params.value}`});
});

app.get('/cookie', (req, res, next) => {
  res.send({cookie: req.cookies});
});

// Creating your own middleware - logging
app.use((req, res, next) => {
  console.log(req.originalUrl);
  next();
});

// Built in middleware - Static file hosting
app.use(express.static('public'));

// Routing middleware
app.get('/store/:storeName', (req, res) => {
  res.send({name: req.params.storeName});
});

app.put('/st*/:storeName', (req, res) => res.send({update: req.params.storeName}));

app.delete(/\/store\/(.+)/, (req, res) => res.send({delete: req.params[0]}));

// Error middleware
app.get('/error', (req, res, next) => {
  throw new Error('Trouble in river city');
});

app.use(function (err, req, res, next) {
  res.status(500).send({type: err.name, message: err.message});
});

// Listening to a network port
const port = 8080;
app.listen(port, function () {
  console.log(`Listening on port ${port}`);
});
```

## PM2
Programs ran from the console automatically terminate when console is closed/computer's restarted. Register program as daemon to prevent this. Process Manager 2 (PM2) lets us easily start and stop our services.
Useful PM2 console commands. Only use them if you understand what they're doing bc they could cause your web services to stop working:
| Command                                                    | Purpose                                                                          |
| ---------------------------------------------------------- | -------------------------------------------------------------------------------- |
| **pm2 ls**                                                 | List all of the hosted node processes                                            |
| **pm2 monit**                                              | Visual monitor                                                                   |
| **pm2 start index.js -n simon**                            | Add a new process with an explicit name                                          |
| **pm2 start index.js -n startup -- 4000**                  | Add a new process with an explicit name and port parameter                       |
| **pm2 stop simon**                                         | Stop a process                                                                   |
| **pm2 restart simon**                                      | Restart a process                                                                |
| **pm2 delete simon**                                       | Delete a process from being hosted                                               |
| **pm2 delete all**                                         | Delete all processes                                                             |
| **pm2 save**                                               | Save the current processes across reboot                                         |
| **pm2 restart all**                                        | Reload all of the processes                                                      |
| **pm2 restart simon --update-env**                         | Reload process and update the node version to the current environment definition |
| **pm2 update**                                             | Reload pm2                                                                       |
| **pm2 start env.js --watch --ignore-watch="node_modules"** | Automatically reload service when index.js changes                               |
| **pm2 describe simon**                                     | Describe detailed process information                                            |
| **pm2 startup**                                            | Displays the command to run to keep PM2 running after a reboot.                  |
| **pm2 logs simon**                                         | Display process logs                                                             |
| **pm2 env 0**                                              | Display environment variables for process. Use `pm2 ls` to get the process ID    |
### Registering a new web service
Follow these steps to setup another subdomain that accesses different web service on your web server:
1. Add the rule to Caddyfile to tell it how to direct requests for the other domain
2. Create a directory and add the files for the web service
3. Configure PM2 to host the web service
### Modify Caddyfile
1. SSH into your server
2. Copy section for startup subdomain and alter it to represent desired subdomain and give it different port number that's not currently used on server. Ex:
```js
tacos.cs260.click {
  reverse_proxy _ localhost:5000
  header Cache-Control none
  header -server
  header Access-Control-Allow-Origin *
}
```
3. Restart Caddy to load new settings:
```js
sudo service caddy restart
```
## UI Testing
Test driven development (TDD) is proven to accelerate application creation, protect against regression bugs and demonstrate correctness.
### Automating the brower - Playwright
Playright is backed by Microsoft, integrates well w/ VS Code, and runs as Node.js process. 
Ex:
```js
import { test, expect } from '@playwright/test';

test('testWelcomeButton', async ({ page }) => {
  // Navigate to the welcome page
  await page.goto('http://localhost:5500/');

  // Get the target element and make sure it is in the correct starting state
  const hello = page.getByTestId('msg');
  await expect(hello).toHaveText('Hello world');

  // Press the button
  const changeBtn = page.getByRole('button', { name: 'change welcome' });
  await changeBtn.click();

  // Expect that the change happened correctly
  await expect(hello).toHaveText('I feel not welcomed');
});
```
Must have your application running to test.
To run in VS Code select "Test Explorer" tab. 
### Testing various devices - BrowserStack
Lets you pick from list of physical devices that you can run interactively or use when running automated tests w/ Selenium.

## Endpoint testing
Generally easier than writing UI tests bc it doesn't require a browser. We'll explore w/ Jest. Test service using VS code debugger. 
To launch a service using Jest, create another file with suffix of ".test.js". Jest automatically imports itself when it discovers a test file
store.test.js:
```js
test('that equal values are equal', () => {
  expect(false).toBe(true);
});
```
A test func takes a description as 1st parameter. Description is meant to be human readable. 2nd parameter is func to call. This test calls Jest "expect" func and chains it to the toBe func. Can read this as "expect false to be true" which means that this test will fail.
To run test, install Jest package w/ NPM:
```
npm install jest -D
```
Then, replace scripts sectino of package.json file w/ command to run Jest tests:
```js
"scripts": {
  "test": "jest"
},
```
Now can run "test" command to execute tests.
```js
npm run test
```
### Testing endpoints
NPM package "supertest" lets us make HTTP requests w/out having to send them over the network:
```js
npm install supertest -D
```
This test will expect HTTP status code of 200 (OK), and that body fo response contains obj that we expect the endpoint to return. If something goes wrong, end func will contain an error and pass error along to done func. Otherwise, done is called w/out error
store.test.js:
```js
const request = require('supertest');
const app = require('./server');

test('getStore returns the desired store', (done) => {
  request(app)
    .get('/store/provo')
    .expect(200)
    .expect({ name: 'provo' })
    .end((err) => (err ? done(err) : done()));
});
```
Test for updateStore endpoint. Copy the getStore endpoint, change the description, change the HTTP func ver to put, and send body of put request using chained send func:
```js
const request = require('supertest');
const app = require('./server');

test('updateStore saves the correct values', (done) => {
  request(app)
    .put('/store/provo')
    .send({ items: ['fish', 'milk'] })
    .expect(200)
    .expect({ items: ['fish', 'milk'], updated: true })
    .end((err) => (err ? done(err) : done()));
});

test('getStore returns the desired store', (done) => {
  request(app)
    .get('/store/provo')
    .expect(200)
    .expect({ name: 'provo' })
    .end((err) => (err ? done(err) : done()));
});
```
Can write tests first then write code based on design represented by tests. When tests pass, you know your code is complete. 

# Data Services
Historically, SQL databsases have served as general piurpose data service solution. Now specialty data services w/ better support are more commonly used, called "NoSQL" solutions b/c don't use general purpose relational database paradigms popularized by SQL DBs.
Some popular data services:
| Service       | Specialty             |
| ------------- | --------------------- |
| MySQL         | Relational queries    |
| Redis         | Memory cached objects |
| ElasticSearch | Ranked free text      |
| MongoDB       | JSON objects          |
| DynamoDB      | Key value pairs       |
| Neo4J         | Graph based data      |
| InfluxDB      | Time series data      |
## MongoDB
We will use MongoDB. A mongo DB is made up of 1 or more collections that each contain JSON documents. Can think of collection as large array of JS objs, each w/ unique ID. Sample of collection of houses available for rent:
```js
[
  {
    _id: '62300f5316f7f58839c811de',
    name: 'Lovely Loft',
    summary: 'A charming loft in Paris',
    beds: 1,
    last_review: {
      $date: '2022-03-15T04:06:17.766Z',
    },
    price: 3000,
  },
  {
    _id: '623010b97f1fed0a2df311f8',
    name: 'Infinite Views',
    summary: 'Modern home with infinite views from the infinity pool',
    property_type: 'House',
    beds: 5,
    price: 250,
  },
];
```
Mongo has no strict schema requirements. Each doc in collection usually follow similar schema, but each doc can have specialized fields present and common fields missing. To add new field to Mongo collection, just insert field into docs as desired. If field isn't present, or has different type in some docs, then doc simply doesn't mathc query criteria when field is referenced.
Follows JS-inspired flavor. Queries for rent collection from above:
```js
// find all houses
db.house.find();

// find houses with two or more bedrooms
db.house.find({ beds: { $gte: 2 } });

// find houses that are available with less than three beds
db.house.find({ status: 'available', beds: { $lt: 3 } });

// find houses with either less than three beds or less than $1000 a night
db.house.find({ $or: [(beds: { $lt: 3 }), (price: { $lt: 1000 })] });

// find houses with the text 'modern' or 'beach' in the summary
db.house.find({ summary: /(modern|beach)/i });
```
### Using MongoDB in your app
Install mongoDB package:
```js
➜ npm install mongodb
```
Then use MongoClient obj to make client connection to DB server. Requieres username, password, and hostname of db server:
```js
const { MongoClient } = require('mongodb');

const userName = 'holowaychuk';
const password = 'express';
const hostname = 'mongodb.com';

const url = `mongodb+srv://${userName}:${password}@${hostname}`;

const client = new MongoClient(url);
```
W/ client connection, can get db obj and from that a collection obj. Collection obj allows you to insert, and query for, docs. Just call "insertOne" func on collection obj and pass it JS obj to insert JS obj as Mongo doc. When you insert doc, if db/collection doesn't exist, Mongo will automatically make it for you.
```js
const collection = client.db('rental').collection('house');

const house = {
  name: 'Beachfront views',
  summary: 'From your bedroom to the beach, no shoes required',
  property_type: 'Condo',
  beds: 1,
};
await collection.insertOne(house);
```
To query for docs, use find func on collection obj. Find func is asynchronous so use await keyword.
```js
const cursor = collection.find();
const rentals = await cursor.toArray();
rentals.forEach((i) => console.log(i));
```
If you don't supply parameters to find func, it will return all docs in collection. Output:
```js
[
  {
    _id: new ObjectId('639a96398f8de594e198fc13'),
    name: 'Beachfront views',
    summary: 'From your bedroom to the beach, no shoes required',
    property_type: 'Condo',
    beds: 1,
  },
];
```
Can provide a query and options to find func. In ex below, we query for property_type of Condo that has < 2 bedrooms. We also specify options to sort by descending price, limit results to 1st 10 docs:
```js
const query = { property_type: 'Condo', beds: { $lt: 2 } };

const options = {
  sort: { price: -1 },
  limit: 10,
};

const cursor = collection.find(query, options);
const rentals = await cursor.toArray();
rentals.forEach((i) => console.log(i));
```
## Managed Services
3rd party services that manage data service. Allows you to focus more on application and not on the infrstructure. 
### MongoDB Atlas
All major cloud provides offer multiple data services. 
## Keeping your keys out of your code
Protect your credential for connecting to your Mongo database. A common mistake is putting them into your code in a public GitHub repo. Instead you can load your credentials when the app executes. A common way is to have a JSON config file that makes DB connection. Then use config file in development environment and deploy it to your production environment.
Steps:
1. Create file "dbConfig.json" in same directory as DB JS that is used to make DB requests. 
2. Insert MongoDB credential into dbConfig.json file in JSON format:
```js
{
  "hostname": "cs260.abcdefg.mongodb.net",
  "userName": "myMongoUserName",
  "password": "toomanysecrets"
}
```
3. import dbConfig.json content into database.js using Node.js req statement and use data it represents to create connnection URL:
```js
{
  "hostname": "cs260.abcdefg.mongodb.net",
  "userName": "myMongoUserName",
  "password": "toomanysecrets"
}
```
Make sure to incllude dbConfig.json in .gitignorefile so it doesn't get pushed up to GitHub.
## Testing the connection on startup:
```js
const config = require('./dbConfig.json');

const url = `mongodb+srv://${config.userName}:${config.password}@${config.hostname}`;
const client = new MongoClient(url);
const db = client.db('rental');

(async function testConnection() {
  await client.connect();
  await db.command({ ping: 1 });
})().catch((ex) => {
  console.log(`Unable to connect to database with ${url} because ${ex.message}`);
  process.exit(1);
});
```
## Using Mongo from your code
Test that things work right:
```js
const { MongoClient } = require('mongodb');
const config = require('./dbConfig.json');

async function main() {
  // Connect to the database cluster
  const url = `mongodb+srv://${config.userName}:${config.password}@${config.hostname}`;
  const client = new MongoClient(url);
  const db = client.db('rental');
  const collection = db.collection('house');

  // Test that you can connect to the database
  (async function testConnection() {
    await client.connect();
    await db.command({ ping: 1 });
  })().catch((ex) => {
    console.log(`Unable to connect to database with ${url} because ${ex.message}`);
    process.exit(1);
  });

  // Insert a document
  const house = {
    name: 'Beachfront views',
    summary: 'From your bedroom to the beach, no shoes required',
    property_type: 'Condo',
    beds: 1,
  };
  await collection.insertOne(house);

  // Query the documents
  const query = { property_type: 'Condo', beds: { $lt: 2 } };
  const options = {
    sort: { score: -1 },
    limit: 10,
  };

  const cursor = collection.find(query, options);
  const rentals = await cursor.toArray();
  rentals.forEach((i) => console.log(i));
}

main().catch(console.error);
```
To execute above ex:
1. create directory called mongoTest
2. save above content to file named index.js
3. create file "dbConfig.json" w/ DB credentials
4. npm init -y
5. npm install mongodb
6. node index.js
Should output:
```js
{
_id: new ObjectId("639b51b74ef1e953b884ca5b"),
name: 'Beachfront views',
summary: 'From your bedroom to the beach, no shoes required',
property_type: 'Condo',
beds: 1
}
```

# Authorization services
To remember a user's data, you need a way to uniquely associate data w/ a particular credential. Usually means you authenticate a user by asking for info like email and password. You then remember, for some period of time, that user has authenticated by storing an authentication token on user's device. Often that's stored in a cookie that's passed back to web service on each request. 
Determining the authorization of a user is important (what they are allowed to do). Once you can authenticate a user, you can store their authorization too. 
Authorization services often use standard protocols for authenticating and authorizng. These include standards like OAuth, SAML, and OIDC. Additionally, they usually support concepts like Single Sign On (SSO) and Federated Login. SSO allows a user to use the same credential for multiple web apps. Ex, you can log into github using google. Federated login allows a user to log in once and then the authentication token is reused to automatically log the user into multiple websites. Ex, gmail lets you also use google docs and youtube w/out logging in again.

## Account creation and login
1st step towards supporting authentication in web app is providing way for users to uniquely identify themselves. Usually requires 2 service endpoints. 1 to initially create an authentication credential and a 2nd to authenticate or login on future visits. Once a user is authenticated, we can control access to other endpoints. Ex, web services often have a getMe endpoint that gives info about current user. 
### Create authentication endpoint
Takes email and password and returns a cookie containing the authentication token and user ID. If email already exists, returns a 409 (conlfict) status code.
```js
POST /auth/create HTTP/2
Content-Type: application/json

{
  "email":"marta@id.com",
  "password":"toomanysecrets"
}
```
```js
HTTP/2 200 OK
Content-Type: application/json
Set-Cookie: auth=tokenHere

{
  "id":"337"
}
```
### Login authentication endpoint
Takes an email and password and returns a cookie containing the authentication token and user ID. If email doesn't exist or password's bad, returns a 401 (unauthorized) status code.
```js
POST /auth/login HTTP/2
Content-Type: application/json

{
  "email":"marta@id.com",
  "password":"toomanysecrets"
}
```
```js
HTTP/2 200 OK
Content-Type: application/json
Set-Cookie: auth=tokenHere

{
  "id":"337"
}
```
### GetMe endpoint
Uses the authentication token stored in cookie to look up and return info abt authenticated user. If token/user doesn't exist it returns a 401 (unauthorized) status code.
```js
GET /user/me HTTP/2
Cookie: auth=tokenHere
```
```js
HTTP/2 200 OK
Content-Type: application/json

{
  "email":"marta@id.com"
}
```
### Web service
Web service using express:
```js
const express = require('express');
const app = express();

app.post('/auth/create', async (req, res) => {
  res.send({ id: 'user@id.com' });
});

app.post('/auth/login', async (req, res) => {
  res.send({ id: 'user@id.com' });
});

const port = 8080;
app.listen(port, function () {
  console.log(`Listening on port ${port}`);
});
```
### Handling requests
1st step is to read credentials from body of HTTP request. Since body is designed to conatin JSON we tell Express that it should parse HTTP reqs, w/ content type of application/json, automatically into JS obj. Do this w/ express.json middleware. Then, read email and password directly out of req.body obj. 
```js
app.use(express.json());

app.post('/auth/create', (req, res) => {
  res.send({
    id: 'user@id.com',
    email: req.body.email,
    password: req.body.password,
  });
});
```
Now we can change code to add a check to see if we already have a user w/ that email. If we do, return 409 (conflict) status code. Otherwise, create new user and return user ID:
```js
app.post('/auth/create', async (req, res) => {
  if (await getUser(req.body.email)) {
    res.status(409).send({ msg: 'Existing user' });
  } else {
    const user = await createUser(req.body.email, req.body.password);
    res.send({
      id: user._id,
    });
  }
});
```
### Using the database
We want to persistently store users in Mongo, so we set up our code to connect to and use DB:
```js
const { MongoClient } = require('mongodb');

const userName = 'holowaychuk';
const password = 'express';
const hostname = 'mongodb.com';

const url = `mongodb+srv://${userName}:${password}@${hostname}`;

const client = new MongoClient(url);
```
W/ mongo collection obj, we can implement getUser and createUser funcs:
```js
function getUser(email) {
  return collection.findOne({ email: email });
}

async function createUser(email, password) {
  const user = {
    email: email,
    password: password,
    token: 'xxx',
  };
  return collection.insertOne(user);
}
```
But, we're missing a real authentication toke and we can't store a clear text password in our DB.
### Generating authentication tokens
To generate reasonable authentication toke, use uuid package (Universally unique identifier), which creates a hard to guess, random, unique ID:
```js
const uuid = require('uuid');

token: uuid.v4();
```
### Securing passwords
Failing to secure passwords is a major security concer. Even if your app isn't very valuable, users often reuse passwords, so hackers could have their passwords for other websites too.
Instead of storing password directly, we want to cryptographically hash the password so that we never store actual password. To validate a password, hash login password and compare it to our stored hash of the password.
To hash passwords, use bcrypt package, which creates secure one-way hash of password.
```js
const bcrypt = require('bcrypt');

async function createUser(email, password) {
  // Hash the password before we insert it into the database
  const passwordHash = await bcrypt.hash(password, 10);

  const user = {
    email: email,
    password: passwordHash,
    token: uuid.v4(),
  };
  await collection.insertOne(user);

  return user;
}
```
### Passing authentication tokents
Use HTTP cookies to pass generated authentication token to browser when login endpoint is called and get it back on subsequent requests. cookie-parser package provides middleware for cookies.
When user is successfully creates, or logged in, we set cookie header. Since we're storing an authentication token in cookie, we want it to be as secure as possible, so we use httpOnly, secure and sameSite options.
- httpOnly tells browser not to allow JS running on browser to read cookie
- sercure requires HTTPS to be used when sending cookie back to server.
- sameSite will only return cookie to domain that generated it
```js
const cookieParser = require('cookie-parser');

// Use the cookie parser middleware
app.use(cookieParser());

apiRouter.post('/auth/create', async (req, res) => {
  if (await DB.getUser(req.body.email)) {
    res.status(409).send({ msg: 'Existing user' });
  } else {
    const user = await DB.createUser(req.body.email, req.body.password);

    // Set the cookie
    setAuthCookie(res, user.token);

    res.send({
      id: user._id,
    });
  }
});

function setAuthCookie(res, authToken) {
  res.cookie('token', authToken, {
    secure: true,
    httpOnly: true,
    sameSite: 'strict',
  });
}
```
### Login endpoint
Login authorization endpoint needs to get hashed password from db, compare it to provided password using bcrypt.compare, and if successful set authenticaiton token in cookie. If password doesn't match, or no user w/ given email, endpoint returns status 401 (unauthorized).
```js
app.post('/auth/login', async (req, res) => {
  const user = await getUser(req.body.email);
  if (user) {
    if (await bcrypt.compare(req.body.password, user.password)) {
      setAuthCookie(res, user.token);
      res.send({ id: user._id });
      return;
    }
  }
  res.status(401).send({ msg: 'Unauthorized' });
});
```
### GetMe endpoint
To implement this, get user obj from db by querying on authentication token. If there's not an authentication token, or there's no user w/ that token, return status 401 (unauthorized)
```js
app.get('/user/me', async (req, res) => {
  authToken = req.cookies['token'];
  const user = await collection.findOne({ token: authToken });
  if (user) {
    res.send({ email: user.email });
    return;
  }
  res.status(401).send({ msg: 'Unauthorized' });
});
```

# WebSocket
It's fully duplexed. This means that after initial connection is made from client, using vanilla HTTP, then upgraded by server to WebSocket connection, relationship changes to peer-to-peer connection where either party can efficiently send data at any time.
## Creating WS conversation
JS running on browser can initiate WS connection w/ browser's WS API. 1st create WS obj buy specifying port to communicate on.
Send messages w/ send func, and register callback using onmessage func to receive messages.
```js
const socket = new WebSocket('ws://localhost:9900');

socket.onmessage = (event) => {
  console.log('received: ', event.data);
};

socket.send('I am listening');
```
Server uses ws package to create WebSocketServer that's listening on same port that browser's using. By specifying a port when create WebSocketServer, you're telling server to listen for HTTP connections on that port and to automatically upgrade them to WS connection if req has connection: Upgrade header.
When connection is detected, calls server's on connection callback. Server can send messages w/ send func, can register callback using on message func to receive messages.
```js
const { WebSocketServer } = require('ws');

const wss = new WebSocketServer({ port: 9900 });

wss.on('connection', (ws) => {
  ws.on('message', (data) => {
    const msg = String.fromCharCode(...data);
    console.log('received: %s', msg);

    ws.send(`I heard you say "${msg}"`);
  });

  ws.send('Hello webSocket');
});
```
## WebSocket Chat
Disable chat features if name is ever empty:
```js
const chatControls = document.querySelector('#chat-controls');
const myName = document.querySelector('#my-name');
myName.addEventListener('keyup', (e) => {
  chatControls.disabled = myName.value === '';
});
```
Appends new message to html:
```js
function appendMsg(cls, from, msg) {
  const chatText = document.querySelector('#chat-text');
  chatText.innerHTML = `<div><span class="${cls}">${from}</span>: ${msg}</div>` + chatText.innerHTML;
}
```
Send message when enter is hit:
```js
const input = document.querySelector('#new-msg');
input.addEventListener('keydown', (e) => {
  if (e.key === 'Enter') {
    sendMessage();
  }
});
```
Send message func:
```js
function sendMessage() {
  const msgEl = document.querySelector('#new-msg');
  const msg = msgEl.value;
  if (!!msg) {
    appendMsg('me', 'me', msg);
    const name = document.querySelector('#my-name').value;
    socket.send(`{"name":"${name}", "msg":"${msg}"}`);
    msgEl.value = '';
  }
}
```
Set WS protocol to be non-secure (ws) if HTTP, otherwise secure (wss) if HTTPS. Notify user that chat's ready by listening to onopen and appending text to display w/ appendMsg func:
```js
// Adjust the webSocket protocol to what is being used for HTTP
const protocol = window.location.protocol === 'http:' ? 'ws' : 'wss';
const socket = new WebSocket(`${protocol}://${window.location.host}/ws`);

// Display that we have opened the webSocket
socket.onopen = (event) => {
  appendMsg('system', 'websocket', 'connected');
};
```
Displays received messages using appendMsg func:
```js
socket.onmessage = async (event) => {
  const text = await event.data.text();
  const chat = JSON.parse(text);
  appendMsg('friend', chat.name, chat.msg);
};
```
If WS closes, display that to user and disable controls:
```js
socket.onclose = (event) => {
  appendMsg('system', 'websocket', 'disconnected');
  document.querySelector('#name-controls').disabled = true;
  document.querySelector('#chat-controls').disabled = true;
};
```
### Web service
Simple express app. Serve up html, css, and js files w/ static middleware:
```js
const { WebSocketServer } = require('ws');
const express = require('express');
const app = express();

// Serve up our webSocket client HTML
app.use(express.static('./public'));

const port = process.argv.length > 2 ? process.argv[2] : 3000;
server = app.listen(port, () => {
  console.log(`Listening on ${port}`);
});
```
### Websocket server
Instead of letting WebSocketServer control both HTTP connection and upgrading to WS, we want to use HTTP connection that Express is providing and handle the upgrade to WS ourselves. Done by specifying noServer option when creating WSServer then handling upgrade notification that occurs when client reqs upgrade of protocol from HTTP to WS:
```js
// Create a websocket object
const wss = new WebSocketServer({ noServer: true });

// Handle the protocol upgrade from HTTP to WebSocket
server.on('upgrade', (request, socket, head) => {
  wss.handleUpgrade(request, socket, head, function done(ws) {
    wss.emit('connection', ws, request);
  });
});
```
### Forwarding messages
W/ WS server we can use connection, mesage, and close events to forwards messages between peers. On connection, we insert an obj representing connection into list of all connections from chat peers Then when message is received, we loop thru peer connections and forward it to everyone except peer who initiated the request. Finally, remove a connection from peer connection list when it's closed:
```js
// Keep track of all the connections so we can forward messages
let connections = [];

wss.on('connection', (ws) => {
  const connection = { id: connections.length + 1, alive: true, ws: ws };
  connections.push(connection);

  // Forward messages to everyone except the sender
  ws.on('message', function message(data) {
    connections.forEach((c) => {
      if (c.id !== connection.id) {
        c.ws.send(data);
      }
    });
  });

  // Remove the closed connection so we don't try to forward anymore
  ws.on('close', () => {
    connections.findIndex((o, i) => {
      if (o.id === connection.id) {
        connections.splice(i, 1);
        return true;
      }
    });
  });
});
```
### Keeping connections alive
WS connection will eventually close automatically if no data's sent across it. To prevent that, WS protocol supports ability to send ping message to see if peer's still there and receive pong responses to confirm it.
Use setInterval to send ping every 10 sec to each peer connection and clean up any connections that didn't respond to previous ping:
```js
setInterval(() => {
  connections.forEach((c) => {
    // Kill any connection that didn't respond to the ping last time
    if (!c.alive) {
      c.ws.terminate();
    } else {
      c.alive = false;
      c.ws.ping();
    }
  });
}, 10000);
```
In connection handler, listen for pong response and mark connection as alive:
```js
// Respond to pong messages by marking the connection alive
ws.on('pong', () => {
  connection.alive = true;
});
```

# Web Frameworks
Seek to make writing of web apps easier by providing tools for completing common tasks. Includes modularizing code, creating single page apps, simplifying reactivity, and supporting diverse hardware devices.
Some take things like HTML, CSS and JS and create new hybrid file formats that combine things like HTML and JS into 1 file. Abstracting away core web file formats puts focus on functional components rather than files.
## Vue
combines HTML, CSS and JS into 1 file. HTML represented by "template" element
## Svelte
Also combines HTML, CSS, and JS into 1 file. Requires a transpiler to generate browser-ready code, instead of runtime virtual DOM
## React
Combines JS and HTML into its components format. CSS must be declared outside the JSX file. Component highly leverages funcitonality of JS and can be represented as func or class.
## Angular component
Defines what JS, HTML, and CSS are combined together. Keeps fairly strong separation of files that're usually grouped together in directory rather than using single file representation.

# React
Created by Jordan Walke for use at Facebook.
Abstracts HTML into JS variant called JSX. JSX is converted into valid HTML and JS using preprocessor called Babel. 
React.createElement func then generates DOM elements and monitors data they represent for changes. When change is discovered, React will trigger dependent changes.
## Components
Let you modularize the functionality of your app. Allows underlying code to directly repr the components that user interacts w/. Also enables code reuse as common app components often show up repeatedly.
### The render function
1 of primary purposes of component is to generate UI. Done w/ component's "render" func. Whatever's return by this fun is inserted into component HTML elemnt.
Ex: JSX file contains react component "demo" would cause react to load demo component, call render func, and insert result into place of Demo element. Demo isn't valid html, that is replaced w/ resulting rendered html.
JSX:
```jsx
<div>
  Component: <Demo />
</div>
```
React component:
```jsx
function Demo() {
  const who = 'world';
  return <b>Hello {who}</b>;
}
```
Resulting html:
```html
<div>Component: <b>Hello world</b></div>
```

### Properties
React components allow you to pass info to them in form of element properties. Component receives properties in its constructor and can display them when rendered.
JSX:
```jsx
<div>Component: <Demo who="Walke" /><div>
```
React component:
```jsx
function Demo(props) {
  return <b>Hello {props.who}</b>;
}
```
Resulting html:
```js
<div>Component: <b>Hello Walke</b></div>
```
### State
Component can have internal state. Created by calling React.useState hook func. useState func returns a var that contains the current state and func to update the state. Ex: Create a state var called clicked and toggles the click state in updateClicked func that gets called when paragraph text is clicked.
```jsx
const Clicker = () => {
  const [clicked, updateClicked] = React.useState(false);

  const onClicked = (e) => {
    updateClicked(!clicked);
  };

  return <p onClick={(e) => onClicked(e)}>clicked: {`${clicked}`}</p>;
};

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Clicker />);
```
Can user JSX w/out func. Simple var representing JSX will work anyplace you would otherwise provide a component.
```jsx
const hello = <div>Hello</div>;

ReactDOM.render(hello, document.getElementById('root'));
```

### Class style components
React team is moving away from class style representaiton, and for that reason you probably shouldn't use it. Ex: Class style component for Clicker component we created above. Major difference is that properties are loaded on constructor and state is set using a setState func on component obj.
```jsx
class Clicker extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      clicked: false,
    };
  }
  onClicked() {
    this.setState({
      clicked: !this.state.clicked,
    });
  }
  render() {
    return <p onClick={(e) => this.onClicked(e)}>clicked: {`${this.state.clicked}`}</p>;
  }
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Clicker />);
```
### Reactivity
Controls how a component reacts to actions taken by user or events that happen within the app. Whenever a component's state or properties change, the render func for the component and all its dependent component render funs are called.

# Toolchains
Meant to abstract away some of the complexity of web programming:
- Code repository - Stores code in a shared, versioned, location
- Linert - removes, or warns, of non-idiomatic code usage
- Prettier - Formats code according to a shared standard
- Polyfill - Generates backward compatible code for supporting old browser versions that don't support the latest standards
- Bundler - Packages code into bundles for delivery to the browser. This enables compatibility (ex. w/ ES6 module support), or performance (w/ lazy loading)
- Minifier - Removes whitespace and renames vars in order to make code smaller and more efficient to deploy
- testing - Automated tests at multiple levels to ensure correctness
- Deployment - Automated packaging and delivery of code from the development environment to the production environment.
Our toolchain: github as code repo, Vite for jsx, TS, development and debugging support, ESBuild for converting ES6 modules and transpiling (w/ babel underneath), Rollup for bundling and tree shaking, PostCSS for CSS transpiling and simple bash script (desployReact.sh) for deployment.

# Reactivity
Making UI react to user input/data, is one of foundations of REact. Enables reactivity w/ 3 major pieces of React component: props, state, and render.
When component JSX is rendered, React parses JSX and creates a list of references to component's state/prop objs. React monitors those objs and if changed detected, it will call component's 'render' func so that impact of change is visualized.
Following ex has 2 components: parent '<Survey/> and child <Question/>. Suvery has state named color. Question has property named color. Survey passes state to Question as property. Any change in Survey's color will be reflected in Question's color.
Question has state named answer. Value displayed as part of its content. User can interact w/ this state thru HTML radio input elements. When 1 of inputs is changed, Question's onChange func is called and answer state is updated.
Updates happen asynchronously, and therefore you don't know when its going to happen, just that it will eventually happen.
```jsx
// The Survey component
const Survey = () => {
  const [color, updateColor] = React.useState('#737AB0');

  // When the color changes update the state
  const onChange = (e) => {
    updateColor(e.target.value);
  };
  return (
    <div>
      <h1>Survey</h1>
      {/* Pass the Survey color state as a property to the Question.
          When the color changes the Question property will also be updated and rendered. */}
      <Question color={color} />

      <p>
        <span>Pick a color: </span>
        {/* Pass the Survey color state as a property to the input element.
            When the color changes, the input property will also be updated and rendered. */}
        <input type='color' onChange={(e) => onChange(e)} value={color} />
      </p>
    </div>
  );
};

// The Question component
const Question = ({ color }) => {
  const [answer, updateAnswer] = React.useState('pending...');

  function onChange({ target }) {
    updateAnswer(target.value);
  }

  return (
    <div>
      <span>Do you like this</span>
      {/* Color rerendered whenever the property changes */}
      <span style={{ color: color }}> color</span>?
      <label>
        <input type='radio' name='answer' value='yes' onChange={(e) => onChange(e)} />
        Yes
      </label>
      <label>
        <input type='radio' name='answer' value='no' onChange={(e) => onChange(e)} />
        No
      </label>
      {/* Answer rerendered whenever the state changes */}
      <p>Your answer: {answer}</p>
    </div>
  );
};

ReactDOM.render(<Survey />, document.getElementById('root'));
```

# React Hooks
Allow React func style components to be able to do everything that a class style component can do and more. As new features are added to React, they're included as hooks. 
## useEffect hook
Allows you to represent lifecylce events. Ex, if you want to run a func everytime the component finishes rendering, could do the following:
```jsx
function UseEffectHookDemo() {
  React.useEffect(() => {
    console.log('rendered');
  });

  return <div>useEffectExample</div>;
}

ReactDOM.render(<UseEffectHookDemo />, document.getElementById('root'));
```
Can also take action whne component cleans up by returning a cleanup func from func registered w/ useEffect. Ex, everytime component is clicked the state changes, so the component is rerendered. Causes both cleanup func to be called in addition to hook func. If func wasn't rerendered, only cleanup func would be called.
```jsx
function UseEffectHookDemo() {
  const [count, updateCount] = React.useState(0);
  React.useEffect(() => {
    console.log('rendered');

    return function cleanup() {
      console.log('cleanup');
    };
  });

  return <div onClick={() => updateCount(count + 1)}>useEffectExample {count}</div>;
}

ReactDOM.render(<UseEffectHookDemo />, document.getElementById('root'));
```
Userful to create side effects like tracking when a component is diplayed or hidden, or creating and disposing of resources.
## Hook Dependencies
Can control what triggers a useEffect hook by specifying its dependencies. In following ex, we have two state vars, but only want useEffect hook called when component is initially called and when first var is clicked. Done by passing array of dependencies as 2nd parameter to useEffect call.
```jsx
function UseEffectHookDemo() {
  const [count1, updateCount1] = React.useState(0);
  const [count2, updateCount2] = React.useState(0);

  React.useEffect(() => {
    console.log(`count1 effect triggered ${count1}`);
  }, [count1]);

  return (
    <ol>
      <li onClick={() => updateCount1(count1 + 1)}>Item 1 - {count1}</li>
      <li onClick={() => updateCount2(count2 + 1)}>Item 2 - {count2}</li>
    </ol>
  );
}

ReactDOM.render(<UseEffectHookDemo />, document.getElementById('root'));
```
If you specify an empty array [] as hook dependency, then it's only called when component is 1st rendered.
Hooks can only be used in func style components and must be called at top scope of func. Hook can't be called inside loop or conditional. Ensures that hooks are always called in same order when component is rendered.
# Router
Provides essential functionality for single-page apps. W/ multiple-webpage app the headers, footers, navigation, and common components must be either duplicated in each HTML page, or injected before the server sends the page to the browser. W/ single page app, browser only loads one HTML page and then JS is used to manipulate the DOM and give it the appearance of multiple pages. Router defines the routes a user can take thru the app, and automatically manipulates the DOM to display the appropriate framework components. We use react-router-dom Version 6
Basic implementation has BrowserRouter component that encapsulates the entire app and controls the routing action. Link, or NavLink component captures user nav events and modifies what's rendered by the Routes comopnent by matching up the to and path attributes.
```jsx
// Inject the router into the application root DOM element
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  // BrowserRouter component that controls what is rendered
  // NavLink component captures user navigation requests
  // Routes component defines what component is routed to
  <BrowserRouter>
    <div className='app'>
      <nav>
        <NavLink to='/'>Home</Link>
        <NavLink to='/about'>About</Link>
        <NavLink to='/users'>Users</Link>
      </nav>

      <main>
        <Routes>
          <Route path='/' element={<Home />} exact />
          <Route path='/about' element={<About />} />
          <Route path='/users' element={<Users />} />
          <Route path='*' element={<Navigate to='/' replace />} />
        </Routes>
      </main>
    </div>
  </BrowserRouter>
);
```
# Vite
A common way of taking advantage of all the technologies is to use a Command Line Interface (CLI) to initially set up a web app. CLI saves you the trouble of configuring the toolchain parameters and gets you quickly started w/ a default app.
We'll use Vite. To make new React-based app using Vite, run following commands:
```js
npm create vite@latest demoVite -- --template react
cd demoVite
npm install
npm run dev
```
This will create a new web app in the demoVite directory, download the required 3rd party packages, and start up the app using a local HTTP debugging server. Can tell Vite to open your browser to the URL that's hosting your app by pressing o, or press h to see all the Vite CLI options.
## Generated Project
Files made by vite:
| Directory    | File              | Purpose                                                                                                                   |
| ------------ | ----------------- | ------------------------------------------------------------------------------------------------------------------------- |
| ./           |                   |                                                                                                                                |
|              | index.html        | Primary page for the application. This is the starting point to load all of the JSX components beginning with `main.jsx`. |
|              | package.json      | NPM definition for package dependencies and script commands. This is what maps `npm run dev` to actually start up Vite.   |
|              | package-lock.json | Version constraints for included packages (do not edit this).                                                             |
|              | vite.config.js    | Configuration setting for Vite. Specifically this sets up React for development.                                          |
| ./public     |                   |                                                                                                                           |
|              | vite.svg          | Vite logo for use as favicon and for display in the app.                                                                  |
| ./src        |                   |                                                                                                                           |
|              | main.jsx          | Entry point for code execution. This simply loads the App component found in `App.jsx`.                                   |
|              | index.css         | CSS for the entire application.                                                                                           |
|              | App.jsx           | JSX for top level application component. This displays the logs and implements the click counter.                         |
|              | App.css           | CSS for the top level application component.                                                                              |
| ./src/assets |                   |                                                                                                                           |
|              | react.svg         | React logo for display in the app.                                                                                        |

Browser loads index.html which provides HTML element #root that the React app will be injected into. Also includes script element to load main.jsx
main.jsx creates React app by associating #root el w/ App component found in App.jsx. Causes all the component render funcs to execute and the generated HTML, CSS and JS to be executed in index.html
## Building a production release
When you execute npm run dev, you're bundling code to a temp dir that the Vite debut HTTP server loads from. When you want to bundle your app so that you can deploy to a production environment, you need to run npm run build. Executes the build script found in package.json and invokes the Vite CLI. vite build transpiles, minifies, injects proper JS and outputs everything to deployment-ready version contained in a distribution subdirectory named dist.
## Deploying a production release
Deployment script for Simon React(deployReact.sh) creates a production distribution by calling npm run build, then compying the resulting dist dir to your production server.
