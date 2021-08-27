---
title: "Light Beam Shader"
permalink: /light-beam-shader/
excerpt: "Quibli Light Beam Shader"
toc: true
---

## Light Beam Shader Brief Overview

The _Light Beam_ shader can be used for the light rays as seen in the anime movies, as well as for other creative cases. For example, it can play the role of a foggy halo in the background, or a light sword.  
The _Light Beam_ shader has an ability to decay with distance — once the needed parameters are set up, the halo, for instance, will be visible from distance but will gradually become less visible (more transparent) as the camera approaches it.  
The _Light Beam_ is in HDR colors, meaning that it can glow if the scene has some kind of a bloom in it.  

![Quibli Light Beam Shader Interface](/quibli-doc/assets/images/manual_images/quibli_light_beam_shader_interface.png)  
*Quibli Light Beam Shader Interface*

## Beginning to Work with Light Beam Shader

* Create a material
* In the **Inspector** panel, in the **Shader** drop down menu choose **Quibli** ▶︎ **Light Beam**.  
Now you can apply this material to a 3D game object on your Scene or in the Hierarchy panel. 

## Parameters of Light Beam Shader

**Color** The parameter for selecting the color of the shader. As the _Light Beam_ is in additive blending mode, you cannot make dark colors with it.

**TIP.** _Color_ alpha controls opacity.
{: .notice--info}

**Depth Fade Distance** Controls the visibility of objects behind the light beam. If 0, the _Light Beam_ occludes the objects behind it. If the value is high, the objects behind the _Light Beam_ are fully visible.  

**TIP.** _Depth Fade Distance_ with higher values is useful for making a pseudo-fog effect.
{: .notice--info}

**Camera Distance Fade Far** Sets the far point in the scene where the shader fades into full transparency.  If the camera is farther than this value, the beam is 100% visible (alpha is ‘1’).  

**Camera Distance Fade Close** Sets the close point in the scene where the shader fades in from transparency. If the camera is closer than this value, the beam disappears.  

**UV Fade X** Sets the intensity of the transparency-to-color gradient on the X axis.  

**UV Fade Y** Sets the intensity of the transparency-to-color gradient on the Y axis.  

**Enable GPU Instancing**  Enabling turns on the manipulation of the main parameters in the code.  

**TIP.** Most of the parameters of the _Light Beam_ shader work similarly to the according parameters in the analogous _LightPlane_ shader in **Flat Kit**. If you didn’t find some specific info about these parameters in this manual, you might want to have a look into the [LightPlane chapter of the Flat Kit manual](https://flatkit.dustyroom.com/#37-lightplane-shader){:target="_blank"}.
{: .notice--info}

