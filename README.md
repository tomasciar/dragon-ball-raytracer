# Dragon Ball Raytracer
A real-time WebGL2 animation of the seven Dragon Balls floating above a grassy landscape, with drifting clouds, distant hills, and a flying Shenron silhouette.

The entire scene is generated procedurally in a GLSL fragment shader. No 3D models, textures, images, or external libraries are used.

## How it works
The renderer draws a fullscreen quad and casts a camera ray for each pixel. The fragment shader checks for intersections with seven spheres and a ground plane, then shades the nearest visible surface.

- **Dragon Balls:** Procedural red stars, orange gradients, specular highlights, and subtle independent bobbing motion.
- **Lighting:** Diffuse shading and hard shadows calculated with secondary rays toward a point light.
- **Environment:** Procedural grass, rolling hills, sky gradients, and drifting clouds.
- **Shenron:** A small animated silhouette drawn directly in the shader.

JavaScript handles shader compilation, canvas sizing, and animation timing. All visual rendering happens on the GPU.

## Running locally
Open `index.html` in a browser with WebGL2 support. No installation or build step is required.
**Built with:** JavaScript, WebGL2, and GLSL ES 3.00.
