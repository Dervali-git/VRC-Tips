**This is the method I used for a custom idle prone in SDK3**

Copy the default locomotion "vrc_AvatarV3LocomotionLayer.controller" from VRCSDK\Examples3\Animation\Controllers and make a custom one
![image](https://user-images.githubusercontent.com/68404726/116763732-2860c400-a9e4-11eb-9b46-d4591b8aa994.png)  

In the Locomotion controller, go to prone and replace it with a custom version of VRCSDK\Examples3\Animation\BlendTrees\vrc_ProneLocomotion.asset
![image](https://user-images.githubusercontent.com/68404726/116763739-331b5900-a9e4-11eb-866e-7fc981bc39cd.png)


In that Blendtree replace the existing default prone with your custom one (You can also create a new state switch to not using a Blendtree, I did not simply to make it easy to swap back)
For a Laydown prone animation, see [here](Resources\Lay_Down.anim)
![image](https://user-images.githubusercontent.com/68404726/116763761-44646580-a9e4-11eb-856d-12719fb6b94d.png)

If you change the prone animation, I recommend adding a [not in fully body tracking] condition to the transition from standing to crouching.
In the Parameters tab of the Locomotion animator, add an int "TrackingType"
![image](https://user-images.githubusercontent.com/68404726/116763791-652cbb00-a9e4-11eb-98c2-35cc44fee944.png)
Then select the transitions going into Prone and add a condition for 'TrackingType' NotEqual '6' This makes it so the game does not attempt to enter this animation when in full body tracking.
![image](https://user-images.githubusercontent.com/68404726/116763886-bccb2680-a9e4-11eb-9409-c6cb42f65368.png)

