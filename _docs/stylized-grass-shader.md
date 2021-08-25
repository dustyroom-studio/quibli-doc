---
title: "Stylized Grass Shader"
permalink: /stylized-grass-shader/
excerpt: "Quibli Stylized Grass Shader"
toc: true
---

## Stylized Grass Shader Brief Overview

The _Stylized Grass_ shader is a specialized shader to be used with the grass foliage. 

![Quibli Stylized Grass Shader Interface](/quibli-doc/assets/images/manual_images/quibli_stylized_grass_shader_interface.png)  
*Quibli Stylized Grass Shader Interface*


## Beginning to Work with the Stylized Grass Shader

* Create a material
* In the **Inspector** panel, in the **Shader** drop down menu choose **Quibli** ▶︎ **Stylized Grass**.  
Now you can apply this material to ... .

## Parameters of the Stylized Grass Shader

### Texture and Color Parameters

**BaseMap** The 2D sprite to be used as a grass blade.  

**Top Color** The color of the upper part of the grass blade.  

**Bottom Color** The color of the lower part of the grass blade.  

**Emission** The color of glowing. The _Emission_ parameter in the bottom of the shader interface needs to be turned on.  

### Wind Motion Parameters

**Wind Speed**

**Wind Intensity**

**Wind Frequency**

**Wind Direction**

**Wind Entropy**

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