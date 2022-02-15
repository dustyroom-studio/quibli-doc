---
title: "Known Limitations of Quibli"
permalink: /limitations/
excerpt: "Known Limitations of Quibli"
toc: false
---

In this chapter the known limitations of working with Quibli are described.

#### VR Single Pass mode is not working.
Currently VR works in multi-pass mode only. We are working on it, it is our prioritised feature to implement.

#### In _Foliage_ and _Grass_ shaders, there is no support for the shadows when working with additional lights.
During making of the _Foliage_ and _Grass_ shaders, we had to completely revisit Unity's emission behavior for these shaders, in order to flexibly control the color shading. Otherwise, there would have been a poor looking shadow rendered over the foliage objects, which there would be no control over.

#### Quibli does not include a tool for automatic prefab placement.
Our grass needs to be placed with a mesh-painting tool, like [Polybrush](https://unity.com/features/polybrush){:target="_blank"}, as opposed to being spawned by Unity’s terrain tool.

#### Foliage can not be used with Terrain.
Currently the _Foliage_ and _Grass_ shaders don't work on the 'details' objects painted with Unity Terrain, which is a way of an automatic prefab/texture placement.

#### _Foliage Generator_ doesn't produce the trunks of the trees.
Also, it doesn't create conventional flower plants. It works with included as well as external meshes and processes them so that the generated plants can work as stylized leafy parts of  the foliage. However, using the proper textures and a bit non-literal approach, the floral decorations can be created with the _Foliage Generator_.

#### [FIXED in v. 1.0.1] ~~Foliage Billboards rotate and tilt with camera.~~
~~This is not a limitation but rather a quirky side effect of the [billboard approach](../foliage-generator/#billboard-approach) to creating and shading the foliage, which is very worth mentioning. This effect can be seen if a plant was created to be acting as a billboard and is located closely to the camera. Particularly, it is noticeable in a VR headset. The effect is that the plant always turns itself to be looking into the camera.~~  
Please, use the _Billboard Face Camera Position_ parameter in Foliage Shader's [Global Billboard Parameters](foliage-shader/#global-billboard-parameters).

#### Shaders that are built in the Shader Graph.
This is not a limitation but rather a technical detail worth mentioning. The following shaders are built in the Shader Graph: [Grass](../grass-shader), [Cloud3D](../cloud3d-shader), [Cloud2D](../cloud2d-shader), [Foliage](../foliage-shader). The [Stylized Lit](../stylized-lit-shader), [Skybox](../skybox-shader) and [Light Beam](../light-beam-shader) shaders are made as the hlsl script files.
