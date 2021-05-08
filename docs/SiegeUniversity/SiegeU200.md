# Siege University 200: Individual Study Topics

## 200: Concepts and Terminology

***

### A

**Action**: What a trigger does when its conditions are tested "true". Actions include the direct execution of a number of functions and the sending of **messages**. Messages are sent via the game's message delivery system to other objects in the game that are waiting for them, such as other triggers, gizmos, and actors. 

**Actor**: A Game Object with AI (artificial intelligence), but also includes the party. Actors include all monsters, ambient creatures, and NPCs; they also include other objects you wouldn't normally consider an actor, but have [actor] blocks in their template, like certain doors and chests. Actors that can be manipulated in SE have a SCID, but all actors (even ones that don't appear in SE, like the starting player character or monsters spawned from generators) have a GOID. 

**Artificial Intelligence (AI)**: Code that determines how an actor interacts with the world by scanning for objects/actors the actor can see. AI sends messages to its two subsections (brain and jobs) for interaction commands. 

&emsp;&emsp;&emsp;**Brain**: The higher level of AI. The Brain is responsible for high-level behavior and typically runs Jobs in response to stimuli. The Individual Brain (per actor) decides how to interact with objects/actors (i.e. attack, guard, flee). Every actor can be assigned a brain, even things not assigned intelligence in the real world, like trees, chests, furniture, etc. A Party Brain can be assigned to control group tactics, like healing friends, supporting friends, or moving and attacking in formation. 

&emsp;&emsp;&emsp;**Jobs**: The lower level of AI. Jobs are responsible for handling specific functions, using chores to accomplish those tasks. Jobs manage:

&emsp;&emsp;&emsp;* Movement: Following, moving in formation, guarding, moving 

&emsp;&emsp;&emsp;* Attacking: How to get there, what animations to use 

&emsp;&emsp;&emsp;* Item manipulation: Getting items, dropping, equipping 

&emsp;&emsp;&emsp;* Talking to other actors: Selecting the appropriate conversation, syncing dialog and animations, playing any special actions that occur as a result of the conversation 

&emsp;&emsp;&emsp;* Other actions: Using, drinking, going unconscious/conscious, special monster behaviors, fleeing, dying 


&emsp;&emsp;&emsp;**Chores**: Used by Jobs, but not a dedicated section of AI. Chores can also be used by objects through attached skrits or external gizmos. Chores are useful for controlling animations, including playing, blending, and modifying. 

### C

**Component**: Represents the code or skrit used to handle a certain aspect of a GO. For example, the mind component of an actor runs AI. Components are defined by the template(s) that a GO specializes. (Siege U: 201 - Templates) 

**Conditions**: A predetermined requirement or set of requirements that must be met before the trigger's actions will be executed. Conditions include testing whether a certain kind of object has entered, exists within, or has exited a specified area; whether the trigger has received a particular message from another object or the game itself; or both. (Siege U: 203A - Triggers I, Siege U: 203B - Triggers II)

### D

**Door**: A numbered line of polygons on a node, usually along an edge, used for connecting other nodes.

## 201: Templates

## 202: Lorebooks

## 203a: Triggers I

## 203b: Triggers II

## 204: Moods

## 205: Fades

## 206: Elevators

## 207: Non-Interactive Sequences (NIS)

## 208a: Non-Player Characters (NPC)

## 208b: Talk Skrits

## 209: Quests

## 210: Sounds

## 211: Naming Key

## 212: Siege FX

## 213: Dungeon Siege Resource System

## 214: Siege Max - Characters

## 215: Siege Max - Objects

## 215: Siege Max - Terrain

## 217: Actor and Party Commands