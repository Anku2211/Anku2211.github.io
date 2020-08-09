---
title: HTML5 CANVAS- DRAWING
date: 2020-08-09 22:20:52
tags:
---
 
 The HTML5 2d context provides us with a powerful graphic API to implement advanced and effective graphics applications that run in a browser. It will let us know about graphics and how to work on a paint application. The paint application lets us draw text, lines, rectangles, circle, curve and path both open and closed.


The Coordinate System 
The Canvas coordinate system by default places it’s origin at the upper-left corner of the canvas. Transforming the coordinate system is essential and helps us a lot with the numerical values. We can transform the coordinate system in the following ways -

Translate 
Rotate
Scale
Create custom transformation ( shear)



Drawing Rectangles

The Canvas API provides three methods for clearing, drawing and filling the rectangles 


clearRect(double x, double y, double w, double h)
strokeRect (double x, double y, double w, double h)
fillRect (double x, double y, double w, double h)

strokeRect( ) draws the rectangle and fillRect fill the rectangle. We use context’s lineJoin property to round the corner of rectangles.

                 context.lineJoin = ‘round’
                 context.lineJoin = ‘butt’   (by default)









Color & Transparency

If we want to use different colours to draw and fill the rectangles then we can do that by setting the  strokeStyle and fillStyle properties of the context.


                
context.strokeStyle = ‘goldenrod’
context.fillStyle = ‘rgba (0, 0, 255, 0.5)’

Here we used goldenrod colour for to draw the fist rectangle and semi transparent blue for filling the second rectangle.



Gradient & Patterns
We can specify gradients and patterns for strokeStyle and fillStyle attributes. 
The Canvas element provides both linear and radial gradients.

 
Linear Gradient

We can create a linear gradient by using the createLinearGradient( ) method.
createLinearGradient( ) returns an instance of  CanvasGradient. It sets the fillStyle to the gradient and calls for fill( ) method.  After  creating the gradient we add five color - stop to the code by invoking CanvasGradient’ s  addColorStop ( ) method. This method takes two parameters, first parameter represents the position of the color- stop and the second one represents the CSS3 color string.


Radial Gradient

To create a radial gradient, we specify two circles, which represents the end of a cone. Like createLinearGradient( ) , createRadialGradient ( ) method returns an instance of CanvasGradient. We add color-stop to the gradient and set the fillStyle to the gradient.
CanvasGradient
createLinearGradienr(double x0, double y0, double x1, double y1)

CanvasGradient

createRadialGradient( double x0, double y0, double r0, double x1, double r1)


Patterns

Canvas element lets us stroke and fill both shapes and text with patterns. The pattern can be an image, a canvas, a video element. We can create this with createPattern( ) method which takes two arguments -

The pattern itself

String that specify how the browser repeats the patterns

We can specify one of the following value for the second argument :
( repeat, repeat-x, repeat-y, no-repeat )

Javascript creates an image, and creates a pattern with that image and the repetition argument that you specify when you select the radio button. The application then uses that pattern to fill the  entire Canvas.

