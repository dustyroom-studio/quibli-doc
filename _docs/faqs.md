---
title: "Frequently Asked Questions (FAQs)"
permalink: /faqs/
excerpt: "Frequently Asked Questions (FAQs)"
toc: false
---

#### What is the difference between Quibli and Flat Kit?
> Please, look at [this chapter](../quibli-flat-kit), which compares the two.

---

#### After installing Quibli there are some issues.
> Please, look into the [Troubleshooting](../installation#troubleshooting) section.

---

#### The scenes in Unity look darker/brighter than the screenshots.
> The screenshots on the Asset Store are taken from the scenes, without any processing or color correction whatsoever, i.e. they should look virtually the same as the scenes, minus the embedded description text. The differences may occur if your project is in **_Gamma color space_**, as the scenes were made in **_Linear color space_**. Another reason may be in the **unfinished setup** ([how to finalize Quibli setup?](../installation/#finalizing-quibli-installation)), when the scene can't find the needed forward renderer.

---

#### Which Rendering Pipelines does Quibli support?
> Quibli supports Universal (URP, fka LWRP) only. It won't work in Built-In RP and HDRP.

---

#### What is the Shader Compilation Target Level of Flat Kit shaders?
> The object shaders target 3.5 (or es 3.0 and WebGL 2.0).

---

#### I'm getting errors after moving the Quibli folder from _Assets_. 
> This is due to a [bug in Shader Graph](https://issuetracker.unity3d.com/issues/shadergraph-reference-to-hlsl-file-is-lost-after-moving-it-to-a-different-folder) which has been fixed in URP 12 (Unity 2021.2). To work-around the issue in earlier versions of URP, please click the "Reimport Quibli files" button in the Readme file after you've moved the Quibli folder.

---

#### Is Quibli mobile-friendly?
> The short answer is yes, Quibli shaders are mobile-friendly. The longer answer is the following.
The performance of the shaders is comparable to the Unity standard Lit shader; the Quibli post effects work similarly to the Unity post effects. But, of course, you have to be mindful of the modeling optimization.
Also, below you can find a few general Unity optimization points I could think of that performance depends on.
- The performance depends on the hardware you are working/testing it on. If it is not an ancient phone, for example, Quibli was tested to be running smoothly with the appropriate number of shaders and parameters engaged.
- Check if the test device meets the requirements: the object shaders target 3.5 (or es 3.0 and WebGL 2.0).
- Also, if possible, try reusing materials as much as possible. Although SRP batching should deal with it, it still is a good practice to keep the materials number moderate.
- If you use many objects on the scene, make sure you use occlusion culling.
- The performance gain can vary significantly based on the number of vertices and materials used.
- The Quibli Foliage and Cloud2D shaders use transparency. If you use a lot of alpha clipping, it is expected that the performance can be struggling. If the framerate is still low, please try out any Unity shader with alpha clipping. The low performance might be caused by the fact that the hardware can't handle alpha clipping well enough.
- If you can, toggle the unused parameters off. Some of them are still in use even if they are at the 0 value. That's why most of the Quibli's main parameters can be bypassed by pressing a tick off.

---

#### How do I get 50% discount for Quibli if I have (am going to purchase) Flat Kit?
> Please, log into the same account with which you purchased Flat Kit, open the Quibli's Asset Store page — you should see the automatically applied 50% discount there.



