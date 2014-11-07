webgl-2d-screen
===============

A tiny library that can use WebGL instead of canvas 2D, for the simple use case of using a canvas as a screen of pixels. That is, if you are using canvas 2D and just doing putImageData of a full screen, then you can use this. It will use GL if available, which is generally faster, or normal canvas 2D if not.

Based on

https://github.com/jrmuizel/full-scene-rasterizer/blob/master/library-canvas.js

License: MIT

