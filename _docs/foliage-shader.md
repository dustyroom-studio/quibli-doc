---
title: "Foliage Shader"
permalink: /foliage-shader/
excerpt: "Quibli Foliage Shader"
toc: true
---


## Foliage Shader Brief Overview

The _Foliage_ shader is a specialized shader to be used with the models to give them a foliage look. We're talking not only about the ones made using the [Foliage Generator](../foliage-generator) tool, but also other models, including primitives, letters, monkeys, everything you usually want to cover with leaves.  


![Quibli Foliage Shader Interface](/quibli-doc/assets/images/manual_images/quibli_foliage_shader_interface.png)  
*Quibli Foliage Shader Interface*


## Beginning to Work with the Foliage Shader

* Create a material
* In the **Inspector** panel, in the **Shader** drop down menu choose **Quibli** ▶︎ **Foliage**.  
Now you can apply this material to a mesh.


## Parameters of the Foliage Shader

### Coloring Parameter (Gradient)

**Shading Gradient**

The same Gradient Editor is also available for the following shaders: [Stylized Lit](../stylized-lit-shader), [Foliage](../foliage-shader), [Skybox](../skybox-shader), [Cloud2D](../cloud2d-shader). You can find the detailed explanation of the _Gradient_ in the ['Gradient' sub-chapter of 'Stylized Lit shader' chapter](../stylized-lit-shader/#gradient)  
{: .notice--info}

### Texturing Parameters

**Shape Texture**  

**Clip Threshold**   

**Fill Texture**  

**Fill Impact**  

**Fill Scale**  

**Billboard Scale**  

**Offset Along Normal**  

### Additional Coloring Parameters

**Smoothness**  

**Fresnel Power**  

**Fresnel Color**  

### Wind Parameters

**Wind**  

**Wind Direction**  

**Wind Speed** 

**Wind Turbulence** 

**Wind Strength** 

### Global Billboard Parameter

**Billboard Rotation**  
_Billboard Rotation_ parameter has three options:  
  * Nothing
  * Each Face
  * Whole Object

![Foliage Shader Billboard Rotation parameter options](/quibli-doc/assets/images/manual_images/quibli_foliage_shader_billboard_rotation_options.png)  
*Foliage Shader Billboard Rotation parameter options*
