---
title: "What Is Quibli? A Brief Overview"
permalink: /
excerpt: "What is Quibli? How it differs from Flat Kit?"
layout: single
---

<!--
**<span style="font-size:larger;">[Full documentation online](https://quibli.dustyroom.com)</span>**
{: .notice--info}
-->

<!--
Important!
{: .notice--danger}
-->

## Quibli Brief Overview

Quibli is a collection of shaders, effects and scripts whose main task is to help easily create the look of the Japanese animation films. Quibli’s capabilities extend way beyond this, however, and we have included the demo scenes with all the used resources showing that.

One of the highlight features of Quibli is the [Gradient Editor](stylized-lit-shader/#gradient) found in the shaders. In a nutshell, you can have up to 8 independent colors in a single gradient. The combinations of these color stops define the diversity of the material results. You can have a full rainbow (or any other entire palette). And it is possible to vary the blending steepness of the colors within a single gradient (red to orange is stepped and yellow to green is smooth — whatever you can imagine).

And, what’s even more important, is that it is a real-time effect, you don’t have to save any textures: you change the color on the ramp and you immediately see it change.

While working on the materials for the included [Demo scenes](demo-scenes), there were so many interesting things appearing during the parameter tweaking — one move of a color ramp slider completely changed the look of the material. A move of a single _Shading Offset_ parameter of the [Stylized Lit shader](stylized-lit-shader) changed the material to a completely another one, instantly. It was even tough to decide which of these variants looked better. The folders of ‘saved for later’ presets were brimming with widely different materials: ranging from subtly shaded toon surfaces to vibrant unnatural popping-off-screen color palettes. The scenes were painting themselves, and despite the fact that we had to keep only the best results for the demo scenes, so many equally great looking materials were left off. No matter whether you are looking for conventional toon materials, want to add a tiny bit of spice to that look, or are in an experimental mood and are looking to explore uncharted fields — it is all done easily.

Of course, it is very important to have the stylistically fitting models. Particularly, the nature objects, like trees, bushes etc (more on this you’ll find further down this manual). That’s why another highlight feature of Quibli is its foliage generating capabilities. Here you can find everything for an effortless plant creation as well as shading that supports wind.

In addition to the shaders, and post effects, we included the tools used in making the [Demo scenes](demo-scenes). All the foliage models were made with [Foliage Generator](foliage-generator), a flexible tool for creating and modifying anime-looking plants. The stretched wires between the electric poles in the [City](demo-scenes#city-scene) demo scene, for example, are generated and can be modified in the Unity Editor using the [Curve Renderer](curve-renderer) tool.

Quibli is easy to use and is beginner friendly. However, the foliage and cloud generating tools may have a slightly steep learning curve for complete beginners. 

## Requirements

  * Unity version **2020.3.30f1** or higher; **2021.3.5f1** or higher;
  * Universal Rendering Pipeline (also known as 'URP', previously known as 'LWRP');
  * The Shader Compilation Target Level for mobile devices should be 3.5 (or es 3.0 and WebGL 2.0).

## What Is Included in Quibli?

{% include mermaid.html %}
<div class="mermaid">
graph TD
A[Quibli] --> B(Shaders)
A --> C(Post Effects)
A --> D(Scripts)
A --> E(Demo Scenes)
B --> G[Stylized Lit Shader]
G --> H[Foliage Shader]
H --> I[Grass Shader]
I --> J[Skybox Shader]
J --> K[Cloud3D Shader]
K --> L[Cloud2D Shader]
L --> M[Light Beam Shader]
C --> N[Stylized Detail]
N --> O[Stylized Color Grading]
D --> Q[Foliage Generator]
Q --> R[Grass Generator]
R --> S[Curve Renderer]
E -->|with all models + materials| T[Nature Scene]
T --> U[City Scene]
U --> V[Kitchenware Scene]
V --> W[Plants Scene]
W --> X[Mugs Scene]
X --> Y[Sample Scene with Quibli]
Y --> Z[Clouds Scene]
</div>
