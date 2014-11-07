webgl-2d-screen
===============

A tiny library that can use WebGL instead of canvas 2D, for the simple use case of using a canvas as a write-only screen of pixels. That is, if you are using canvas 2D and just doing putImageData of a full screen, then you can use this. It will use GL if available, which is generally faster, or normal canvas 2D if not.

Based on

https://github.com/jrmuizel/full-scene-rasterizer/blob/master/library-canvas.js

License: MIT

Usage
-----

Just run Web2DScreen on your canvas,

        var wrappedCanvas = WebGL2DScreen(canvas);

and use the wrapped canvas normally. For example, in an Emscripten project you might have something like

        var canvas = document.getElementById('canvas');

in your HTML (this is where it finds the canvas HTML element, and then points to it from where Emscripten-generated code will see it), then you would just add

        canvas = WebGL2DScreen(canvas);

right after that line.

