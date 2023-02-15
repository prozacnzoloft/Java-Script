# Introduction
The **Document Object Model** is a inbuilt JS object used to **modify**, **change** and **delete** content of a webpage. Examples include toggling a menu, rotating between images in a slide show, showing errors in a form etc.
The DOM itself is a property of the window object which can be used to access the toolbars and dimensions of the window and other things like that. We can think of the window object as the global top level object representing a tab in the browser.

# The DOM Tree

![DOM Tree](https://www.w3schools.com/js/pic_htmltree.gif)

In the diagram of DOM tree we can see that the Document is the root node. It has one child node, html. The Document node is the parent node of the html node. Similarly the html node has two children the head node and the body node. The head node and the body node are siblings. Again coming down through body note we see that the a node has two nodes. However the  attribute node doesnot parttake in the parent-child-sibling relation of DOM tree, instead they are accessed by using the property of the element node they belong to.

# Selecting node
In order to work with the elements of a webpage first we need to select the element. There are 5 ways of doing that that we learn here.

## getElementById()

    const byID = document.getElementById('defaultId');
    console.log(byID, typeof byID);

This will select the element of Id of given Id name from the webpage.


## getElementByTagname()

    const byTag = document.getElementsByTagName('p');
    console.log(byTag, typeof byTag);

This will select the element of tag of given Tag name from the webpage.

## getElementByClassname()

    const byClass= document.getElementsByClassName('defaultClass');
    console.log(byClass, typeof byClass)

This will select the element of class of given class name from the webpage.

## querySelector('cssSelector')

    const byQuery = document.querySelector('p');
    console.log(byQuery, typeof byQuery)

This will select the first element of given tag name from the webpage,

## querySelectorAll('cssSelector')

    const byQueryAll = document.querySelector('p')
    console.log(byQueryAll, typeof byQueryAll)

This will return an array of all elements matching the selector of give tag name from the webpage.

## Changing style of elements
### Direct inline styling
Syntax:

    element.style.cssProperty = 'value';

This way only works on a single element and not an an array of element objects. Also, the css property here is written in camel case as opposed to normal snake case in css file.

## Creating elements
In order to create an element in html file we need to use the `createElement(tagName)` method and then append the resulting element to the element in file.
Example:

    const name1 = document.querySelector('tag1');
    const name2 = document.createElement('tag2');
    name1.appendChild(name2);

This code will add an element of tag `<tag2>` to first element of tag `<tag3>` in the html file.

## Modifying text contents of an element
In order to modify the text contents of an element we can use either of these three ways:

innerText:
This returns or sets the value of inner text as it is excluding the tag and format of html document.

textContent:
This returns or sets the value of the inner text according to given format from code file.	

innerHTML
This returns or sets the inner html code of an element.


The working of all three of these methods is explained by example below.

    const def = document.querySelector(sampleId)
    console.log(def.innerText)
    console.log(def.innerHTML)
    console.log(def.textContent)

## Modifying attributes of an element
To work with the styling of an element we can use the `.style` property of a DOM element.

### Creating an attribute

setAttribute.
Example:

    element.setAttribute('class', 'className')

### Removing an attribute

removeAttribute.
Example:

    element.removeAttribute('class')

### getting an attribute.
getAttribute.
Example:

    element.getAttribute('attributeName');

This returns the value of the attribute that is mentioned.

### Working w/ classes

#### adding a class to an element

    node.classList.add("className")

#### deleting a class from list of classes in an object

    node.classList.remove("className")

#### checking if a class of className is in the class attribute of an element or not

    element.classList.contains("className")

## Removing an element from the page

element.remove();

## Navigating the DOM
From previous notes we are clear about element relation of a DOM tree (parent, children and siblings), now we learn to navigate through them so that we do not have to make a constant for each element we want to access.

There are three methods of navigating through elements of DOM:
**Parent Node Traversal
Child Node Travelsal
Sibling Node Traversal**

Before that we need to understand that the DOM treats the text or comments of a html file as nodes.

### Parent node traversal
Here we learn to navigate from a child element to its parent element
Example:

    let okay = document.querySelector('.sampleClassName');
    okay.parentNode			//navigates to the parent node, probably a #text
    okay.parentElement		//navigates to the parent element
    okay.parentElement.parentElement	//navigates to the grandparent element

### Child traversal
Here we learn to navigate from parent element of a file to it's children element

`element.childNodes` will give you an array of all nodes that are the children of selected element.
`element.childNodes[i]` will navigate to node of i index among the children of selected element.
`element.firstChild` will navigate to the first child node of selected element
`element.lastChild` will navigate to the last child node of selected element.

`element.children` will give you an array of all children elements of selected element
`element.children[i]` will navigate to element of i index among the element children of selected element.
`element.firstElementChild` will navigate to the first child element of selected element
`element.lastElementChild` will navigate to the last child element of selected element

### Sibling Traversal
`element.previousSibling` navigates to the node before itself
`element.nextString` navigates to the node after itself
`element.previousElementSibling` navigates to the element before itself
`element.nextElementSibling` navigates to the element after itself

## Event listeners
Events in Java Script are the actions performed by the user on the page. We can listen to what the user does and respond accordingly. There are two ways to add event listeners to an element of html



    //in html
    <element tag onEvent="script"> inner text </element>
    
    //or 
    //in js
    element.addEventListener('event', script);

Some common events of Java Script include '`click`' , '`onchange`' , '`mouseover`' etc.

### Capturing and bubbling
While elements with same event listeners are nested and the event occurs, we need to define the path the code will follow.
In the `addEventListener` property there can be a third argument which defines the order of flow of execution of scripts of different nested elements.
**Capturing** means the script of the outermost element will be executed first and then the flow comes in-ward to the target element whereas in **Bubbling** the script of the target element is executed first and the wave goes outwards. 
Default value of third argument is true and capturing wave is followed. 
Apart from this we can also stop propagation of this wave of listening and execution of code by using the `stopPropagation`() property.
Event delegation is the method of not executing the default task of an element on occurrence of an event. Example: We can make a `<a>` tag  not open a link. 
