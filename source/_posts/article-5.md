---
title: Images and Videos in HTML5 Canvas
date: 2020-08-09 22:30:16
tags:
---

We can draw images, scaled or unscaled, anywhere in the Canvas, and we can access and manipulate the color and transparency of each pixel. By combining image manipulation with other methods of Canvas API we can create extra effects, such as animations and multiplayer games, data visualization or particle physics simulations.

The Canvas context provides four methods for drawing and manipulating images : 

drawImage( )
getImageData( )
putImageData( )
createImageData( ) 

We can draw an image into a Canvas by drawImage( ) method as well as another canvas into a canvas, or a  video frame into a canvas by this method.

getImageData( ) gives us access to the underlying pixels of an image, and putImageData( ) lets us put pixels back into an image.

We can create blank image data objects with createImageData( ) method. We can pass  the method either the width & height of image data in css pixels, or we can pass the method an existing ImageData object, in which  case the method returns a new blank ImageData object with the same width & height as the object you passed to the method.

Draw Images

drawImage( ) method lets us draw all or part of an image, anywhere inside a canvas, and it lets us scale the image along the way. We can also draw into an offscreen canvas, which lets us do clever things with images, such as panning an image, or fading an image into canvas.




Draw an image into a Canvas

   var canvas = document.getElementById('canvas'), 
   context = canvas.getContext('2d'),  
   image = new Image();
   image.src = './img/wall1.jpg'; image.onload = function(e) {
   context.drawImage(image,0,0); };
  

By using the above code we can create an image. The above code sets the source of the image and after waiting for the image to load, draws the image into the canvas’s upper-left corner. If you draw the image before it’s loaded then according to the canvas specification drawImage( ) will fail.

The drawImage( ) Method

The drawImage method draws an image referred to as the source image, into a canvas, referred to as the destination canvas. It lets us draw every part of the image scaled or unscaled.  The drawImage ( ) method can take three different argument sets :

drawImage( image, dx, dy)
drawImage( image, dx, dy, dw, dh )
drawImage( image, sx, sy, sw, sh, dx, dy, dw, dy ) 

The first argument in all three cases is an image but it can be another canvas or video element. In the first  use of drawImage( ) listed above draws an entire image at a specified location in the destination canvas. 
The second use of drawImage ( ) also draws an entire image at a specified location in the destination canvas but with scaled image to a specific width and height. 
The third use of drawImages ( ) draws all or part of an image to a specific location in the destination canvas which is scaled to a specific width and height.



Scaling Images
 
function drawImage() {
context.clearRect(0, 0, canvas.width, canvas.height);
if (scaleCheckbox.checked) {
context.drawImage(image, 0, 0, canvas.width, canvas.height);
}
else {
context.drawImage(image, 0, 0); }
}
 

With the help of above code by putting a checkbox we can draw a scaled image in the canvas.

Offscreen Canvases

Offscreen canvases are used as temporary holding places for images. As the user manipulates the scale then it copies the offscreen canvas to the onscreen canvas and it also copies the object of the offscreen canvas to the onscreen canvas.
Using an offscreen canvas typically involves four steps :

   1.Create the offscreen canvas element.
   2.Set the offscreen canvas’s width & height.
   3.Draw into the offscreen canvas.
   4.Copy all or the part of the offscreen canvas onscreen.

We can  create a offscreen canvas like this :

         var offscreenCanvas = document.createElement(‘canvas’);

This one line code  creates a new canvas that is not attached  to any DOM element and therefore will not be visible, that’s why the term is offscreen. By default the size of the offscreen canvas will be the default size for canvases that are 300pixel wide and 150 pixel high.

So these all are the different methods related to drawing of images  by which we can draw and can also manipulate the images. All these methods provide us to scale, draw images as well as another canvas into the Canvas by which we can make our stuff much better.
