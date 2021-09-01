---
title: "Grass Shader"
permalink: /grass-shader/
excerpt: "Quibli Grass Shader"
---

## Grass Shader Brief Overview

The _Grass_ shader is a specialized shader to be used with the grass foliage. 

![Quibli Grass Shader Interface](/quibli-doc/assets/images/manual_images/quibli_grass_shader_interface.png)  
*Quibli Grass Shader Interface*


## Beginning to Work with the Grass Shader

* Create a material
* In the **Inspector** panel, in the **Shader** drop down menu choose **Quibli** ▶︎ **Grass**.  
Now you can apply this material to an object on the scene or to a prefab (for example, a grass patch). 

## Parameters of the Grass Shader

### Texture and Color Parameters

**BaseMap** The 2D sprite to be used as a grass blade.  

**Top Color** The color of the upper part of the grass blade.  

**Bottom Color** The color of the lower part of the grass blade.  

**Emission** The color of glowing. The _Emission_ parameter in the bottom of the shader interface needs to be turned on.  

### Wind Motion Parameters

**Wind Speed** How fast the material displaces the object.  

**Wind Intensity** The amount of deviation of the object from its initial position. In other words, it is how strong the movement is.  

**Wind Frequency** The scale of the sway intervals. Higher values result in denser, more fine-grained noise.  

**Wind Direction** The direction of the motion.  

**Wind Entropy** Sets the amount of noise that introduces nonlinearities to the object’s motion.  

### Wind Gusts Parameters

**Gust Intensity**

**Gust Frequency**

**Gust Speed**

**Gust Color**

### Grass Patches Parameters

**Patches Color**

**Patches Threshold**

**Patches Scale**

**Patches Blurriness**

**Patches Offset**

### Rendering Parameters

**Enable GPU Instancing** Enabling turns on the manipulation of the main parameters in the code.  

**Emission**
