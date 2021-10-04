---
title: "Quibli and Flat Kit"
permalink: /quibli-flat-kit/
excerpt: "Quibli and Flat Kit"
---

## Quibli and Flat Kit

We describe [Flat Kit](http://u3d.as/1uVy){:target="_blank"} as a one-stop choice for getting bread-and-butter toon look and a great tool for experimentation. With Flat Kit you can take a scarily boring plain scene and turn it into a pro-looking polished material in the matter of half an hour. Quibli takes this idea to the next level.

The main point of **Flat Kit** is the fact that it is **a set of general creative easy-to-use tools**: a Stylized Surface family of shaders, the Water shader, the Outline and Fog Renderer Features (real-time post effects), additional scripts.

The main points of **Quibli** are **flexibility in coloring of the shaders [Stylized Lit](../stylized-lit-shader), [Foliage](../foliage-shader), [Skybox](../skybox-shader), [Cloud2D](../cloud2d-shader)** and **foliage and cloud creation using [Foliage Generator](../foliage-generator)** designed for _that_ animation film look. Although there is an overlap in shading look and Flat Kit’s _Stylized Surface_ shaders have some of the similar parameters as Quibli’s _Stylized Lit_ shader, namely Rim, Glare and Height Gradient, these shaders are different in workflow, possibilities / limitations and URP properties.

Some of the results from Flat Kit’s Stylized Surface shader can be reproduced with Quibli and vice versa. But there is no such an easy-to-use Quibli Gradient Editor in Flat Kit, which makes it effortless and fun to create stunning visuals. In Flat Kit there are a ‘Step’ and a ‘Curve’ coloring modes in Stylized Surface shaders, but they require saving an internal texture. More info about ‘Step’ and ‘Curve’ modes can be found [in Flat Kit documentation](https://flatkit.dustyroom.com/#311-the-main-parameters-of-the-shader){:target="_blank"}. Also, if you are going to shade the plants, the Quibli [Foliage shader](../foliage-shader) is the one to choose.

Both Quibli and Flat Kit are the type of tools where a small parameter change can have a drastic change of the look of the scene. This is a key sign of a good creation tool, when you perhaps are searching for the stylistic direction.

If you use both Quibli together with Flat Kit, you have the best of both worlds. Create perfect eye-candy materials with Quibli, apply Outlines and Fog from Flat Kit.

## Quibli and Flat Kit Comparison Chart

| Asset | **Quibli** | **Flat Kit**
| --- | --- | --- |
| In short | Everything you need to achieve a stylized look of traditional Japanese animation | Everything you need to achieve any variation of minimal or toon shading |
| Shaders included | [Stylized Lit](../stylized-lit-shader), [Foliage](../foliage-shader), [Grass](../grass-shader), [Skybox](../skybox-shader), [Cloud3D](../cloud3d-shader), [Cloud2D](../cloud2d-shader), [Light Beam](../light-beam-shader) | [Stylized Surface](https://flatkit.dustyroom.com/#31-stylized-surface-shader){:target="_blank"}, [Terrain](https://flatkit.dustyroom.com/#36-terrain-shader){:target="_blank"}, [Water](https://flatkit.dustyroom.com/#35-water-shader){:target="_blank"}, [LightPlane](https://flatkit.dustyroom.com/#37-lightplane-shader){:target="_blank"}, [Gradient Skybox](https://flatkit.dustyroom.com/#34-gradient-skybox-shader){:target="_blank"} |
| Post Effects included | [Stylized Detail](../stylized-detail-post-effect), [Stylized Color Grading](../stylized-color-grading-post-effect) | [Outline Image Effect](https://flatkit.dustyroom.com/#42-outline-image-effect){:target="_blank"}, [Fog Image Effect](https://flatkit.dustyroom.com/#41-fog-image-effect){:target="_blank"} |
| Anime foliage model creation in Unity Editor | **Yes**, with [Foliage Generator](../foliage-generator) | No |
| Anime cloud creation in Unity Editor | **Yes**, **3D clouds**: with [Foliage Generator](../foliage-generator) + [Cloud3D shader](../cloud3d-shader); **2D clouds**: with [Cloud2D shader](../cloud2d-shader) | No |
| Scripts | [Foliage Generator](../foliage-generator), [Curve Renderer](../curve-renderer) | [UV Scroller](https://flatkit.dustyroom.com/#51-uv-scroller){:target="_blank"}, Orbit Motion, [Linear Motion](https://flatkit.dustyroom.com/#52-linear-motion){:target="_blank"}, [Buoyancy](https://flatkit.dustyroom.com/#53-buoyancy){:target="_blank"} |
| Mobile friendliness | The object shaders target 3.5 (or es 3.0 and WebGL 2.0) | The object shaders target 3.5 (or es 3.0 and WebGL 2.0) |
| Basic outlines (shader-based) | **Yes**, [Stylized Lit shader](../stylized-lit-shader) | **Yes**, [Stylized Surface shader](https://flatkit.dustyroom.com/#31-stylized-surface-shader){:target="_blank"} |
| Advanced outlines (post effect) | No | **Yes**, [Outline Image Effect](https://flatkit.dustyroom.com/#42-outline-image-effect){:target="_blank"} |
| Real-time Gradient editor | **Yes**, in the following shaders: [Stylized Lit](../stylized-lit-shader), [Foliage](../foliage-shader), [Skybox](../skybox-shader), [Cloud2D](../cloud2d-shader)| No (‘Steps’ and ‘Curve’ modes require saving color info into offline internal textures) |
| Independent per-step color gradient | **Yes** | No |
| Number of possible independent shade colors per material | **8** (using a single Gradient Editor) | **3** (_Base color_ and 2 _additional cel layers_) parameters |
| Wind | **Yes**, in [Grass shader](../grass-shader) and [Foliage shader](../foliage-shader) | No |
| Skybox shader | **Yes**, with **up to 8 color multi-stop gradient** color editor | **Yes**, with **2 colors** interpolation |
| Textures support (maps) in main shaders | Albedo, Normal, Detail | Albedo, Normal, Emission |
| Shaders built in Shader Graph | [Grass](../grass-shader), [Cloud3D](../cloud3d-shader), [Cloud2D](../cloud2d-shader), [Foliage](../foliage-shader) | - |
| Pipelines support | URP | URP, Built-In RP LTS |

