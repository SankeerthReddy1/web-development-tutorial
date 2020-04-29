### This is the documentation for the web tutorials we are going to work on.

### HTML5

_The Contents of the HTML5_

* Introduction to HTML
* Elements
* attributes
* styles
* Links & Images
* Tables
* Lists
    * ordered List 
    * unOrdered List
* classes and ID's 
* Layout 
* Responsive 


## Introduction 

HTML is the standard markup language for creating Web pages.
Browser utilizes the  html tags to display content on the screen. Each Html tags have a specific scematic meanings and browser has default styles added to the HTML tags.

# Lets get Started -
_So HTML isn't pretty?_

Plain HTML isn't but it can be made awesome looking using styles and libraries(CSS, Bootstrap, etc) and clickable (JavaScript).
Every html starts with the tag
``` html
<!DOCTYPE html>
```
This way the browser recognizes that this is a valid .html file.
You're probably wondering what a tag is.    <br>
A tag is

``` html
<something here inside>
```

it consists of an opening tag and usually (not every tag has one) a closing tag:

``` html
</something that was in the opening tag>
```

Eveything that's between the opening and the closing tag is affected by the action this tag does. The

``` html
<!DOCTYPE html>
```

doesn't have a closing tag and neither does

``` html
<br>
```
Br is the tag for new line.  

After that our html has

``` html
<html> tag
```

The html tag has a closing tag:

``` html
</html>
```

In between the html tags, our code looks just like a human - it starts with

``` html
<head> some code here </head>
```

and after the head we have

``` html
<body> some code here </body>
```

 Between the head tags we place the head elements.

# The following elements go inside the head element:
<blockquote>
title = what is shown at the tab in your browser <br>
style = here we put rules for styling (in another language called CSS) <br>
link = links <br>
meta = tags always go inside the head element, and they provide metadata about the HTML document. <br>
script = actions for you page <br>
</blockquote>

``` html
<head>
  <meta charset="UTF-8">
  <title>HTML Reference</title>
  <meta name="description" content="Free Web tutorials">
  <meta name="keywords" content="HTML, CSS, JavaScript">
  <meta name="author" content="John Doe">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
```
__Example for Script Tag__ 

``` html
<script>
document.write("Hello World!")
</script>
<script src="demo_defer.js" async></script>
<script src="demo_defer1.js" defer></script>
<noscript>Your browser does not support JavaScript!</noscript>
```

``` html 
<head>
  <link rel="stylesheet" type="text/css" href="theme.css">
  <link rel="stylesheet" type="text/css" href="print.css" media="print">
  <style>
    h1 {color:red;}
    p {color:blue;}
  </style>
</head>

```

Most of the things you will want to add (like sentences, pictures, etc)
will be added in the body tag. Now lets learn more about them.

# how to write comments in Html file:
``` html
<!-- Write your comments here -->

<!-- This comment
is also legit -->
```

## Elements 

``` html
<div>Headings</div>
<h1>This is heading 1</h1>
<h2>This is heading 2</h2>
<h3>This is heading 3</h3>
<h4>This is heading 4</h4>
<h5>This is heading 5</h5>
<h6>This is heading 6</h6>
<p> <strong>Headings</strong> are just like paragraphs **BUT** they have different font sizes. h1 is the biggest heading and h6 is the smallest.
<span>Headings have default styling drak and blod</span>
Search engines use the headings to index the structure and content of your web pages and users skim your pages by its headings. Also, by using headings the User Experience is better than if we only use paragraphs./p>
```

## Simple text formatting tags
``` html
<b> - Bold text
<strong> - Important text
<i> - Italic text
<em> - Emphasized text
<mark> - Marked text
<small> - Small text
<del> - Deleted text
<ins> - Inserted text
<sub> - Subscript text
<sup> - Superscript text
```

## Schematic Elements and Non Schematic Elements 

A semantic element clearly describes its meaning to both the browser and the developer.

Examples of non-semantic elements: <div> and <span> - Tells nothing about its content.

Examples of semantic elements: <form>, <table>, and <article> - Clearly defines its content.

``` html 
<article>
<aside>
<details>
<figcaption>
<figure>
<footer>
<header>
<main>
<mark>
<nav>
<section> 
<summary>
<time>
```
## Images
Up until now, we've been using only text. How about we add some pictures? <br>
In HTML pictures are added using:

``` html
<img src = "a_link_to_your_image"/>
```
Note how the tag is closed - the tag is both an opening and a closing tag.
TO DO: Talk about relative/absolute links

But what should happen when our image doen't load?
Or the device the user is using displays only text?
We add an alt attribute. It is a good practice to always have the alt attribute.

``` html
<img src = "a_link_to_your_image" alt="What your image is about"/>
```

## Links
Now let's learn about links. For exammple, you want when a user clicks on a text, to open your other site.

``` html
<a href = "link_address_here"> The text the user should click here </a>
```

But have you noticed how some links open in the same tab and others for example open in a new tab? This is done with **the target attribute**.
The target attribute specifies where to open the linked document and it can have one of the following values:
<blockquote>
_blank - Opens the linked document in a new window or tab <br>
_self - Opens the linked document in the same window/tab as it was clicked (this is default) <br>
_parent - Opens the linked document in the parent frame <br>
_top - Opens the linked document in the full body of the window  <br>
framename - Opens the linked document in a named frame <br>
</blockquote>

That's pretty much all about links. Not that hard, right?

## Lists
Lets's say you want to go shopping. Do you write long paragraphs about what you want to buy?
Probably not. You use lists. And HTML has lists too.
In HTML, just like in the real world, our lists can be either ordered or unordered.

### ordered lists

``` html
<body>
        <ol>   <!-- Everything between the opening and the closing ol list is taken as a list item -->
            <li> list item 1 </li>  <!-- what is between the opening and closing li is considered a SINGLE list item -->
            <li> list item 2 </li>
            <li> list item N </li>
        </ol>
</body>

```
By default this list is shown with arabic numbers.
We can change this with the type property (that's CSS and we'll talk soon about CSS).

### unordered lists

``` html
<body>
        <ul>  
            <li> list item 1 </li>  
            <li> list item 2 </li>
            <li> list item N </li>
        </ul>
</body>

```
By default, the list item here are shown with circles in front. If we want to change that,
we use the CSS **list-style-type**, which we'll talk about later.

## Tables
To represent data, we sometimes use tables (Google Spreadsheets, Excel, etc).
HTML has tables too and they are quite easy to use.

``` html
<table>
  <tr>
    <th>table row 1 first square</th>
    <th>table row 1 second square</th>
  </tr>
  <tr>
    <td>table row 2 first square</td>
    <td>table row 2 second square</td>
    <td>50</td>
  </tr>
  <tr>
    <td>table row 2 first square</td>
    <td>table row 2 second square</td>
  </tr>
</table>
```

An HTML table is defined with the table tag.
Each table row is defined with the tr tag. A table header is defined with the <th> tag.
By default, table headings are bold and centered. A table data/cell is defined with the td tag. 