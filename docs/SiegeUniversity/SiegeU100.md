# Siege University 100: Basic Studies

# The Basics of the Siege Editor

## Introduction

Building a region for Dungeon Siege using the Siege Editor ("SE") is a straightforward task, even for a beginning mod maker. This Siege U tutorial has two purposes: familiarization with the Siege Editor and familiarization with Siege University. At the conclusion of this tutorial, you will be familar with basic SE functionality and will possess an understanding of how Siege U works.

This tutorial will walk you through building a simple, small region. It will not delve into all the options of each section, nor will it offer much more than a cursory explanation of the motives of building a region. These topics are covered in further detail in the Siege Editor Manual (included during the installation of the Siege Editor) and further, more specific Siege U tutorials.

### What You Need For This Tutorial

* Dungeon Siege, updated to version 1.09B or later 
* Siege Editor, with the Preferences configured to Appendix B 
* Siege Editor Manual (included with the Siege Editor during installation) 
* [Siege U 100 companion map](/assets/siegeu/100/CGMTutorial.zip)

### What This Tutorial Assumes You Have Already Learned

* Nothing

### What This Tutorial Will Teach You

* Basic familiarization with SE 
* Node Placement 
* Object Placement 
* Lighting 
* Fading 
* Moods 
* Monster Placement 
* Tanking/untanking maps for play in Dungeon Siege 

### Opening An Example

The best way to start is to first take a look at a sample map before beginning this Tutorial. Download the [Siege U 100 companion map](/assets/siegeu/100/CGMTutorial.zip) and extract it according to the DSReadme.rtf included with it.

Once you have the companion map installed on your computer, you will need to "untank" it. When working on a map in SE, you are working on the "bits"; that is, the changes you make are stored in different files in different locations (all within My Documents\Dungeon Siege\Bits). However, for performance reasons and size constraints, these files are compressed into a single "tank" file for use within Dungeon Siege.

Any time that you want to work on a map in SE, you need to edit the bits.
Any time that you want to open a map in DS, you need to "tank the bits" and create a .dsmap file for DS to use. 

Fortunately, most of the conversion work is only one-way -- from SE to DS. That is, once you have started working on bits, you only need to tank when you are ready to test your regions. Once you have tested them and are ready to continue editing, you do not need to untank the map; you can just continue editing the same bits. The only time that you need to untank a map is when you do not already have the current bits on your computer (which would happen if you download a new map).

To untank the companion map into its editable format, follow these steps:

1. Start the Siege Editor. 
2. Select Convert .dsmap to Files... from the File Menu. 
3. For the Source File, browse to where you installed Tutorial.dsmap (the default is the Maps folder in the Dungeon Siege game directory).
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/1_100.png">
4. For the Destination Folder, leave it at its default setting (My Documents\Dungeon Siege\Bits) 
5. Click OK to start the process.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/2_100.png">
6. Once the conversion process is complete, you will see the results with a success message.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/3_100.png">
7. Select Open... from the File Menu. 
8. Expand the gpg_cgm map on the Load Region dialog, and select the region named tutorial. 
9. Click OK.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/4_100.png">

### Basic Movement Controls Within SE

 All actions and movement in SE are controlled with the mouse. Please note that a three-button, scroll-wheel mouse is required for the Siege Editor to function properly with it's default key settings.

* To move around a map, right click and hold, then move the mouse in the desired direction. 
* To zoom, scroll the mouse wheel. 
* To move vertically, hold down shift while right clicking and moving the mouse, or hold down both the left and right mouse buttons while moving the mouse. 
* To rotate the region, click and hold the middle mouse button, then move the mouse. 

Now that you have seen the end result, let us walk through building a copy of this region together. The region you build does not have to match the example identically, so don't worry about switching back and forth to compare regions.

## 101: Nodework

Assembling terrain is the most important aspect of designing regions for Dungeon Siege. By snapping together some of our 3,800 different nodes, you can create almost any type of environment imaginable -- from vast, rolling plains, to the deepest vertical dungeons, and everything in between.

### Create A Map

1. Choose New Map from the File Menu. [default hotkey = Ctrl+M] 
2. Enter a name for the map. This name will not be visible within Dungeon Siege and cannot contain any spaces and must be in lowercase. For example, my_world.
3. Enter a screen name. This is the name of the map you will see within Dungeon Siege. For example, My World. 
4. Enter a description of the map. For example, This is my SU 100 map. 
5. Leave everything in the Advanced section as is.
6. Click OK.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/1_101.png">

### Create A Region

1. Choose New Region from the File Menu. [default hotkey = Ctrl+N] 
2. From the drop down under Select Map to Create Region, choose the map you just created.
3. Enter a name into the Region Name box. For example, my_house.
4. In the Advanced section, click on the Default buttons for both Scid Range and Region ID. The Scid Range and Region ID settings must be unique for all regions in the map. Accepting the defaults ensures that no numbers will be duplicated in the map.
5. Select the Target Node (starting node) you will build the world around:
  * Expand the grass_1 directory and scroll down to the houses folder.
  * Expand the houses directory and select the node "t_grs01_houses_generic-b-log.sno.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/2_101.png">
6. Click *OK*.
7. Click on the floppy disk icon in the upper left toolbar to bring up the Save dialogue. Make sure all options are checked and click Save. [default hotkey = Ctrl+S]
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/3_101.png">
8. Your region will now look like a house sitting in black space.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/4_101.png">

### Add Floors And Walls

1. Click on the Custom View tab at the bottom found at the lower left side of SE.
2. Expand the tree to CGM_Afterlife_Tutorial/Nodes.
3. Select "t_xxx_flr_08x08-v0.sno" (floor node).
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/5_101.png">
4. Click on the house node and use the Source Doors: arrow buttons located at the lower left side of the editor to rotate through the node’s doors until you get to Door 1. You will see a red line on the door in the Main Window, with an arrow pointing away from the node. [default hotkeys = a, d]
5. Use the Destination Doors: buttons to rotate the floor node (t_xxx_flr_08x08-v0.sno) so Door 6 of the floor node is connected to Door 1 of the house node. [default hotkey = w]
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/6_101.png">
6. Select the floor node you just added and rotate through its doors until Door 3 is highlighted.
7. With "t_xxx_flr_08x08-v0.sno" still selected in the Custom View panel, click Attach Node to add another floor node so Door 6 of the new node is connected.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/6_101.png">
8. Snap more floor nodes around the house node by rotating to unconnected doors and adding nodes as described above. Be careful not to overlap one node over another. Node doors can only connect to one other door, so if you overlap nodes, your region will not connect correctly and has the potential to crash or display strange behavior.
9. Save after placing every few nodes. When you save, it also connects all node doors that are adjacent to other nodes. Important note: After the target node has been placed (which is the house in this tutorial), all new nodes must connect to other nodes. If deleting a node cuts off several nodes from the target node, they will automatically be deleted. To avoid deleting an entire string of nodes, never delete a node unless you have just saved.
10. You should now have a house in the center of a grassy area.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/7_101.png">
11. Add a field to the right side of the house. Select "t_grs01_field-rows-corner-b.sno." 
12. Rotate the field-row corner so Door 2 connects to the terrain and the textures match up. 
13. Continue adding field-row nodes, using all of the variations in the folder. Create a field that is three field-row nodes wide and six field-row nodes long. 
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/7_101.png">
14. Add a Chicken Coop and Well. First select "t_grs01_houses_coop-a.sno" and add it next to one of the field-row edge nodes, then select "t_xxx_flr_well-a.sno" and add it to the other side of the grassy terrain. 
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/8_101.png">
15. Continue building out the grassy terrain around the house, field, and coop using the available floor node variations. 
16. Add rock cliffs around your farm to make it into a valley. Choose from any of the wall ("wal") type nodes (ex: t_xxx_wal-12-thck) and add them to the edges of the region so Doors 1 and 2 always connect to the ground level. 
17. Use the corner ("cnr") type nodes to change Wall direction by snapping them to unconnected wall sides.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/9_101.png">
Save

At first glance, the generic node naming conventions might seem a bit unintelligible. However, they actually can be decoded into useful information. With any node set, there are at least five different subsets separated by underscores that make up each node's name. Let's look at the name of the generic node "t_xxx_cnr_12-ccav.SNO," found in Terrain Nodes/Generic/Corner. The first part of the name, "t," refers to "terrain." The second part of the name is the set identifier. For example, "xxx" indicates the node is part of the generic set and has a swappable texture. (A swappable textures means that you can select a node, and then go to Node | Current Node Set to change the texture of the node to a different texture set.) If this part was something different, such as grs01, it would tell us that the node belongs to the Grass_1 set and has a grassy-looking texture. Following the set identifier, is the node type. For example, there are fifteen different node types that make up the Generic set, plus water versions for all of them. "Cnr" tells us that it's a Corner type node. If it was something else, for example, "for," we would know that it's a Forest type node, and so on. Usually, the next part of the name refers to the node's size (for nodes that have multiple sizes). "12" means that this node is 12 meters high, so any nodes we want to connect to it must also have a "12" somewhere in their name. 

At this point, the basic properties of the node have been identified, and all further information defines variation. "-ccav" means this node has an inward curve, or is concave. If it was "-cnvx," then the node would have an outward curve (convex). Both corner types allow you to turn a wall ninety degrees. The ".SNO" is the filename extension, and means "Siege Node."

## 102: Objects

### Add Details To House

Populating your world with objects is fast and easy. Within Siege Editor, an object is any model that is not terrain. This part of the tutorial will deal with "non-interactive objects", which are decorative objects that do not contain AI or animation components, and cannot be selected by the player in-game. Objects, in general, are far more flexible than terrain. They can be scaled, rotated, and placed with great precision. The key to good object placement is using enough to make an area appear lush and realistic, while minimizing the amount of different objects used, so performance remains reasonable. 

Before you can add and move objects, you must be in the correct mode. Under the Object Menu, look at the options under Mode. "Placement Mode" must be checked to add an object to your region. "Movement Mode" must be checked to move an object within your region. Placement Mode has a button that appears on the Object Toolbar, since you will only want to be in Placement Mode when you are ready to add an object. If you remain in Placement Mode all the time, you will add objects when you try to simple click-select an existing object.

<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/0_102.png">

1. Rotate the view until you are looking straight down into the house. 
2. Expand "cgm_afterlife_tutorial/objects/house". 
3. Select "rug_round_blue." 
4. Click on the center of the house floor to place the rug. 
5. To move the rug after it is placed, click on the rug to select it (a green selection box will appear around the rug when it is selected) and move it to the center of the house by dragging the mouse.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/1_102.png">
6. Continue placing objects in the house using the method above. Use each of the house objects in the Custom View window to furnish the house. 
7. To rotate objects, select an object and choose Properties from the Object Menu and click the "Rotation" tab in the Object Properties window. Rotate the "Yaw (Y):" control to spin it about the Y-axis.
Note: The Properties window can be resized and moved. If it covers the object that you are trying to rotate, resize and move it so that you can see the object as you rotate it.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/1b_102.png">
8. Place a candle on a windowsill.
  * Select "candle_short" from the Custom View panel and place it on the floor near a window.
  * To place the candle on the sill, look under the Object Menu and uncheck Object-->Mode-->Auto Snap to Ground. Click the candle to select it (you are out of Placement Mode, right?), then click and hold the left mouse button over it, then press and hold the Shift key. Holding the Shift key allows you to only change the vertical position of an object. Raise the candle up to the level of the windowsill. You can release the shift key while holding the mouse button to move the candle horizontally. Try to position the candle so that the bottom of its green selection box just disappears into the sill. Don't worry if the light source on the candle remains at floor level -- we'll covering lighting later on. 
9. Note that some objects (like the rug) will not block the player's movement in the game, while others (the bed) will block the player. You can find out if an object is "blocking" or "non-blocking" by viewing its Properties. Look for the value marked "does_block_path" under the "Template Properties" tab.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/1c_102.png">

### Add Details To Surrounding Farmland

1. Add a crop to your farm in front of the house.
  * When working with foliage, you can easily randomize the size and orientation of the objects as you place them by using the "Next Object" function. Select Next Object… from the Object Menu. On the Next Object Placement Settings window check the Random Orientation/Yaw (Y) and Scale/Random Scale boxes. Set Minimum Multiplier to "0.65" and Maximum Multiplier to "1.1." Click "OK". Now each time you place an object, Siege Edit will randomly vary its scale from 0.65 to 1.1 times normal size, as well as randomly vary its rotation. 
  <img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/2_102.png">
  * Select "grs_cabbage" from the foliage directory and click on the field area to add your crop, varying the rows to give them a realistic look. Placing foliage, trees and other plants "too neatly" almost always looks artificial. 
2. Add a forest around your house.
  * Select "grs_bush_rhod_sm." Add clumps of six to eight rhododendrons around the valley, as well as a few bushes around the corners of the house, the back of the chicken coop and some at the base of the canyon wall. Create two clumps behind and on either side of the well.
  * Select "grs_flr_aster_blue" and add them around the outskirts of the rhododendron patches here and there and around the well and house.
  * Select "grs_pine_9m_sway" and add them on top of the rhododendron clumps. The trees should look as if they are growing out of the rhododendron undergrowth. This will help blend the trees into the terrain, giving a much more natural appearance. Space the trees so they touch a bit, but without too much overlap. Add in some "grs_aspen_red_lg_sway_grassy" in the same way for variety. 

### Add Starting Positions

1. Select the Starting Positions Gizmo from the gizmos folder and place seven of them in front of the house. Move the original starting position that was automatically created with the house node to be grouped with the others. These define the location where your heroes will enter when the map is loaded.
2. Save.

## 103: Lighting

Lighting a region well can make a decent environment something spectacular. Lighting can range from subtle tones to full-on vibrant color, depending on the mood you want to set. A well-lit level makes an area feel believable to the player – for example, every light object in the world (i.e. - a candle) has an obvious lightsource (i.e. - the glow and flicker of its flame).

The following steps will explain how to set ambient light for your region, how to create sunlight using directional lights, and how to place and modify point lights. Before we start, let's make sure you can see lighting changes. Under Preferences (View Menu), ensure that "Ignore Vertex Color" (under "Rendering") is not checked. 

<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/0_103.png">

### Ambient Light

Set the general brightness of your region's terrain, objects, and actors by adding region-wide ambient light: 

1. In the Lighting Menu, select Ambient Lighting to bring up the Region Ambient Light Settings window. 
2. In the Ambient Intensity portion, select the value box labeled General: and enter a value of "0.2" (the "General" setting will affect terrain). Repeat this for Object: with a value of "0.2" (affects objects), and Actor: with a value of "0.25" (affects actors). 
3. View your changes by clicking the Update button. Your region will get very dark - don't panic! We haven't added the sunlight in yet. 
4. Click *OK*.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/1_103.png">

### Directional Lights

Create sunlight for your region by adding directional lights:

1. In the Lighting Menu, select Edit Directional Lights. 
2. In the Edit Directional Lights window, click the New button. A number, representing the ID of a new directional light, will appear in the small box to the left of the button. Select this number, and click the Edit button. This will open the Directional Light Properties window. 
3. Create sunlight for your region. Select the Lighting tab. In the Direction section, enter a value of 2.0 in the "X:" box. 
4. In the "Options" section of the window, make sure all boxes are checked. Note that selecting "On Timer" will make the light change its color and intensity in game based on time of day. Click OK. 
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/2_103.png">
5. Create lighting to realistically illuminate shadows in your region. Add a second directional light and click Edit.  Under Color in the Color Values portion of the window, make the light a shade of blue by entering in the values 0.5 for Red:, 0.55 for Green:, and 0.98 for Blue:. Click Apply, and then click the Lighting tab to continue configuring the light. 
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/3_103.png">
6. In the Lighting window for the shadow light (step 5), enter a Direction value of –2.0 for X:. In the Intensity: box, enter a value of 0.7. Do not check any additional check boxes under Options. 
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/4_103.png">
7. In the Edit Directional Lights window, click Update All, and then click OK.  There may be a pause as Siege Editor updates the region’s lighting before the window disappears. 

### Point Light

Add individual light sources to your region:

1. Add a light source near the candle.  Select point light from the Custom View (under gizmos), and place it near the candle in the house. 
2. Select the point light and, using the same method for moving objects, position the light slightly above the candle that you placed on the windowsill. 
3. Select the light and right click on it. Click Properties, and then click on the Lighting tab. 
4. Set the reach of the light by entering a value of 2.0 for the Inner Radius: box, and a value of 5.0 for Outer Radius:. 
5. Click Choose Color.  In the Color window, select a bright shade of yellow.  Click OK. 
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/5_103.png">
6. Under Options (still on the Object Properties window), check the Occlude box so that the light will be blocked by terrain, and check the Draw Shadows box so that actors near the light will cast shadows. Leave the rest of the options as they are. Click OK to close the Object Properties window. 
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/6_103.png">
7. Under the Lighting Menu, select Update All Node Lighting to see your changes applied. 
8. Save.

## 104: Fading

Fading is the term we use to describe terrain becoming invisible at times when you do not want it to obstruct the camera. This is done with a mixture of node camera flag settings and special trigger gizmos that control node behavior. A detailed explanation of fading can be found in Siege U: 205 - Fades.

### Node Camera Flags

1. Add the door top to the house. The node "t_grs01_houses_generic-b-log-door-top.sno" connects to Door 16 of the house node. 
2. Set Camera Flags to define how the game camera will behave when it encounters the nodes in your region. From the Node Menu, choose Select All Nodes. 
3. Choose Properties from the Node Menu to bring up the Node Properties dialogue box. Under the General tab, only Occludes Light and Bounds Camera should be checked. By occluding the light for all the nodes in the region, no light rays will shine through nodes; that helps create realistic shadows. "Bounds Camera" prevents the player's camera from passing beyond the nodes. For example, the camera will stay within the boundary of the region's walls, following corners, without jumping beyond. Click OK.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/0_104.png">
4. Select just the house node. Open Node Properties again and adjust the settings so only Occludes Light and Occludes Camera are checked. By occluding the camera on the house, the player will not see through the house if he walks so that the house is between the camera and his character. The Siege Engine will automatically adjust the camera up or to the side to keep the character in view. Click OK.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/0b_104.png">
5. Select just the Door Top node. Open Node Properties again and adjust the settings so only Occludes Light and Camera Fade are checked. "Camera Fade" will cause the node to fade when the camera ray intersects in (like if you walked inside the house). Click OK.
Note: If the "Camera Fade" flag is checked, "Occludes Camera" and "Bounds Camera" should not be checked. Doing so can cause all sorts of problematic behavior in-game.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/0c_104.png">
6. Save.

### Fading Nodes With Triggers

Add the roof node to the house by snapping either "t_grs01_houses_generic-b-roof-shingle.sno" or "–thatch.sno" to Door 15 of the house node.

To make the roof fade away when somebody goes inside the building, and fade back in when somebody leaves the building:

1. Change the roof node's fade flags.
  * Select the roof node and open its Node Properties dialog.
  * Under Fade Settings, set the Section, Level, and Object fields all to 5, then click OK. The value "5" doesn't have any special significance, other than that we know no other nodes have those values. When we command 5,5,5 to fade, only the roof will fade.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/0d_104.png">
2. Add two fade triggers.
  * Under the Settings Menu, select Region.
  * Copy the value from the Region GUID field. Click Cancel.
  * Select "trigger_generic" from the gizmos folder.
  * Click on the floor in the doorway of the house to make a new trigger there.
  * Select the gizmo by clicking on it, then right click on the trigger and select Properties.
  * Select the Trigger Properties tab.
  * Press the New button at the bottom-left. In the Triggers field (directly above), this has created a new trigger attached to our trigger_generic object. It is hidden right now.
  * Click the box marked with a plus symbol to the left of "trigger_generic", which will bring down the text "trigger_0". Click on "trigger_0" to select it.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/1_104.png">
  * Click the Add Condition button on the right.
  * Select "party_member_within_bounding_box" from the drop-down dialogue that pops up, then press OK.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/1b_104.png">
  * Change the values (in the Value column) for Half diag X, Y, and Z to 1, 1, and 0.5, respectively. This creates a bounding box that is long and thin.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/1c_104.png">
  * Click the Add Action button, and select "fade_nodes_global" in the drop-down dialog, and press OK.
  * Paste the region GUID (from step 2b) into the value field for the Region ID.
  * Set the Section, Level, and Object all to 5 (remember step 1b?).
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/1d_104.png">
  * Double-click on the field in the Value column, to the right of Fade Type. This will bring up a drop-down list of all valid choices; select out:black.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/1e_104.png">
  * Click the Rotation tab, and enter in 20 as the Y value. OR rotate the trigger so that the bounding box covers the entire floor beneath the doorway.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/1f_104.png">
  * Click OK on the bottom of the Object Properties window.
  * With the trigger selected, click on Copy in the Edit Menu. [default hotkey = Ctrl+C]
  * Point the mouse cursor at the front steps of the farmhouse, and press Ctrl+V [default hotkey for Edit Menu | Paste]. This creates a copy of the first trigger. 
  * Rotate and position the trigger so that its bounding box completely covers the bottom stair. This way the character will always trigger it when he crosses the first step.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/2_104.png">
  * Select the second trigger, and bring up its properties.
  * Change the value for Fade Type to *in*.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/2b_104.png">
3. Save.

## 105: Moods

Moods are atmospheric settings used to polish and optimize a level. They consist of weather events such as rain, snow, and fog, music, ambient noises, and a few other advanced features that are covered in greater detail in Siege U: 204 - Moods. For now, we have provided a pre-created mood to use with this tutorial.

1. Create a new generic trigger in the middle of the start points. Refer to section 105, steps 2c - 2i if you need assistance. 
2. Add a new Condition and choose "party_member_within_sphere." 
3. Change the Radius (of the sphere) to 5. 
4. You should see a sphere debug HUD with the new trigger in the middle (you may need to move the Object Properties dialogue out of the way). Visually verify that this encompasses all of the start points. 
5. Add a new Action to the trigger and choose "mood_change." 
6. Enter the following value for the Mood Name: "map_world_fh_r1_4" (no quotes). 
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/1_105.png">
7. Click OK to close the Object Properties dialogue. 
8. Save. 

## 106: Monster Placement

Monster placement is one of the easiest aspects of the Siege Editor, but also one of the most influential. Where the monsters are placed directly affects how the game will eventually play out. A few simple guidelines:

* Never place monsters right next to Starting Positions. 
* The monster classes are similar to the player classes: Melee, Ranged, and Magic. 
* Monsters appear in 3 variations: Normal, Revealing, and Generators. 
  * Normal monsters are visible and ready to attack the player when spotted. For example, the Krugs at the start of Dungeon Siege. 
  * Revealing monsters are visible but play an animation when the player is spotted. They do not attack and are not targetable until the animation has completed. For example, the gargoyles that sit on pedestals in the Crypts. 
    * You can also hide revealing monsters. Those monsters cannot be seen by the player until the player reaches the reveal trigger set by the designer. 
  * Generator monsters do not exist until the player triggers the generator. Once activated, the generator will spawn monsters based on its settings. 

For this tutorial you will be placing 2 groups of monsters: one group of Melee/Normal and one group of Melee/Generator.

**[Note: This "exploding door" generator is not included with Dungeon Siege v1.0. If you do not have Dungeon Siege v1.09B or greater, skip down to the "Move over to the well node" paragraph and continue on. Once you have upgraded your version of Dungeon Siege, we encourage you to revisit the "exploding door".]**

First is the Generator group:

1. From the Custom View open the monsters folder and select "tutorial_gen_explode_door-krug_grunt". 
2. Find the house node, and place the "exploding door" object near the doorway. 
3. Adjust the door to fit into the doorway.  If it is too small to cover the doorway, open the door's Properties, click on the Template Properties tab, and adjust the scale_multiplier setting until the door fits. 
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/1_106.png">

You’ve just placed an exploding door that will spawn in a Krug Grunt (a very tough monster) so watch out when approaching the house. Also of note, you’ll see a red circle around the door generator; this is its detection range. In game, when a player enters that circle, the door will explode and a Krug Grunt will appear.

Move over to the well node.  If you did not place shrubbery behind the well, go ahead and add two groves now.  This is a good place to have a Krug Scavenger ambush.

1. Select "krug scavenger" from the custom view. 
2. Place three Krug Scavengers near the well. 
3. Select one Scavenger and move it to the middle of the area between the groves. 
4. Select another Scavenger, and drag it inside one of the forest groves (Note: watch the outermost circle as you do this. This is the monster’s player detection range, just as with the door generator. You’ll want to make sure each of the Scavengers detection circles overlap, so they will converge on the player at the same time). 
5. Repeat step 4 with the third Scavenger, moving it to the other forest grove. 
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/2_106.png">
6. Save.


## 107: Opening Your Map in Dungeon Siege

Now that you have built a map, you need to test it. In order to do that, you will need to "tank" your map into a DS-readable format.

1. Save your map. If you tank and have not saved recently, any unsaved changes will not be tanked. 
2. Under the *File Menu*, select "Save Map as .dsmap..." 
3. Select the map you would like exported. We suggested "my_world" at the beginning of this tutorial, but if you have forgotten the name of the map you have been working on, it is displayed in the title bar of Siege Editor. (The title bar is the top strip of the SE window that contains the minimize/maximize/close buttons.)
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/1_107.png">
4. Click OK. It is highly advised that you accept the default Destination File, as it vastly simplifies the export/import process. Advanced users may elect to redirect the map to a different location, but we'll stay with the easy route for now. 
5. On the following window, the only recommended fields to change are "Title", "Author", "Copyright", and "Description". All other fields should be modified by advanced users only.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/2_107.png">
6. Click Start!.
7. A "Processing Resource File..." progress display will appear. The final status will be listed in the "Status" window as "Success!" if you followed these steps properly. If any errors result, read the error message and start the export over. Often times the error is the result of varying from the default settings.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/3_107.png">
8. Click Close.

Let's try your map out! 

1. Close Siege Editor. 
2. Launch Dungeon Siege. 
3. Select "Single Player", "Start a New Game", and choose your hero. 
4. At the "Load Map" screen, select your map, click Next, and choose "Normal" difficulty.
<img style="display:block; margin:auto;" src="{{site.baseurl}}/assets/siegeu/100/4_107.png">
5. Assuming you built your map correctly, you should be standing at one of your starting locations. Congratulations and watch out for that door!

## Conclusion:

That concludes this tutorial. You should now be familiar with the Siege Editor and its basic functionality. We have covered placing nodes, objects, and monsters; we have discussed lighting, fading, and moods. Finally, we discussed how to convert your map into DS-usable format and back to SE-editable bits. If you would like to delve further into modding Dungeon Siege, check out the advanced topics covered in the Siege University 200 and 300 series.

***

## Appendix A: Tips

Here are some tips from the GPG level designers that might simplify your SE interaction:

* Use the "generic" node set by default. It contains the greatest variety of nodes and offers the most compatability. 
* Use the generic 8x8 (t_xxx_flr_08x08-v0.sno) or 4x4 (t_xxx_flr_04x04-v0.sno) node as your starting node. It is a very simple and clean node, offering the most expandability. 
* Get used to using a,d,w for node placement and orientation. The hotkeys are much faster than using the Source Doors, Destination Doors, and Attach Node buttons. 
* If you keep the "focus" on a node (ie - you don't select another node), you can try out different nodes on a particular door easily. For example, select a node that you would like to attach another node to. Select the door you would like to connect to (use a and d), select the node you want to attach to that door, and then hit w until the node lines up. Now, select another node from the list on the left and carefully click on the "root" node in the main window (the node you attached the 2nd node to). If the selection does not drop from that "root" node, you can hit w and rotate the new node in the place of the 2nd node. 
* You can add nodes and objects from the Main View window to the Custom View window. Right-click on the node and select "Add to Custom View". This is extremely helpful when you are doing "bulk" nodework, especially with walls and corners. That will greatly speed up your efficiently, since you won't have to scroll the Main View window so much. 

## Appendix B: Siege Editor Preferences

Here are the suggested Preference settings for generic SE work. The Preferences can be adjusted under View | Preferences. For information on what the settings are, click on the "Help" button on the Preference menu or refer to the Siege Editor Manual.

*Node Settings* checked:

* Draw Door Nodes
* Draw Stitch Doors

*Rendering* checked:

* Dynamic Lighting 
* Static Lighting 
* Dynamic Shadows 
* Static Shadows 

*Misc* checked:

* Update Lighting/Effects 
* Draw Light Data 
* Right Click Camera Scrolling 

*Content Display*: development name

*Key Movement Delta*: 0.1

*Zoom Rate*: 0.5

