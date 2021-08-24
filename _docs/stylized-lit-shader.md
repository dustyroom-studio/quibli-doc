---
title: "Stylized Lit Shader"
permalink: /stylized-lit-shader/
excerpt: "Quibli Stylized Lit Shader"
toc: true
---

## Stylized Lit Shader Brief Overview
_Stylized Lit_ shader is a main lit shader to be used in the majority of situations. It is a stylized shader, whose output ranges between a strict one-color flat surface to a cartoon style look, to a vivid acid-color experimental mess, with lots of the sweet spots in between.

## Beginning to work with the Stylized Lit Shader
* Create a material
* In the **Inspector** panel, in the **Shader** drop down menu choose **Quibli** ▶︎ **Stylized Lit**.  
Now you can apply this material to a 3D game object on your Scene or in the Hierarchy panel.  

## Parameters of the Stylized Lit Shader
### Main Shading Parameters
**Gradient** Clicking on an icon of the _Gradient_ opens the _Gradient Editor_ where you can freely add up to eight individual independent color _breakpoints_ (color stops) and move them across the ramp. The layout of the colors on the _breakpoints_ corresponds to the layout of the colors on the scene object the material is applied to. When you move the _breakpoint_ or change the color values in _Gradient Editor_, the shading changes on the affected object(s) simultaneously, **in real time**. It is extremely useful for fine-tuning the color positions on the object.  

**TIP.** Whenever you make up an interesting gradient in the Gradient Editor, you can save it by pressing the ‘New’ button in the ramp presets section of the Gradient Editor. This adds an icon of the gradient to the collection, which is really useful if you want to quickly preview different possible gradients.  
![Using presets in the Gradient Editor](/quibli-doc/assets/images/manual_images/gradient_editor_ramps_presets.jpg)  
*Using presets in the Gradient Editor*
{: .notice--info}

**TIP.** There are ‘smooth’ and ‘fixed’ color gradations in the Gradient editor. You can have a sharp transition from one color to another by selecting a _Fixed_ mode (using 1 color stop), or _Smooth_ mode (using 2 tightly located color stops). You can have a smooth color transition only if you use the _Smooth_ mode.  
{: .notice--info}

**Shading Offset** _Shading Offset_ moves the gradient over the model. It’s a convenience parameter, because this effect can be also made by moving all the stop points in the _Gradient Editor_.  

**Enable Specular** _Specular_ adds a glare to the object. It can be used for adding a small sharp ‘metallic’ specular, a matte diffused one or anything in between. Smaller values make the glare sharper, larger values smoothen the glare. Pressing _Enable Specular_ ‘on’ enables the set of parameters to control the _Specular_. _Specular_ is an HDR effect.  

**Enable Rim** Clicking this tick box turns Rim on or off and opens a set of _Rim_ parameters.  
In some cases it can be used as a contouring pseudo-outline effect, it can accentuate the edges of the models on the scene. _Rim_ depends on the main light’s rotation and the normals of the shaded model.
_Rim_ is an HDR effect. If your scene has a bloom effect enabled, _Rim_ can glow, which you can see in many anime movies.    

Please, note that _Rim_ is not a substitution for the proper outline effect, like the advanced [Outline Image Effect in Flat Kit](https://flatkit.dustyroom.com/#42-outline-image-effect)
{: .notice--warning}

**Rim Color** Sets the color of the Rim. This parameter is in HDR.  

**Light Align** Moves the Rim on the model toward the main light (usually it is a Directional Light). This can be helpful to add stylization on larger _Rim_ values.

GIF HERE!!!!!

**Rim Size** How much of the model the Rim covers.  

**Rim Edge Smoothness** How smoothly the Rim fades out into the base shading. Smaller values can be used as a sharp contouring effect. Larger values combined with large **Rim Size** values can result in a soft inner glow, which can add some nonlinearities to the material look.  

**Enable Height Gradient** Ticking this box turns _Height Gradient_ on and opens the parameters for its adjustment. _Height Gradient_ is a world-space ‘color-to-transparency fade-out’ gradient overlay placed over the material. _Height Gradient_ is an HDR effect.  

**NOTE.** _Height Gradient is a world-space parameter, which means that if two objects share the same material with the _Height Gradient_ ‘on’, they share common coordinates of the _Height Gradient_, unlike, for example, the main albedo _Gradient_, whose coordinates are local per object. That’s why if you put these two objects some distance apart, they can look different. To make these objects look similar you need to create a separate material for each one.  
{: .notice--warning}

**TIP.** In a _City_ Demo scene the _Height Gradient_ is sometimes used as a subtle pseudo ambient occlusion, particularly on the electric poles and houses, which otherwise would have looked kind of detached from the pavement.  
{: .notice--info}

**TIP.** If your scene has some kind of a bloom effect, raising the intensity of the HDR of _Specular_, _Rim_, _Height Gradient_ parameters create a glowing effect. It can contribute to the anime look greatly.  
{: .notice--info}

Once you enable _Height Gradient_, the following parameters will appear.  

**Gradient Color** This color chooser picks the source color of the gradient. The destination color is going to be the same one but transparent.  

**Center X**  The source point on the horizontal axis, from which the _Height Gradient_ is spread.

**Center Y**  The source point on the vertical axis, from which the _Height Gradient_ is spread.  

**Size** How spread the _Height Gradient_ is.  

**Gradient Angle** Rotates the _Height Gradient_ around the **Center X** and **Center Y** values in world-space.  

**Enable Vertex Colors** If enabled, the final shading of the object is multiplied by the mesh’s vertex color values. It is a debug parameter, usually this is not used for changing the look.

### Texture Mapping Parameters
**Texture Maps**
_Texture Maps_ is a collapsible/expandable group of parameters that control the albedo, bump (normal) and detail maps. To use these parameters, please, make sure the model is UV-unwrapped.

**Albedo** The input for a diffuse texture. Select the texture by clicking on the _Select_ texture slot.  
_Tiling_ shrinks and repeats the texture by _X_ and _Y_ axis. Values less than 1 stretch the texture, values bigger than 1 squeeze the texture.  
_Offset_ moves the texture over the UV map along _X_ and _Y_ axis.  

**Detail Map** The input for another kind of diffuse texture. This one has two additional blending modes, which is useful for adding some kind of details into the material.  
_Tiling_ and _Offset_ parameters are the same as in _Albedo_, please look there for the description.  

**TIP.** As this texture input is independent from the _Albedo_ map, you can place a copy of the texture you are using in _Albedo_ map slot, set _Blending Mode_ to _Add_ and by raising the _Detail Impact_ you will have a brighter and more contrast material. We’ve done it in the included  _Unity Default Sample Scene_ — the _Ellen_ character has an increased brightness and vividness thanks to this trick.
{: .notice--info}

**TIP.** If you don’t use any detail textures, select any color in _Detail Color_ chooser, pick an appropriate _Blending Mode_, then by adjusting the _Detail Impact_ slider you can change the overall tint of the material by moving a single control.
{: .notice--info}

**Bump Map** The input for normal maps.  
_Tiling_ and _Offset_ parameters are the same as in _Albedo_, please look there for the description. 

### Lighting Parameters
**Lighting**
_Lighting_ is a collapsible/expandable group of parameters that manages the behavior of some of the important light and shadow controls.  

**Light Color Impact** This parameter defines how much of an influence the main light’s color has onto the material. Having this parameter allows you to add a night/day/morning/sunset feel to the scene. By automating the light’s color it is possible to achieve the day cycle effect.

**Override Shadows** Once enabled, a few shadow-related parameters appear.  

**Shadow Attenuation Remap** This range slider is a multi-tool, which can control the tightness, intensity and the scale of the cast shadow. Drag the left and right brackets of the range slider to tighten up or loosen down the shadow edges, move the slider by clicking and dragging its center in order to adjust the intensity. To become familiar with what this parameter does, please, experiment with it a bit.  

**Shadow Color** This control picks up the color of the cast shadow.  
If _Shadow Color_’s Alpha is set to 0 in the color chooser, you’ll get Unity’s native shadows. In other words, Alpha influences the Shadow Color’s impact.  


**Override Lightmaps**  


**Baked Light Lookup**  


**Override Light Direction** This is a particularly useful parameter. By enabling it, the material skips the light rotation information from the main light (usually Directional Light) and lets you control the lighting/shading positions manually and independently per material. In other words, if you want to rotate the shadow, specular, rim etc separately and specifically for any given model, you can do it using this feature.  

### Wind Parameters
**Wind** The _Wind_ part of the shader allows you to apply a shader-based displacement to the mesh(-es) the material is applied to. The movement is reminiscent of grass bending in the wind.  

**Enabled** Enables the _Wind_ section of the shader.  

**Intensity** How strong the movement is.  

**Frequency** The scale of the sway intervals. Higher values result in denser, more fine-grained noise.

**Speed** How fast the material displaces the object.  

**Direction** The direction of the motion.  

**Noise Amount** Introduces nonlinearities to the object’s motion.  

### Rendering Parameters
**Rendering Options**  
_Rendering options_ is a collapsible/expandable group of parameters that deal with opacity and transparency alongside a few other rendering and instancing parameters.  

**Surface Type** The two options are _Opaque_ and _Transparent_. If _Transparent_ Surface Type is selected, the Blend Mode menu becomes available with the following Blend Mode options: _Alpha_, _Premultiply_, _Additive_ and _Multiply_.  

**Render Faces** Determines what faces to render. The three options are _Both_, _Front_, _Back_.  

**Alpha Clipping** If this checkbox is in the ‘Enabled’ state, the _Threshold_ parameter appears.  

**Threshold** This parameter cuts out a transparent portion of the material. Moving it sideways determines how soon the transparent portion is ‘transparent enough’ to be cut out.  

**Enable GPU Instancing**  Enabling turns on the manipulation of the main parameters in the code.  

**TIP.** Some of the parameters, like _Rim_, _Specular_, _Height Gradient_ and others work similarly to the according parameters in the analogous _Stylized Surface_ shader in **Flat Kit**. If you didn’t find some specific info about these parameters in this manual, you might want to have a look into the [Stylized Shader chapter of the Flat Kit manual](https://flatkit.dustyroom.com/#31-stylized-surface-shader).
{: .notice--info}

## Troubleshooting

Below you can find answers to the typical possible questions when working with Stylized Lit shader.

#### Can't apply the texture
  * Please, make sure the model you are applying the material to is UV-unwrapped.
  * If you are using a custom texture, please, make sure the format is supported.

#### Can't turn off the cast shadows
  * In URP there is no option to turn the cast shadows off from a shader. You'll need to set _Cast Shadows_ to _off_ on the _Mesh Renderer_. Please, refer to this [chapter](#lighting-parameters), where the working with shadow is described.
