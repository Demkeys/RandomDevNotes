----
Raymarching Shaders
* Raymarching 1: The Basics https://medium.com/@ArmstrongCS/raymarching-1-the-basics-d6f3e70fb430
* What is Ray Marching? https://computergraphics.stackexchange.com/questions/161/what-is-ray-marching-is-sphere-tracing-the-same-thing/163
* How do Raymarch shaders work? https://gamedev.stackexchange.com/questions/67719/how-do-raymarch-shaders-work
* Five part series on raymarching. First part: https://medium.com/@si.ashbery/learning-to-draw-with-a-pencil-made-of-code-aa21b2a7b963
----
GPUs and Partial Derivatives

* https://gamedev.stackexchange.com/questions/62648/what-does-ddx-hlsl-actually-do
* https://developer.download.nvidia.com/cg/ddx.html

* https://developer.nvidia.com/gpugems/gpugems/part-iv-image-processing/chapter-24-high-quality-filtering
Complex filtering depends on knowing just how much of the texture (or shading) we need to filter. Modern GPUs such as the GeForce FX provide partial derivative functions to help us. For any value used in shading, we can ask the GPU: "How much does this value change from pixel to pixel, in either the screen-x or the screen-y direction?"
These functions are ddx() and ddy().
----
When programming shaders in Unity, if you get the following error: `Program 'geom', error X8000: Validation Error: Declared output vertex count (120) multiplied by the total number of declared scalar components of output data (10) equals 1200.  This value cannot be greater than 1024.`

...it has something to do with how Geometry shaders work. Refer to these sources for answers.
* https://docs.microsoft.com/en-us/windows/win32/direct3dhlsl/overviews-direct3d-11-hlsl-gs-index
* https://developer.nvidia.com/gpugems/gpugems3/part-vi-gpu-computing/chapter-41-using-geometry-shader-compact-and-variable-length
----
Making multiple shader program variants:
* https://docs.unity3d.com/Manual/SL-MultipleProgramVariants.html
This also explains the famous shader keyword limit issue.
----
C# Events and Delegates
* Events (C# Programming Guide): https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/events/
* Delegates (C# Programming Guide): https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/delegates/
* Handling and Raising Events: https://docs.microsoft.com/en-us/dotnet/standard/events/
* Delegate Class: https://docs.microsoft.com/en-us/dotnet/api/system.delegate
* EventHandler Class: 
----
tex2D vs tex2Dlod

[https://gamedev.stackexchange.com/questions/114851/why-cant-i-sample-a-texture-in-a-vertex-shader](https://gamedev.stackexchange.com/questions/114851/why-cant-i-sample-a-texture-in-a-vertex-shader)
"Vertex texture fetches are a little bit special. They're only supported in Shader Model 3 and up, and they're unable to use the tex2d() function.
That may sound odd, but tex2D() is really a shortcut that says "figure out the right mip level to sample automatically" - in a fragment shader this is done using implicit derivatives, but those aren't available at the vertex stage.
So, we need to use the more explicit tex2dlod() form (which works at both the vertex and fragment stages). This takes a 4-component vector, whose x and y are the familiar texture coordinates in uv space, and w indicates which mip level to sample from (0 being the highest resolution available)."

_Personal note: Apparently the only reason tex2Dlod is needed is because tex2D uses implicitely provided derivates for mip levels, which are only available in the fragment stage. In the vertex stage, those derivates have not yet been calculated, and then tex2Dlod is required, if you wanna sample a texture in the vertex stage. tex2Dlod requires you to provide a mip level to use when sampling, where 0 is the highest resolution available for that texture._

----
Mip Map

In computer graphics, mipmaps (also MIP maps) or pyramids[1][2][3] are pre-calculated, optimized sequences of images, each of which is a progressively lower resolution representation of the same image. The height and width of each image, or level, in the mipmap is a power of two smaller than the previous level. Mipmaps do not have to be square. They are intended to increase rendering speed and reduce aliasing artifacts. A high-resolution mipmap image is used for high-density samples, such as for objects close to the camera. Lower-resolution images are used as the object appears farther away. This is a more efficient way of downfiltering (minifying) a texture than sampling all texels in the original texture that would contribute to a screen pixel; it is faster to take a constant number of samples from the appropriately downfiltered textures. Mipmaps are widely used in 3D computer games, flight simulators, other 3D imaging systems for texture filtering and 2D as well as 3D GIS software. Their use is known as mipmapping.

----
Unity Coroutines
* Coroutines: https://docs.unity3d.com/Manual/Coroutines.html
* WaitForSeconds: https://docs.unity3d.com/ScriptReference/WaitForSeconds.html
* AsyncOperation: https://docs.unity3d.com/ScriptReference/AsyncOperation.html
----
