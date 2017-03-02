#Arroracing

## Team:
Jason Tang, Tim Clancy, Davin Hazard, Luke Carlson

https://drive.google.com/file/d/0B6BUWGkuVE_ob2hES25rQnNDaHc/view?usp=sharing

## Techniques used and why
For our game design, we chose to implement a simple environment in order to focus primarily on game logic and experience. A large component of our design is teleportation. We implemented this by tagging objects as being “Teleportable” and integrating this with first person projectile logic. To prevent motion sickness, we made the teleportation blocks stationary and added a pause between shooting the next site and teleporting there. 

## Motion sickness
We don’t really have motion sickness because there’s only two objects that are moving and we have fading in/out between teleportations.  The level is pretty flat so everything looks smooth. Originally we had the player standing on moving plates but changed the deisgn to reduce sickness.

## How to play
Hold the bow with the left hand.  Put right hand behind the shoulder to draw an arrow- pull the trigger for damage and push on the pad for teleport.  When the right hand is on the bow it'll vibrate until it's no longer pulling the arrow at a correct position or if the button is no longer pressed.  The longer the bow is dragged, the longer the arrow shoots.  
The objective is to race the opponent to the other side by teleporting across the pads.  You can slow your opponent by shooting the blocks in their path. When a block is shot, it is temporarily dropped. 
The first player to reach the end of their path wins and the game is reset to the lobby. 

## Hardest part
The hardest part is making the multiplayer section work well.

## What do we think we should’ve done differently
We changed our design dramatically after beta after given feedbacks.  It would be better if we did more for alpha or we changed our design earlier than a few days before the final product.

## What do we think you should’ve done differently
Beta is a great time for us to check out what works and what doesn’t, but the time between beta to the final isn’t enough.  Especially when we have great feedbacks in Beta, we want to put those into the game and then hear back feedbacks again.





## General Idea
Our general plan for this game is “arrow racing,” a unique take on archery combat. Players will need to hit a series of targets to progress across a track by teleporting, reaching checkpoints along the way. A secondary goal is stopping the opponent from finishing their own track by shooting arrows at them to reset their position to the previous checkpoint.

## Technical Requirements and Time Estimates
Arrow shooting seems like the most important task. Arrow shooting will involve two coordinated actions (pulling back the string and releasing) and calculation of arrow trajectories (2 days).
Multiplayer seems like the most difficult task to implement because it will require successfully replicating game state across multiple clients. While Unreal Engine provides useful tools such as RPCs to make this an easier process, we’re still left with some issues like how to draw the opponent when realistically they’re otherwise just floating hands (1 week).
Teleportation, Game Mechanics, VR UX will also be crucial aspects but seem like their difficulty will lie more on the design decisions side (making sure teleportation looks good, VR feels good, and game mechanics make sense) and the implementation will be less difficult (3 days).

## Division of Work
- Luke: teleportation, game mechanics, requirement 3, some arrows.
- Tim: multiplayer and map generation, some arrows.
- Jason: arrow shooting.
Realistically this division means almost nothing since we’re going to need to make so many initial prototypes of aspects in this game before being able to test anything. Also, good arrows will be very important.

## Schedule
Two people should work on the archery. How to shoot on things while the other two work on the general setting of the map and create objects for portal, checkpoint, goal and maybe wall in certain area.
Before alpha we join together to make sure teleportation works.
Two people then work on setting levels, multiplayer and UI display of scores etc. while the other two work on collision and teleportation.
At this point it would be beta and we’ll basically try to work on the game design after this point.  Make things prettier, arrows with effects, and even round-end upgrades.

## Mechanics and Style
We could try to incorporate powerups and stationary targets in the game in order to broaden gameplay.
For archery, we’ll have the left hand hold the bow and right hand hold the arrow. Config for lefties.
To wield different arrows (for shooting opponent vs teleporting) we draw from different quivers- the one on the right leg is teleporting and left leg is shooting at the opponent
Game mechanics: two players race through different teleportation portals on the map. They can either advance by shooting at the next teleportation portal to arrive there, or they can shoot the opponent to reset them back to the previous checkpoint. The first one to goal wins.
Each player has only 1 health- if a player gets hit, they respawn at the previous checkpoint. 
We’ll have different paths for different players.
We could have particle effects on the arrow to make trajectories easier to calibrate.
We can have some sort of a warning when opponent draws the attacking arrow.
