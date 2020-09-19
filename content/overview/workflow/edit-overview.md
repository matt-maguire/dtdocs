---
title: Editing an Image - Workflow Overview
id: workflow-overview
draft: false
weight: 20
author: "people"
---

When we process an image in darktable, we are normally taking a file with the raw image data collected off the sensor of a camera that captured an image at some scene, and we are applying a series of processing steps to turn that raw image into something that looks pleasing on some sort of display, whether it be a picture on a computer monitor or a print on a piece of paper. The steps that take the image from the data captured at the scene to the final image on the display are performed by a sequence of modules, each module doing its specific job before passing the image on to the next module for the next processing steps. This handing off of the image from one module to the next is what we call the *pixel pipe*, and you can think of it as a production line in a factory, where each subsequent worker builds on top of the work that was done before.

In the early stages of the pixel pipe, the modules are often doing initial adjustments and corrections to the image to allow for the physical characteristics of the camera and the lens. These are often based on physics equations related to the nature of the light collected a the scene, and we refer these steps as being in the *scene-referred* part of the pixel pipe. At some point in the pixel pipe, there'll be a transition where a module takes the data from the scene-referred part of the pixel pipe, and it will transform it into a format that is more aligned with the characteristics of the disply device(s) we are going to use. Modules after that said to be working in *display-referred* space, and they will perform actions on the image to make it look good for the display.

Traditionally in darktable, this transition from scene-referred to display-referred modules happened fairly early in the pipline, and a lot of the processing happened in display-referred space. With the technologies of the time, this worked quite well, and you can continue to use this original workflow with a display-referred emphasis if you wish.

However, with modern day camera, there have been advances in sensor technology that allows these cameras to capure a very wide dynamic range, and displays that can handle high dynamic ranges are also becoming popular. When you try to handle such images using modules in display-referred spaces such as the Lab colour space, the mathematical models start to break down, and you can find that artifacts like halos, hue shifts, etc. become more difficult to control. By moving some of these later display-referred modules earlier in the pixel pipe, and adjusting the mathematical models to work in scene-referred space, it becomes much easier to control these undesirable effects. So, from darktable 3.0, a new *scene-referred* workflow was introduced which places emphasis on doing as much processing as possible in the scene-referred part of the pixel pipe, and leaving the transition to display-referred processing as late as possible.

So, which workflow should you choose? If you are new to darktable, we would recommend that you learn about the new *scene-referred* workflow. For existing users who are already used to doing their image processing using the old *display-referred* workflow, then this will continue to be supported for the time being. Of course, if you want the benefits to be gained from the new scene-referred workflow, we certainly encourage users to check it out.

More information can be found in the *display-referred* and *scene-referred* specific section of this user guide. They will provide an quick summary of some key modules used in those two workflows, and show where they sit in the pixel pipe. The following table describes the symbols that are used to provide information about the modules listed in those summaries.

| Symbol | Description |
| ------ | ----------- |
| :tv: | Display-referred space |
| :camera: | Scene-referred space |
| :shinto_shrine: | Bridge between scene-referred and display-referred pixelpipe |
| :microscope: | "technical" contains every module related to some physical reality: lens, sensor, in/out color spaces and various signal reconstructions (highlights, noise, etc.) |
| :art: | "grading" modules are used artistically and for doing color and tones corrective and creative work (including chromatic adaptation / white balance) |
| :fairy: | "effects" modules used to achieve some cosmetic or specific effect (local contrast, sharpness, high/low-freq, retouch, liquify, etc.) |


