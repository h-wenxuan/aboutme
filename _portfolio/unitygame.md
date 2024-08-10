---
title: "Unity Game"
excerpt: "Developed a third person shooting game using Unity's AI navigation to control NPCs <br/><img src='/aboutme/images/start.png' style='width:300px; height:auto;'>"
collection: portfolio
---

My friend and I developed a third-person shooting game in Unity called "Saving the Prince", designed to immerse players in a dynamic battle against various monsters with the ultimate goal of rescuing the prince. We utilized various resources from the Unity Asset Store, such as the [Third Person Character Controller](https://assetstore.unity.com/packages/essentials/starter-assets-thirdperson-updates-in-new-charactercontroller-pa-196526) for players, NPCs, and enemies, and the [Sun Temple map](https://assetstore.unity.com/packages/3d/environments/sun-temple-115417) for the game's environment. We also sourced skins and animations from [Mixamo](https://www.mixamo.com/#/) for a smooth visual experience. To learn how to apply a variety of skins to the third-person character, I recommend watching this [YouTube video](https://www.youtube.com/watch?v=lPBdjwIr4Lk). Additionally, all the character behaviors in the game are implemented using C#, which we learned from this Unity project.

**Player Mechanics**

The player character is central to the game, designed with a focus on fluid movement for precise aiming. We employed a capsule collider to allow the players to interact with the environment, NPCs and enemies, triggering events and taking damage to make the game more risky and exciting for players. The game offers a distinctive third-person shooter experience by adding a Player Aim Camera, adjusting the shoulder offset, positioning the player to the left of the screen. This enhances the player's visibility and aiming precision and this [video](https://www.youtube.com/watch?v=FbM4CkqtOuA&t=1519s) explained the steps on how to achieve this perfectly.
![Player]({{ site.baseurl }}/images/player.png)

Two key scripts were also added to the PlayerArmature (Player's skeleton):
1. Third person shooter controller: Manages mouse sensitivity for both normal and aiming modes, as well as determining the bullet's spawn point and direction of travel
2. Player Stats: Tracks the player's total health, reflecting it on a health bar displayed at the top right corner and handles scene transitions when the player's health is depleted.

![health]({{ site.baseurl }}/images/health.png)

**NPC**

Like the player, NPCs has also been equipped with capsule colliders set to 'Is Trigger.' When a player's collider interacts with an NPC's collider, a text box is triggered, providing instructions for the game and immersing the player further into the story.
![NPC]({{ site.baseurl }}/images/NPC.png)

**Enemy**

The enemies in the game are powered by Unity's sophisticated AI, utilising [Unity’s NavMesh](https://www.youtube.com/watch?v=ieyHlYp5SLQ&t=97s) to navigate the game environment. After baking the NavMesh, it highlights the areas where enemies can move, ensuring they interact with the terrain realistically. The NavMesh Agent is then attached to each enemy to facilitates their movement, allowing them to patrol predefined points, chase the player, or disengage based on specific conditions.
![Enemy]({{ site.baseurl }}/images/enemy.png)

The Enemy Controller script is vital to enemy's behavior. It defines the patrol logic, chase conditions (distance between enemy and player), and when enemies should return to patrolling if the player moves out of range. This adds a layer of unpredictability and challenge, as players must avoid suffering too much damage before completing the task.
![Chase]({{ site.baseurl }}/images/Chase.png)

Additional scripts for the enemy include:
1. Enemy Damage: This script manages the interactions between the player and the enemy. When the player's collider comes into contact with the enemy's, the player takes damage, losing health. This makes close encounters with enemies risky and encourages players to strategize their movements and shooting the enemies.
2. Bullet Target: When the player successfully hits an enemy with a bullet, this script detects the collision and applies damage to the enemy, contributing to player progress.
3. Enemy Stats: This script tracks the enemy's health and dictates what happens when their health is depleted. It also manages scene transitions when the player completes their task, ensuring that the game remains smooth and satisfying.

![screens]({{ site.baseurl }}/images/screens.png)

**Other Functions**

To further immerse players in the world of "Saving the Prince," detailed animations and sound effects have been integrated:
1. Impact Animations: Different animations play depending on whether a bullet hits an enemy or a wall, enhancing the realism of the game.
2. Sound Effects: Custom sound effects for shooting and impact make combat more satisfying. These sounds also help to create an atmosphere of tension and excitement.

![hitanimation]({{ site.baseurl }}/images/hitanimation.png)

**Future Improvements**

While "Saving the Prince" already offers a compelling gameplay experience, there are a few areas for potential improvements:
1. Player Instructions: Implementing a tutorial or on-screen prompts could help players understand the controls better, such as how to zoom in by pressing the right mouse button or sprint by pressing Shift. This would make the game more accessible to new players.
2. Enemy Health Bars: Adding health bars to enemies could provide players with valuable information during combat, allowing them to gauge how much damage they have already inflicted and strategise accordingly.
3. Expanded NPC Interaction: Adding more complex interactions with NPCs, such as branching dialogue options or side quests, could enrich the narrative.
