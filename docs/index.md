# Welcome to JsonifyCraft

JsonifyCraft is a content creation mod that allows defining your own custom items, blocks, and more with JSON!

It's currently available for the following Minecraft versions:

* 1.12
* 1.14
* 1.15
* 1.16

To download, <a href="https://www.curseforge.com/minecraft/mc-mods/jsonifycraft" target="_blank">visit the CurseForge page</a>.

If you need help, a few of us are active over on [Discord](https://discord.gg/Ca2hx6X).

## Usage

The mod, once installed and the game has started at least once, will create a `gameobjects` folder under the Minecraft directory. Add JSON files under this folder in any order, and objects will be added to your game. Syntax for each object is available under the `Game Objects` section of this documentation.

## Design Notes

This project was designed to make the process of adding objects to the game easier. Yes, ContentTweaker exists, and I frequently use it, but that requires some level of comfort with scripting. I find that a good JSON framework is easier to work with and, potentially, automate.

That being said, in order to make this a *good* JSON framework, I have one big rule for myself that I'm striving to make the cornerstone of this project:

You should be able to pop the same JSON file in the `gameobjects` folder, regardless of what version of Minecraft you're using, and the exact same game objects should be created in-game.
