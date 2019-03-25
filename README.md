
INDEX: 
Types of AI 
What each type test
                      Design Patterns           
Common themes: Archetypes 
                              
Scalability 
                     Finite State Machine 
                     Rule System 
                     Hierarchical Task Network
 
 
/TYPES OF AI

//General terms 
Agents
A game entity that tries to achieve a goal.

Algorithmic Agents
Code that provides intentional behaviour to agents (NPC’s, animals, enemies…).

AI Players
Agents that act as players (they mimic their behaviour) and usually are opponents.
(This can be used in a local game mode).

NPC’s
They can be agents.
Characters have a list of  individualized elements, such as a personality or the capability to evolve,

Enemies & CO vs Helpers & CO (companion, ally, friend, pet, minion…)

Vendors / Servicers: A part from letting the player buy items, they can serve as a narrative facilitator. They are placed in a recognizable location. 

More targeted AI
Mules
AI that takes over the player for a particular action or set of actions. 

Cheating AI: AI that adapts to the game circumstances. 
Example: The classic example  is the racing game where AI cars catch the player in an unbelievable manner. This is also an example of the Rubber Banding Effect. 

  Controllers 
Groups of agents that act as a whole. 

What they have in common: 
All this NPC’s can be QuestGivers, if they are narrative facilitators.
They also have to be perceived, thanks to: 1) location, 2) actions 3) their looks 
Examples: 
Location: 
Actions: 
Looks: 

IF I GOT TIME, ADD ANOTHER WAY TO CLASSIFY THEM (BEHAVIOUR-BASED) 


TODO 1: Identify all AI types in your game. 
Take into account:
1.1) Which AI can interact with which other AI? Esto no es muy básico o meh?
1.2) 
1.3) How will you make sure that each one is visible or accessible? 





What each tests

Design Patterns: 

NPC Design patterns are answers to the question: How do we, as developers, use our NPCs to generate interactions with the player?. 

Each pattern has got an objective, or test, and the most interesting patterns for RPG-like are: 

Adversary AI 
Enemy != Opponent. 
Enemy: a simple agent that attacks the player. In RPG’s it is common that they provide loot once killed. 
Agents of this type test the player’s combat ability. 
Example: a skeleton in a dungeon crawler. 
Opponent:
_ Does not have to directly interact with the player 
_ More complex behaviour 
_ “Faceless enemy” 
_ May have goals of his own
_ May have a relation with the narrative 
_ Wants to slow down the player’s progression 
Agents of this type test the player’s capacity to develop new strategies. 


Example: ? 
2) 


Role Model AI 
At the initial stages of a game there is a need to make the player understand a set of rules that the game hosts. Later on, a similar need appears when the player acquires a new weapon, or item, or when (s)he has to perform a certain task. 
Rather than using a lame classic tutorial, there exists the better option of using a NPC where it follows a certain behaviour to solve a situation. The player then mimics this behaviour.  

For instance, in stealth missions, an NPC can take the lead, and show the user how to go through a set of enemies, which encourages practical learning. 

Thus, agents of this type test the player’s ability to learn and quickly adapt to new or upcoming threats, as well as the situational awareness 


Editable AI 

Section credits to Julian Togelius (http://julian.togelius.com/).

Visualized AI 
Visualized AI refers to any hint given by the game of NPCs actions or behaviour. This can be done through 





To Avoid: 
“Metagaming” : when a player uses knowledge not in disposition of the character (s)he controls in order to succeed in the gameplay. 
>An example would be when you complete a level, and afterwards you go back with the purpose of grinding. Then, you, the player, already know where is every enemy, and how to defeat it, so it breaks the believability. 
>How to avoid it: as a developer you could perfectly: 
alter the location of (some) enemies every time the player re-enters the level, or even just 
swap the location of groups of enemies. 
This way, the game keeps the surprise factor (tension), with the character and the player at the same time. 

 
“Rubber Banding”: 






EXERCISE: 
1) Decide, in your game, which agents are going to be enemies and which opponents, if any.     
2) Are they going to be Cheating AI? To what extent? 
       

Themed enemy Groups

Thematic Consistency
Before learning how to generate proper themed enemy group, there must be a thematic consistency involving not only enemies, but including every game element, that needs to have mainly artistic and narrative commonalities with the others. 
In the case of enemies, though, this concept has to do rather with behaviour. For instance, when the player encounters a certain type of enemy, and after killing it, it drops certain loot, thus, the next time the player encounters it, (s)he will expect that the enemy-loot relationship is kept. 


Themed enemy Groups
Definition + structure: 
There are three concepts regarding enemy themes in video games: 

The first one corresponds to different variations of a single enemy. 
This enemy is neither a boss, nor a common enemy, but rather more similar to a mini-boss. 
Normally, it is a recurring enemy template, that appears in various phases of the game and that has a set of traits that persist throughout the different manifestations of itself. 
These enemies have a relation to the game’s lore and atmosphere, and can even be a part of it. 
> An example would be the trolls of God of War (...) 
                                        the Big Daddies of Bioshock (...) 
                                        the typical “elementals” in any game (fire, ice, etc) 
The second one corresponds to the summation of single common enemies that conform a group. 
Minions are commonly used in this approach. 
The third one corresponds to a combination of unequal enemies that, when put together, conform a recurring but interesting enemy structure that goes along well within a given gameplay context. 

IMPORTANT HERE ADD GROUP TYPES (encounter, etc) 



Behaviour Rules: 
Grouping / Formations: 

https://www.oreilly.com/library/view/ai-for-game/0596005555/ch04.html

The problem: 
Once a group of enemies is defined, the developer must decide how the group movement will be achieved. That is to say: 
Enemies are aware of other enemies in the group (coding here). 
Therefore, the enemy has a “field of view” which can vary in size, thus depending on how you want a certain group to behave, enemies within the group will have a larger or smaller F.OV. 



Types of formations: 
http://www.stat.columbia.edu/~jakulin/FT/#5
Wedge Formation: 


> This formation is useful because every enemy in the outside triangle can fire forwards without shooting to enemy allies, but the percentage reduces to a half when firing to the sides. 
At the same time, it is hard to penetrate to the inside of the formation. 
> Useful for long-range enemies. 


Diamond Formation: 


Specially useful for games with 8 directions as it cover the 4 flanks equally. 

Step / vertical Formation: 
Ideal to counter side attacks. 
Line Formation: 
Ideal to counter frontal attacks. 



Spawning: 
The “problem”: 
All these enemies have a level and a location in the map, but the wrong management of these variables can lead to an irritating gameplay: 
“Random Encounters”: games and sagas  such as Dragon Quest or Pokémon have a particular management of these enemies’ spawning: it is (almost) aleatory. 

Sometimes, these enemies are invisible (Pokémon) and in other cases the may be hard to avoid (Dragon Quest) because of the number of enemies wandering around without apparent purpose and that the fight triggers within a broad “triggering area”. 

In response of this, the developer may 
script larger themed enemy areas (The Witcher), with a strong enemy-environment relation, or they can either
use randomness to a certain point and only then it becomes scripted, or ...
use “In_Field enemies”: 
In-Field enemies are enemies that are marked with an icon / symbol in the map so as to give the player the chance to avoid them. Be aware of this technique drawback: letting the player avoid too many enemies, and make it impossible to avoid some of them. 

Art Cohesion: 



Interesting Attacks?? 
https://rpg.hamsterrepublic.com/ohrrpgce/Making_Complex_Attacks 



TODO: Design a themed enemy group for your game. 
Take into account: 
Define the basic group structure + thematic consistency (artistic traits???). 
Define the formation and spawning. 










 


Scalability 

The are two main definitions of scalability in video game terms: the first one is the art of balancing enemies and player stats when the gameplay progresses, and the other one is to expand the logic that handles a single NPC to the whole “NPC community”, which has to do with programming, and is laid out below:  

Finite State Machines 
vs
Rule Systems 
vs 
Hierarchical Task Networks 

Rule System vs Learning System: 
In video games, a Rule System refers to logic generated by the developer and used by the NPC’s with everything planned to succeed. 
That is to say, it is a static methodology. 
Rather than this, using a Learning System, like a Hierarchical Task Network, can help automate the process. 

Problem: state machines are great for individual NPC’s, but not enough to handle a complex AI structure with multiple game situations and decisions. 

Solution:   
Hierarchical Task Networks (HTS) are used in RPG’s, RTS and FPS.  They are a system to handle all the tasks developed by NPC’s in the game. on top of that, it promotes context-sensitive behaviour. 

Credits to Troy Humphreys  

Structure and WorkFlow:  
World State
The HTS has got a World State, that contains all the variables related to NPC’s actions, or “tasks”, which target a certain problem. 

Sensors
These tasks have an effect in the world and are tracked by sensors. This event is communicated to the World State thanks to the sensors. 

Tasks
Tasks have conditions that triggers them, and they also have operators, which are the meanings of the tasks translated in terms of HTS. 
Two different tasks can have the same operator: 

task 1 = 
task 2 = 
operator = 

These tasks can be primitive, like punching the player, or compound: 
Compound tasks involve different methods of solving them, and each one has each own conditions and subtasks. 

Domain
If we order all the NPC’s tasks according to its priorities, the result is the HTS domain, a task hierarchy panel. There is a root task, and then a series of tasks that can be achieved or failed, and the NPC moves on  the next one. 

Planner 
Quote >> The planner is triggered when: A) a task is completed or failed, B) a NPC does not have a task, or C) the NPC World State changes >> 

First, the planner goes through every possible task in a stack (let it be primitive or compound) and decomposes them to find out if the conditions in the World State allow the task to be executed. 







Then, the task is added to the plan in the form of primitive tasks operators that will be executed by the: 
Plan Runner. 
The plan runner executes all the tasks of a given plan. It also applies each task’s effect to the World State. 
If a condition of a plan is not valid, the plan is discarded and the planning process starts again. 






MAIN SCHEME 
(insert drawn scheme) 

How to approach the plan conditions in a Group of Enemies:  




This is an advanced example of conditions that trigger a plan: the group strength, the player direction and the distance to the player. This scheme is a simple ampliation of two conditions (player direction and position) proper of a single-enemy scheme, but with the added group strength. 



EXAMPLES: 








 












