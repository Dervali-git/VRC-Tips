**Anchor Overrides and why you NEED to set them**

In order for Unity to apply lighting to your avatar it needs to know which light probe to use for the overall brightness of each mesh comprising your avatar. This tends to be the tail by default on avali bodies because it is the furthest part of the mesh. However each mesh will have it's own source for brightness unless you manually configure one by setting an Anchor Override. 

This __will__ result in strange lighting where parts of your body appear brighter/darker then others. Or where your lighting doesn't match the scene because your tail is clipping through the floor or wall and picking up a light probe from outside the map. 

Luckily it is EASY to set Anchor Overrides! For _every_ Mesh on your avatar, in the 'Skinned Mesh Renderer' component, find the 'Anchor Override' option and set it to your 'Chest' bone. 
Why Chest? Because it is center mass to the avatar and should provide a good overall light sample.

This is the default Davali in this example so I need to set the Anchor Override for _both_ the 'Body' and 'ChestFluff' meshes. You want all the Anchor Overrides to be the same transform, in this case 'Chest' to ensure consistent lighting.
![image](https://user-images.githubusercontent.com/68404726/116763496-3235f780-a9e3-11eb-8878-d81a4a5cd6d6.png)
![image](https://user-images.githubusercontent.com/68404726/116763508-3bbf5f80-a9e3-11eb-8060-b921f3845caa.png)
