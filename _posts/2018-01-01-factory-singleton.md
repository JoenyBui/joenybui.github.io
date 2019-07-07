---
layout: post
author: Joeny Bui
---

# Singleton Design Pattern

Restricts the instantiation of a class to one "single" instance.  This is useful when exactly one object is needed to coordinate actions across the system.

* used for centralized management of internal or external resources 
* provide a global point of access to themselves
* implementation involves a static member in the class and a private constructor
* ensure it works in multi-threaded environment

## Examples

* logger classes - provides a global logging access point in the application component
* configuration classes - design the classes which provide the configuration settings
* accessing resources in shared mode - accessing from multiple classes on a serial port (singleton allows synchronization)
* factories implementation as a singleton
* using reflection you can avoid modifying the factory class code (registration)

## Consideration

* multithreading
* serialization - when using Serializable interface need to have to implement readResolve method
* classloaders - loaded by two different class loader will have two instance
* global access point

# Factory Design Pattern (Abstract Factory)

![FDP](https://www.oodesign.com/images/stories/factory%20implementation.gif)

The client needs a product, the factory object will return a new product given the information about the type of object it needs.  Advantage is that new components can be added without changing a single line of code.

* Create object without exposing the instantiation logic to the client.
* Refers to the newly created object through a common interface.

