---
title: "Stylized Color Grading Post Effect"
permalink: /stylized-color-grading-post-effect/
excerpt: "Stylized Detail Post Effect"
toc: true
---

## Stylized Color Grading Post Effect Brief Overview
 

![Stylized Detail Post Effect interface](/quibli-doc/assets/images/manual_images/stylized_detail_post-effect_interface.png)  
*Stylized Detail Post Effect interface*

## Beginning to Work with Stylized Color Grading Post Effect

**STEP 1.** The _Stylized Detail_ effect has to be added to the currently used _Forward Renderer_ as a _Renderer Feature_. The _Renderer Feature_ is called **Quibli post processing** and includes **Stylized Post Processing** and **Stylized Detail** in the **Before Post Processing** **After Post Processing** sections. The steps are below.  
![Stylized Post Effects Renderer Features loaded in Forward Renderer](/quibli-doc/assets/images/manual_images/quibli_post_processing_renderer_features.png)  
*Stylized Post Effects Renderer Features loaded in Forward Renderer*
{: .notice--info}

  * Locate the currently active _Forward Renderer_. It can be done in a few ways. One of them is to look at your camera’s _Inspector_ panel ▶ _Forward Renderer_ field. Search for this _Forward Renderer_, select it and look at the _Inspector_ panel;  
  * Click **Add Renderer Feature**;  
  * Locate the **Quibli post processing** item in the menu. Select it.  
  * In the **Before Post Process** part of the _Quibli Post Process_, please, click the '+' button and select **Stylized Color Grading** in the drop down menu.  

**STEP 2.** After **_STEP 1_** above is completed, as the _Stylized Color Grading_ effect is a _Volume Override_ created to be used in the _Volume_ component of the camera, it should be added as a part of the post-processing onto the camera. The steps are below. 
{: .notice--info}

  * Select a camera;  
  * Press **Add Component** on the bottom of _Inspector_ panel;  
  * Type **Volume** in the search box, or locate it manually in **Miscellaneous** ▶ **Volume**, click on it once found;  
  * Click **Add Override** in the Volume;  
  * Select **Quibli** ▶ **Stylized Color Grading**.

_Stylized Color Grading_ effect is ready to be used now.  

In the _Demo Scenes_ everything has already been set up and are ready to be used. Once you set up Quibli as described in the [installation guide](../installation), all the _Forward Renderers_, _Renderer Features_ and _Volume Overrides_ are already installed and configured.
{: .notice--info}

## Parameters of Stylized Color Grading Post Effect

