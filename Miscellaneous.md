----
When programming shaders in Unity, if you get the following error: `Program 'geom', error X8000: Validation Error: Declared output vertex count (120) multiplied by the total number of declared scalar components of output data (10) equals 1200.  This value cannot be greater than 1024.`

...it has something to do with how Geometry shaders work. Refer to these sources for answers.
* https://docs.microsoft.com/en-us/windows/win32/direct3dhlsl/overviews-direct3d-11-hlsl-gs-index
* https://developer.nvidia.com/gpugems/gpugems3/part-vi-gpu-computing/chapter-41-using-geometry-shader-compact-and-variable-length
----
