# Week 1: HTML & CSS
---
Welcome to the first session of ACM BITS Pilani Dubai's 2022 Coding BootCamp !! We hope this bootcamp will set a rock solid foundation to your journey in Computer Science!

This week, we'll be learning about HTML and CSS, and we'll cover these topics today.


- Intro to Web-Dev
- Languages (HTML/CSS/JS/SQL)
- Tags (h, p, b, div, span, etc.)
- HTML Tables
- Semantic HTML
- Intro to CSS
- Different methods to link CSS with HTML
- Selectors and Visual Rules
- "How to use Dev Tools?"
- Colors
- Position (absolute, relative, fixed)
- Typography
- Grid
- Flexbox
- Forms

---
## What is Web Development ?
Web development refers to the process of  building, creating, and maintaining websites. It can be divided in to two parts; 
-  **Front-end/Frontend**: 
The front-end as the name suggests refers to the actual website that all the users will be able to see and interact with. A **front end developer** would would write code for the design, layout, colour schemes, animations, etc. of the website and make sure that it **looks beautiful and  modern**.

- **Back-end/Backend**:
The back-end refers to the functions of the website which is not seen by the  users, these include information retrieval from databases,image loading, form submissions, login/logout authentication, API Calls, etc. A **backend developer** would write code to perform all the above mentioned tasks, with the aim of making the website get these tasks done as **fast as possible** so that the website will have **minimal lag**.
A developer that is responsible for writing code for both frontend and backend is called a Full Stack Developer.
The three main languages which you will encounter frequently in Web Development are: 
- **HTML**: The HyperText Markup Language or HTML is the standard markup language for documents designed to be displayed in a web browser.
- **CSS**: Cascading Style Sheets (CSS) is a style sheet language used for describing the presentation of a document written in a markup language such as HTML or XML.
- **JavaScript**: JavaScript often abbreviated JS, is a programming language that is one of the core technologies of the World Wide Web, alongside HTML and CSS. This language is used for coding the behaviour of a website (for e.g. what happens when you click a button). Many frameworks and tools used for web development  are based on Javascript, such as React,Vue, Angular. Javascript is also used for server-side/backend programming, based on NodeJS framework. Many useful JS modules and packages are availible via npm (Node Package Manager).

This week, we'll be focusing on the concepts of HTML and CSS. 
## What is HTML?
HTML stands for Hyper Text Markup Language, and it is the standard markup language for creating web pages. HTML describes the structure of a Web page, and consists of a series of elements (usually starting with `<html>` and ending with `</html>`). Elements tell the browser how to display the content
## HTML Tags
Elements are denoted as "tags" in HTML, starting with `<>`and ending with `</>` . There is a tag for every element of a web page, for example:
```html
<html></html> <!-- This is the HTML document tag, marks the start and end of HTML document-->
<title></title> <!-- Title of a webpage -->
<body></body> <!-- Body of a webpage -->
<script></script> <!-- You can write Javascript code here, this tag is usually inside <body> at the ending before </body> -->
<p></p> <!-- Paragraph tag, usually you place your text inside a <p> tag or a <div> tag -->
<h1></h1> <!-- Header Text Tag -->
<h2></h2> <h3></h3> <h4></h4> <!-- You can give smaller header text sizes also 1:biggest 6:smallest>
<!--This is a comment tag -->
<br> <!-- This is a new line tag, does not need a closing tag -->
<img src="/././*.jpg"> </img> <!--This is an image tag -->
<audio></audio> <!-- This is an audio tag, if you want to play sounds on the webpage -->
<div></div> <!-- This is a very commonly used tag, basically if you want create a -->
<!--box section.You can place other content inside and the size/colour and other properties can be changed using CSS. -->
<a href="someotherwebsite.com"> Click me pls :') </a> <!-- This is link tag which redirects to another website -->
<form></form> <!-- This tag is used for denoting forms (signup/login/other) -->
<input></input> <!-- This tag is used for creating an "input text" field>
<button>Click here</button> <!-- Used for creating a button>
<ul>           <!-- The <ul> tag stands for unordered list -->
    <li> </li>  <!-- the <li> element signifies a list item inside the UL.-->
    <li> </li>
    ..
</ul>

```
<centre><img src="assets/ross_list.jpg" alt="drawing" style="width:500px;"/></centre>
*Ross didn't know about HTML lists. Don't be like Ross.*
Here is an example of how tags are arranged in an HTML document:

```html
<html>
<head>
  <link rel="stylesheet" href="styles.css"> <!-- This tag is used to link other files-->
</head>
<title> This is the title on the tab area of browser </title>
<body>      <!--Signifies body of the webpage-->

<h1>Header Element</h1>
<p>Paragraph element</p>

<ul>
    <li>List Item1</li>
    <li>List Item2</li>
    <li>List Item3</li>
</ul>
<div>
    <img src="image.jpg"></img> 
</div>
<script><!-- You can write any javascript code inside here to change the behaviour of the website --> </script>
</body>

</html> <!-- signifies the end of the HTML document -->
```
You can also access the entire list of HTML tags [here](https://www.w3schools.com/tags/default.asp).

## HTML Tables
You can also create tables in HTML using the `<table>` tag. For each row inside a table, you need to include a `<tr></tr>` tag, and for each column element inside a row, `<td>` tag is used. If you also want to add table header, then you can make another  Let's look at an example:
```html
<html>
    <title>Our table</title>
    <head> <!--Adding some css to be able to see the table border-->
	<style> 
	table, th, td {
 	 border: 1px solid black;
	  border-collapse: collapse;
	}

	</style>
    </head>
    <body>
        <table >
            <tr> <th>Column 1</th> <th>Column 2</th> <th>Column 3</th>
            </tr>
            <tr> <td>R1C1</td> <td>R1C2</td> <td>R1C3</td>
            </tr>
            <tr> <td>R2C1</td> <td>R2C2</td> <td>R2C3</td>
            </tr>
        </table> 
        <!-- Here R1C1 means Row 1 column 1 -->   
    </body>

</html>
```
<img src="assets/Ourtable.jpg" alt="drawing" style="width:300px;"/>
<br>

*Output of the above code*
## Semantic HTML
A semantic element in HTML clearly describes what it means to both the developer and the browser. Non-semantic elements such as `<div>` and `<span>` tell us nothing about its content from the name, however elements such as `<form>`, `<table>`, `<article>` clearly denote that they contain a form, table and article.
<img src="assets/htmlsemantic.gif" alt="drawing" />
For example in the above image, if we use the header/nav/footer tag at any location in the HTML file, then they would refer to that part of the webpage since the browser already knows by the tag name which location the content should go.
<img src="assets/chandler_semantic.jpg" alt="drawing" style="width:450px;" />
*Unfortunately Chandler still doesn't know the semantics of his life*

## Intro to CSS

**Cascading Style Sheets**, fondly referred to as CSS, is a simply designed language intended to simplify the process of making web pages presentable. CSS allows you to apply styles to web pages. More importantly, CSS enables you to do this independent of the HTML that makes up each web page. It describes how a webpage should look: it prescribes colors, fonts, spacing, and much more. In short, you can make your website look however you want. CSS lets developers and designers define how it behaves, including how elements are positioned in the browser.

Let's take a look at some syntax of CSS.
```CSS
h1{  /* Here, the h1 part is called selector since it selects only the h1 html tags and applies these properties.*/
    color:blue;
    size:12px;
    background-color:red;
/* The curly braces part is called the declaration.*/
}
```
## Different ways to link CSS with HTML
There are three ways to link a CSS file with HTML: 
- #### External CSS:
When we talk of external CSS, we have our CSS stylesheet stored in a different file than the HTML file. 
To use the CSS style sheet, each HTML page must include a reference to the external style sheet file inside the <link> element, inside the head section, for e.g.
```HTML
<html>
    <head>
        <link rel="stylesheet" href="mystyle.css">
    </head>
    <body>

        <h1>This is a heading</h1>
        <p>This is a paragraph.</p>

    </body>
</html>
```
- #### Internal CSS:
An internal CSS stylesheet may be used if the design and colours of the stylesheet are unique to that specific HTML file, i.e it doesn't need to be shared among other HTML pages. The internal CSS is defined inside of the `<style>` tag, inside the `<head>` section. for e.g.
```HTML
<html>
<head>
<style>
body {
  background-color: linen;
}

h1 {
  color: maroon;
  margin-left: 40px;
}
</style>
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```
- #### Inline CSS:
An inline CSS style is applied when we want to apply a unique style to a single element on a webpage. This can be done using the `style` property within a tag and specifying the properties in that.
```HTML
<html>
<body>

<h1 style="color:blue;text-align:center;">This is a heading</h1>
<p style="color:red;">This is a paragraph.</p>

</body>
</html>
```
## CSS Selectors and Visual rules
CSS selectors are used to "find" (or select) the HTML elements you want to style. There are a few ways in which you can use CSS selectors:
- **Simple selectors**: Using Simple Selectors you can select HTML elements based on their name, id or class. For e.g.
```CSS
 p {   /*Here, all <p> elements on the page will be center-aligned, with a red text color */
  text-align: center;
  color: red;
}

#para1 {
/* The CSS rule below will be applied to the HTML element with id="para1"  */
text-align: center;
  color: red;
}
.center {
 /*all HTML elements with class="center" will be red and center-aligned*/   
  text-align: center;
  color: red;
}
```
   
- **Combinator selectors**: Using this method, you can select HTML elements based on a defined relationship between elements, for example child of an element, adjacent to an element, etc.
```CSS
/* selects all <p> elements inside <div> elements (Descendant selector)*/
div p {
  background-color: yellow;
}
/* selects all <p> elements that are children of a <div> element (Child Selector) */
div > p {
  background-color: yellow;
}
/* Sibling elements must have the same parent element, and "adjacent" means "immediately following"
The below rule selects the first <p> element that are placed immediately after <div> elements (Adjacent Sibling selector) */
div + p {
  background-color: yellow;
}
/* The general sibling selector selects all elements that are next siblings of a specified element.
The below rule selects all <p> elements that are next siblings of <div> elements 
 */
div ~ p {   
  background-color: yellow;
}
```
Now moving on to **CSS Visual Rules**, these are basically the rules which we write inside the declaration part `{}` of the rules in a CSS Stylesheet. Let's look at some basic CSS rules to get started:

```css
/* 
CSS declaration format:
property-name: value;
*/
/* Lets take a paragraph tag for example. */
<some tag>{
font-size: 30px;   /* The font-size CSS property is used to set text sizes. Font size values can be many different units or types such as pixels*/
background-color: blue; /* The background-color CSS property controls the background color of elements.*/
width: 200px !important; /*The CSS !important rule is used on declarations to override any other declarations for a property and ignore selector specificity */
opacity: 0.5; /* The opacity CSS property can be used to control the transparency of an element. The value of this property ranges from 0 (transparent) to 1 (opaque). */
font-weight: bold;  /*The font-weight CSS property can be used to set the weight (boldness) of text.*/
text-align: right; /* The text-align CSS property can be used to set the text alignment of inline contents. This property can be set to these values: left, right, or center*/
color : #2a2aff ; /*Using the color property, foreground text color of an element can be set in CSS. You can set the value to either "red", "blue", etc or it can be a hex value like #2a2aff*/
background-image: url("../resources/nyancat.png"); /*The background-image CSS property sets the background image of an element. An image URL should be provided in the syntax url("moon.jpg") as the value of the property.*/
font-family: "Courier New"; /* The font-family CSS property is used to specify the typeface of the text. When using a multi-word font name, it is best practice to wrap them in quotes*/
}
```
## How to use browser DevTools?


