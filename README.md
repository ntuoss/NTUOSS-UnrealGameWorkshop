# NTUOSS Unreal Engine 4 Workshop

##### *made with love by [Yong Hao](https://github.com/HORACEYOUNG) for NTU Open Source Society*

*Leave a star if you like this~*

![](Images/UnrealLogo.png)

---

### Workshop Details

**When**: Friday, 1 Nov 2019. 6:30 PM - 8:30 PM.
**Where**: LT1, NTU North Spine Plaza
**Who**: NTU Open Source Society

**Questions**: We will be hosting a Pigeon Hole Live for collecting questions regarding the workshop.

Feedback & Error Reports: We will send out the link for collecting feedback as usual.
​	

For further discussion or cooperation please contact YO0001AO@e.ntu.edu.sg.

***Disclaimer: This workshop is for educational purposes only. The artistic resources are retrieved from Nintendo Co., Ltd. and information regarding Unreal concepts are retrieved from [Unreal Document](https://docs.unrealengine.com/en-US/index.html). The idea and content of the workshop is inspired by [Virtus Learning Hub](https://www.virtushub.com/), who is a provider and educator in the field of game-related softwares. For more beneficial information, you can always check out his channel on youtube and other content creators as well***

***No prototype or outcome of any type is intended for commercial use.***

---
### Prerequisites

1. **Download Unreal Engine 4 Software(as UE4 in upcoming texts) and the GitHub ropo for the workshop**

   [You can download UE4 by clicking this link.](https://www.unrealengine.com/en-US/download)

   [You can download the GitHub Repo by clicking this link.]( https://github.com/ntuoss/NTUOSS-UnrealGameWorkshop )
   
   **Warning: We highly recommend you to download UE4 prior to coming to this workshop as it may take 30 - 60 minutes to complete the download. Meanwhile do remember to register an Epic Games account as you may be required to do so.**


2. **Basic Object-Oriented Programming Knowledge (optional)**

   **In this workshop, all the scripts are going to be written in Blueprint. **

   The Blueprints Visual Scripting system in Unreal Engine is a complete gameplay scripting system based on the concept of using a **node-based interface** to create gameplay elements from within Unreal Editor. As with many common scripting languages, it is used to define object-oriented (OO) classes or objects in the engine. As you use UE4, you'll often find that objects defined using Blueprint are colloquially referred to as just "Blueprints."

   This system is extremely flexible and powerful as it provides the ability for designers to use virtually the full range of concepts and tools generally only available to programmers. In addition, Blueprint-specific markup available in Unreal Engine's C++ implementation enables programmers to create baseline systems that can be extended by designers.

---
## Task 0. Introduction

### What is Unreal 4 Engine?

![](Images/UnrealUISample.png)

The Unreal Engine is a game engine developed by Epic Games, first showcased in the 1998 first-person shooter game Unreal. Although initially developed for first-person shooters, it has been successfully used in a variety of other genres, including platformers, fighting games, MMORPGs, and other RPGs. With its code written in C++, the Unreal Engine features a high degree of portability and is a tool used by many game developers today, with it being source-available. The most recent version is Unreal Engine 4, which was released in 2014.

In a few words:

- Developed by Epic Games
- High Graphics Quality
- And most importantly: Blueprint, which enables you to write logic without coding.

---
## Task 1. Create your first Project

​	After you’ve finished downloading the UE4 Engine and signed in your Epic Games account, you’ll be directed to the following interface to create your very first project.

​	![](Images/1.0.CreateProject.png)

First of all, we’re going to introduce the Blueprint Visual Scripting Language in the following sections, so make sure you choose Blueprint instead of C++ and choose “Third Person” under the tag.

![](Images/1.0.a.ChooseScriptingLanguage.png)

Next, we’re building a mobile game today, so choose the platform to be “Mobile/Tablet” and leave the other two options as they were.

![](Images/1.0.b.ChooseOtherSettings.png)

Finally, choose a location for your project and give your project a name and click Create Project, you’re now good to go!

![](Images/1.0.c.CreateProject.png)

## Task 2. UE4 Level Editor UI Overview

The **Level Editor** provides the core level creation functionality for Unreal Editor. This is where levels are created, viewed, and modified mainly by placing, transforming, and editing the properties of [**Actors**](https://docs.unrealengine.com/en-US/Engine/Actors/index.html).

In Unreal Editor, the scenes in which you create your game experience are generally referred to as [Levels](https://docs.unrealengine.com/en-US/Engine/Levels/index.html). You can think of a level as a 3D environment into which you place a series of objects and geometry to define the world your players will experience. Any object that is placed in your world, be it a light, a mesh, or a character, is considered to be an Actor. Technically speaking, *Actor* is a programming class used within the Unreal Engine to define an object that has 3D position, rotation, and scale data. For sake of ease, however, it will be easiest to think of an Actor as *any object that can be placed in your levels*.

After your computer has finished loading your project, your UE4 Editor should look something like this below:

![](Images/2.0.a.UIOverview.png)

It feels quite messy for the beginners I understand, so here I’ll do a brief introduction on the Editor’s User Interface you you have an idea on what do all these parts do. The details of the following elaboration can be found at [Unreal Documentation: Editor Interface](https://docs.unrealengine.com/en-US/Engine/UI/LevelEditor/index.html)

![](Images/2.0.b.InterfaceBreakdown.jpg)



1. Tab Bar and Menu Bar

   ![](Images/2.0.c.TabBar.jpg)

   The Level Editor has a tab along the top providing the name of the level currently being edited. Tabs from other editor windows may be docked alongside this tab for quick and easy navigation, similar to a web browser.

   To the right of the Tab Bar is the name of the current project.

   ![](Images/2.0.d.MenuBar_Windows.jpg)

   The **Menu Bar** in editor should be familiar to anyone who has used Windows applications previously. It provides access to general tools and commands that are used when working with levels in the editor.

2. Toolbar

   ![](Images/2.0.e.toolbar.jpg)

   The **Toolbar** panel, like in most applications, is a group of commands providing quick access to commonly used tools and operations.

3. Modes

   ![](Images/2.0.h.modes.jpg)

   The **Modes** panel contains a selection of various tool modes for the Editor. These change the primary behaviour of the Level Editor for a specialized task, such as placing new assets into the world, creating geometry brushes and volumes, painting on meshes, generating foliage, and sculpting landscapes.

4. Content Browser

   A file manager section in which you manage all the files and resources within the project.

5. Viewports

   ![](Images/2.0.f.ViewPort.jpg)

   The **Viewport** panel is your window into the worlds you create in UnrealEd.

   This panel contains a set of viewports, each of which can be maximized to fill the entire panel and offer the ability to display the world from one of three orthographic views (Top, Side, Front) or a perspective view giving you complete control over what you see as well as how you see it.

6. World Outliner

   ![](Images/2.0.j.scene_outliner.jpg)

   The **World Outliner** panel displays all of the Actors within the scene in a hierarchical tree view. Actors can be selected and modified directly from the **World Outliner**. You can also use the Info drop down menu to turn on an extra column that shows Levels, Layers, or ID Names.

7. Details

   ![](Images/2.0.g.details_panel.jpg)

   The **Details** panel contains information, utilities, and functions specific to the current selection in the viewport. It contains transform edit boxes for moving, rotating, and scaling Actors, displays all of the editable properties for the selected Actors, and provides quick access to additional editing functionality depending on the type of Actor(s) selected in the viewport. For instance, selected Actors can be exported to FBX and converted to another compatible type. The Selection Details also allows you to view the materials used by the selected Actors, if any, and quickly open them for editing.

   

---

## Task 3. Introduction to Blueprint Visual Scripting

### Task 3.1. Blueprint Overview

The **Blueprints Visual Scripting** system in Unreal Engine is a complete gameplay scripting system based on the concept of using a node-based interface to create gameplay elements from within Unreal Editor. As with many common scripting languages, it is used to define object-oriented (OO) classes or objects in the engine. As you use UE4, you'll often find that objects defined using Blueprint are colloquially referred to as just "Blueprints."

Let us take a look and have a intuitive concept about blueprint, navigating to ThirdPersonBP -> Blueprints -> ThirdPersonCharacter:

![](Images/3.2.1.b.BlueprintOverview.png)



This system is extremely flexible and powerful as it provides the ability for designers to use virtually the full range of concepts and tools generally only available to programmers. In addition, Blueprint-specific mark-up available in Unreal Engine's C++ implementation enables programmers to create baseline systems that can be extended by designers.

The workflow of the blueprint scripting language can be visualized as below (adopted from [link](https://www.youtube.com/watch?v=MWepzQqAS60&list=PLL0cLF8gjBpqRUy7r0DtVY3Fcdgq5Wk-h&index=3)):

![](Images/3.1.a.BlueprintWorkflow.png)

The blueprint programming language is almost like the real spoken language, where you have a subject,  a verb, and an object, to describe a certain action that the subject has done to the object. While in blueprint, what we have is the structure in the image above, where when certain “events” happen, an action will be applied to an object. The subject here depends on the context to be either the system or the player.

Now let’s look at the different categories of blueprints in the Unreal Engine.

### Task 3.2. Categories of Blueprint

#### 3.2.1. Level Blueprints

The level blueprint contains the blueprint code to control the entire level. It can only reference the objects within the level and the effects of one level blueprint will not be carried along to the next level.

Let us try out the level blueprint with a fairly simple example: we’re going to control a light in the scene, and after a few seconds, make it disappear.

First of all, let us create a point light object by dragging it from the modes panel to the scene:

![](Images/3.2.1.d.AddLight.png)

Now open the level blueprint by navigating to Blueprints -> Open level blueprints:

![](Images/3.2.1.c.OpenLevelBlurprints.png)

To add components to the level blueprint, right click and add one “Event Begin Play”, one “Point Light” Reference and one “Toggle Visibility” to the game, and insert one “delay” between “Event Begin Play” and “Toggle Visibility”:

![](Images/3.2.1.e.LevelBlueprint.png)



#### 3.2.2. Class Blueprints

Like we’ve mentioned earlier, blueprint is an object-oriented programming language, the class blueprint is designed for individual objects. Objects in game like player, enemies, items, buffs, or even health bars can all be written in the form of class blueprints. Class blueprints can be duplicated, which is extremely useful as you do not have to rewrite your code for objects that perform the same functions.

Let’s try an example by making multiple lights that will be turned off once your character touched them.

Navigate to the folder “ThirdPersonBP”, right click and under blueprint tab select “Blueprint Class”, you’ll be having something as shown below:

![](Images/3.2.2.BPClass.png)

![](Images/3.2.2.SelectBPClass.png)

Here we select actor as it’s the most common template for blueprint class. We will name it light setup, and you will see something as below:

![](Images/3.2.2.WhiteBall.png)

This is the default template of the blueprint class, the white ball in the centre represents the origin of the object. We now add a point light by click “Add Component” by clicking on the button on the top left side of the screen, then add a static mesh component and select the material called “SM_Lamp_Wall”:

![](Images/3.2.2.AddComponent.png)

![](Images/3.2.2.Lamp.png)

Then add a box collision component to the light, this is to detect if the player has contacted the lamp for actions to happen:

![](Images/3.2.2.BoxCollider.png)

Then navigate to the event graph and write blueprint as below:

![](Images/3.2.2.LightBP.png)

This basically means any object that get in touch with the box collision of the point light, it will be first casted to the ThirdPersonCharacter class, and if successful, the designated event will happen, in this case “Toggle Visibility”. Now get back to the game and we will notice the light will be toggled once the player get close to the point light:

![](Images/3.2.2.ToggleLight.png)



#### 3.3.3. Variables and Loops in Blueprint

##### 3.3.3.1. Variables

Like any other programming language, blueprint has several generic variable types to play with, as the list below:

![](Images/3.3.3.VariableType.png)

You might has already noticed the types that are familiar to you, like Boolean integer and float. Some other important ones and their descriptions are listed below:

Vector: composed three floating point numbers in the form of (x,y,z)

Rotator: contains the rotation information of the object

Transform: contains the information of position, rotation, and scale.

To view the content of the variables, simply adopt the blueprint below:

![](Images/3.3.3.PrintVar.png)

##### 3.3.3.2. Branches and Conditions

Branches are very much like the if statements in general programming language, it has different output depending on different input true or false values, like below:

![](Images/3.3.3.2.Branch.png)

##### 3.3.3.3. Loops

Again Very much like for and while loops in general programming language.

###### 3.3.3.3.1. For Loop

![](Images/3.3.3.3.1.Forloop.png)

It will execute the loop body for (Last Index - First Index + 1) Times. You can manage the index from the index node like what we did, to print out the index for every loop it takes.

###### 3.3.3.3.2. While Loop

![](Images/3.3.3.3.2.WhileLoop.png)


## Task 4. Build the Game
In this workshop we’re going to create an endless runner game, like the Temple Run and the Subway Run, using blueprints and Unreal 4 Engine.

### Task 4.1. Create the Project and adjust the camera

We’ve already covered how to create a project in the previous sectors. The only difference of our current project is we’re going to build a mobile game, so switch from desktop/console to mobile/tablet and the rest is pretty much the same.

![](Images/4.1.CreateProject.png)

In an endless running game, you’ll notice that the camera does not move throughout the game, let’s adjust the camera right now. Navigate to ThirdPerson - > ThirdPersonBP -> and open ThridPerson Character:

![](Images/4.1.BP.png)

In Viewport, click on the camera icon and move it a little up and behind to your like, and bring the head down a little bit to make it look down to the character:

![](Images/4.1.Camera.png)

Switch to event graph, and delete the Gamepad Section as we do not want the camera to move:

![](Images/4.1.delete.png)

Move to the Movement Input, change “InputAxis MoveForward” to “Event Tick” as we want our character to move endlessly:

![](Images/4.1.EventTick.png)

### Task 4.2. Set Up the floor Tile

The material of the floor tiles can be found at the folder named “EndlessAssets”

Create a folder named “EndlessFiles”, then create a folder under it called “Tiles”. We’re going to organize all the files under “EndlessFiles” folder:

![](Images/4.2.EndlessFiles.png)

Then drag and drop three files to import them to the engine, namely “FloorTile_Diff.png”, “FloorTile_EM.png”, and “FloorTile_Nrm.png”.

![](Images/4.2.ImportTiles.png)

Right click “FloorTile_Diff”, and click “Create Material”:

![](Images/4.2.CreateMaterial.png)

Create Three Texture Sample and assign the three files to them. Connect them to the material as below:

![](Images/4.2.TileMaterial.png)

Then in create a blueprint folder and under it, create a blueprint class called “MaterTile”, add a static mesh component and assign the material we’ve created to it:

![](Images/4.2.Cube.png)

Scale the cube to (10, 10, 0.1) to make it plane-like. Then add an arrow component to indicate the direction where we want our tile to expand:

![](Images/4.2.Arrow.png)

### Task 4.3. Endlessly Spawning the Tile

Create a box collision at the edge of the tile. Whenever the play collides with it, a new tile will be spawned:

![](Images/4.3.TileBox.png)

Trigger the event by “On Component Begin Overlap”:

![](Images/4.3.StepOne.png)

Write a function to spawn tiles in the game mode blueprint:

![](Images/4.3.SpawnTile.png)

Back to the MasterTile Blueprint:

![](Images/4.3.SpawnBlueprint.png)

Create a new level and run a for loop, we can see our character running in the endlessly spawning tiles:

![](Images/4.3.TenTikes.png)

![](Images/4.3.PlayerOnTile.png)

And to destroy the tiles after we’ve run past it, simply add a destroy actor node after spawning the tile.

### Task 4.4. Switching Lanes

To move the player character to the exact centre of each lanes, we need to indicate where the centre of the lanes are by adding arrows to it:

![](Images/4.4.LaneArrow.png)

Now navigate to ThirdPersonCharacter blueprint and create a few variables:

![](Images/4.4.New Variable.png)

where lane is the current lane, new lane is the one that the player is gonna move to, and Lane Y is an array to hole the world location of the centres of each lane.

Then build the blueprint as below:

![](Images/4.4.SwitchLanes.png)

In side Lerp Timeline, create a float track with two key frames, length 0.1 and value from 0 to 1:

![](Images/4.4.LerpTimeline.png)

### Task 4.5. Pipe Obstacle

Move the mesh called “Low_Obstacles_Pipes.fbx” to a new folder called mesh, and remember to tick “Combine All Meshes”:

![](Images/4.5.MoveMesh.png)

Open up the PipeMain Material and adjust it as following:

![](Images/4.5.PipeMat.png)

Create a blueprint class and assign the material we’ve just adjusted:

Randomly spawn pipes on lanes. Repeat 3 times for all lanes:

![](Images/4.5.SpawnPipe.png)

### Task 4.6. Box Obstacles

Move “box.fbx” and “Crate_Diffuse.png” to the folder and modify the material as below:

![](Images/4.5.BoxMaterial.png)

Then modify the spawning pipes blueprint a little bit to spawn the boxes as well:

![](Images/4.6.SpawnBox.png)

### Task 4.7. Pickup Coins

Drag “pickup_kineticEnergy.fbx” to the mesh folder and modify it like this:

![](Images/4.7.CoinMat.png)

Create the blueprint class out of the material modified.

In ThirdPersonGameMode, add a variable called “Total Coins”. That’s where we’re gonna store how many coins we’ve picked up:

![](Images/4.7.TotalCoins.png)

Then when the player hits the coin, destroy it and play a sound:

![](Images/4.7.DestroyCoin.png)

Spawn the coin back in the tile blueprint:

![](Images/4.7.SpawnCoin.png)

### Task 4.8. Scoring

Create a widget blueprint to display the scores:

![](Images/4.8.Widget.png)

Create a textbox at the right hand corner of the screen:

![](Images/4.8.TextBox.png)

Then navigate the the ThirdPersonGameMode to create a variable to increment the scores:

![](Images/4.8.Scores.png)

Modify the tile spawn blueprint so that 25 are added to the score whenever a tile is spawned, and a plus 50 are added when a coin is picked up

### Task 4.9. Death

Create Ragdoll:

![](Images/4.9.CreateRagDoll.png)

In ThirdPersonCharacter, write a function to disable the movement of the character:

![](Images/4.9.DeathFunction.png)

Remember to set the mesh “BlockAllDynamic”

Fire off the Death Event whenever the player collides with a pipe or a box

## Acknowledgements

Many thanks to NTUOSS and its supportive committee~

Greatest love for all of you who come today~

Yours,

YH