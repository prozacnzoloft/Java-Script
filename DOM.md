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

## querySelector('Tag name')

    const byQuery = document.querySelector('p');
    console.log(byQuery, typeof byQuery)

This will select the first element of given tag name from the webpage,

## querySelectorAll()

    const byQueryAll = document.querySelector('p')
    console.log(byQueryAll, typeof byQueryAll)

This will return an array of all elements matching the selector of give tag name from the webpage.
