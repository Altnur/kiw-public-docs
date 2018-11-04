# Base

The base of the game, and it should had all the basics elements to compose, at least, a flexible base for a RPG game.

It should include:

## Characters

Controllable entities, either by a player (with input) or IA

- Characters has 2 states: Controllables or not.
- It has, also, a basic speed attribute for movement. More attributes can be added with mods.
- It has an inventory, that is a list of Item objects, that can be used individually.
- Sprite animations can be played from scripts.
- Characters can use tiles, or other charactes, present in the world, to trigger functions.

## Item

An item is an entity that is present in the inventory of a character.

It can be used, either in the inventory, or anywhere else from the scripts.

## Tile

Entity that, unlike a character, are normally fixed (But they can also move, like platforms)

Sprite animations can be played from scripts.

The difference between a tile, and a character, is that a character has a [rigidbody](https://docs.unity3d.com/ScriptReference/Rigidbody.html), so it can trigger collision and physics functions.

## Generator

Can generate tiles and characters.

## HUD

Basic element for showing information.

They are panels, with a custom background.
Or text with custom color.

## Mods

All objects listed above can have scripts, so all objects are moddable.

The game itself, will be a composition of internal mods, so, in that way, the game is as flexible as I need it.

These are the types of mods available from this stage:

- Characters: For new races, enemies, etc...
  Example:
    - New races
    - Types of enemies
- Items: For new items
  Example:
    - New potion
    - New weapons
- Generator: For generating new types of maps
  Example:
    - New type of biome generation
    - New type of town
- CharacterScript: Script associated to every character (For extra mods applied to all characters, aside from new character mods)
  Example:
    - Basic needs system
    - Skills system
- WorldScript: Script general, with a single instance, that is always running
  Example:
    - Weather system

And with this stage, we can make a complete RPG. We can make a supermod for teams, and make submods for equipment from that, for example. Or make an attribute HP, that when it reach 0, it makes the character not controllable, and plays the dead animation.

Also, if a lua script need to extends a functionality from another script, a method "GetContent" is available from the scripts.
Example:
Let say, we want the items to be able to be equipped, so, we create a base mod, called "ItemEquipable", and we make mods from that base mod.
Then, in our little mod that create a new helmet, we put this in the start of the script:

``` lua

script:Run(GetContent("ItemEquipable"):GetText("script"));

```

That would run the script for the generic mod to create equipable items