---
title: "Skybox Shader"
permalink: /skybox-shader/
excerpt: "Quibli Skybox Shader"
toc: true
---

### Skybox Shader Brief Overview
The _Gradient Skybox_ shader is a modified version of the Flat Kit’s [Gradient Skybox](https://flatkit.dustyroom.com/#34-gradient-skybox-shader) shader.
Instead of two colors that you pick in two color choosers to form a gradient in the skybox, the Quibli version has a single Gradient editor with a continuous color ramp. It means that you can have up to 8 independent color stops in the skybox with varying transition smoothness.


![Quibli Skybox Shader Interface](/quibli-doc/assets/images/manual_images/quibli_skybox_shader_interface.jpg)
{:.image-caption}
*Pic. Quibli Skybox Shader Interface*

![Quibli Skybox Shader Interface](/quibli-doc/assets/images/manual_images/quibli_skybox_shader_interface.jpg)
*Pic. Quibli Skybox Shader Interface*


### Beginning to Work with the Skybox Shader
* Create a material
* In the **Inspector** panel, in the **Shader** drop down menu choose **Quibli** ▶︎ **Skybox**.

Now you can apply this material as your skybox: either drag it onto any empty spot of your scene in Game View, or go to **Lighting** panel ▶︎ **Environment** tab ▶︎ select this material in the **Skybox material** field.


### Parameters of the Skybox Shader
**Gradient** Clicking on the colored rectangle opens a _Gradient Editor_, where you can make a gradient to be displayed on the skybox. For more info about _Gradient Editor_, please, refer to the _Gradient_ parameter description of the [Stylized Lit Shader](../stylized-lit-shader) chapter in this manual.  

**Intensity** This parameter defines how strong (read: bright) the skybox is.  

**Exponent** A bias towards either of the ends of the _Gradient_.  

**Direction X Angle** Rotation in world-space on the X axis.  


**Direction Y Angle** Rotation in world-space on the Y axis.
