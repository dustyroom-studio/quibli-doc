---
title: "What Is Quibli? A Brief Overview"
permalink: /
excerpt: "What is Quibli? How it differs from Flat Kit?"
toc: true
---

## Quibli Brief Overview

Quibli is a collection of shaders, effects and scripts whose main task is to help easily create the look of the Japanese animation films. Quibli’s capabilities extend way beyond this, however, and we have included the demo scenes with all the used resources showing that.  

One of the highlight features of Quibli is the [Gradient Editor](stylized-lit-shader#main-shading-parameters) found in the shaders. In a nutshell, you can have up to 8 independent color stops. The combinations of these color stops define the diversity of the material results. Within a single Gradient Editor you can have a smooth gradual blend from a color to another one, then a steep change to another color and so on. The [Kitchenware demo scenes](demo-scenes#kitchenware) display the variety of this. You can have a full rainbow (or any other entire palette). And you can vary the blending of the colors within a single gradient (red to orange is stepped and yellow to green is smooth — whatever you can imagine).  
And, what’s even more important, is that it is a real-time effect, you don’t have to save any textures: you change the color on the ramp and you immediately see it change.  

While working on the materials for the included [Demo scenes](demo-scenes), there were so many interesting things appearing during the parameter tweaking — one move of a color ramp slider completely changed the look of the material. A move of a single _Shading Offset_ parameter of the [Stylized Lit shader](stylized-lit-shader) changed the material to a completely another one, instantly. It was even tough to decide which of these variants looked better. The folders of ‘saved for later’ presets were brimming with widely different materials: ranging from subtly shaded toon surfaces to vibrant unnatural popping-off-screen color palettes. The scenes were painting themselves, and despite the fact that we had to keep only the best results for the demo scenes, so many equally great looking materials were left off. No matter whether you are looking for conventional toon materials, want to add a tiny bit of spice to that look, or are in an experimental mood and are looking to explore uncharted fields — it is all done easily.  

Of course, it is very important to have the fitting and stylistically correct models. Particularly, the nature objects, like trees, bushes etc (more on this you’ll find further down this manual). That’s why another highlight feature of Quibli is its foliage generating capabilities. Here you can find everything for an effortless plant creation as well as shading that supports wind.

In addition to the shaders, and post effects, we included the tools used in making the [Demo scenes](demo-scenes). All the foliage models were made with [Foliage Generator](foliage generator), a flexible tool for creating and modifying anime-looking plants. The stretched wires between the electric poles in the _City_ demo scene, for example, are generated and can be modified in the Unity Editor using the [Curve Renderer](curve-renderer) tool.


## What Is Included in Quibli? (Graph)

{% include mermaid.html %}
<div class="mermaid">
graph TD
A[Quibli] --> B(Shaders)
A --> C(Post Effects)
A --> D(Scripts)
A --> E(Demo Scenes)
B --> G[Stylized Lit Shader]
G --> H[Stylized Foliage Shader]
H --> I[Stylized Grass Shader]
I --> J[Skybox Shader]
J --> K[Cloud2D Shader]
K --> L[Light Beam Shader]
C --> M[Stylized Detail Post Effect]
D --> N[Foliage Generator]
N --> O[Curve Renderer]
E -->|with all models + materials| P[Nature Scene]
P --> Q[City Scene]
Q --> R[Kitchenware Scene]
R --> S[Mugs Scene]
S --> T[Sample Scene with Quibli]
T --> U[Clouds Scene]
</div>




