# Q&A

## 1.Describe what it means for HTML tags to have 'semantic value' and the effect this should have on how HTML documents are constructed.

Every tag in HTML has semantic value. 
That is, every tag has a very specific meaning that the browser will translate into document appearance and structure. 

While building an HTML form, one of the most important steps is to structure it correctly.

 It is important for mainly two reasons: 
 
 1. to guarantee that your form will be usable and 
 2. to make it accessible (that is, usable by differently-abled people).

## What is Semantic HTML

Semantic HTML is HTML that introduces meaning to the web page rather than just presentation. 

For example, a `<p>` tag indicates that the enclosed text is a paragraph. 
This is both semantic and presentational, because people know what a “paragraph” is and browsers know how to display them. 

In HTML4* tags like `<b>` and `<i>` are not semantic, because they define only how the text should look (bold or italic) and do not provide any meaning to the text.

Other examples of semantic HTML tags include:

the header tags `<h1>` through `<h6>`,`<blockquote>`, `<code>`, and `<em>`.

## Why Care About Semantics

The benefit of writing semantic HTML stems from the goal of a web page—to communicate. 
And by adding semantic tags to your documents, you are providing additional information about your document, which aids in communication.

Semantic HTML tags provide information about the contents of those tags that goes beyond just how they look on a page. 
Text that is enclosed in the `<code>` tag is immediately recognized by the browser as some type of coding language. 

It is entirely possible that some user agent could create an entire code library just by reading a website's `<code>` snippets.
In a less futuristic scenario, using semantic tags gives you many more hooks for styling your content. 

This means that perhaps today you prefer to have your code samples display in the default browser style. 
But then tomorrow, you want to call them out with a gray background color, and later you want to define the precise mono-spaced font family or font stack to use for your samples.
If you have all your code samples defined with the semnatic `<code>` tag, this is very easy to do.


## 2.Describe the function of the div tag and discuss the advantages and disadvantages of using it.

The HTML `<div>` tag is used for defining a section of your document. With the div tag, you can group large sections of HTML elements together and format them with CSS.

divisions, often called simply “divs,” have no special semantic value.

they are intended to be used as generic buckets for content, often for the creation of text boxes or other visually styled elements on a page. 

The HTML specification urges web page authors to use `<div>` as “an element of last resort, for when no other element is suitable.” 

## Advantages

1.	More flexible - you can layout the same markup many ways, which means when you have to do a re-branding/update to the site,
        you may not even have to touch the HTML 

2.	Easier to understand and debug: Having 1 master table for layout is easy to work with, but 
    when you start having to go down to 6 or 7 nested tables to achieve your design, it becomes a nightmare. 
    Everyone who has worked with tables has had the nightmare of tracking down an unclosed tag that breaks 
    the layout somewhere but it's impossible to find easily.
    
3.	Easier to maintain: With table-based layouts, making a change to the tables means you have to change every single page. 
    Using CSS, you just change the main CSS file, and all pages get the update automatically
    
4.	Less code: The more complex your layout, the more tables you have to use. 
    I have converted many sites from table-based layout to Div-based layout, and the pages always come out with a smaller file-size
    
5.	More accessible/SEO friendly: Much of your markup is taken by "infrastructure" code in tables. 
    Google only indexes a certain amount of your source, and the farther down the page the actual content is, 
    the less Google has to go on when determining the purpose of the page. 
   

## Disadvantages


1.	The most obvious disadvantage of the DIV tag is the fact that it doesn't aid in adding semantics to the page.

2.	The DIV tag is a generic holder of content.
    As such, a parser has no understanding of why that content is being pulled out and placed in its own container. 
    
3.	For instance, in XHTML, the DIV tag would have been used to surround this question and answer block, 
    allowing the page authors to add CSS styles like a set width and colors. 
    In HTML 5, we have more specific container tags that make it easier for a parser (like a search engine) to understand the way the page is laid out,
    and determine what information is important, and what information is secondary.
    
3.	Explain how unordered and ordered list items can be added to an HTML page.
    Include an explanation of the `type` attribute that can be added to ordered lists.
    
    To add unordered list item: 
    An unordered list starts with the `<ul>` tag.
    Each list item starts with the `<li>` tag.
    
  Code:
```
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
```
```
Output:
•	Coffee
•	Tea
•	Milk
```
  To add ordered list item:
  An ordered list starts with the `<ol>` tag.
  Each list item starts with the `<li>` tag.

Code:
```
<ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```
```
Output:
1.	Coffee
2.	Tea
3.	Milk
```

Ordered HTML Lists - The Type Attribute
A type attribute can be added to an ordered list, to define the type of the marker:

|Type	        |Description                                                 |
|---------------|------------------------------------------------------------|
|type="1"	|The list items will be numbered with numbers (default)      |
|type="A"	|The list items will be numbered with uppercase letters      |
|type="a"	|The list items will be numbered with lowercase letters      |
|type="I"	|The list items will be numbered with uppercase roman numbers|
|type="i"	|The list items will be numbered with lowercase roman numbers|


## 4.Explain the function of the HTML anchor tag. Be sure to discuss its different attributes, like `href` and `target`, what values they take, and the effects of those values.

The `<a>` tag defines a hyperlink, which is used to link from one page to another.
The most important attribute of the `<a>` element is the href attribute, which indicates the link's destination.

By default, links will appear as follows in all browsers:
•	An unvisited link is underlined and blue
•	A visited link is underlined and purple
•	An active link is underlined and red

|Attribute  |href                                                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------|
|Value:     |URL                                                                                                                    |
|Description| Specifies the URL of the page the link goes to. If the href attribute is not present, the `<a>` tag is not a hyperlink| 

Example:
```
<p>An absolute URL: <a href=http://www.google.com>google</a></p>
 
<p>A relative URL: <a href="tag_a.asp">The anchor tag</a></p>
```


Attribute: target

|Value	          |Description                                                   |
|-----------------|--------------------------------------------------------------|
|_blank           |Opens the linked document in a new window or tab              |
|_self	          |Opens the linked document in the same frame as it was clicked |
|_parent	  |Opens the linked document in the parent frame                 |
|_top	          |Opens the linked document in the full body of the window      |
|framename	  |Opens the linked document in a named frame                    |


Syntax:

```
<a target="_blank|_self|_parent|_top|framename">
```


Example:
```
<p>
Open link in a new window or tab: 
<a href=http://www.google.com target="_blank">Visit google</a>
</p>
```

## 5.Explain the purpose and function of the `form` element's two attributes, `action` and `method`.

The HTML`<form>` element represents a document section that contains interactive controls to submit information to a web server.


|Attribute  | action                                                                                                                |
|-----------|-----------------------------------------------------------------------------------------------------------------------|
|Value      |Description                                                                                                            |
|URL        |Where to send the form-data when the form is submitted.                                                                |
	         
	          

Possible values:

An absolute URL - points to another web site
```
 (like action="http://www.example.com/example.htm")
```
A relative URL - points to a file within a web site 
```
(like action="example.htm")
```

```
Syntax:
<form action="URL">
```

```
Example:
<form action="demo_form.asp" method="get">
  First name: <input type="text" name="fname"><br>
  Last name: <input type="text" name="lname"><br>
  <input type="submit" value="Submit">
</form>
```


|Attribute  | method                                                                                                                 |
|-----------|------------------------------------------------------------------------------------------------------------------------|
|Value:     |get, post                                                                                                               | |Description|The method attribute specifies how to send form-data(the form-data is sent to the page specified in the actionattribute)|                                                        

The form-data can be sent as URL variables (with method="get") or as HTTP post transaction (with method="post").
```
Example:
<form action="demo_form.asp" method="get">
  First name: <input type="text" name="fname"><br>
  Last name: <input type="text" name="lname"><br>
  <input type="submit" value="Submit">
</form>
```

## 6. The `input` element has an attribute called "type." Discuss the purpose and function of this attribute, and list some of the values 'type' can be.


|Attribute: |type                                                                                                                    |
|-----------|------------------------------------------------------------------------------------------------------------------------|
|Value:     |Description                                                                                                             |
|button	    |Defines a clickable button (mostly used with a JavaScript to activate a script)                                         |
|checkbox   |Defines a checkbox                                                                                                      |
|color	    |Defines a color picker                                                                                                  |
|date	    |Defines a date control (year, month and day (no time))                                                                  |
|datetime   |The input type datetime has been removed from the HTML standard. Use datetime-local instead.                            |
|dttimelocal|Defines a date and time control (year, month, day, hour,  minute, second, and fraction of a second (no time zone)       |
|email	    |Defines a field for an e-mail address                                                                                   |
|file	    |Defines a file-select field and a "Browse..." button (for file uploads)                                                 |
|hidden	    |Defines a hidden input field                                                                                            |
|image      |Defines an image as the submit button                                                                                   |
|month	    |Defines a month and year control (no time zone)                                                                         |
|number	    |Defines a field for entering a number                                                                                   |
|passwor    |Defines a password field (characters are masked)                                                                        |
|radio	    |Defines a radio button                                                                                                  |
|range	    |Defines a control for entering a number whose exact value is not important (like a slider control)                      |
|reset	    |Defines a reset button (resets all form values to default values)                                                       |
|search	    |Defines a text field for entering a search string                                                                       |
|submit	    |Defines a submit button                                                                                                 |
|tel	    |Defines a field for entering a telephone number                                                                         |
|text	    |Default. Defines a single-line text field (default width is 20 characters)                                              |
|time	    |Defines a control for entering a time (no time zone)                                                                    |
|url	    |Defines a field for entering a URL                                                                                      |
|week	    |Defines a week and year control (no time zone)                                                                          |


```
Syntax:
<input type="value">

Example:
<input type="button" value="Click me" onclick="msg()">
```




