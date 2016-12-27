
# HTML Cheat Sheet

HTML stands for Hypertext Markup Language. It's the language of the web! It tells your browser how to load and display web pages.

## Basic outline

```html
<!DOCTYPE html>
<html>
<head>
  <title>This is document title</title>
  <script src="[PATH TO SCRIPT HERE]" type = "text/javascript"></script>
</head>
<body>
  <h1>This is a heading</h1>
  <p>Document content goes here.....</p>
</body>
</html>
```

## Links
* ```<a href="[YOUR PATH HERE]"> click me! </a>```	Basic Link

## Text Formatting
* ```<h?> ... </h?>```	Heading (?= 1 for largest to 6 for smallest, eg h1)
* ```<em> ... </em>```	Italic Text
* ```<strong> ... </strong>```	Strong - Shown as Bold in most browsers
* ```<em> ... </em>```	Emphasis - Shown as Italics in most browsers

## Section Divisions
* ```<div> ... </div>```	Division (or Section) of Page Content
* ```<p> ... </p>```	Paragraph of Text
* ```<br>```	Line Break
* ```<hr>```	Basic Horizontal Line

<br><br>
## Images
* ```<img src="url" alt="text">```	Basic Image
  * Tag Attributes:
    * src="url"	URL or filename of image (required!)
    * alt="text"	Alternate Text (required!)
    * width="100px"	Image width (in pixels or %)
    * height="100px"	Image height (in pixels or %)

## Lists
#### Ordered List
```html
<ol>
  <li> item #1</li>
  <li> item #2</li>
</ol>
```
<ol>
  <li> item #1</li>
  <li> item #2</li>
</ol>

#### Unordered List
```html
<ul>
  <li> bullet 1</li>
  <li> bullet 2</li>
</ul>
```
<ul>
  <li> bullet 1</li>
  <li> bullet 2</li>
</ul>
