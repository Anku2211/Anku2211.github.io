---
title: HTML5 Canvas To Draw Graphics On Webpage
date: 2020-08-09 19:50:13
tags:
---
HTML5 Canvas To Draw Graphics On Webpage

HTML (Hyper Text Markup Language) is the standard markup language for documents designed to be displayed in a web browser. The other technologies like CSS(Cascading Style Sheets) and scripting language like Javascript are used with it.

HTML5 let us implement exciting desktop-like applications that run in the browser. So here you will get to know about HTML5 Canvas.

Canvas

Canvas is one of the best features in HTML5. We use this for creating better versions of our web applications. The main power of canvas lies in canvas context.
By default the browser made a canvas of size 300x150 pixels but we can also change the size of the canvas element by using CSS.
The Canvas API :

The canvas element provides an API only for two attributes and three methods.

Canvas Attributes -
        1. Width 
        2. Height 

Canvas Methods -

GetContext() - Return the graphic context.

toDataURL(type, quality) - Returns the data URL that you can assign to the src property of an img element.

toBlob(callback, type, args..) - Creates a Blob that represents a file containing the canvas’s image.

Canvas Context :  

The canvas element works as a container for a context. We use the canvas element to get a reference to the canvas’s context that provides an API for drawing shapes and text, displaying and modifying images, etc.

Canvas 2d Context Attributes :

canvas -  Use of canvas attribute is to access the width and height of canvas.

fillStyle -  This specifies the colour, gradient and pattern that context uses to fill the shapes or text.

font - specifies the font that the context uses when we call fillText() or strokeText().

lineCap - specifies how the browser draws the endpoint of a line.

lineWidth - determines the width, in screen pixel of the line that you draw in the canvas.

lineJoin - specifies how lines are joined when their endpoints meet.

Console & Debugger :

All the browsers which support HTML5 like Chrome, Firefox, Opera and Safari give you access to a console and debugger. We can write to the console with the console.log() method and it will appear on the console. With the help of debuggers we can set breakpoints, watch expressions, examine variables and so on.

Performance: 

We need to make performance optimization if we are implementing animation, games or Canvas based applications for mobile devices. 
There are three tools for doing this :

Profilers
Timelines 
jsPerf

Profilers and Timelines are provided directly by the browser.
Profilers and timeline are essential to discovering performance barriers in our code. Profilers also show us how many times each function in our application is called and how long it takes.

Timelines give us a record of events that occur in our   application.It will give us the detailed record of each event like their duration and affected area of the window.

jsPerf is a website that helps you to create performance tests and make them publicly available. jsPerf shows us all the test cases which are publicly available.
