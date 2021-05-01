**Laying / Sitting Animation Prefab**

[Click here to download](https://github.com/Dervali-git/VRC-Tips/raw/main/Reasources/Laydown%20Animation-Action-v4%20-%20Choices%20-%20Nirvash.unitypackage)
_Note: These anmations are tuned for the Davali and soon Kitavali._
### Instructions
Set your Action layer to the included **ActionLayer_Laydown_Pose-Multiple**
Open your Parameters and add the following
| Name | Type | Default | Saved
|--|--|--|--
| SittingAnim | Int | 0 | No
| PoseSpace | Bool | Unchecked | Your choice

Open your Menu and add a Sub Menu pointing to the included **SubMenu_Laydown** in the folder "VRC Menu and Param"

![image](https://user-images.githubusercontent.com/68404726/116765013-ceaec880-a9e8-11eb-8187-37dad397e920.png)


The parameter 'PoseSpace' is used to optionally disabled the feature of adjusting your position to match the animation when it is set to True. This is included by a toggle on the included Laydown Menu


Included animations are:
 -  Lay down on back
 -  Idle   
 -  Sit Crossed Legs 
 -  Sit Legs forward 
 - Lay on Left Side
 - Lay on Right Side 
  - Sit Legs Down
  
  ![image](https://user-images.githubusercontent.com/68404726/116765040-e9813d00-a9e8-11eb-9149-9ab38c3f9f84.png)


### Credits
Animations are from mixamo.com you can find them by searching "Sit" or "Lay"
Icons from from VRC or icons8.com. Huge thanks to alexx1 for the hint on getting temp pose spaces working right and the inspiration to do more than just lay down.



