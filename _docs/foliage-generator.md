---
title: "Foliage Generator"
permalink: /foliage-generator/
excerpt: "Quibli Foliage Generator Script"
---

## Foliage Generator Brief Overview
Creating anime-looking bushes and trees requires not only specific shading but also properly created models in regards to display of the shading. Simply put, the desired effect would have both large-scale and small-scale details. Of course, this can be done using a 3D-editors’ particle systems by combining both big and small emitters, but the good-looking plants would easily have 50 thousand vertices per model. So, another way is to create models from textured planes. The plants are usually modelled by placing (either carefully or haphazardly) the planes that contain the textures of the branches. This conventional method results in a blob of quads (or other plain low-poly meshes) tied together, which looks like a large scale model made of smaller parts. The problem is that each of the quads has its own normal. After rotating and moving all the quads while forming, let’s say, a bush, all the normals would also be chaotically rotated and pointed in all imaginable directions. Thus, later in Unity, the shader would take each of the quads and apply its shading using data from all of these chaotic normals. Such a bush usually would not look well. Knowing this, you’d make the normals look better by borrowing them from something more simple like a sphere. A sphere’s normals point evenly in a way that would look nice with toon shading. But creating a bush and its variations still would take much time. The _Foliage Generator_ prefab allows you to create a plant in seconds. It automatically forms the model from the ‘branch’ of your choice, wraps them (as many of them as you’d need) around a carrier model and handles the normals. After generating, the model appears in your project folder ready to be dragged onto the scene. Then you’ll need to just apply a material with the _Quibli_ shader containing a branch texture in its _Albedo_ map slot. We did all the foliage models in the demo scenes this way. Quibli includes already made models, textures and materials.

![Quibli Foliage Generator Interface](/quibli-doc/assets/images/manual_images/foliage_generator_inspector_interface.png)  
*Quibli Foliage Generator Interface*

## Beginning to work with Foliage Generator

The _Foliage Generator_ can be loaded into a scene in two ways.

### Loading Method #1 — Prefab

To start working with the _Foliage Generator_ as a Prefab, please do the following:

1. Locate the **Foliage Generator prefab** in
_**Project** panel ▶︎ **Assets** folder ▶︎ **Quibli** folder ▶︎ **Common Resources** folder ▶︎ **Prefabs** folder_;
1. Drag it to the Hierarchy panel or directly into the scene;

### Loading Method #2 — Component

Another way to add the _Foliage Generator_ to the scene is to use it as a Component.

  1. Create an empty Game Object: right-click in the empty space in the **Hierarchy panel** ▶︎ select and click **Create Empty**
  1. Select the created empty Game Object
  1. In the **Inspector panel**, please, click **Add Component**
  1. Search for ‘Foliage Generator’, or locate it manually under **Scripts** ▶︎ **Dustyroom** ▶︎ **Foliage Generator**. Click on it once found.
  1. It is ready to be tweaked.

### Operating the Foliage Generator After Loading

When you have the _Foliage Generator_ loaded to the scene, you'll probably want to [adjust the parameters or load an existing preset](#parameters-of-the-foliage-generator) and will need to [apply a material to an exported mesh](#applying-materials-to-the-exported-meshes) — to finalize the plant model. Please, keep reading this chapter to get acquainted with the details of doing these steps.

  1. Adjust needed parameters or load a preset. The explanation of the parameters can be found [below](#parameters-of-the-foliage-generator);
  1. Click _Export Mesh_ button;
  1. Locate an exported model in the export target folder. By default, it is:  
_**Project** panel ▶︎ **Assets** folder ▶︎ **Quibli** folder ▶︎ **Common Resources** folder ▶︎ **Common Models** folder_;
  1. Add this model in your scene (it looks pink)
  1. Apply the material to it.

## Parameters of the Foliage Generator

### Generation Parameters

**Generation**
A group of parameters that control the creation of the plant mesh.

- **Carrier Mesh** The triangles of this mesh are used for placement of the spawned _Particles_. Quibli comes with a handful of these. Also, of course, you can create your own ones.
- **Particle Mesh** The building block of the foliage. Multiple copies of this mesh are combined in the exported mesh. In other words, this is what would be a ‘branch’ of the plant. These particles aka branches are applied to the _Carrier Mesh_ to form the resulting plant model. You can use the simplest Quad model from Unity or select one from Quibli’s package.
- **Carrier Scale** Scaling applied to the _Carrier Mesh_ when spawning _Particles_. The bigger the _Carrier Mesh_ the more pronounced the shape of the resulting plant model would be.
- **Particle Scale** Scaling applied to each individual _Particle_. This parameter controls how large the ‘branch’ of the plant model would be. The smaller the values the more detailed the resulting mesh is going to be. More so, if the _Carrier Scale_ values are high, smaller branches will contribute to the overall shape of the _Carrier Mesh_. If the _Particle Scale_ values are high, however, the resulting plant’s look would have less of the initial _Carrier Mesh_’s shape.
- **Particle Scale Variance** Randomness of scale applied to each individual _Particle_.
- **Particles** A number of _Particles_ to generate. In other words, this parameter sets how many of the branches the plant will have.
- **Offset Along Normal** ‘Inflate’ the mesh by moving each _Particle_ along the _Carrier Mesh_ normal by this value.
- **One Normal Per Particle** If enabled, the vertices within each _Particle_ will have the same normal values.

**TIP.** _One Normal Per Particle_ parameter is useful to hide plane intersections.
{: .notice--info}

- **Particle Rotation Range** How much _Particle_ rotation can deviate from _Carrier Mesh_ normals.
- **Particle Rotation Bias** Nudge _Particles_ to face the positive X axis.

**TIP.** _Particle Rotation Bias_ is useful for billboard foliage. ‘Billboard’ means that the meshes always face the camera regardless of the camera’s position and rotation. It is a handy feature because you can make up the plant model from only a handful of planes to spare resources, and this plant will always create an impression of a more complex one.
{: .notice--info}

- **Bias Toward Rotation**

### Normal Noise Parameters

- **Normal Noise**
A group of parameters that control the nonlinearities in the normals of the generated mesh.
- **Enable** Turns the _Normal Noise_ group on.
- **Frequency**
- **Amplitude**
- **Octaves**
- **Scale** The scale of the internal noise map that controls the nonlinearities.
- **Seed**

### Parameters of Export

**Export**
A set of parameters for controlling the export process of the generated mesh.

- **Folder Path** This is where the generated plant model would go. Currently it is set to the common folder which contains all the foliage meshes used in the Demo scenes.
- **File Name Prefix** is a part of the title of the model that is going to be generated.
- **Append Mesh Name** Adds the _Carrier Mesh_ name to the name of the exported mesh.
- **Append Take Number** Adds the value from the _Take Number_ field to the exported filename.
- **Take Number** This is the current iteration number of the model. Only used if “Append Take Number” is enabled.
- **Append Timestamp** Enables the option to add time to the name of a generated mesh.
- **Export On Edit** If enabled, the mesh will be automatically updated and overwritten upon every change of any of the parameters of the _Foliage Generator_. It is useful for a rapid preview of the changes to the parameters.
- **Debug / Export Debug Mesh** This is the tick box, which lets you export the initial _Carrier Mesh_ without the branches / _Particle Meshes_ but with all the processing applied to it. It is useful if you need to see what’s going on if you are struggling with the shape and look of the filial generated foliage model.
- **Export Mesh** This is a button, which generates the final foliage model. Once generated, it is placed in the folder selected in the _Folder Path_ field found in _Export_ group of parameters. To use this mesh in your scene, drag and drop it from that folder to the scene. The model will look pink at first, because so far it has no material applied onto it. You can use the ready materials from the Demo scenes or create your own.

Every time you press the _Export Mesh_ button, the generated model is slightly different, as each time the new seed of random is used.

When a model is generated, the _Foliage Generator_ gives this model a name, which consists of prefixes like ‘Carrier Mesh’, ‘Particle Mesh’, a word from the ‘File Name Prefix’ field. Pressing _Export Mesh_ will always create a new model every time you use a different _Carrier Mesh_, _Particle Mesh_ and values in _Export_ group. That’s because the title of the generated mesh would be different in this case. Otherwise, _Export Mesh_ will just overwrite the existing model and will update it in a scene.

**TIP.** It is convenient to use presets with _Foliage Generator_: every time you export a nice model, save the parameters for later. After changing everything up on the _Foliage Generator_ interface you can always load a preset (preferably previously titled in a proper way) to fix that bush that bothers you. Because the preset, whose _Carrier Mesh_, _Particle Mesh_ and _Export Parameters_ are loaded but not altered, will not create a new separate mesh, but overwrite and update the model that was created earlier (if it was already created).
{: .notice--info}

## How to Create a Basic Plant

In the [section below](#applying-materials-to-the-exported-meshes) we'll discuss two ways of shading the Foliage Generator-made mesh. As the _Foliage Generator_ and [Foliage shader](../foliage-shader) are best buddies, let's assume, you want to use a specialized _Foliage shader_ for this task. Here is a quick plant cook-up guide.

  * Load the _Foliage Generator_. [Here's how](#beginning-to-work-with-foliage-generator);
  * Set the parameters according to screenshot in the [Brief Overview section](#foliage-generator-brief-overview):
  * Export mesh. [Here's how](#parameters-of-export);
  * Create a material like on the screenshot in the _Foliage_ shader chapter — [Brief Overview](../foliage-shader/#foliage-shader-brief-overview) (or use one from the _Sample Scene with Quibli_ Demo scene folder.

**Some explanation.** In the second step we created a mesh with a thought of using it as a billboard, explained [here](../foliage-shader/#global-billboard-parameter). That's why we used only a handful of _Particles_. The _Particle Rotation Bias_ was set to '1' to make the particles fully rotate using _Foliage_ shader's _Billboard_ parameter. _Bias Toward Rotation_ was set to '-90', because this way the _Foliage_ shader renders the faces only once. Should you set it to '90' instead, the shader will render front _and_ back faces. The _Particle Scale_ is set to a small number to generate a smaller mesh with pronounced shape (please, look through the [Generation Parameters](#generation-parameters) section for more descriptions.

## The Next Steps After Using the Foliage Generator

### Updating The Existing Exported Models Later

If you didn't change the name of the exported model after you created and used it, and given that you didn't change any parameters that contribute to the name of the exported mesh in the ongoing _Foliage Generator_ interface (see the descriptions of the parameters above), you can always come back to the _Foliage Generator_ in any of the scenes ([load the script](#beginning-to-work-with-foliage-generator) anywhere, anytime) and update the exported mesh — change the _Particle Scale_ or _Particles_ parameters, for example, — as soon as the model is exported, it will update existing one. That's where saving presets of the _Foliage Generator_ is useful. Please, dee the screenshot below.

![Using the Preset menu for the Foliage Generator](/quibli-doc/assets/images/manual_images/foliage_generator_presets_menu.png)  
*Using the Preset menu for the Foliage Generator*

### Applying Materials to the Exported Meshes

The _Foliage Generator_ script makes up a mesh ready to be imported in your scene, but to finalize its look as, let’s say, a bush or a tree, the material is needed. With Quibli you can have it done in two ways.
  * Use the [Stylized Lit shader](../stylized-lit-shader). Although the _Stylized Lit_ shader is not designed *specifically* for plants, its wide range of use cases encompasses foliage as well. Choose colors in the Gradient Editor, apply a texture and adjust alpha cutout, maybe add details and you are good to go.
  * Use the specialized [Foliage shader](../foliage-shader). Its niche controls give access to finer details in regards to finalizing the shaping of the models look, and not only the coloring. It has a _Wind_ set of parameters, the color controls are more streamlined for working with Foliage, a separate slot for alpha clipping map. The beautiful thing is that this shader can also turn the foliage models not made by the _Foliage Generator_ into plants. More on this you can find in [Foliage shader](../foliage-shader) chapter.

When you drag the exported plant model into the scene, you'll notice that it is pink, which tells that it is has no material yet. You can create a material or choose one the bundled materials coming with Quibli, and either drag it onto the model, or select a material in the model's _Mesh Renderer_.
