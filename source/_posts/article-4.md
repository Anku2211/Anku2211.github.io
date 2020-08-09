---
title: Modification of TEXT in HTML5 Canvas
date: 2020-08-09 22:30:05
tags:
---

The Canvas element provides  some basic features that you can find in a simple text editor, such as text selection, copy and paste, and scrolling. Canvas supports some text necessities such as stroking and filling text, placing text on the canvas and measuring the width of text in pixels. 
#### The canvas context provides three methods related to text :

    1.strokeText (text, x, y)
    2.fillText (text, x, y)
    3.measureText(text)

The measureText( ) method returns an object with a width property, which represents the width of the text that we pass to the method.
#### There are three Canvas context properties that are related to text :

    1.font
    2.textAlign
    3.textBaseline 

The font property lets us set the font of text which we draw, and textAlign and textBaseline let us position text within the canvas. 

It uses fillText( ) and strokeText( ) to fill and stroke the text. Each of these methods takes three arguments. The  first argument is the text, and the remaining two arguments specify the text’s location. 

The exact location of the text depends upon the textAlign and textBaseline properties. Both strokeText and fillText takes an optional fourth argument that specifies the width of text. If  we use strokeText ( ) or fillText( ) with the optional fourth argument and the text exceeds that width, then the Canvas specification requires the browser to resize the text so that it fits in the specified width.  Browsers can change the size of font or scale the text horizontally, but in both the cases the text must still be readable

    Eg.    context.fillText (text, 65, 450);
           context.strokeText (text, 65, 450);

### Setting Font Properties

We can set the font of the text that we draw in a canvas with the context’s font property. The default Canvas font is 10px sans-serif. The default value for font-style. font -variant, and font weight are all normal.
    
    Font Property              Valid Values
         
    font-style                 Three values are allowed : normal, italic oblique.            

    font-variant               Two values are allowed : normal, small-caps.

    font-weight                Defines the thickness of font’s characters : normal   
                               bold, bolder, lighter.(Goes from 100 to 900)

    font-size                  values for font size : xx-small, x-small, medium, large,
                               x-large, xx-large, smaller, larger, length, %.

    line-height                The browser always forces this property to its default 
                               value, which is normal.

    font-family                Two types of font family names are allowed : family-name, 
                               such as Helvetica, verdana, palatino and generic-family 
                               names : serif, sans-serif, monospace, cursive and fantasy.


### Positioning Text

We can set both the horizontal and vertical position of the text in the Canvas.  For the positioning of text we use textAlign and textBaseline methods.

       Property                Description

       text-Align              Specifies how text is aligned horizontally. Valid values are
                               start, left, center, right, end. The default value is start.

       textBaseline            Specifies how text is aligned vertically. Valid values are
                               top, bottom, middle, alphabetic, ideographic, and hanging. The default value is alphabetic.

### Valid values for textAlign are as follows :

    start
    center
    end
    left
    right                             

### Valid values for textAlign are as follows :

    top       
    center
    end
    left     
    bottom 
    middle 
    alphabetic
    ideographic
    hanging  


### Centering Text

We can center text about a point with the textAlign and textBaseline attributes of the Canvas context.
          context.textAlign = “center”
          context.textBaseline = “middle”  

### Measuring Text

To do anything interesting with text, we must be able to measure the width and height of text. To place the cursor at the end of a line of text, we must calculate the width of the text. The Canvas context provides a measureText( ) method that lets us measure the width, in  pixels, of a string. The measureText( ) method returns a TextMatrics object that contains a single property : the width of the string.

           getWidth : function(context) {
                      Return context.measureText (text).width;
                      }
 
### Drawing Text Around An Arc

We can draw text around an arc with the following steps :

    1.Calculating each character’s position along the arc.
    2.Translating the context to that position.
    3.Rotating the context by π-angle.
    4.Stroking or Filling the character or we can do both.

