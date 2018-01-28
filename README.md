# glslify-big-triangle-boilerplate

This is an opinionated starter repo for writing fragment shader code with the aid of the glslify ecosystem. Want to get started right away in your browser? consider [glslb.in](http://glslb.in/)

`npm run start` to start the devserver.

Annotated dependency list:

- `glsl-hsv2rgb`: An example of a glslify library. Does some fancy math to convert between color spaces, and does it with branchless logic.
- `regl`:  Declarative wrapper over WebGL state machine. A regl command is analogous to a react component. We have a single command, `drawTriangle`.
- `glslify`: Enables importing libraries from node_modules, aka `#pragma glslify: hsv2rgb = require('glsl-hsv2rgb')`. Makes GLSL fun.
- `webpack`:  Handles packing index.js and it's dependencies into bundle.js, suitable for the browser.
- `webpack-dev-server`: Runs webpack in a mode that auto-reloads in your browser.
- `glslify-loader`: Runs glslify for webpack and resolves `.glsl` files to javascript strings.
- `raw-loader`: Sidekick for `glslify-loader`. Resolves and loads raw text files for webpack, in this case `fragment.glsl`
