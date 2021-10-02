---
title: "Frequently Asked Questions (FAQs)"
permalink: /faqs/
excerpt: "Frequently Asked Questions (FAQs)"
toc: false
---

#### What is the difference between Quibli and Flat Kit?
> Please, look at [this chapter](../quibli-or-flat-kit), which compares the two.

---

#### After installing Quibli there are errors in the Console.
> Please, look into the [Troubleshooting](../installation#troubleshooting) section.

---

#### **Q.** The scenes in Unity look darker/brighter than the screenshots.
> **A.** The screenshots on the Asset Store are taken from the scenes, without any processing or color correction whatsoever, i.e. they should look virtually the same as the scenes, minus the embedded description text. The differences may occur if your project is in **_Gamma color space_**, as the scenes were made in **_Linear color space_**. Another reason may be in the **unfinished setup** ([how to finalize Quibli setup?](../installation/#finalizing-quibli-installation)), when the scene can't find the needed forward renderer.

#### **Q.** Which Rendering Pipelines does Quibli support?
> **A.** Quibli supports Universal (URP, fka LWRP) only. It won't work in Built-In RP and HDRP.

#### **Q.** I'm getting errors after moving the Quibli folder from _Assets_. 
> **A.** This is due to a [bug in Shader Graph](https://issuetracker.unity3d.com/issues/shadergraph-reference-to-hlsl-file-is-lost-after-moving-it-to-a-different-folder) which has been fixed in URP 12 (Unity 2021.2). To work-around the issue in earlier versions of URP, please click the "Reimport Quibli files" button in the Readme file after you've moved the Quibli folder.
