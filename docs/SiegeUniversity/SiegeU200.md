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

### F

**Fades**: The act of making nodes visible or invisible is called "fading". Triggers that activate fading actions are usually called fade triggers. When a node is faded out (completely invisible), all objects associated with that node are also invisible.

**Frustum**: The "world frustum" is the area around a party member where the world is "loaded" and visible to the player. It is a box-like shape whose center is permanently focused on the active party member (or members, in the case of a multiplayer game). Any node or GO outside this area is "unloaded"--compressed down into a small data structure until it comes within the frustum. As the player moves, nodes and objects are "streamed" into the frustum and loaded. Any nodes or objects leaving the frustum are "streamed out" and unloaded. We generally cannot directly "talk to" a node or object outside the frustum (since it is in an unloaded state), but any messages sent to these nodes or objects are queued by the game's messaging system to be delivered when the node/object gets loaded again.

### G

**Game Object (GO)**: A GO, or more generally, "object", is nearly any mesh (3D object) in the game that isn't a node. Objects can be placed and moved on, above, or below nodes, and include things like actors, furnishings, gizmos, lights, etc. The generic term "object" is also used to talk specifically about meshes that don't have another more specific name (like actor or gizmo), such as trees, chairs, rocks, fences, etc. All GO's are defined by their "template". 

**Gas Files**: Essentially plain text files which are written in a specific format that the Siege Engine knows how to read and interpreted at run time. These files actually help define the game while the gaming engine knows how to make sense of all this data, how to properly display it, and how to allow the user to interact with it.

The types of data that are defined in Gas files vary widely. Gas files can define what a tree looks like, where a monster is placed in the world, how the world itself is built, what happens in the world, and even what the user interface looks like or what the default preferences for the game are. The engine then takes all this information and magically makes it all work when you run the game. 

&emsp;&emsp;&emsp;Hex numbers appear differently in Gas files than in the Siege Editor. When hex numbers are saved out to Gas files, they always appear with eight (8) digits, even if there are leading zeros. For example, numbers written as "0x4444, 0x12345678, 0xaa, 0x8" will appear in Gas files as "0x00004444, 0x12345678, 0x000000aa, 0x00000008", respectively. 

**Generator**: A Siege Editor gizmo that creates monsters once triggered. A generator creates monsters based on its settings, edited in SE. (Siege U: 100)

**Gizmo**: A logical Game Object placed and manipulated in SE. Gizmos are self-contained pieces of skrit or other functionality that accomplish specific actions in the game. Gizmos are connected or "wired" to many other objects, actors, and gizmos. Gizmos include things like AI commands, elevators, creature generators, sound and sfx emitters, light manipulators, and lots more. Much of the functionality of triggers will be in activating/deactivating gizmos. The trigger itself is a gizmo. Gizmos share the same identifiers as all objects: SCIDs and GOIDs. 

**GOID**: See Identifiers.

**GUID**: See Identifiers.

### I

**Identifiers**: All nodes and objects have recognizable template names that you use to identify them (like krug_scavenger), but SE needs to keep track of each unique "instance" of that node or object. For example, you may have 20 Krug Scavengers in your region, but each of those 20 instances has the same template name, krug_scavenger. Internally, the game engine assigns several of the following "identifiers" to make the instances unique. Each identifier is an eight-digit hexadecimal number, preceded by "0x", which looks like this: 0xe589a1ff. 

&emsp;&emsp;&emsp;**Global Unique Identifier (GUID)**: Each Node and Region is assigned a Node or Region GUID (pronounced "gwid") on creation. The GUID is a unique number per map (see the SE Manual for more info).

&emsp;&emsp;&emsp;**Static Content Identifier (SCID)**: A SCID (pronounced "skid") is a unique number assigned to every object placed in SE. SCIDs are used to reference almost every kind of object, including actors and gizmos. 

&emsp;&emsp;&emsp;**Global Object Identifier (GOID)**: Every object in the game is assigned a GOID by the game engine. They are different from SCIDs in that a SCID is used to connect objects in SE. GOIDs are used to reference and connect objects dynamically in the game engine. Sometimes an object doesn't have a SCID, like the starting player character or a monster spawned from a generator, but it always has a GOID. 

### L

**Level Of Detail For Items (LODFI)**: LODFI is both a way of removing objects from the world to reduce rendering time and an optimization for save game and multiplayer. LODFI is a pair of values in the [aspect] block of a template called lodfi_lower and lodfi_upper. 

For the purposes of rendering time, LODFI works to remove objects with LODFI values greater than 0 from the world so that they are not drawn. Objects whose LODFI is lower than the value represented by the in-game object detail bar, whose range is from 0.2 to 1.0, will be drawn. Objects whose LODFI is higher than this setting are not drawn. 

However, LODFI is used for many things even if the detail slider is not involved. For example, while a path-blocking bed in a farmhouse is considered "required" due to its blocking property and should never go away regardless of the slider, it should not be marked as -1. It should instead be marked as 0 so it's still considered a LODFI object but is always loaded. LODFI objects are not saved out in the save game (because their state cannot change) and they are not transmitted over the network in multiplayer. They do not show up in AI sensor queries and are considered 100% pure eye candy. They are specially permitted to block paths, and that's what the local-plain is meant for, but they're still considered a LODFI Object in the eyes of the save game system. 

From the perspective of the loader, objects can be broken down into three LODFI categories: 

&emsp;&emsp;&emsp;* Global: Objects with lodfi_upper < 0. Used for anything that is generally interactive, like monsters, doors, or openable chests. 
&emsp;&emsp;&emsp;* Local-LODFI: Objects that are client-side only and are used for decorations and have lodfi_upper >= 0. 
&emsp;&emsp;&emsp;* Local-plain: Special objects that are loaded locally but may have global effects. The server needs to load them for frustums outside its screen player's (usually reserved for blocking objects), and are set on the server if lodfi_upper == 0, it is a multiplayer session, and aspect:does_block_path = true.

As described in components.gas: 

`[lodfi_upper] { type = float; default = -1.0; constrain = range[ 0.0, 1.0 ];
	doc = "Upper bound for level of detail for items - will always render if 
	object detail level higher than this (set -1 for critical/global)"; }
[lodfi_lower] { type = float; default = -1.0; constrain = range[ 0.0, 1.0 ];
	doc = "Lower bound for level of detail for items - will not render at all 
	if object detail level lower than this"; }`

The numbers correspond to the object detail slider on the options menu, where the lowest detail setting was chosen to be 0.2 and the highest is 1. The upper/lower_lodfi settings in [aspect] define a range. If the object detail is lower than the range, it never loads, and if it's higher, then it always loads. If it's somewhere in the middle then there is a random chance it will load (this is good for shrubs). Here is the algorithm that the loader uses when deciding to load an object: 

&emsp;&emsp;&emsp;* If lodfi_upper <= 0 then load always 
&emsp;&emsp;&emsp;* If object detail level > lodfi_upper then load always 
&emsp;&emsp;&emsp;* If object detail level < lodfi_lower then never load 
&emsp;&emsp;&emsp;* Pick random number between lodfi_lower and lodfi_upper. If object detail level < this then don't load, otherwise load. 

Note again that we chose a minimum value for the object detail bar of 0.2, and not 0 as perhaps would be expected. 

### M

**Map**: The sum collection of all stitched regions. This is the entire "world". The map is not directly referenced within SE since you are already working on a region inside it. You cannot reference a region in a different map. 

**Messages**: Used to send events throughout the game. Messages are used to trigger the AI, activate gizmos, control animations, etc. Messages can be sent as "normal" or "delayed"; normal messages are processed immediately. Delayed messages can be sent to unloaded SCIDs (see Identifiers), which are queued until the objects are loaded. Data contained in messages includes the sender, the recipient, and optional data elements. 

**Mod**: A user-created modification of Dungeon Siege. Mods can be very simple (changing a texture on one weapon) to very complex (a entirely new story with new map and features). Also known as "Siegelet".

**Moods**: A block of settings that specifies the fog near and far distance, the fog color, the music and how often it repeats, the ambient track, the weather type and density, the wind speed and direction, the EAX settings, and even (in some cases) the size of the frustum. (Siege U: 204 - Moods)

### N

**Node**: The basic building block of terrain. Nodes are individual 3D tiles locked together to create the game world. Nodes can be individually selected, and are identified in SE by a Node GUID (see Identifiers). 

### O

**Object**: See Game Object.

### P

**Parameterized Content (pcontent)**: Randomly generated content, defined by a set of rules. For example, a chest can be loaded with a specific range of weapons to drop, instead of adding a specific template name. For further information, examine the compressed file components.gas. 

**Party Member**: Also considered an actor (and therefore a GO), a party member is the player's character or group of characters, including the packmule. The starting party member doesn't have a SCID, but all the party members that join him/her do since they start life as objects in SE. All party members have a GOID. 

**Properties**: Used to define components. For example, the Aspect component has a property called "scale_base" that defines the size of the object in game. 

### R

**Region**: A discrete "level" composed of nodes. SE loads individual regions for editing. Regions are "stitched" to each other so they appear seamless in game. Regions are identified in SE by a Region GUID, and must be assigned to a map.

### S

**SCID**: See Identifiers.

**Skrit**: A scripting language that can trigger and manipulate game events. Many gizmos are self-contained pieces of skrit. (Siege U: 303 - Skrit) 

**Siege Editor (SE)**: The Siege Editor is the primary tool used for constructing maps for Dungeon Siege. 

**Siege Max (SM)**: The Dungeon Siege game pack for gmax, from discreet. Siege Max allows the modification and creation of custom 3D models and animations that can be directly imported into Dungeon Siege. (Siege U: 214 - Siege Max: Characters, Siege U: 215 - Siege Max: Objects, Siege U: 216 - Siege Max: Terrain)

**Siege Objects**: Siege Objects are SE-specific objects that can be placed and manipulated within SE, but are never selectable within the game itself. Falling into this category are Starting Positions, Point Lights, Spot Lights, and Decals. Siege Objects are defined in the code and do not have templates at all. 

**Sound Effect Descriptor (SED)**: .GAS files that contain configurable information that affects the playback of a particular sound sample. An SED can control the playback rate of a sample, the maximum number of simultaneous instances of a sample that may be played, and the override falloff distance of a sample. (Siege U: 210 - Sounds)

**Special Effects**: Mainly particle effects. A particle in Dungeon Siege is a forward-facing, textured polygon, which can blend with other particles and other objects. Special effects run on two objects: a source and a target. Effects are most commonly visual, but certain effects can collide or cause damage. Also referred to as "Siege FX", "flamethrower", and "worldfx". (Siege U: 212 - SiegeFX)

**Stitch**: Region stitching is the process of joining two region boundaries so they are read into DS as if they were the same region.

### T

**Templates**: At the most basic level, a template tells the game engine how to use certain game resources - such as art, sound, and physics properties - to create (instantiate) a Game Object (rock, tree, sword, a Krug, etc.) in the world. A template is simply a block of text that defines the characteristics of a Game Object. (Siege U: 201 - Templates)

**Trigger**: A Siege Editor gizmo that makes something happen in the game when you want it to happen. To accomplish this, a trigger does two things: 

1. Tests to see whether certain conditions are true 
2. If true, executes certain actions. 

(Siege U: 203A - Triggers I, Siege U: 203B - Triggers II) 

### U

**User Interface (UI)**: The on-screen controls that a player uses to play Dungeon Siege. Sometimes referred to as "GUI", which stands for "Graphical User Interface" (as opposed to a text-based interface).

## 201: Templates

### Introduction

#### What You Need For This Tutorial

#### What This Tutorial Assumes You Have Already Learned

#### What This Tutorial Will Teach You

#### Untank Logic.dsres

### Show Me A Template!

### Template Structure

#### Components

#### Fields

#### Values

### Specialization

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
