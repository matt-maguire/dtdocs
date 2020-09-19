---
title: Editing an Image - Scene Referred Workflow (ToDo)
id: edit-scene-referred
draft: false
weight: 20
author: "people"
---


The following tables shows modules commonly used in the scene-referred workflow, with an indication where they work in linear scene-referred space or gamma-corrected display-referred space, and whether they are technical, grading or special effect modules. This workflow is well suited to modern high dynamic range camera and displays.

The raw image comes in at the bottom of the table, and the modules are stacked one-by-one on top of that until the final processed image comes out the top.

|    | Module Name | Type | Remark |
| ---| ----------- | ---- | ------ |
|<--|Processed image out||in JPG, PNG, TIFF, etc..|
|:tv:| output colour profile|:microscope:|always on, transforms from working colour profile to final output colour profile, eg. sRGB|
|:tv:|vignette           |:fairy:||
|:tv:| color zones       |:art:|can do hue mappings etc..|
|:tv:| local contrast    |:fairy:|preferred over sharpen module|
|:shinto_shrine: |Filmic |:microscope:|enabled by default; bridge between HDR scene referred and SDR display-referred space. |
|:camera:|color balance      |:art:|can adjust contrast and saturation, can also do ACES CDL colour grading|
|:camera:|channel mixer      |:art:|can be used to make monochrome image or tweak primary colours via matrix mutiplication|
|:camera:|contrast equalizer |:art:||
|:camera:|input color profile|:microscope:|always on, transforms from camera raw space to working colour profile, eg. Rec.2020 RGB|
|:camera:|tone equalizer     |:art:|useful to adjust shadows and highlights|
|:camera:|exposure           |:microscope:|enabled by default|
|:camera:|spot removal       |:fairy:|if needed|
|:camera:|crop and rotate    |:microscope:||
|:camera:|haze removal       |:microscope:|if needed|
|:camera:|perspective correction|:microscope:|if needed|
|:camera:|lens correction    |:microscope:|if needed|
|:camera:|denoise (profiled) |:microscope:|preferred module for noise reduction|
|:camera:|demosaic           |:microscope:|always on|
|:camera:|chromatic abberation|:microscope:||
|:camera:|highlight reconstruction|:microscope:|enabled by default|
|:camera:|white balance      |:art:|enabled by default|
|-->|raw image in|||

