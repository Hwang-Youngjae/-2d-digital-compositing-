What is Digital Compositing?
========================
Digital compositing is the process of digitally assembling multiple images to make a final image, typically for print, motion pictures or screen display. It is the digital analogue of optical film compositing.

Mathematics
-----------
The basic operation used in digital compositing is known as 'alpha blending', where an opacity value, 'α', is used to control the proportions of two input pixel values that end up a single output pixel.

As a simple example, suppose two images of the same size are available and they are to be composited. The input images are referred to as the foreground image and the background image. Each image consists of the same number of pixels. Compositing is performed by mathematically combining information from the corresponding pixels from the two input images and recording the result in a third image, which is called the composited image.


![An-overview-of-the-video-compositing-process](https://user-images.githubusercontent.com/71237760/93716938-7ccdd680-fbad-11ea-9b13-9cb3e7d90d88.png)

Matte Painting
----------------
![unnamed](https://user-images.githubusercontent.com/71237760/93717006-f1a11080-fbad-11ea-89af-0b88f1da668c.jpg)

Chroma Key
-----------

![greenscreen_studio2](https://user-images.githubusercontent.com/71237760/93717063-447ac800-fbae-11ea-85aa-33bf9213509a.jpg)



What is Alpha and Color(Digital Color)?
====================================
1. What is Alpha?
-------------
The alpha channel controls the transparency or opacity of a color. Its value can be represented as a real value, a percentage, or an integer: full transparency is 0.0, 0% or 0, whereas full opacity is 1.0, 100% or 255, respectively.

When a color (source) is blended with another color (background), e.g., when an image is overlaid onto another image, the alpha value of the source color is used to determine the resulting color. If the alpha value is opaque, the source color overwrites the destination color; if transparent, the source color is invisible, allowing the background color to show through. If the value is in between, the resulting color has a varying degree of transparency/opacity, which creates a translucent effect.

The alpha channel is used primarily in alpha blending and alpha compositing.

![Figure2](https://user-images.githubusercontent.com/71237760/93716869-1052d780-fbad-11ea-930e-6e0326addb04.jpg)


![RGBA_comp](https://user-images.githubusercontent.com/71237760/93716906-4d1ece80-fbad-11ea-8d89-f7ef9df2a495.png)

