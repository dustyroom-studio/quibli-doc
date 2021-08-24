---
title: "Stylized Detail Post Effect"
permalink: /stylized-detail-post-effect/
excerpt: "Stylized Detail Post Effect"
toc: true
---

### Stylized Detail Post Effect Brief Overview
After a profound research about the stylistic directions and unique characteristics of the overall look of the Japanese animation films, we concluded the gained knowledge into a single post effect. It is a tool that helps shape these subtleties that you see or simply feel in the movies but maybe cannot put your finger on.  

The _Stylized Detail_ is a post effect designed to add another layer of ‘that look’ you can see in traditional Japanese animation films (of course, it can and should be used in any creative project). Under the hood it does some complex processing to make the scene appear sharper, nuanced at the large scale and at the same time with simplified smaller details.  

### Beginning to Work with Stylized Detail Post Effect
1. The _Stylized Detail_ effect has to be added to the currently used _Forward Renderer_ as a _Renderer Feature_. The _Renderer Feature_ is called **Quibli post processing** and includes **Stylized Detail** in the **After Post Processing** section. To load it, please do the following: 
  1.1. Locate the currently active _Forward Renderer_. It can be done in a few ways. One of them is to look at your camera’s _Inspector_ panel ▶ _Forward Renderer_ field. Select this _Forward Renderer_;  
  1.2. Click **Add Renderer Feature**;  
  1.3. Locate the **Quibli post processing** item in the menu. Select it.  


2. Then, as the _Stylized Detail_ effect is a _Volume Override_ created to be used in the _Volume_ component of the camera, it should be added as a part of the post-processing onto the camera:
  2.1. Select a camera;  
  2.2. Press **Add Component** on the bottom ot _Inspector_ panel;  
  2.3. Type **Volume** in the search box, or locate it manually in **Miscellaneous** ▶ **Volume**, click on it once found;  
  2.4. Click **Add Override** in the Volume;  
  2.5. Select **Quibli** ▶ **Stylized Detail**.

_Stylized Detail_ effect is ready to be used now.  

### Parameters of Stylized Detail Post Effect

**Intensity** Sets how strong the _Stylized Detail_ effect is.  

**Blur** Increases the radius of the filter. It is advised to be used subtly.  

**Edge Preserve** Keeps the edges sharp, while the _Blur_ parameter is in action.  

**Range Start**  A depth value where the effect starts to kick in.  

**Range End** A depth value where the effect ends its impact. The effect works between the _Ranfe Start_ and _Range End_ effect. If you enable only one of these parameters and leave the other in ‘off’ state, the disabled parameter would mean ‘infinity’.  

