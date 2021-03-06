# UnityUtilitys

A set of utility classes for doing common things in unity. The following are included.

## AutoGenClass
A class for automatically generating source code files for unity. This helps automate certain repetative tasks in unity, like creating initialization scripts for scenes

## EventSystemInspector
A custom inspector for the event system included. Allows spying on the event system in the inspector for debugging



## Execution Order
Adds the ExecutionOrder Attribute which allows scripts to control their execution order in source code.

## Resource Generator
Auto Generates a source code file that maps resource assets names to their paths, which helps make programs more resistant to errors caused by typos in string literals

## Data Structures
Singleton: Parent class for creating singleton like objects in unity, that reinitialize on scene load.
Thunk: Wraps a function call and cache for retreiving an object in the future.
Wrapper: Wraps a value, allowing it to be passed by reference, edited from multiple places, or passed as read only.

## CEventSystem
An observer based event system.
Allows objects to register themselves to an event channel and event sub channel, and receive events on those channels.
Then, other objects can broadcast events into the event system to have them received on all listeners on the same channel.
This event system allows for objects that broadcast events to be decoupled from objects that receive events.

## Draw Extensions
Currently only contains the method extension DrawCross, which draws a 3D cross in unity at a point.

## SceneInitializerGenerator
Auto generates a class called InitializeScene, with a single static method Init.
Works with the MonoBehaviour class SceneInitializer to automatically execute code on scene load. Will attach any monobehaviour with the AutoInit Attribute, allowing it to begin runing.
This pattern is currently in revision, since I have not yet found a solution that is both easy to work with and bug free.