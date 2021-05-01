**Texture Max Size in Unity**

Something to double check for textures in Unity is the Max Size value, which if incorrectly set can result in textures getting downscaled and loosing detail.

Select the texture image in Unity and in the inspector check the Max size value, it seems to default to 2048, which is often lower then some textures.  
_This will never upscale your texture, only downscale them. If you have 4k textures, but set it to 8k, your model will still have 4k textures._

![image](https://user-images.githubusercontent.com/68404726/116764130-95c12480-a9e5-11eb-843a-3116e45edbca.png)
