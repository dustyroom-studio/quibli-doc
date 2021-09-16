---
title: "Known Limitations of Quibli"
permalink: /limitations/
excerpt: "Known Limitations of Quibli"
toc: false
---

In this chapter the known limitations of working with Quibli are described.

#### In _Foliage_ and _Grass_ shaders, there is no support for the shadows when working with additional lights.
During making of the _Foliage_ and _Grass_ shaders, we had to completely revisit Unity's emission behavior for these shaders, in order to flexibly control the color shading. Otherwise, there would be a poor looking shadow rendered over the foliage objects, which there is no control over.

#### Quibli does not include a tool for automatic prefab placement.
Our grass needs to be placed with a mesh-painting tool, like [Polybrush](https://unity.com/features/polybrush){:target="_blank"}, as opposed to being spawned by Unity’s terrain tool.

#### Foliage can not be used with Terrain.
Currently the _Foliage_ and _Grass_ shaders don't work on the 'details' objects painted with Unity Terrain.

#### _Foliage Generator_ doesn't produce the trunks of the trees.
Also, it doesn't create conventional flower plants. It works with included as well as external meshes and processes them so that the generated plants can work as stylized leafy parts of  the foliage. However, using the proper textures and a bit non-literal approach, the floral decorations can be created with the _Foliage Generator_.

#### Foliage 'Whole Object' Billboards always look into camera.
This is not a limitation but rather a quirky side effect of the [billboard approach](../foliage-generator/#billboard-approach) to creating and shading the foliage, which is very worth mentioning. This effect can be seen if a plant was created to be acting as a billboard and is located closely to the camera. Particularly, it is noticeable in a VR headset. The effect is that the plant always turns to be looking into the camera. Originally, billboarding was implemented to improve performance: it allowed to use fewer [particles](../foliage-generator/#generation-parameters) and still get an impression of the full model. This rotating side-effect is more subtle if the model is placed far into the background, where having the full high-poly models are not necessary. On the [Sample Scene with Quibli](../demo-scenes/#sample-scene-with-quibli) we created both billboard (low-poly, rotating) and non-billboard (high-poly, fully 3D) models, but since all the models on that scene are placed closely to the camera, the rotating issue is very noticeable. We are looking for the ways to overcome this problem.