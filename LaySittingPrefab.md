## **Laying / Sitting Animation Prefab**
![image](https://github.com/Dervali-git/VRC-Tips/raw/main/Resources/Screenshots/LaySitBannerS.png)

**This is still a beta version that is not final**

[Click here to download](https://github.com/Dervali-git/VRC-Tips/releases/download/LaySit10/Laydown.Animation-Action-v10.-.Multi.-.Nirvash.unitypackage)  
_Note: These animations are tuned for the Davali. But can be used on most humanoid models. (Only matters for desktop really)_

### About
This is a set of animations and an animation controller used to add sit and laydown animations to SDK3 avatars for use by VRChat users not using Full Body Tracking. (Or hip tracking)     
Using these animations will lock your locomotion in place (you can no longer move using a thumb stick or keyboard) however you can still physically move in your placespace or by using OVR Advanced Settings playspace moving. (Although your feet are rooted in place)  For Desktop your head will be locked in place vertically when in laying animations, and your entire body will move when you turn your head in sitting animations.      
By default the animation will also adjust your position and view point to match, this can be disabled, see the notes on 'PoseSpace' parameter below.   

Included animations are:  
 - Lay down on back (1)
 - Lay on Left Side (2) 
 - Lay on Right Side (3)
 - Sit (51)
 - Sit Crossed Legs (52)
 - Sit Legs forward (53)
 - Sit Legs Down (54)
 - Lay on Left Side [VR only] (6) 
 - Lay on Right Side [VR only] (7) 
 - Sleeping Left [VR only] (4) 
 - Sleeping Right [VR only] (5) 
     
  ![LaydownRadial](https://user-images.githubusercontent.com/68404726/120073653-e799b080-c05e-11eb-8cb7-ba2844c6c150.png)

### Known Bugs
  * For some reason the 'Sleeping' animations have the legs pulled in too close to the body in FBT. They are set right in the animation, (and IK targets) but it just doesn't apply. If you have any idea the reason or a fix, let me know!    
  * Entering into a VR only pose in Desktop freezes you
  * The animator quickly does a pose when the avatar loads then goes to the idle state. For some reason after adding the blendtrees for the height adjustment, the first pose will cause you to be high up. This fixes that. 
  
### Changelog
  * V10 - **Parameter Updates!** 
    * Adds a Locomotion toggle on the second Menu page
	  * You can not enable locomotion for laydown poses in desktop, it simply breaks them.
    * Fixes trying to enter a VR only pose from another pose

   


### Instructions  
*Screenshots are below*  
Import the Unity Package you downloaded above. The contents should extract to 'Assets\Laydown'   

Then in the **Playerable Layers** drop down in the **VRC Avatar Descriptor** set your **Action** layer to the included **ActionLayer_Laydown_Pose-Multiple**   
     
Next in the **Expressions**  drop down, open your **Parameters** and add the following
| Name | Type | Default | Saved
|--|--|--|--
| SittingAnim | Int | 0 | No
| PoseSpace | Bool | Unchecked | Recommended
| PlaySpace | Float | 0 | Maybe?
| ResetPose | Bool | Unchecked | No
| Locomotion |  Bool | Unchecked | No

>If SittingAnim is saved and you were last sitting in the avatar, as soon as you load in you'd switch to sitting. This is unlikely to be the desired behavior, which is why you _should not save that parameter_.   
>  
> The parameter 'PoseSpace' is used to optionally disabled the feature of adjusting your position to match the animation when it is set to True. This is included by a toggle "Don't Move View" on the included More menu 
>
>PlaySpace is used for rasing the animation up. This is used by the "Height Adjust" radial puppet in the More menu.
>
>ResetPose resets your current view to match a change in PlaySpace. This is used by the "Reset View" button in the More menu.
>
>Locomotion is used to allow you to toggle your movement on and off
  
Open your **Menu** and add a Sub Menu pointing to the included **SubMenu_Laydown** in the folder 'Assets\Laydown\VRC Menu and Param'  

![image](https://user-images.githubusercontent.com/68404726/116765891-454dc500-a9ed-11eb-92ec-f3d5e92ee35a.png)

**That should be all you need to do to add this to your avatar! Feel free to reach out to me for suggestions or questions. Nirvash#0001**     



### Credits
Base animations are from mixamo.com you can find them by searching "Sit" or "Lay"     
Icons from from VRC or icons8.com.   
Huge thanks to alexx1 for the hint on getting temp pose spaces working right and the inspiration to do more than just lay down. Check out their customizable SDK3 avali in this world - [Louis Rossmann's Repair shop ](https://vrchat.com/home/world/wrld_d9c8c442-f69f-4b14-bf76-b9369853f702) (Yes that is the correct world)   
AlakaiDergal helped inspire the toggles for Locomotion



