### Notes relating to 3D modeling and 3D modeling apps (Blender, VRoid Studio, etc.)
----
Blender Data-block:
* What are Data-blocks, users and fake users? https://docs.blender.org/manual/en/latest/files/data_blocks.html

Explanation: 
* The base unit for any Blender project is the data-block. Examples of data-blocks include: meshes, objects, materials, textures, node trees, scenes, texts, brushes, and even Workspaces. 
* When a data-block is referenced somewhere in the blend file, it is said to have one user. Every reference to that data-block adds another user to it. So for example, if a scene has two cube objects and both cubes are using one material, that material has two users.
* Data-blocks that have zero users get cleaned up (removed) when the blend file is closed. This means, for example, if there are any textures, materials, etc. with zero users, they will be removed when the blend file is closed. To make a data-block persist with zero users, add a Fake User (shield icon) for it.
----
