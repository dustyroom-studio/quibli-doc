---
title: "Cloud2D Shader"
permalink: /cloud2d-shader/
excerpt: "Quibli Cloud2D Shader"
toc: true
---

### Cloud2D Shader Brief Overview
_Cloud2D_ shader is an easy and flexible way to add the clouds to your scene. It works with 2D planes, or quads, and it works regardless of whether you have the skybox or not. The shader is applied to 2D objects like Quads, meaning, there is no real topology in the clouds, which is very beneficial to the performance.  

_Cloud2D_ shader was made in a Shader Graph, so you can easily edit and modify it in the Shader Graph editor.  

When you move a cloud horizontally or vertically it is being continuously morphed upon the internal noise map. The effect is that when you duplicate it and move it anywhere, this copy will never look the same as the original source. It is handy, since you can effortlessly populate the sky with differently looking clouds just by copying and moving without the need of duplicating and altering materials for each copy. Moreover, if you animate the motion of these planes, you’ll get moving and, at the same time, always-changing clouds instead of static-shaped sprites/models.

### Beginning to Work with Cloud2D Shader

* Create a material
* In the **Inspector** panel, in the **Shader** drop down menu choose **Quibli** ▶︎ **Cloud2D**.
Now you can apply this material to a default Unity Quad model, for example.

### Parameters of the Cloud2D Shader

**Main gradient** The parameter where you set the main colors of a cloud. Clicking on the Gradient ramp opens the _Gradient Editor_ where you can set up to color 8 stops. You can find more information about the _Gradient Editor_ in the part about the _Stylized Lit Shader_.  

**Geometry gradient**  Opens a similar _Gradient Editor_ as the one in _Main Gradient_. This gradient specifically uses black and white channel only, so it does not impact any color work but rather the shape of the cloud, more precisely, the fading out of the contour of a cloud into transparency. White color is fully visible (opaque), black is fully invisible (transparent). Thus, if you have a tightly placed black → white color stops, the edges of a cloud will be sharper than if the gradient would be more smooth. You can have up to 8 color stops.  

**Edge Distortion** Distorts the contour of a cloud using an internal noise map.  

**Base Vertical Offset** Moves a cloud upwards and downwards in an exponential way — it stretches the cloud near the extreme values of this parameter.  

**Shadow** This Is the section responsible for controlling the shadows of a cloud.  

**Color** Sets the color of the shadowed part of a cloud.  

**Amount**  Sets how visible the shadow is.  

**Distortion** Increases the intensity of the ‘grainy’ effect, where grains are made by being mapped onto the internal displacement map.  

**Center** Sets the coordinates of the center of the shadow.  

**Range** Sets how spread out the shadow is.  

**Edge Highlight** Opens the color chooser to pick up the color of a halo visible around a cloud.  

**Opacity** Sets how visible the _Edge highlight_ is.  

**Height gradient strength** Controls vertical shading of the cloud using the _Main Gradient_.  

**Random Offset** Changing the values on the axis moves the internal displacement map of a cloud against the mesh itself along that axis. Dragging the cloud itself and tweaking _Random Offset_ have the same effect, because translating the mesh does not preserve the noise stamp (seed) it is being mapped to. The cloud is always being projected onto a static world-space internal noise map to form the fluffiness of it.  
_Random Offset_ can be used as a parameter to change the seed of random. Animating either this parameter or the cloud itself can be used to create the effect of a realistic ever-changing cloud.  

**Geometry density** This is a group of parameters that control the small-, medium- and large-scale details of a cloud shape.  

**Large** Changes the size of large-scale details in the internal displacement map. Increasing the value makes the details smaller; decreasing the values makes the details larger.  

**Medium** Changes the size of medium-scale details in the internal displacement map.  

**Small** Changes the size of small-scale details in the internal displacement map.  

**Face Camera** It is a ‘billboard’ aka ‘always look into the camera’ effect, which is helpful in situations when the clouds may be approachable by the camera and not desired to be seen from an angle. So, as you are getting closer to the clouds, _Face Camera_ parameter makes sure the cloud will always rotate to look into the camera.  

### Misc Info About the Cloud2D Shader
The _Cloud2D_ shader is made inside the Shader Graph. You can tweak and customize its core as you like. If you want to save your customization work, please do so through saving as a new shader file in order not to break the default one.

**NOTE.** In order to use a custom plane model, please make sure it is UV-unwrapped.
{: .notice--warning}

**TIP.** To make one complex-looking cloud in the demo scenes, we use two materials: one is dark inside and light outside, the second one is vice versa, darker on the edges. This way it is easier to emphasize the inner parts of the cloud chunks. You can have a look into the _Unity Default Sample Scene Quiblified_ or into the _Nature_ demo scenes to see the effect.  
{: .notice--info}

