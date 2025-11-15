---
title: "Donuts!!!"
date: 2025-11-15T21:50:00+01:00
draft: false
author: "SnarlyHydra"
authorLink: "https://github.com/SnarlyHydra"
description: "My creation of donuts on Blender"
---


![Picture 1](/images/Donuts/Torusshape.jpg)

Add shape-Mesh-Torus

![Picture 2](/images/Donuts/ShadeSmooth.jgp)

Right click- Shade Smooth

![Picture 3](/images/Donuts/SubdivisionSurface.jgp)

Modifiers- Add Modifier- Generate- Subdivision Surface

![Picture 3](/images/Donuts/More Natural Shape.jpg)


Hit TAB to enter Edit Mode, click on point, tap "G" and drag mouse using scroll wheel to give object more natural shape.


![[Scale.jpg]]

Click on point in the center, hold ALT and click on a center edge, press "S" to scale the middle part down slightly. 

![[Creating Icing.jpg]]

With the main donut selected, press Shift+D to duplicate the object. Right click to keep the new mesh in the same place. Name this new mesh to "Icing". With the icing selected, go to edit mode and click the Toggle X-ray button. Select all the middle vertices around the donut and hit the delete key, clicking "Vertices".

![[Solidify.jpg]]

Go to properties on the icing. Click Generate- Solidify. Drag "Offset" all the way to 1.


![[Designing Icing.jpg]]

Enable snapping. deselect Increment. Select Face Project. Turn off Proportional Editing, enable the Subdivision property to increase number of faces. 
Now, you can select vertex, press "G" and drag up or down (Using scroll wheel), to create an icing dripping effect.

![[Second Subdivision Surface.jpg]]

With icing selected, add another Subdivision Modifier.

![[Extruding Icing.jpg]]

Enter edit mode, select two vertices, hit "E" to extrude, left click. Repeat 3 times for one icing drip.


![[Shrink Wrap.jpg]]

With Icing selected, go to the modifiers page and add a new modifier. Deform- ShrinkWrap.
Use the eye dropper tool next to the modifier and select the donut. Then move the ShrinkWrap modifier to the top of the modifier stack, as it needs to be done before the solidify modifier.
Apply the solidify modifier on the icing.


![[Inflate Tool.jpg]]

Enter Sculpt mode and select the Inflate tool. Adjust the brush size and strength of your tool and then sculpt the endings of the icing. This creates a more natural "pooling" effect for the icing.


![[Mask tool.jpg]]

Hit the "M" key to enter the mask tool mode. Adjust brush size and set strength to 1. Apply the mask to the low points of your icing, trying to keep it as even as possible, avoiding the icing drips.
Shift+I to invert the mask.

![[Filter Brush and Smooth Brush.jpg]]

Use the filter brush to create an "icing rim" around the donut. Once, happy with size, remove the mask. Select the smooth tool to smooth out some areas that may be too thick or messy.

![[Icing Material.jpg]]

With Icing selected, go to the materials tab and create a new material. Change the colour to pink and turn the roughness down to about 0.2/0.3.


![[Donut Material.jpg]]

Do the same for the donut. Choosing an orangey/yellow colour.

![[Parenting.jpg]]

Select Icing. Shift+click Donut body. Ctrl+P and click Object (Keep Transform), to parent the Donut and Icing together.

![[Countertop.jpg]]

Add mesh- Plane. To add counter top.

![[Image Texture Counter.jpg]]

Add new material on the plane. Base Colour- Image texture.

![[Marble Image.jpg]]

Apply a marble image to the material.


![[Marble Nodes.jpg]]

Enter the Shading tab at the top of the screen to open up the nodes area. Add a new node to change the roughness of the marble. This is to give it more texture. 



![[Texturing Marble.jpg]]

These are the nodes and settings needed to add sufficient texture to the marble counter top.


![[Donut Base Texture.jpg]]

Enter Texture Paint mode at the top of the screen. "/" to isolate the donut base when it is selected. 
Ass new material, add Image Texture. Edit this to the same colour as the donut base as before. 

![[UV Unwrap Texture Paint.jpg]]

Paint in a slightly lighter colour around the donut to make it appear more natural.


![[Geometry Nodes for Sprinkles.jpg]]

Enter the Geometry Node tab a the top of the screen and with the icing selected, hit "New Geometry Node". Add a node that says "Distribute Points on Faces" and connect it to a new node called "Join Geometry". Don't forget to also join "Group Input: Geometry" to "Join Geometry: Geometry". This ensures that you can have both the points on face (sprinkles) and keep the icing mesh.


![[Beginning Sprinkles.jpg]]

Shift+A-Mesh-UV Sphere to add a sprinkle shape. 



![[Object Info Nodes.jpg]]

Drag and drop the UV Sphere information into the Geometry Nodes section. This translates all the data into the "Object Info" node. Add "Instances on Points" node, and connect "Object Info: Geometry" to "Instances on Points: Instances".

![[Weight Paint.jpg]]

Enter Weight Paint mode and paint where you want sprinkles to be.



![[Weight Paint Geometry Nodes.jpg]]



In Geometry Nodes, add new node called "Names Attribute". Attach "Distribute Points on Face: Density Factor" to "Named Attribute: Attribute". 


![[Scaling Down.jpg]]

Scale the donut, sprinkle and counter down to 0.1m. You may run into some issues with the sprinkles at this point. My sprinkles became tiny. 
If this happens, select sprinkle, press "S" to scale it up in size, CTRL+A to apply scale changes.


![[Cylinder.jpg]]

To start making long sprinkles, add a cylinder mesh and scale it down to the smallest value it can go.

![[Bevel.jpg]]

Select the top and bottom face and CTRL+B to bevel the faces to appear more rounded. 

![[Multiply and bend sprinkles.jpg]]

SHIFT+D to duplicate. Enter Wireframe mode, highlight the top of the sprinkle and press G+Z to elongate. Repeat process 3 times. With the last sprinkle, CTRL+R to add loop cuts. Go to the modifier stack and add a Simple Deform Modifier, ensuring you switch the mode to "Bend".



![[Long Sprinkles Geometry Nodes.jpg]]

Drag and drop all 4 Sprinkle information into Geometry Nodes And attach "Collection Info- Instances" to "Instance on Points- Instance".
Add "Rotate Rotation" node and switch it to Local. Assign a random value to the rotation node.

![[2 Donuts.jpg]]

This is what the second donut should look like after playing around in Geometry Nodes.



![[Link Sprinkles.jpg]]

Select all of the sprinkles (including the round sprinkle) and link them all together. Create a new material on the bent sprinkle to do this.

![[Sprinkle Colour Variation.jpg]]

With the bent sprinkle selected, go to the shading tab. SHIFT+A to add an Object Info Modifier. SHIFT+A again to add Colour Ramp modifier. Join "Colour" to "Base Colour". 
With Colour Ramp, you can select whatever colours you wish your sprinkles to be and adjust the sliders to vary the proportion of these colours on the donuts.

![[Sprinkled Donut.jpg]]


![[Rendered Donuts.jpg]]

Place camera and Light in desired places and click "Rendered Viewport". You may have to change "Render through CPU" to "Render through GPU". 

![[Plate.jpg]]

SHIFT+A- mesh- circle to give a foundation to the plate. From here, you have to extrude and shade-smooth until you have a shape that you are happy with.


![[Splashback.jpg]]

Duplicate the marble countertop and position it behind the original to create a "splashback" for the scene.


![[Donut Layout.jpg]]

Duplicate and position the donuts for the scene. Here, you can change the colour of the icing and decide which donuts you want to have certain sprinkles. The colour of the icing can be changes in the materials window on the selected donut.


![[Lighting Properties.jpg]]

Delete the "Light" object that is already in the scene. Selecting the World window on the left hand side, change the "Colour" to "Sky Texture". This will create a dynamic "Sun" in our scene that we can edit the properties of. I wanted to go for a natural evening glow for my scene, so these are the changes in Elevation and Sun Rotation that I made.


![[Donut Render.jpg]]

This is what the first render looks like. From here, I can go back and add more objects to create a scene, I could tweak some colours, focus on shadows.
