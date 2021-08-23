---
title: "What Is Quibli? A Brief Overview"
permalink: /
excerpt: "What is Quibli? How it differs from Flat Kit?"
toc: true
---

Quibli is a collection of shaders, effects and scripts whose first task is to help easily create the look of the japanese animation films. Quibli’s capabilities extend way beyond this, however, and we have included the demo scenes showing that.  

One of the highlight features of a Quibli shader is the Gradient Editor. In a nutshell, you can have up to 8 independent color stops. The combinations of these color stops define the diversity of the material results. Within a single Gradient Editor you can have a smooth gradual blend from a color to another one, then a steep change to another color and so on. The _Kitchenware_ demo scenes display the variety of this. You can have a full rainbow (or any other entire palette). And you can vary the blending of the colors within a single gradient (red to orange is stepped and yellow to green is smooth — whatever you can imagine).  
And, what’s even more important is that it is an instant effect, you don’t have to save any textures: you change the color on the ramp and you immediately see it change.  

While working on the materials for the demo scenes, there were so many interesting things appearing during the parameter tweaking — one move of a color ramp slider completely changed the look of the material. A move of _Shading Offset_ parameter changed the material to a completely another one, instantly. It was even tough to decide which of these variants looked better. The folders of ‘saved for later’ presets were brimming with widely different materials: ranging from subtly shaded toon-ish surface materials to vibrant unnatural popping-off-screen bunches of colors. The scenes were shading themselves, and despite the fact that we had to keep only the best results for the demo scenes, so many equally great looking materials were left off. No matter whether you are looking for conventional toon materials, want to add a tiny bit of spice to that look, or are in an experimental mood and are looking to explore uncharted fields — it is done easily.  

Of course, it is very important to have the fitting and stylistically correct models. Particularly, the nature objects, like trees, bushes etc (more on this you’ll find further down this manual). That’s why another highlight feature of Quibli is its foliage generating capabilities. Here you can find everything for an effortless plant creation as well as shading that supports wind.


## What Is Included in Quibli?

{% include mermaid.html %}
<div class="mermaid">
graph TD
A[Quibli] --> B(Shaders)
A --> C(Post Effects)
A --> D(Additional Tools)
A --> E(Demo Scenes)
B --> G[Stylized Lit Shader]
G --> H[Cloud2D Shader]
H --> I[Light Beam Shader]
I --> J[Skybox Shader]
J --> K[Foliage Shader]
K --> L[Stylized Grass Shader]
C --> M[Stylized Detail Post Effect]
D --> N[Wire Renderer]
N --> O[Foliage Generator]
E -->|with all models + materials| P[Nature Scene]
P --> Q[City Scene]
Q --> R[Kitchenware Scene]
R --> S[Mugs Scene]
S --> T[Unity Default Sample Scene Quiblified Scene]
T --> U[Clouds Scene]
</div>

## Quibli or Flat Kit?

We describe [Flat Kit](http://u3d.as/1uVy) as a one-stop choice for getting bread-and-butter toon look and a great tool for experimentation. With Flat Kit you can take a scarily boring plain scene and turn it into a pro-looking polished material in the matter of half an hour. Quibli takes this idea to the next level.  

The main point of **Flat Kit** is the fact that it is **a set of general creative easy-to-use tools**: a Stylized Surface family of shaders, the Water shader, the Outline and Fog Renderer Features (real-time post effects), additional scripts.  

The main point of **Quibli** is **flexibility in coloring of the shader** and **foliage creation** designed for _that_ animation film look. Although there is an overlap in shading look and Flat Kit’s _Stylized Surface_ shaders have some of the similar parameters as Quibli’s _Stylized Lit_ shader, namely Rim, Glare and Height Gradient, these shaders are very different in workflow, possibilities / limitations and URP properties. Some of the results from Flat Kit’s Stylized Surface shader can be reproduced with Quibli and vice versa. But there is no such an easy-to-use Quibli Gradient Editor in Flat Kit, which makes it effortless and fun to create stunning visuals. In Flat Kit there are a ‘Step’ and a ‘Curve’ coloring modes in Stylized Surface shaders, but they require saving an internal texture. More info about ‘Step’ and ‘Curve’ modes can be found [here](https://flatkit.dustyroom.com/#311-the-main-parameters-of-the-shader).  

Both Quibli and Flat Kit are the type of tools where a small parameter change can have a drastic change of the look of the scene. This is a key sign of a good creation tool, when you perhaps are searching for the stylistic direction.  

If you use both Quibli together with Flat Kit, you have the best of both worlds. Create perfect eye-candy materials with Quibli, apply Outlines and Fog from Flat Kit.  


### Quibli and Flat Kit Comparison Chart

| Asset | **Quibli** | **Flat Kit**
| --- | --- | --- |
| In short | Everything you need to achieve a stylized look of traditional japanese animation | Everything you need to achieve any variation of minimal or toon shading |
| Shaders included | Stylized Lit, Cloud2D, Light Beam, Gradient Skybox, Stylized Grass | Stylized Surface, Stylized Surface with Outline, Terrain, Water, Light Beam, Gradient Skybox |
| Mobile friendliness | Yes | Yes |
| Outlines (shader-based) | No | Yes |
| Outlines (post effect) | No | Yes, [Outline Image Effect](https://flatkit.dustyroom.com/#42-outline-image-effect) |
| Fog (post effect) | No | Yes, [Fog Image Effect](https://flatkit.dustyroom.com/#41-fog-image-effect) |
| Stylized Detail (post effect) | Yes | No |
| Independent per-step color gradient | Yes | No |
| Number of possible independent shade colors per material | **8** (in any desirable degree of smoothness) | **3** (Using _Base color_ and 2 _additional cel layers_) |
| Real-time Gradient editor | Yes | No (‘Steps’ and ‘Curve’ modes require saving color info into offline internal textures) |
| Wind | Yes | No |
| Skybox shader | Yes, with **up to 8 color multi-stop gradient** color editor | Yes, with **2 colors** interpolation |
| Light Plane shader | Yes, called _Light Beam_, a more advanced version of a Light Plane shader | Yes |
| SRP batching | Yes | No |
| Pipelines support | URP | URP, Built-In RP LTS |
| Textures support (maps) | Albedo, Normal, Detail | Albedo, Normal, Emission |
| Additional tools | Wire Renderer, Foliage Generator | [UV Scroller](https://flatkit.dustyroom.com/#51-uv-scroller), CameraMouse Orbit, [Linear Motion](https://flatkit.dustyroom.com/#52-linear-motion), [Buoyancy](https://flatkit.dustyroom.com/#53-buoyancy) |






