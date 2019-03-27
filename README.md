“I am Marc Doctor, student of the Bachelor’s Degree in Video Games by UPC at [CITM](https://www.citm.upc.edu/ing/estudis/graus-videojocs/). This content is generated for the second year’s subject Project 2, under supervision of lecturer [Ricard Pillosu](https://www.linkedin.com/in/ricardpillosu/?originalSubdomain=es).”

# INTRO
The approach is this research is to let developers be able to recognize types of AI in their games, and then letting them know design solutions to structure them, while taking into account the interactions with the player. Lastly, there is a section to cover how AI is managed code-wise to extrapolate a single NPC behaviour to a whole NPC community. 

# Types of AI in RPGs 

## General terms 
**Agent**:
A game entity that tries to achieve a goal.

**Algorithmic Agents**: 
Code that provides intentional behaviour to agents (NPC’s, animals, enemies…).

**AI Players**: 
Agents that act as players (they mimic their behaviour) and usually are opponents.
(This can be used in a local game mode).

**NPCs**: 
They are agents that on top of that have a list of  individualized elements, such as a personality or the capability to evolve. 

**Vendors / Servicers**: A part from letting the player buy items, they can serve as a narrative facilitator. They are placed in a recognizable location. 

**Cheating AI**: AI that adapts to the game circumstances. 
Example: The classic example  is the racing game where AI cars catch the player in an unbelievable manner. This is also an example of the Rubber Banding Effect. 


## More targeted AI + distinctions: 
**Mules**
Two definitions: 

**1)** AI that takes over the player for a particular action or set of actions. 
An example would be if you have to craft any 
Another example would be in a terror game, when you have entered a safe zone, the AI can take  the control of the player movement momentarily. 

**2)**   AI with the mere purpose of transporting the player avatar items. 


### Helpers: Servicers vs Vendors
A servicer is distinguished from a vendor because the vendor only sells items, while the servicer does something for the player: repairing items, teleporting them to save points…
In a game, this two figures can either appear overlapped or separated. 

### Friends: Sidekick vs Ally vs Companion
**Sidekick**
A sidekick gives the player all sorts of help: item / enemy locations, resources… But it is not common that this agent enters combat to aid the player. 

**Ally**
The ally, in addition to the sidekick, also helps the player in combat. Moreover, whilst the sidekick may remain in a certain spot even if the player continues progressing, the ally does usually have the role of being part of an attack squad, or troop, being the exact opposite of the “enemy” type. 

**Companion**
What distinguishes companions from the two above types is that they can be controlled by the player. 
Furthermore, they are not plain as allies, but instead they contribute to the narrative. 

## Commonalities in all NPCs: 
**1)** All this NPCs can be **QuestGivers**, if they are narrative facilitators. The QuestGiver, though, they can appear as a **separate figure which only serves that purpose.**
Examples: 
In a Fallout game there is a great amount of common NPCs, and almost any of them can be a QuestGiver; it does not matter the occupation of this NPC in the world. 
In contrast, Bloodborne treats the QuestGiver normally as a lonely person separated from the rest, with his/her own attire and in a special atmosphere. Sometimes they are not even physically visible. 
 
**2)** They also have to be **perceived, thanks to: 1) location, 2) actions 3) their looks.**
Example: 
Vendors are placed in a building, indoors, whilst QuestGivers are located outdoors, and in a very clear landscape. 


**3)** They can be classified in the **“Act React Interact”** model: 

<img src=https://raw.githubusercontent.com/thedoctormarc/AI_RPG_Design/master/Images/actreactetc.PNG>

**Act:** NPCs that fall inside this category are programmed in an unidirectional manner: they only care about the player, and they have a very specific mission with almost no room for behaviour changes.  

**React:** Combat-related NPCs that follow a simple conduct pattern: perceive a stimulus, decide a plan, and react to it, in a hostile manner in the case of enemies.  Thus, the main difference is that they need to be almost constantly aware of the player’s actions, and, furthermore, of other enemies actions. 

**Interact:** This type of NPCs are prone to be the most accurate and elaborate in terms of human behaviour. In RPGs of higher complexity they make moral decisions on the go, though they behaviours instead can be scripted. 

**4)** In terms of believability and regarding the influence to the narrative, NPCs either have **embedded or emergent behaviours.**
**An embedded NPC** (or an embedded NPC community) holds a set of behaviour rules that remain unaltered by the player’s actions. 
**Emergent NPC** situations, though, involve the fact that NPC, can change their motivations, for instance change factions; let it be because of the player’s actions. 
An example would be Fallout 4 and the fact that depending on the character’s actions, at the end one faction can annihilate another one, or in another scenario this interaction does not even happen. 

[link](https://www.researchgate.net/publication/303496966_The_Non-Player_Character_Exploring_the_believability_of_NPC_presentation_and_behavior) 

# Uses of the different ypes 

## Design Patterns: 

NPC Design patterns are answers to the question: How do we, as developers, use our NPCs to generate interactions with the player?. 

Each pattern is a type of AI that has got an objective, or test, and the most interesting patterns for RPG-like are: 

### Adversary  
One must differenciate the Enemy with the Opponent. 

**Enemy:** a simple agent that attacks the player. In RPG’s it is common that they provide loot once killed. 
Agents of this type test the player’s combat ability. 
Example: a skeleton in a dungeon crawler. 

**Opponent:**
_ Does not have to directly interact with the player 
_ More complex behaviour 
_ “Faceless enemy” 
_ The subtype **“Manipulator”** has goals of his own
_ The subtype **“Manipulator”** may have a relation with the narrative 
_ **Wants to slow down the player’s progression** 
Agents of this type **test the player’s capacity to develop new strategies.** 


Example: 
The typical enemy that when the player is trying to solve a puzzle, it appears to frustrate them. 
Harpies in God of War can appear in that situation with that sole purpose. 
Donkey Kong used to throw barrels to prevent the player from advancing. 


### Role Model  
At the initial stages of a game there is a need to make the player understand a set of rules that the game hosts. Later on, a similar need appears when the player acquires a new weapon, or item, or when (s)he has to perform a certain task. 
Rather than using a lame classic tutorial, there exists the better option of using a NPC where it follows a certain behaviour to solve a situation. The player then mimics this behaviour.  

For instance, in stealth missions, an NPC can take the lead, and show the user how to go through a set of enemies, which encourages practical learning. 

Thus, agents of this type **test the player’s ability to learn and quickly adapt to new or upcoming threats, as well as the situational awareness**


### Editable 
Sometimes NPC are programmed and sealed at development time.
Nevertheless, there is the possibility to give the player the chance to alter the AI. 
Usually the player can only customize his items, weapons and stats. Using this concept, the player has also got access to the mentioned elements, but now the ones that belong to NPCs. 

This type of AI tests the player’s


### Visible
Visible AI refers to any hint given by the game of NPCs actions or behaviour. The most common uses are when the enemy positions are revealed to the player using an symbol in a minimap. A more advanced technique would be to reveal enemies’ traces or pathfinding routes. 
**This type of AI tests the player’s spatial awareness, reactions, and environment management.** 

[link](http://julian.togelius.com/Treanor2015AIBased.pdf)  



## A key aspect to avoid when thinking of NPC behaviour: 
**“Metagaming”:** when a player uses knowledge not in disposition of the character (s)he controls in order to succeed in the gameplay. 
An example would be when you complete a level, and afterwards you go back with the purpose of grinding. Then, you, the player, already know where is every enemy, and how to defeat it, so it breaks the believability. 
**How to avoid it:** as a developer you could perfectly: 
alter the location of (some) enemies every time the player re-enters the level, or even just 
swap the location of groups of enemies. 
This way, the game keeps the surprise factor (tension), with the character and the player at the same time. 

 
# Themed enemy Groups

## Thematic Consistency
Before learning how to generate proper themed enemy group, there must be a thematic consistency involving not only enemies, but including every game element, that needs to have mainly artistic and narrative commonalities with the others. 
In the case of enemies, though, this concept has to do rather with **behaviour**. For instance, when the player encounters a certain type of enemy, and after killing it, it drops certain loot, thus, the next time the player encounters it, (s)he will expect that the enemy-loot relationship is kept. 


## Themed enemy Groups
Definition + structure: 
There are three possibilities regarding enemy themes in video games: 

1) **The first one** corresponds to different variations of a single enemy. 
This enemy is neither a boss, nor a common enemy, but rather more similar to a mini-boss. 
Normally, it is a recurring enemy template, that **appears in various phases of the game** and that has a set of **traits** that persist throughout the different manifestations of itself. 
These enemies have a relation to the game’s lore and atmosphere, and can even be a part of it. 

Examples would be the trolls of God of War, 
                                        the Big Daddies of Bioshock, (...) 
                                        the typical “elementals” in any game (fire, ice, etc)... 

A **difference with a common miniboss** is that the miniboss may not be a **recurring enemy**. Furthermore, they sometimes have a relationship between themselves that, only when the player kills all of them, (s)he is rewarded or/and discovers a narrative secret. 

2) **The second one** corresponds to the summation of single common enemies that conform a group. 

A typical model is the **patrol**. This enemy group goes from point A to point B repeatedly, unless the player comes nearby. 

3) **The third one corresponds** to a combination of unequal enemies that, when put together, conform a recurring but interesting enemy structure that goes along well within a given gameplay context. 

A common scheme is the **encounter**: a tank, or big enemy, surrounded by weaker enemies. This type of tanks uses these enemies as protection, but it can be the other way around, so that the tank is an HP absorver, and distracts the player while the weaker enemies are the ones to finish him. 


## Behaviour Rules: 
## Grouping / Formations: 

### The problem: 
Once a group of enemies is defined, the developer must decide how the group movement will be achieved. That is to say: 
Enemies are **aware of other enemies in the group**. 
Therefore, the enemy has a **“field of view”**, which can be represented as an area around them, which can vary in size, thus depending on how you want a certain group to behave, enemies within the group will have a larger or smaller F.OV. 
<img src=https://raw.githubusercontent.com/thedoctormarc/AI_RPG_Design/master/Images/flocking.jpg>


## Types of formations: 
Depending of how many enemies are within a single group, the FOV will increase / decrease. In addition, certain formations are more prone to be used with enemies of different behaviours. 

**Wedge Formation:** 

<img src=https://raw.githubusercontent.com/thedoctormarc/AI_RPG_Design/master/Images/wedge.gif>
This formation is useful because every enemy in the outside triangle can fire forwards without shooting to enemy allies, but the percentage reduces to a half when firing to the sides. 
At the same time, it is hard to penetrate to the inside of the formation. 
Useful for long-range enemies. 


**Diamond Formation:** 

<img src=https://raw.githubusercontent.com/thedoctormarc/AI_RPG_Design/master/Images/diamond_formation.png>
Specially useful for games with 8 directions as it cover the 4 flanks equally. 

**Column Formation:** 
Ideal to counter side attacks. 

**Line Formation:** 
Ideal to counter frontal attacks. 

<img src=https://raw.githubusercontent.com/thedoctormarc/AI_RPG_Design/master/Images/column_and_line.gif>


## Spawning
### The “problem”
All these enemies have a level and a location in the map, but the wrong management of these variables can lead to an irritating gameplay: 

**“Random Encounters”:** games and sagas  such as Dragon Quest or Pokémon have a particular management of these enemies’ spawning: it is (almost) aleatory. 

Sometimes, these enemies are invisible (Pokémon) and in other cases the may be hard to avoid (Dragon Quest) because of the number of enemies wandering around without apparent purpose and that the fight triggers within a broad “triggering area”. 

In response of this, the developer may 

**1)** script larger themed enemy areas (The Witcher), with a strong enemy-environment relation, or they can either

**2)** use randomness to a certain point and only then it becomes scripted, or ...

**3)** use “In_Field enemies”: 

**In-Field enemies** are enemies that are marked with an icon / symbol in the map so as to give the player the chance to avoid them. Be aware of this technique drawback: letting the player avoid too many enemies, and make it impossible to avoid some of them. 

## Common Attacks 
### Waves 
These enemies can attack in the form of waves, meaning that the whole group attacks the player at the same time. The two main variants are: 

**1)** The long range group, that attacks while keeping the formation and position.

**2)** The melee group goes towards the player while keeping the formation. Once it gets to the player, it can A) still maintain the formation, or B) surround the player, 

### Hit and Run 
Hit and Run is the common attack pattern in RTS. Anyways, a RPG can still have groups with Hit and Run behaviours. 


# Scalability 

The are two main definitions of scalability in video game terms: the first one is the art of balancing enemies and player stats when the gameplay progresses, and the other one is to expand the logic that handles a single NPC to the whole “NPC community”, which has to do with programming, and is laid out below.   

## Finite State Machines vs Rule Systems vs Hierarchical Task Networks 

### Rule System vs Learning System: 
In video games, a Rule System refers to logic generated by the developer and used by the NPC’s with everything planned to succeed. 
That is to say, it is a static methodology. 
Rather than this, using a Learning System, like a Hierarchical Task Network, can help automate the process. 

**Problem:** state machines are great for individual NPC’s, but not enough to handle a complex AI structure with multiple game situations and decisions. 

**Solution:**
## Hierarchical Task Networks 
Hierarchical Task Networks (HTS) are used in RPG’s, RTS and FPS.  They are a system to handle all the tasks developed by NPC’s in the game. on top of that, it promotes context-sensitive behaviour. 



### Structure and WorkFlow:  
**World State**
The HTS has got a World State, that contains all the variables related to NPC’s actions, or “tasks”, which target a certain problem. 

**Sensors**
These tasks have an effect in the world and are tracked by sensors. This event is communicated to the World State thanks to the sensors. 

**Tasks**
Tasks have conditions that triggers them, and they also have operators, which are the meanings of the tasks translated in terms of HTS. 
Two different tasks can have the same operator: 

task 1 = 
task 2 = 
operator = 

These tasks can be **primitive**, like punching the player, or **compound**: 
Compound tasks involve different methods of solving them, and each one has each own conditions and subtasks. 

**Domain**
If we order all the NPC’s tasks according to its priorities, the result is the HTS domain, a task hierarchy panel. There is a root task, and then a series of tasks that can be achieved or failed, and the NPC moves on  the next one. 

**Planner** 
> The planner is triggered when: A) a task is completed or failed, B) a NPC does not have a task, or C) the NPC World State changes  

First, the planner goes through every possible task in a stack (let it be primitive or compound) and decomposes them to find out if the conditions in the World State allow the task to be executed. 
Then, the task is added to the plan in the form of primitive tasks operators that will be executed by the: 

**Plan Runner** 
The plan runner executes all the tasks of a given plan. It also applies each task’s effect to the World State. 
If a condition of a plan is not valid, the plan is discarded and the planning process starts again. 

[link](http://www.gameaipro.com/GameAIPro/GameAIPro_Chapter12_Exploring_HTN_Planners_through_Example.pdf) 



<img src=https://raw.githubusercontent.com/thedoctormarc/AI_RPG_Design/master/Images/htn_scheme.PNG>


### How to approach the plan conditions in a Group of Enemies:  


<img src=https://github.com/thedoctormarc/AI_RPG_Design/blob/master/Images/Example_Behaviour.PNG>

This is an advanced example of conditions that trigger a plan: the group strength, the player direction and the distance to the player. This scheme is a simple ampliation of two conditions (player direction and position) proper of a single-enemy scheme, but with the added group strength. 

**Group Strength:**

<img src=https://raw.githubusercontent.com/thedoctormarc/AI_RPG_Design/master/Images/group_Strenght.PNG>

# References 

[AI Players](http://virt10.itu.chalmers.se/index.php/AI_Players)

[Algorithmic Agents](http://virt10.itu.chalmers.se/index.php/Algorithmic_Agents)

[Agents](http://virt10.itu.chalmers.se/index.php/Agents) 

[Thematic Consistency](http://virt10.itu.chalmers.se/index.php/Thematic_Consistency) 

[HTN](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.103.4477&rep=rep1&type=pdf)

[Behaviour and Design](http://www.diva-portal.org/smash/get/diva2:561201/FULLTEXT01.pdf)

[HTN](http://www.gameaipro.com/GameAIPro/GameAIPro_Chapter12_Exploring_HTN_Planners_through_Example.pdf) 

[Group Code Behaviour](https://pdfs.semanticscholar.org/2661/4b67383dbd30299aa3336f17f58afcb3f3f5.pdf)

[Themed enemy groups](https://michaelripplinger.com/2018/11/21/whats-an-rpg-without-a-themed-enemy-group/) 

[Random Encounters](https://www.giantbomb.com/random-encounter/3015-123/)

[Unit FOV](https://www.oreilly.com/library/view/ai-for-game/0596005555/ch04.html) 

[Rule vs Learning System](https://www.tricentis.com/artificial-intelligence-software-testing/ai-approaches-rule-based-testing-vs-learning/)












 












