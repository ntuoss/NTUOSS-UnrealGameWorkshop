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

1. **Unreal Engine 4 Software (as UE4 in upcoming texts)**

   [You can download UE4 by clicking this link.](https://www.unrealengine.com/en-US/download)

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

## Task 3. Introduction to Blueprint
## Task 4. Build the Game (May Involve Multiple Tasks)
## Task N. Export the Game
## Acknowledgements

Many thanks to NTUOSS and its supportive committee~

Greatest love for all of you who come today~

Yours,

YH