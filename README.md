[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/MjLLqDcN)
# HW1
## W1L2 In-Class Activity

Put your notes from the W1L2 (Thurs, Jan 9) in-class activity here.

Object: 
UI on the scene (Seeds planted and seeds remaining)
Actions: 
Numbers are updating throughout gameplay according to the seeds that the player plants
Attributes: 
Text

Object:
Player 
Actions:
WASD keys movement 
Plants a seed in the current position the player is standing in
Attributes: 
Sprite

Object:
Plants being planted onto the screen
Actions:
Several plants being planted any location in the scene when player presses space bar 
A single seed is planted one at a time  
Player can’t keep planting seeds once it runs out
Attributes: 
Sprite


## Devlog
Prompt: Include the HW1 break-down exercise you wrote during the Week 1 - Lecture 2 (Jan 9) in-class activity (above). If you did not attend and perform this activity, review the lecture slides and write your own plan for how you believe HW1 should be built. If your initially proposed plan turned out significantly different than the activity answers given by Prof Reid, you may want to note what was different. Then, write about how the plan you wrote in the break-down connects to the code you wrote. Cite specific class names and method names in the code and GameObjects in your Unity Scene.


Write your Devlog here!
The plan I wrote in the breakdown activity connects to the code in several ways. Structurally, I identified three main objects of the game: the player, the text UI, and the seeds being planted. Thus, the code includes a Player class and PlantCountUI class. Since I noted that the player affects the seeds being planted, the method PlantSeed() is inside the Player script and accesses the values related to the Player component. In Update(), my code implements the players movement in the Unity scene using if statements when the WASD keys are pressed and makes a call to the PlantSeed() method under an if statement to detect whether the spacebar was pressed in each frame. Inside the PlantSeed() method, my code references _numSeedsLeft from the Player class to put my code for the planting action under an if statement that checks if _numSeedsLeft is greater than 0. In my breakdown I noted that one of the actions that player has is that they cannot keep planting seeds when it runs out. As a result, when _numSeedsLeft is greater than zero and the player has seeds remaining, my code instantiates a single clone of the plant prefab in the main scene according to the player's position. When _numSeedsLeft becomes 0, the code does not run and no more seeds can be planted. Furthermore, I also identified that the UI text in the corner of the scene updates according to the number of seeds planted and remaining. Hence, to keep track of the number of seeds, in PlantSeeds(), I subtracted -1 from _numSeeds, which is the starting number of seeds the player has when the game begins setting that new value equal to _numSeedsLeft and added +1 to _numSeedsPlanted. I then displayed these updated values as UI on the screen by referencing to the UpdateSeeds() method from the PlantCountUI script. As for the visual representation of the objects I identified in my breakdown, the PlantCountUI script implements the UpdateSeeds() method to change the UI text in the scene based on the integer parameters passed through it and the player and plants are represented through sprites in the scene. 



## Open-Source Assets
If you added any other outside assets, list them here!
- [Sprout Lands sprite asset pack](https://cupnooble.itch.io/sprout-lands-asset-pack) - character and item sprites
