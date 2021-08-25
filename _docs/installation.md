---
title: "Quick-Start Guide"
permalink: /installation/
excerpt: "How to quickly install and setup Quibli"
toc: true
---

## Importing Quibli
First of all, you need to import Quibli into your project.  
Please, make sure you have the Universal RP project running (not Built-In RP or HDRP).  

  * In Unity, go to **Window** ▶︎ **Package Manager**; 
  * On the top left, please, find the **Packages** drop down menu. Select **My Assets** item there. You’ll find **Quibli** among your assets. Choose the version you’d like to import;  
  * Click **Download** (if it is not downloaded yet);  
  * Click **Import**.  

## Finalizing Quibli Installation

After the importing, to finalize the installation it is advised to configure Quibli for Universal Rendering Pipeline. 

### Automatic Finalizing

Quibli comes with the **[Readme]** script tool, whose one of the jobs is to automatically configure URP to be working with Quibli. This procedure can be done and undone manually, which is described in [Manual Finalizing](#manual-finalizing) paragraph.  

If you would like to use your own **Rendering Pipeline Asset File** instead of the one that comes with Quibli, you'll need to do it manually. The procedure is described in [Manual Finalizing](#manual-finalizing) 
{: .notice--warning}

  * Please, locate and select the **[Readme] tool** in  
_**Project** panel ▶︎ **Assets** folder ▶︎ **Quibli** folder_;  
  * In the **Inspector** panel press the **Configure URP** button. This will set the example _Quibli Rendering Pipeline Asset_ into **Graphics** and **Quality** windows found in **Project Settings**.  

### Manual Finalizing

  * Locate the **Quibli URP Config** file in  
**Project** panel ▶︎ **Quibli** folder ▶︎ **[Render Pipeline] URP** folder ▶︎ **Example Settings** folder.  
You can use your own custom settings file. The Quibli one is needed for viewing the Quibli Demo scenes.
{: .notice--info}
![Quibli URP Config file location](/quibli-doc/assets/images/manual_images/quibli_urp_config_file_location.png)  
*Quibli URP Config file location*
  * Navigate to _Edit_ ▶︎ _Project Settings_;
  * Open the **Graphics** tab and select **Quibli URP Config** file in the **Scriptable Render Pipeline Settings** field;
![Graphics Settings Panel](/quibli-doc/assets/images/manual_images/quibli_project_setings_graphics_settings_panel.jpg)  
*Graphics Settings Panel — select Quibli URP Config file in Scriptable Render Pipeline Settings field*
  * Open the **Quality** tab and select the same **Quibli URP Config** in the field **for all _Quality Levels_** available in your project;
![Quality Settings Panel](/quibli-doc/assets/images/manual_images/quibli_project_setings_quality_settings_panel.jpg)  
*Quality Settings Panel — select Quibli URP Config file in Rendering field for all available quality levels*
  * Important. If you would like to use your own **Rendering Pipeline Asset File** instead of the **Quibli URP Config**, which comes with Quibli, please make sure this asset file has **Depth Texture** and **Opaque Texture** checkboxes enabled. It is required if you would like to build your project to a mobile, for example.
![URP Config file should have Depth Texture and Opaque Texture turned on](/quibli-doc/assets/images/manual_images/urp_config_file_depth_texture_opaque_texture.png)  
*URP Config file should have Depth Texture and Opaque Texture turned on*

**NOTE.** Should you have any difficulties with the installation of Quibli, please read through the [Troubleshooting](#troubleshooting) chapter on this page as well as have a look at the [FAQs](../faqs) page. It your questions are not answered yet, please [Report an Issue]() or write to us to info@dustyroom.com. We should be able to help you quickly. Please, don't forget to include your set-up details like Unity and Quibli versions.
{: .notice--info}

## Troubleshooting

Below you can find typical possible issues when installing Quibli as well as other assets in Unity.  

#### Can't import Quibli
  * First of all, please check if it has been downloaded in the _Package Manager_ (the steps for downloading are described [above](#importing-quibli)). If you are installing Quibli a fresh copy of Quibli, it should be downloaded first. You should see the _Download_ button in the _Package Manager_.
  * If Quibli has been previously downloaded but you cannot see the _Import_, it may be due to the known Package Manager 'cache' issue. You'll need to locate the **Package Manager Cache** in your OS and delete the folder. As soon as you do so, the _Import_ button should appear right away. The cache folder location depends on the OS you are using. Here are the paths:  
> _Mac OS:_ ~/Library/Unity/Asset Store-5.x _(press Shift+Cmd+G in any Finder Window and paste this path)_  
> _Windows:_ %APPDATA%\Unity\Asset Store-5.x _(it is a hidden folder)_  
> _Linux:_ ~/.local/share/unity3d/Asset Store-5.x  

#### After importing, Quibli gives errors
  * First, try restarting Unity. A simple restart indeed sometimes fixes some strange issues.
  * Re-import Quibli. Either delete it from the project and repeat [setting it up](#importing-quibli), or right-click on the _Quibli_ folder in the _Project_ panel and select _Reimport_.
  * This also may be due to unsupported Unity version, for example, a Unity beta release (with a 'b' in its title — the stable ones are named with 'f') not _yet_ stable enough to be listed in the supported Unity versions, or a very old version that hadn't ever been listed in Quibli supported Unity versions.