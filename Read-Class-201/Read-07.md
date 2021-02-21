
# Tables

# What's a Table?
A table represents information in a grid format.

Grids allow us to understand
complex data by referencing
information on two axes.
Each block in the grid is referred
to as a table cell. In HTML a
table is written out row by row.

# Basic Table Structure

* The ```<table>``` element is used
to create a table. The contents
of the table are written out row
by row.

* ```<tr>```You indicate the start of each
row using the opening ```<tr>``` tag. At the end of the row you use a closing ```</tr>``` tag.

* ``` <td>```Each cell of a table is
represented using a ```<td>```
element. At the end of each cell you use a
closing ```</td>``` tag.

![tabel](../img/tabel.PNG) 

# Table Headings

* The ```<th>``` element is used just
like the ```<td>``` element but its
purpose is to represent the
heading for either a column or
a row.

**Note:** Even if a cell has no content,
you should still use a ```<td>``` or
```<th>``` element to represent
the presence of an empty cell
otherwise the table will not
render correctly.

* Using ```<th>``` elements for
headings helps people who
use screen readers, improves
the ability for search engines
to index your pages, and also
enables you to control the
appearance of tables better
when you start to use CSS.

![th](../img/th.PNG)

# Spanning ColumnS
Sometimes you may need the
entries in a table to stretch
across more than one column.

The colspan attribute can be
used on a ```<th> or <td>``` element
and indicates how many columns
that cell should run across.

![td](../img/td.PNG)

# Spanning Rows
The rowspan attribute can be
used on a ```<th> or <td>``` element
to indicate how many rows a cell
should span down the table.

# Long Tables

There are three elements that
help distinguish between the
main content of the table and
the first and last rows


* These elements help people
who use screen readers.
 
* allow you to style these sections
in a different manner than the
rest of the table.

1. ```<thead>```
The headings of the table should
sit inside the ```<thead>``` element.
2. ```<tbody>```
The body should sit inside the
```<tbody>``` element.

3. ```<tfoot>```
The footer belongs inside the
```<tfoot>``` element.

![long-tabel](../img/long-tabel.PNG)
<br>




* The ```<table>``` element is used to add tables to a web
page.
*  A table is drawn out row by row. Each row is created
with the ```<tr>``` element.
* Inside each row there are a number of cells
represented by the ```<td>``` element (or ```<th>``` if it is a
header).
* You can make cells of a table span more than one row
or column using the rowspan and colspan attributes.
* For long tables you can split the table into a ```<thead>```,
```<tbody>```, and ```<tfoot>```.



# WHAT IS AN OBJECT?
Objects group together a set of variables and functions to create a model of a something you would recognize from the real world. In an object,variables and functions take on new names.

* IN AN OBJECT: VARIABLES BECOME KNOWN AS PROPERTIES
 If a variable is part of an object, it is called a property. Properties te ll us about the object.

* IN AN OBJECT: FUNCTIONS BECOME KNOWN AS METHODS
If a function is part of an object, it is called a method.
Methods represent tasks that are associated with the object.

![object](../img/object.PNG)

# Create an Object : LITERAL NOTATION


![object](../img/oop.PNG)

<br>

# Document Object Model (DOM)

The Document Object Model (DOM) specifies
how browsers should create a model of an HTML
page and how JavaScript can access and update the
contents of a web page while it is in the browser window.

The DOM is neither part of HTML, nor part of JavaScript; it is a separate set of rules.
It is implemented by all major browser makers, and covers two primary areas:

* MAKING A MODEL OF THE HTML PAGE :
When the browser loads a web page, it
creates a model of the page in memory.
The DOM specifies the way in which the
browser should structure this model using
a DOM tree.

* ACCESSING AND CHANGING THE HTML PAGE :
The DOM also defines methods and
properties to access and update each
object in this model, which in turn updates
what the user sees in the browser.

# THE DOM TREE IS A MODEL OF A WEB PAGE
As a browser loads a web page, it creates a model of that page. The model is called a DOM tree, and it is stored in the browser's' memory. It consists of four main types of nodes.

1. THE DOCUMENT NODE
2. ELEMENT NODES
3. ATTRIBUTE NODES
4. TEXT NODES

![body-Of-HTML-Page](../img/bodyof.PNG)

<br>

![DOM-Tree](../img/DOMtree.PNG)

# WORKING WITH THE DOM TREE
Accessing and updating the DOM tree involves two steps:
1. Locate the node that represents the element you want to work with.
2. Use its text content, child elements, and attributes.

**STEP 1:** ACCESS THE ELEMENTS
1. SELECT AN INDIVIDUAL ELEMENT NODE.

Here are three common ways to select an individual element:

* **get Element Byld ()** : Uses the value of an element's
id attribute.

* **querySelector ()** : Uses a CSS selector, and returns
the first matching element.

![select-an-individual-element](../img/se.PNG)

2. SELECT MULTIPLE ELEMENTS (NODELISTS)

There are three common ways to select multiple elements:

* **getElementsByClassName()** : Selects all elements that have
a specific value for their cl ass attribute.

* **getElementsByTagName()** : Selects all elements that have the specified tag name.

* **querySelectorAll()** : Uses a CSS selector to select all
matching elements.

![select-multiple-elements](../img/se2.PNG)

3. TRAVERSING BETWEEN ELEMENT NODES

You can move from one element node to a related element node.
 
 * **parentNode** : Selects the parent of the current
element node (which will return just one element).

* **previousSibling / nextSibling** : Selects the previous or next sibling from the DOM tree.

* **firstChild / lastChild** : Select the first or last child of the current element.

![TRAVERSING-BETWEEN-ELEMENT-NODES](../img/se3.PNG)


**Note:** The terms elements and element nodes are used interchangeably but when people say the DOM is working with an element, it is actually working with a node that represents that element.


**STEP 2: WORK WITH THOSE ELEMENTS**

1. ACCESS/ UPDATE TEXT NODES

The text inside any element is stored inside a text node. To
access the text node above:
1. Select the ```<li >```element.
2. Use the fi rstChi l d property to get the text node.
3. Use the text node's only property (nodeVa l ue) to get
the text from the element.

**nodeValue** : This property lets you access or
update contents of a text node.

2. WORK WITH HTML CONTENT
One property allows access to child elements and text content:

* innerHTML
* textContent

Several methods let you create new nodes, add nodes to a tree,
and remove nodes from a tree:

* create Element()
* createTextNode()
* appendChild () / removeChild ()

This is called DOM manipulation.


3. ACCESS OR UPDATE ATTRIBUTE VALUES
Here are some of the properties
and methods you can use to
work with attributes:

* className
* id

 get or update the value of the class and id attributes:

 * **hasAttribute()**
* **getAttribute()**
* **setAttribute()**
* **removeAttribute()**

# ACCESSING ELEMENTS
DOM queries may return one element, or they may return a Nodelist,which is a collection of nodes.

Sometimes you will just want to access one individual element. Other times you may want to select a group of elements.

* GROUPS OF ELEMENT NODES
* FASTEST ROUTE
![element](../img/element.PNG)

![element2](../img/element2.PNG)

# SELECTING ELEMENTS USING ID ATTRIBUTES

* **get ElementByid ()** allows you to select a single element node by specifying the value of its
id attribute.

This method has one parameter: the value of the id attribute on
the element you want to select.This value is placed inside quote
marks because it is a string. The quotes can be single or double
quotes, but they must match.

![quote](../img/quo.PNG)

# NODELISTS: DOM QUERIES THAT RETURN MORE THAN ONE ELEMENT
When a DOM method can return more than one element, it returns a
Nodelist.

**Nodelist :** A collection of element nodes.

Nodelists look like arrays and are numbered like
arrays, but they are not actually arrays; they are a
type of object called a **collection**.


## Here you can see four different DOM queries that all return a Nodelist.For each query, you can see the elements and their index numbers in the Nodelist that is returned.

* **getElementsByTagName('hl ' )**
Even though this query only
returns one element. the method
still returns a Nodelist because
of the potential for returning
more than one element.

* **getElementsByTagName('li ')**
This method returns four
elements, one for each of the
```<li>``` elements on the page.
They appear in the same order
as they do in the HTML page.

* **getElementsByClassName('hot')**

This Nodelist contains only three of the ```<li >```elements because we are searching for elements by the value of their class attribute, not tag name.

* **querySelectorA 11 ('li [id]')**
This method returns four
elements, one for each of the
```<li>``` elements on the page that
have an id attribute (regardless
of the va lues of the id attributes).

![selector](../img/select.PNG)









