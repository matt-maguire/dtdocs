---
title: Editing an Image - Display Referred Workflow (ToDo)
id: edit-display-referred
draft: false
weight: 30
author: "people"
---

The following tables shows modules commonly used in the display-referred workflow, with an indication where they work in linear scene-referred space or gamma-corrected display-referred space, and whether they are technical, grading or special effect modules. This is a legacy workflow that is best suited to low-dynamic range scenarios only.

The raw image comes in at the bottom of the table, and the modules are stacked one-by-one on top of that until the final processed image comes out the top.

|    | Module Name | Type | Remark |
| ---| ----------- | ---- | ------ |
|<--|Processed image out   ||in JPG, PNG, TIFF, etc..|
|:tv:|vignette           |:fairy:||
|:tv:|channel mixer|:art:|can be used to make a monochrome image|
|:tv:|output colour profile|:microscope:|always on, transforms from working colour profile to final output colour profile, eg. sRGB|
|:tv:|sharpen                       |:fairy:||
|:tv:|contrast brightness saturation|:fairy:||
|:tv:|color zones                   |:art:||
|:tv:|local contrast                |:fairy:||
|:tv:|contrast equalizer            |:art:||
|:tv:|shadows and highlights        |:art:||
|:tv:|color balance                 |:art:||
|:tv:|basic adjustments             |:art:|combines exposure, shadows & highlights, contrast, saturation etc. in one module, or you can do these things in separate modules in you want more control|
|:tv:|input color profile|:microscope:|always on, transforms from camera raw space to working colour profile, eg. Rec.2020 RGB|
|:tv:|haze removal       |:microscope:||
|:shinto_shrine: |Base Curve |:microscope:|enabled by default; bridge between scene referred and display-referred space. Could use tone curve here instead|
|:camera:|crop and rotate    |:microscope:||
|:camera:|lens correction    |:microscope:||
|:camera:|spot removal       |:fairy:||
|:camera:|exposure           |:microscope:||
|:camera:|denoise (profiled) |:microscope:||
|:camera:|demosaic           |:microscope:|always on|
|:camera:|chromatic abberation|:microscope:||
|:camera:|highlight reconstruction|:microscope:|enabled by default|
|:camera:|white balance      |:art:|enabled by default|
|-->|Raw image in|||

