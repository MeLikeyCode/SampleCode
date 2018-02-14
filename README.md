This repository contains a small sample of some of the code that I have written. I don't know if I would label this as my absolute **best** work, but I am definitely satisfied with them.

All of this code comes from my Qt Game Engine project (which will be made open source shortly).

Overview
========
I have selected a few classes from my Qt Game Engine project to show off :). I tend to create one .h and one .cpp file for each class. The name of the file is the same as the name of the class.

Here is a brief description of the classes I have chosen (check out the ones that sound interesting to you):

### Sprite
This class represents a set of named animations that you can play via a play() method. 
You can add frames to an animation either from a folder or from a SpriteSheet (see below).

### SpriteSheet
This class represents a sprite sheet. A sprite sheet is a sheet of paper with many little images that are all part of a single animation. This is how graphics for 2d games are usually packaged. This class allows easily extracting certain frames from a sprite sheet.

### Animation
This class is very similar to Sprite, and serves the same purpose, except it represents a *single* animation. My eventual goal is to reimplement Sprite to use a bunch of Animation objects.

### PlayingAnimationInfo
A *very* simple class that represents some information about a currently playing animation such as its name, frames per second, etc...

### EntitySprite
This is an abstract class that basically defines the interface an Entity (another class that is part of my game engine - an Entity is basically anything that can go in a Map) expects from something that can "visualize" it. Concrete EntitySprites need to provide functionality such as setFacingAngle(), playAnimation("run"), etc...

### TopDownSprite
A concrete EntitySprite that makes it very easy to create animation from "top down" graphics.

### AngledSprite
A concrete EntitySprite that makes it very easy to create animations from "angled" graphics (anythin that isn't purely top down basically).

### Graph
This class represents a graph (set of nodes and edges). The most notable function it has is shortestPath() which finds the shortest path between two nodes using the A* algorithm.

### Tree
This class represents a tree.

### PathingMap
This is a really cool class. It represents a region of 2d space that is basically a grid of cells. Each cell can be filled or empty. It has a function for finding the shortest path between two cells (avoiding filled cells obviously). It also has a function for "adding" two PathingMaps together, etc...I use this class heavily in my game engine.

