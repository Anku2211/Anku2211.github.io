---
title: Different Methods Of Drawing And Editing In HTML5 Canvas
date: 2020-08-09 22:29:52
tags:
---


The HTML5 Canvas allows us to draw the different shapes on the canvas by the different methods available in Canvas. It also allows us to edit the coordinates, origin and shapes and filling and stroking to different shapes.
Here we will see some further concepts or methods which we can use for drawing on Canvas.

Path, stroking and Filling

We can fill and stroke the path, arc and rectangles by fill( ), stroke( ) method respectively. When we fill an open path in canvas the browser fills the path as if it were closed.Here are some method related to this -

beginPath( ) - This method begins a new path.

rect( ) / arc( ) - Both create paths for rectangles and arcs, respectively.

stroke( ) / fill( ) - Strokes and fills the path.

closePath( ) - We have to call this method if we want to close an arc.

Path :

Canvas uses a non-zero winding rule for filling a path that intersects with itself. This rule says that every time a line crosses itself add one to the counter for the clockwise segment of the path and subtract one from the counterclockwise path segment.

If the final output count is non-zero then the area lies within the path, and the browser fills it when we invoke fill( ) method. If the final count is zero, then the area does not lie within the path, and the browser does not fill it. We can also apply this rule for the cutout of a shape to fill it. 

Lines &  PathT

The Canvas provides two methods to create a linear path moveTo( ) and lineTo( ). We can create a path by combining these two methods and then we have to use the stroke( ) method to draw the path.


Rubber-band Lines

We use the method called rubberbandShape( ) to draw the rubberband lines. As we drag the mouse it maintains the rubberbandRect( ) which creates the rectangle. This rectangle defined by the two corner -
The location of the mouse down event and the mouse’s current location.
For every mouse move event that occurs while the user is dragging the mouse, the application does three things:

    1.Restores the drawing surface
    2.Update rubberbandRect
    3.Draws a line from the mouse down location to the current mouse location 

Drawing Dashed Lines

Canvas context does not provide a method to draw dashed or dotted lines but we can draw it by ourselves. The code calculates the length of the line and, based on the length of each dash, figures out how many dashes the line will contain. Based on the number of dashes, the code draws a dashed line by repeatedly drawing short line segments. 
				
			
Dial & Gauges

If we want to make a dial showing degrees of a circle then we have to use cutout techniques to give the ring a translucent background by using arc( ) method to draw the outer circle clockwise and inner circle counterclockwise.

Bezier Curves

Originally Bezier Curves used to be designed in automobile bodies but today they are widely used  in most computer graphics systems and HTML5 Canvas is one of them.
There are two types of bezier curves -

Quadratic curve
Cubic curve

Quadratic curves are second degree curves, meaning that they are designed by three points - Two anchor points and one control point.
Cubic bezier curves are third degree curve, so they are designed with four points -
Two anchor points and two control points.

Quadratic Bezier Curve

It is a simple curve that curves only in one direction. We use context.quadraticCurveTo( ) method for this. This method takes four arguments, which represents X and Y coordinates of two points. The first point is the curve’s control which determines the shape of the curve, the second point is the anchor point. The quadraticCurveTo( ) method connects the anchor point to the last point we designed in the curve path.

Cubic Bezier Curve

We use bezierCurveTo( ) method to create a path for a cubic bezier curve. It is a two directional curve, we use to pass three points for this method, two points are control points and last points is the anchor point. 

Polygons

We can use the moveTo( ) and lineTo( ) method combined with some simple trigonometry to draw polygons with any number of sides.

The getPolygonPoint( ) function creates and returns an array of points for a polygon
Defined by the five parameters you passed to the function.
The createPolygonPath( ) function calls getPolygonPoint() to obtain the array of points for the polygon, moves to the first point and then creates a path encompassing all the polygon’s vertices. Finally it is the drawRubber-bandShape( ) function that actually draws the polygon.



