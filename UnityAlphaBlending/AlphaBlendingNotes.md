Learning Alpha Blending in shaders in Unity
===================================================
___NOTE: These are notes I've made after performing tests to better understand Alpha Blending in shaders in Unity. I'm using Unlit Transparent shaders. These notes are for my future reference, but if they help anyone else, great.___

The examples are supposed to show how blending is done and what colors are produced after blending. You can google 'Unity Shader Blending' to learn the basics of Alpha Blending. Those are not covered in these notes. For the sake of simplicity, the scene has simple colors - a black background, a red quad, grey quad and a blue quad. The grey and blue quads are transparent. Each blend produces a different color, so each color is labeled, for example C1,C2,C3,etc. The labels are mentioned in the image, and for each blended color, the calculations are mentioned below. In each calculation, the DstFactor is the color in the frame buffer.
- - - - - - - - - - - - - - - - - - - - - - - -
![](https://github.com/Demkeys/RandomDevNotes/blob/master/Image01.png)
![](https://github.com/Demkeys/RandomDevNotes/blob/master/Image02.png)
- - - - - - - - - - - - - - - - - - - - - - - -
### Render Queues:<br/>
Geometry: 2000 (Front to Back)<br/>
Transparent: 3000 (Back to Front)<br/>

Transparent queue is rendered after Geometry queue. There are various syntaxes and factors that can be used for blending but for this example we are using one syntax... <br/>
Syntax: Blend SrcFactor DstFactor <br/>
Blend SrcAlpha OneMinusScrAlpha <br/>

Red Quad = (0.5,0,0,1) <br/>
Grey Quad = (0.5,0.5,0.5,0.5) <br/>
Blue Quad = (0,0,0.5,0.5) <br/>
Black BG = (0,0,0,1) <br/>
- - - - - - - - - - - - - - - - - - - - - - - -
## C1 - Blending of Grey Quad and Black Background

SrcFactor = (0.5,0.5,0.5,0.5) * 0.5 <br/>
DstFactor = (0,0,0,1) * (1-0.5) <br/>
Result = (0.25,0.25,0.25,0.25) + (0,0,0,0.5) = (0.25,0.25,0.25,0.75) <br/>
- - - - - - - - - - - - - - - - - - - - - - - -
## C2 - Blending of Grey Quad and Red Quad
SrcFactor = (0.5,0.5,0.5,0.5) * 0.5 <br/>
DstFactor = (0.5,0,0,1) * (1-0.5) <br/>
Result = (0.25,0.25,0.25,0.25) + (0.25,0,0,0.5) = (0.5,0.25,0.25,0.75) <br/>
- - - - - - - - - - - - - - - - - - - - - - - -
## C3 - Blending of Blue Quad, Grey Quad and Red Quad

#### Grey Quad and Red Quad
SrcFactor = (0.5,0.5,0.5,0.5) * 0.5 <br/>
DstFactor = (0.5,0,0,1) * (1-0.5) <br/>
Result = (0.25,0.25,0.25,0.25) + (0.25,0,0,0.5) = (0.5,0.25,0.25,0.75) <br/>

#### Blue Quad and Grey (blended, at this point it's not really grey) Quad 
SrcFactor = (0,0,0.5,0.5) * 0.5 <br/>
DstFactor = (0.5,0.25,0.25,0.75) * (1-0.5) <br/>
Result = (0,0,0.25,0.25) + (0.25,0.125,0.125,0.375) = (0.25,0.125,0.375,0.625) <br/>
- - - - - - - - - - - - - - - - - - - - - - - -
## C4 - Blending of Blue Quad, Grey Quad and Black Background

#### Grey Quad and Black Background
SrcFactor = (0.5,0.5,0.5,0.5) * 0.5 <br/>
DstFactor = (0,0,0,1) * (1-0.5) <br/>
Result = (0.25,0.25,0.25,0.25) + (0,0,0,0.5) = (0.25,0.25,0.25,0.75) <br/>

#### Blue Quad and Grey (blended) Quad 
SrcFactor = (0,0,0.5,0.5) * 0.5 <br/>
DstFactor = (0.25,0.25,0.25,0.75) * (1-0.5) <br/>
Result = (0,0,0.25,0.25) + (0.125,0.125,0.125,0.375) = (0.125,0.125,0.375,0.625) <br/>
- - - - - - - - - - - - - - - - - - - - - - - -
## C5 - Blending of Blue Quad and Black Background
SrcFactor = (0,0,0.5,0.5) * 0.5 <br/>
DstFactor = (0,0,0,1) * (1-0.5) <br/>
Result = (0,0,0.25,0.25) + (0,0,0,0.5) = (0,0,0.25,0.75) <br/>
- - - - - - - - - - - - - - - - - - - - - - - -
