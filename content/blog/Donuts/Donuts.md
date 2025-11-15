---
title: "Donuts!!!"
date: 2025-11-15T21:50:00+01:00
draft: false
author: "SnarlyHydra"
authorLink: "https://github.com/SnarlyHydra"
description: "My creation of donuts on Blender"
---


![Picture 0](/images/Donuts/Torusshape.jpg)

Add shape-Mesh-Torus

![Picture 1](/images/Donuts/ShadeSmooth.jpg)

Right click- Shade Smooth

![Picture 2](/images/Donuts/SubdivisionSurface.jpg)

Modifiers- Add Modifier- Generate- Subdivision Surface

![Picture 3](/images/Donuts/MoreNaturalShape.jpg)

Hit TAB to enter Edit Mode, click on point, tap "G" and drag mouse using scroll wheel to give object more natural shape.

![Picture 4](/images/Donuts/Scale.jpg)


Click on point in the center, hold ALT and click on a center edge, press "S" to scale the middle part down slightly. 

![Picture 5](/images/Donuts/CreatingIcing.jpg)


With the main donut selected, press Shift+D to duplicate the object. Right click to keep the new mesh in the same place. Name this new mesh to "Icing". With the icing selected, go to edit mode and click the Toggle X-ray button. Select all the middle vertices around the donut and hit the delete key, clicking "Vertices".

![Picture 6](/images/Donuts/Solidify.jpg)


Go to properties on the icing. Click Generate- Solidify. Drag "Offset" all the way to 1.

![Picture 7](/images/Donuts/DesigningIcing.jpg)


Enable snapping. deselect Increment. Select Face Project. Turn off Proportional Editing, enable the Subdivision property to increase number of faces. 
Now, you can select vertex, press "G" and drag up or down (Using scroll wheel), to create an icing dripping effect.

![Picture 8](/images/Donuts/SecondSubdivisionSurface.jpg)


With icing selected, add another Subdivision Modifier.

![Picture 9](/images/Donuts/ExtrudingIcing.jpg)


Enter edit mode, select two vertices, hit "E" to extrude, left click. Repeat 3 times for one icing drip.

![Picture 10](/images/Donuts/ShrinkWrap.jpg)


With Icing selected, go to the modifiers page and add a new modifier. Deform- ShrinkWrap.
Use the eye dropper tool next to the modifier and select the donut. Then move the ShrinkWrap modifier to the top of the modifier stack, as it needs to be done before the solidify modifier.
Apply the solidify modifier on the icing.

![Picture 11](/images/Donuts/InflateTool.jpg)


Enter Sculpt mode and select the Inflate tool. Adjust the brush size and strength of your tool and then sculpt the endings of the icing. This creates a more natural "pooling" effect for the icing.

![Picture 12](/images/Donuts/Masktool.jpg)


Hit the "M" key to enter the mask tool mode. Adjust brush size and set strength to 1. Apply the mask to the low points of your icing, trying to keep it as even as possible, avoiding the icing drips.
Shift+I to invert the mask.

![Picture 13](/images/Donuts/FilterBrushandSmoothBrush.jpg)


Use the filter brush to create an "icing rim" around the donut. Once, happy with size, remove the mask. Select the smooth tool to smooth out some areas that may be too thick or messy.

![Picture 14](/images/Donuts/IcingMaterial.jpg)


With Icing selected, go to the materials tab and create a new material. Change the colour to pink and turn the roughness down to about 0.2/0.3.

![Picture 15](/images/Donuts/DonutMaterial.jpg)


Do the same for the donut. Choosing an orangey/yellow colour.

![Picture 16](/images/Donuts/Parenting.jpg)

Select Icing. Shift+click Donut body. Ctrl+P and click Object (Keep Transform), to parent the Donut and Icing together.

![Picture 17](/images/Donuts/Countertop.jpg)


Add mesh- Plane. To add counter top.

![Picture 3](/images/Donuts/ImageTextureCounter.jpg)


Add new material on the plane. Base Colour- Image texture.

![Picture 18](/images/Donuts/MarbleImage.jpg)


Apply a marble image to the material.

![Picture 19](/images/Donuts/MarbleNodes.jpg)


Enter the Shading tab at the top of the screen to open up the nodes area. Add a new node to change the roughness of the marble. This is to give it more texture. 


![Picture 20](/images/Donuts/TexturingMarble.jpg)


These are the nodes and settings needed to add sufficient texture to the marble counter top.

![Picture 21](/images/Donuts/DonutBaseTexture.jpg)


Enter Texture Paint mode at the top of the screen. "/" to isolate the donut base when it is selected. 
Ass new material, add Image Texture. Edit this to the same colour as the donut base as before. 

![Picture 22](/images/Donuts/UVUnwrapTexturePaint.jpg)


Paint in a slightly lighter colour around the donut to make it appear more natural.

![Picture 23](/images/Donuts/GeometryNodesforSprinkles.jpg)


Enter the Geometry Node tab a the top of the screen and with the icing selected, hit "New Geometry Node". Add a node that says "Distribute Points on Faces" and connect it to a new node called "Join Geometry". Don't forget to also join "Group Input: Geometry" to "Join Geometry: Geometry". This ensures that you can have both the points on face (sprinkles) and keep the icing mesh.

![Picture 24](/images/Donuts/BeginningSprinkles.jpg)


Shift+A-Mesh-UV Sphere to add a sprinkle shape. 

![Picture 25](/images/Donuts/ObjectInfoNodes.jpg)


Drag and drop the UV Sphere information into the Geometry Nodes section. This translates all the data into the "Object Info" node. Add "Instances on Points" node, and connect "Object Info: Geometry" to "Instances on Points: Instances".

![Picture 26](/images/Donuts/WeightPaint.jpg)


Enter Weight Paint mode and paint where you want sprinkles to be.

![Picture 27](/images/Donuts/WeightPaintGeometryNodes.jpg)


In Geometry Nodes, add new node called "Names Attribute". Attach "Distribute Points on Face: Density Factor" to "Named Attribute: Attribute". 

![Picture 28](/images/Donuts/ScalingDown.jpg)


Scale the donut, sprinkle and counter down to 0.1m. You may run into some issues with the sprinkles at this point. My sprinkles became tiny. 
If this happens, select sprinkle, press "S" to scale it up in size, CTRL+A to apply scale changes.

![Picture 29](/images/Donuts/Cylinder.jpg)


To start making long sprinkles, add a cylinder mesh and scale it down to the smallest value it can go.

![Picture 30](/images/Donuts/Bevel.jpg)


Select the top and bottom face and CTRL+B to bevel the faces to appear more rounded. 

![Picture 31](/images/Donuts/Multiplyandbendsprinkles.jpg)


SHIFT+D to duplicate. Enter Wireframe mode, highlight the top of the sprinkle and press G+Z to elongate. Repeat process 3 times. With the last sprinkle, CTRL+R to add loop cuts. Go to the modifier stack and add a Simple Deform Modifier, ensuring you switch the mode to "Bend".

![Picture 32](/images/Donuts/LongSprinklesGeometryNodes.jpg)


Drag and drop all 4 Sprinkle information into Geometry Nodes And attach "Collection Info- Instances" to "Instance on Points- Instance".
Add "Rotate Rotation" node and switch it to Local. Assign a random value to the rotation node.

![Picture 33](/images/Donuts/2Donuts.jpg)


This is what the second donut should look like after playing around in Geometry Nodes.

![Picture 34](/images/Donuts/LinkSprinkles.jpg)


Select all of the sprinkles (including the round sprinkle) and link them all together. Create a new material on the bent sprinkle to do this.

![Picture 35](/images/Donuts/SprinkleColourVariation.jpg)


With the bent sprinkle selected, go to the shading tab. SHIFT+A to add an Object Info Modifier. SHIFT+A again to add Colour Ramp modifier. Join "Colour" to "Base Colour". 
With Colour Ramp, you can select whatever colours you wish your sprinkles to be and adjust the sliders to vary the proportion of these colours on the donuts.

![Picture 36](/images/Donuts/SprinkledDonut.jpg)


![Picture 37](/images/Donuts/RenderedDonuts.jpg)


Place camera and Light in desired places and click "Rendered Viewport". You may have to change "Render through CPU" to "Render through GPU". 

![Picture 38](/images/Donuts/Plate.jpg)


SHIFT+A- mesh- circle to give a foundation to the plate. From here, you have to extrude and shade-smooth until you have a shape that you are happy with.

![Picture 39](/images/Donuts/Splashback.jpg)


Duplicate the marble countertop and position it behind the original to create a "splashback" for the scene.

![Picture 40](/images/Donuts/DonutLayout.jpg)


Duplicate and position the donuts for the scene. Here, you can change the colour of the icing and decide which donuts you want to have certain sprinkles. The colour of the icing can be changes in the materials window on the selected donut.

![Picture 41](/images/Donuts/LightingProperties.jpg)


Delete the "Light" object that is already in the scene. Selecting the World window on the left hand side, change the "Colour" to "Sky Texture". This will create a dynamic "Sun" in our scene that we can edit the properties of. I wanted to go for a natural evening glow for my scene, so these are the changes in Elevation and Sun Rotation that I made.

![Picture 42](/images/Donuts/DonutRender.jpg)

This is what the first render looks like. From here, I can go back and add more objects to create a scene, I could tweak some colours, focus on shadows.
