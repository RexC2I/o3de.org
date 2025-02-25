---
linktitle: Lua
title: Writing Lua Scripts in Open 3D Engine
description: Use Lua in Open 3D Engine to automate your game project.
toc: true
weight: 100
---

You can use Lua in **Open 3D Engine (O3DE)** to facilitate quick iteration of your game project. Lua is a powerful, fast, lightweight, embeddable scripting language. When you construct new gameplay and game systems, you can run your changes immediately, without compiling your source code.

O3DE uses Lua version {{< versions/lua >}}.

## Building Lua Editor and GridHub

If you built O3DE from source, you must explicitly include **Lua Editor** (Lua IDE) and GridHub as build targets when you build your project. GridHub is O3DE's central connection hub for debugging, and is required to debug Lua scripts from the Lua IDE. To include these targets, add `LuaIDE` and `GridHub` to your build target list: `--target <project>.GameLauncher Editor LuaIDE GridHub`. 

For information about accessing class references in Lua Editor, refer to [Debugging with Lua Editor](debugging-tutorial).

### Example

If you need to build Lua Editor and GridHub after your project is built, navigate to your O3DE source directory, for example `c:\o3de`, and run the following command, inserting the path to your project's build directory.

```
cmake --build c:\<o3de-projects>\<project>\<build> --target LuaIDE GridHub --config profile -- /m
```

## Learning Lua 

For learning the Lua language itself, the [lua.org](http://www.lua.org) website is a good place to start.
+ [Official Lua Documentation](http://www.lua.org/docs.html) - Provides a central location for information about Lua, including a [Getting started](http://www.lua.org/start.html) page.
+ [Programming in Lua](http://www.lua.org/pil/) - This text is a resource for getting started with Lua programming.
+ [Lua {{< versions/lua >}} Reference Manual](http://www.lua.org/manual/{{< versions/lua >}}/) - Provides a reference of all the functions that are available by default in Lua.

## Learning Lua in O3DE 

After you read through this tutorial on writing Lua scripts for the component entity system, learn more about using Lua in O3DE by consulting the following resources.

  + For information on O3DE's built-in Lua editor, refer to [Lua Editor](./lua-editor).
  + For information about the O3DE EBus, refer to [Working with the Event Bus (EBus) system](/docs/user-guide/engine/ebus).
  
## Section Topics

| Topic | Description |
| --- | --- |
| [Adding Lua Scripts to Component Entities](add-lua-script) | Use the Lua Script component to add script functionality to your game entities. |
| [Lua Script Structure](basic-lua-script) | Basic structure of a Lua script. |
| [Lua Editor](lua-editor) | Learn about the Lua Editor. |
| [Properties Table](properties) | Specify the properties of a Lua script component that appear in O3DE Editor. |
| [Using EBuses in Lua](ebus) | Write Lua scripts that use the EBus to communicate between components. |
| [The Lua Environment (Advanced)](environment) | Learn about adding ScriptContext instances and using common code in the O3DE Lua environment. |
| [Debugging Lua Scripts](debugging-scripts) | Learn about debugging Lua scripts in O3DE. |
| [Debugging with Lua Editor](debugging-tutorial) | Use Lua Editor to debug Lua scripts. |

## Related Topics

| Topic | Description |
| --- | --- |
| [Camera Component](/docs/user-guide/components/reference/camera/camera) | Use the Camera component to allow an entity to be used as a camera. |
| [Using Player Input](/docs/user-guide/interactivity/input/working-with-the-input-component) |  Work with the Input component in O3DE. |
| [Input Component Event Bus Interface](/docs/user-guide/components/reference/gameplay/input-event-bus-interface) | Work with the Input component EBus (event bus). |
| [Simple State Component](/docs/user-guide/components/reference/gameplay/simple-state) | Use the Simple State component to provide a simple state machine. |
| [Tag Component](/docs/user-guide/components/reference/gameplay/tag) | Use the Tag component to apply labels to entities. |
| [AWS Client Auth Scripting](/docs/user-guide/gems/reference/aws/aws-client-auth/scripting) | Examples of using the AWS Client Auth Gem with Script Canvas and Lua. |
| [AWS Metrics Scripting](/docs/user-guide/gems/reference/aws/aws-metrics/scripting) | Examples of using Script Canvas or Lua with the AWS Metrics Gem to generate and submit metrics. |
| [Gestures Gem](/docs/user-guide/gems/reference/input/gestures) | The Gestures Gem provides detection for common gesture-based input actions. |
| [Virtual Gamepad Gem](/docs/user-guide/gems/reference/input/virtual-gamepad) | The Virtual Gamepad Gem provides controls that emulate a gamepad on touch screen devices for O3DE projects. |
| [Tweener Lua Script](/docs/user-guide/interactivity/user-interface/animating/tweener-system/tweener-lua-code) | Learn how to use Lua scripting to animate your entities with the Scripted Entity Tweener system. |
| [Tweener Timeline](/docs/user-guide/interactivity/user-interface/animating/tweener-system/tweener-timeline) | Use Scripted Entity Tweener's timeline abilities to chain animations together and exert fine control over them. |
| [Synchronizing Animation Graphs](/docs/user-guide/visualization/animation/character-editor/sync-graph) | Use synchronized animation graphs to synchronize animation between actors. |
