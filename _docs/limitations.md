---
title: "Known Limitations when Working with Quibli"
permalink: /limitations/
excerpt: "Known Limitations when Working with Quibli"
toc: false
---

In this chapter the known limitations of working with Quibli are described.

#### In _Foliage_ and _Grass_ shaders, there is no support for the shadows when working with additional lights.
During making of the _Foliage_ and _Grass_ shaders, we had to completely revisit Unity's emission behavior for these shaders, in order to flexibly control the color shading. Otherwise, there would be a poor looking shadow rendered over the foliage objects, which there is no control over.

