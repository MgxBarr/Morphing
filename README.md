
# Image morphing

## Project Java ING1 S2 

This project involves image morphing, a technique that gradually transforms a source image into a target image using control points. 
These control points are placed on the images to guide the transformation. 
The end result is an animated GIF that illustrates this transition in a fluid and dynamic way, showing each stage of the transformation guided by the control points.

The application comprises 3 different morphs:
* simple shape morphing: broken lines are processed, and the transition is made by moving the control points linearly.
* round shape morphing: curves are processed, and the transition remains the same. 
* image morphing: using Delaunay's triangulation method.

***

## Table of contents

1. Prerequisites
2. Deployment
3. Instructions
4. Examples of use
5. Documentation
6. Technologies used
   
***

## Prerequisites

Install javafx.controls, fxml, graphics, swing dependencies. 
***

## Deployment

Write the following line in VM Run Configurations arguments:

```bash
--module-path /home/cytech/Desktop/Java/openjfx-22_linux-x64_bin-sdk/javafx-sdk-22/lib --add-modules javafx.controls,javafx.fxml,javafx.graphics,javafx.swing
```

## Instructions

### Image selection 
For each type of morphism, users can choose their start and end images by clicking on “Choose left image” and “Choose right image” respectively. 
Please note that the image name must not include spaces, and the extensions accepted are: png and jpg. 
To test the application, if required, you'll find images in the Annexes/ImagesPourTester/ folder.

### Control points 
- For simple morphing: the user can add points to the left-hand image, and the equivalent points appear on the right-hand image. On the latter, the user can move the points to position them according to the end shape. It is recommended to position points on the vertices or edges of shapes. 

- For rounded morphing, the classic control points work in the same way as for simple morphing. In addition, two intermediate points are added between two control points. These appear on both images and are used to draw the curvature of the curve. The user must move these intermediate points to match the curvature of the generated line with the curvature of the rounded shape of the image. For greater precision, it is also necessary to break down the curvature of the rounded shape into several control points.
  
- For image morphing, control points work in the same way as for simple morphing. We recommend positioning the points on characteristic elements of the image, on the subject to be transformed. For example, for faces, place the points on the eyes, nose, ears, or top and bottom of the face.

***

## Examples of use

Example of morphing from a simple rectangular shape to a simple triangular shape:

![](https://github.com/BaptistePlautA/ProjetGL3/blob/Lukas/simple.gif)

Example of a morphing of rounded shapes between a heart and a cross:

![](https://github.com/BaptistePlautA/ProjetGL3/blob/Lukas/arrondi.gif)

Example of image morphing between two Van Gogh paintings:

![](https://github.com/BaptistePlautA/ProjetGL3/blob/Lukas/van_gogh.gif)
***

## Documentation

[ImageIO pour la conversion en GIF](https://docs.oracle.com/en/java/javase/17/docs/api/java.desktop/javax/imageio/ImageIO.html)

[BufferedImage pour le morphing d'images](https://docs.oracle.com/javase/8/docs/api/java/awt/image/BufferedImage.html)

[JavaFX](https://docs.oracle.com/javase/8/javafx/api/toc.html)

***
## Technologies used

The following is a list of the different technologies used in our project:
* [Eclipse](https://eclipseide.org/): Version 2023-03 (4.27.0)
* [java](https://www.java.com/fr/): Version 17.0.6
* [javaFX](https://openjfx.io/): Version 22.0.0
* [github](https://github.com/)
***

